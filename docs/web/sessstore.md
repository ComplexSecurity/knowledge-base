`sessionStorage` is a web storage feature provided by modern web browsers that allows web applications to store data as key-value pairs within the user's browser session. This data is accessible only on the same tab, and unlike [[LocalStorage]], it gets cleared when the tab or browser is closed. 

`sessionStorage` is part of the [[Web Storage API]], along with `localStorage`, providing a more secure and efficient way to handle data on the client side compared to traditional [[cookies]].

Data stored in `sessionStorage` is available only within the tab in which it was set. Opening a new tab or window with the same URL will have a separate `sessionStorage` space. The data in `sessionStorage` is cleared when the tab or browser window is closed. It's not persistent like `localStorage`.

Access to `sessionStorage` is restricted to the same origin (same scheme, host, and port), providing a degree of security against cross-origin data access. `sessionStorage` typically allows more data to be stored compared to cookies (usually at least 5MB per origin).

`sessionStorage` is ideal for storing temporary data that should only persist for the duration of a page session, like user choices or form data within a single tab. It can be used to store state in [[Single Page Applications|SPAs]] where the state should not persist after the tab is closed.

An example usage may be:

```javascript
// Storing data in sessionStorage
sessionStorage.setItem('key', 'value');

// Retrieving data from sessionStorage
let data = sessionStorage.getItem('key');

// Removing data from sessionStorage
sessionStorage.removeItem('key');

// Clearing all data from sessionStorage for the current tab
sessionStorage.clear();
```

In this [[JavaScript]] example, data is stored in `sessionStorage` using `setItem`, retrieved with `getItem`, removed with `removeItem`, and all data in `sessionStorage` can be cleared with `clear`.

There are a couple of differences between this and localStorage:

- **Persistence**: `localStorage` data persists even when the browser is closed and reopened, while `sessionStorage` is cleared after the tab or browser is closed.
- **Scope**: Data in `localStorage` is accessible across all tabs and windows within the same origin, while `sessionStorage` data is limited to the tab where it was created.

