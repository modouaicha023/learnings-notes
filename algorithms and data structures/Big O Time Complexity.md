# Big O Time Complexity

- Big O is a way to categorize your algorithms time and memory requirements based on input
  Like when your input grow , your algorith will grow linearily.

- we use it to help make decisions about what DSA to use
  know how it will perform can help to have the best program .

Big O : "As your input grows, how fast does computation or memroy grow"
notes: growth is with respect to the input

```typescript
function sum_char_codes(n: string): number {
  let sum = 0;
  for (let i = 0; i < n.length; ++i) {
    sum += n?.charCodeAt(i);
  }
  return sum;
}
//we have a N relationship. a O(N) time complexity
```
