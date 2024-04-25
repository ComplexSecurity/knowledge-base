The information contained within a User-Agent HTTP request header is also known as the **User-Agent (UA) string**. This string contains information on the device.

For example, if you browse the web on your smartphone, your device will send a HTTP request header to the web server, saying that it is a mobile device. The website will then respond and show you the mobile version of the page.

An example User-Agent string can be:

```html
Mozilla/5.0 (Linux; Android 12; Pixel 6) AppleWebKit/537.36 (KHTML, like Gecko)
Chrome/93.0.4577.62 Mobile Safari/537.36
```

- **Mozilla/5.0** - Largely ignored as has no relevance to the associated device
- **Linux; Android 12** - details about the OS
  - For mobile UA-strings, the "**Pixel 6**" section provides the device name or device model number
- **AppleWebKit/537.6** - indicates what browser rendering engine is used. A rendering engine is what transforms HTML into a webpage on the screen
- **KHTML, like Gecko** - ensure compatibility for historical reasons
- **Chrome/93.0.4577.62 Mobile Safari/537.36** - more detail on the browser and its version number.
