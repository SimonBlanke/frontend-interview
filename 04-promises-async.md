In welcher Reihenfolge erscheinen die Ausgaben?

```javascript
async function fetchForecasts() {
  console.log("1 - Start");

  const promise = new Promise((resolve) => {
    console.log("2 - Promise erstellt");
    setTimeout(() => {
      console.log("3 - Timeout ausgefuehrt");
      resolve("Forecast-Daten");
    }, 0);
  });

  console.log("4 - Vor await");

  const data = await promise;
  console.log("5 - Daten erhalten:", data);

  return data;
}

console.log("6 - Vor Funktionsaufruf");
fetchForecasts().then((d) => console.log("7 - Then:", d));
console.log("8 - Nach Funktionsaufruf");
```