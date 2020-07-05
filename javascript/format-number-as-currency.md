An easy way to format numbers as currency is using `Intl.NumberFormat`:

For instance, to format numbers as brazilian currency:

```js
let currencyFormatter = new Intl.NumberFormat('pt-BR', {
  style: 'currency',
  currency: 'BRL'
});

currencyFormatter.format(10); // => R$ 10,00
```
