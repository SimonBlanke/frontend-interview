Ein Benutzer tippt in ein Suchfeld, um Zeitreihen-Datensatze zu filtern.
Was ist das Problem mit dieser Umsetzung?

```javascript
function SearchBar({ onSearch }) {
  return (
    <input
      type="text"
      onChange={(e) => onSearch(e.target.value)}
      placeholder="Datensatz suchen..."
    />
  );
}
```