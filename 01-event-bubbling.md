Was passiert wenn der Benutzer auf 'Löschen' klickt? Was wird ausgegeben und warum?

```html
<div id="card" onclick="console.log('card')">
  <div id="body" onclick="console.log('body')">
    <button id="delete" onclick="console.log('delete')">Löschen</button>
  </div>
</div>
```

```javascript
document.getElementById('body').addEventListener('click', (e) => {
  e.stopPropagation();
});
```