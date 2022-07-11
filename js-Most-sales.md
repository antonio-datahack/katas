* ![link to exercise](https://www.codewars.com/kata/5e16ffb7297fe00001114824/train/javascript)

Description:

You work in the best consumer electronics corporation, and your boss wants to find out which three products generate the most revenue. Given 3 lists of the same length like these:

    products: ["Computer", "Cell Phones", "Vacuum Cleaner"]
    amounts: [3, 24, 8]
    prices: [199, 299, 399]

return the three product names with the highest revenue (amount * price).

Note: if multiple products have the same revenue, order them according to their original positions in the input list.



```js
function top3(products, amounts, prices) {
  let newArr = []
  let sortedProducts = []
  let top3 = []
  
  for (let i=0; i < products.length; i++) {
    newArr.push({'products': products.slice(i, i+1).join(), "revenue": amounts.slice(i,i+1).join() * prices.slice(i,i+1).join(), "index": i})
  }
    sortedProducts = newArr.sort((a, b) => b.revenue - a.revenue || a.index -b.index);
    top3 = sortedProducts.map(obj => obj.products)
  return top3.slice(0,3)
}
```
