# common-frontend-animations
Just a collection of animations that are very common but useful. Mostly becuase redoing them every time is a schlep. Next plan is to bundle them in projects generated from terminal.


##Loading animations

```js
var readyStateCheckInterval = setInterval(function() {
  if (document.readyState === "complete") {
      clearInterval(readyStateCheckInterval);
      document.body.classList.remove('loading');
  }
}, 500);
```

```css
#loadingScreen {
  visibility: hidden;
  opacity: 0;
  position: fixed;
  left: 0;
  right: 0;
  width: 100%;
  height: 100%;
  background: #f5f5f5;
  z-index: 100000000;
  font-size: 1.5em;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.2s;
}

#loadingScreen .logo {
  text-align: center;
  line-height: 1;
}

#loadingScreen .logo h6 {
  font-size: 0.8em;
}

#loadingScreen .logo p {
  margin-top: 2em;
}

.loading #loadingScreen {
  visibility: visible;
  opacity: 1;
}
```