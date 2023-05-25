# ES6

## 1. for each
for문 등 반복문 대신 사용 <br>
예) for문으로 배열 i번째를 출력하는데 for each 대신 사용

```javascript
arr.forEach(함수);
arr.forEach((value,index)=>{  });
```
- Array객체에서 사용이 가능
- 일반 for문보다 가독성이 좋고, 객체형을 다루기 쉬움
- return값을 받지 못함 (반환값이 없음)
- 콜백 함수에는 첫 번재 인자에는 배열에서 조회하는 값, 두 번째 인자에는 순서(index)가 들어감

<br>

## 2. map
for문 등 반복문 대신 사용

```javascript
arr.map(함수);
let data = arr.map((item, index)=>{
	return item
});
console.log(item); 
```
- for each과 다르게 return값 자체를 반환
- chainable함
- 대용량 배열 처리시 메모리 overflow 가능성이 있음
- Array객체에서 사용이 가능

<br>

## 3. reduce
(제대로 공부할 것💥)
```javascript
var arr= [1, 2, 3, 4, 5];
var newArr= arr.reduce(function(acc, v, i, arr) {
return acc+ v;
});
// 15
```

## 4. filter
특정 조건에 일치하는 요소만 배열에 담고 싶을 때 사용

```javascript
const fruits = [
  {name: "Apple", price: 1000},
  {name: "Banana", price: 5000},
  {name: "Grape", price: 4000},
  {name: "Watermelon", price: 20000},
]

const chipFruits = fruits.filter((fruit) => {
  return fruit.price < 5000;
})
console.log(chipFruits);
//[{name: "Apple", price: 1000}, {name: "Grape", price: 4000}]
```
## 5. Lambda Cun