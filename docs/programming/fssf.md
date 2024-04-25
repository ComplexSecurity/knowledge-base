The `res.sendFile()` function is a method of the response object (`res`) in [[Express]].js, a web application framework for [[NodeJs|Node.js]]. This method is used to send a file as an [[HTTP Protocol|HTTP]] response to the client. It's particularly useful for tasks like serving static files (e.g., images, PDFs, [[HTML]] files) in response to client requests.

The syntax is:

```js
res.sendFile(path [, options] [, callback])
```

- `path`: The absolute or relative path to the file.
- `options` (Optional): An object to specify options like root directory, headers, etc.
- `callback` (Optional): A callback function that is called after the file is sent or if there's an error.

A usage example:

```js
const express = require('express');
const path = require('path');
const app = express();

app.get('/download-report', (req, res) => {
    const filePath = path.join(__dirname, 'public', 'report.pdf');
    res.sendFile(filePath, (err) => {
        if (err) {
            console.log(err);
            res.status(500).send('Error occurred while sending file.');
        }
    });
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```

!!! info
    In this example, a PDF report is sent to the client when they access the `/download-report` endpoint. The `sendFile()` method is used to send `report.pdf` as the response.

  
The `res.sendFile()` function in Express.js itself is not inherently vulnerable. However, like many other functions that involve file handling and user input, it can become a source of security vulnerabilities if not used properly. The primary concern with `res.sendFile()` is related to [[Directory Traversal|Path Traversal]] attacks when user input is used to determine the file path.

A vulnerable example:

```js
const express = require('express');
const app = express();
const path = require('path');

app.get('/file', (req, res) => {
    // User input is taken directly from the query parameter
    let fileName = req.query.fileName;

    // This usage of res.sendFile() is vulnerable to Path Traversal
    res.sendFile(fileName, { root: path.join(__dirname, 'public') }, (err) => {
        if (err) {
            res.status(500).send('Error occurred while sending file.');
        }
    });
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

!!! danger
    In this example, the server sends a file based on the `fileName` query parameter. An attacker could exploit this by manipulating the `fileName` parameter to access files outside the `public` directory. For example:

```bash
http://example.com/file?fileName=../../etc/passwd
```

This URL could potentially give the attacker access to the /etc/passwd file on a Unix-like system.