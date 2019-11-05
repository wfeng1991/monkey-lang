# monkey-lang
writing an interpreter in go中monkey语言实现，支持first class function

### let binding
```
let age = 1;
let name = "Monkey";
let result = 10 * (20 / 2);
```

### 数组&hash
```
let myArray = [1, 2, 3, 4, 5];
let thorsten = {"name": "Thorsten", "age": 28};
myArray[0]       // => 1
thorsten["name"] // => "Thorsten
```

### function
```
let add = fn(a, b) { return a + b; };

let fibonacci = fn(x) {
  if (x == 0) {
    0
  } else {
    if (x == 1) {
      1
    } else {
      fibonacci(x - 1) + fibonacci(x - 2);
    }
  }
};

let twice = fn(f, x) {
  return f(f(x));
};

let addTwo = fn(x) {
  return x + 2;
};

twice(addTwo, 2); // => 6
```

### buildin function
```
len("a"); // => 1
let a = [1, 2, 3, 4];
fisrt(a); // => 1
rest(a); // => [2, 3, 4]

```
