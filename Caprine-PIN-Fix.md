# To fix the PIN Code popup open the dev console with `F12` or `Ctrl+Shift+I` and use this JS code to show the popup

```javascript
document.documentElement.classList.remove('hide-preferences-window')
```