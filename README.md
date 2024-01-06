# 白嫖大师课
```js
$effect(() => {
  $form.query("sale_delivery_item").take((target) => {
    const result = (target?.value || []).reduce((prev, cur) => {
      return Number(prev) + Number(cur.total)
    }, 0)
    console.log(result)
    $form.setValuesIn("sum", result)
  })
}, [$deps.outbound_count, $deps.sale_price_taxin])
```
