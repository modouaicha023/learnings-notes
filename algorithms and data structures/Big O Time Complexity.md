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

```typescript
function sum_char_codes(n: string): number {
  let sum = 0;
  for (let i = 0; i < n.length; ++i) {
    sum += n?.charCodeAt(i);
  }
   for (let i = 0; i < n.length; ++i) {
    sum += n?.charCodeAt(i);
  }
  return sum;
}
//we have a N relationship. a O(N) (speak: ovène) time complexity
```


```typescript
function sum_char_codes(n: string): number {
  let sum = 0;
  
  for (let i = 0; i < n.length; ++i) {
    const charCode = n.charCodeAt(i);
    
    //capital E
    if(charCode===69){
      return sum
    }
    sum+=charCode
  }
  
  return sum
  
}
//we have a N relationship. a O(N) (speak: ovène) time complexity
// In BigO we often consider the worst case (like the E is in the last caracter of the input , it's still O(N)
```

# Important concepts 
- growth is with the respect to the input 
- Constants are dropped
- Worst case is usually the way we measure

# The common complexities

<img src ="./images/bigOgraph.png"/>

# some examples 

- O(N^2)

```typescript
function sum_char_codes(n: string): number {
  let sum = 0;
  for (let i = 0; i < n.length; ++i) {
    for (let j = 0; j < n.length; ++j) {
      sum += charCode;
    }
  }
  return sum;
}
```

- O(N^3)

```typescript
function sum_char_codes(n: string): number {
  let sum = 0;
  for (let i = 0; i < n.length; ++i) {
    for (let j = 0; j < n.length; ++j) {
      for (let j = 0; j < n.length; ++j) {
        sum += charCode;
      }
    }
  }
  return sum;
}
```

- O(n log n)

- O(n log n)
  - Binary search trees 

- O(sqrt(n)) {to be search !!!!!!!!}