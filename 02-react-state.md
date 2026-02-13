Der folgende Button-Counter funktioniert nicht wie erwartet. Der Wert 'count' ist zu klein
bzw. scheint auf 1 zu bleiben.

```jsx
function UploadCounter() {
  const [count, setCount] = useState(0);

  async function handleFileUpload(file) {
    setCount(count + 1);
    await uploadToServer(file);
    // Bei Fehler wieder reduzieren
    if (!success) {
      setCount(count - 1);
    }
  }

  return (
    <div>
      <p>Uploads: {count}</p>
      <input type="file" multiple onChange={(e) => {
        Array.from(e.target.files).forEach(handleFileUpload);
      }} />
    </div>
  );
}
```