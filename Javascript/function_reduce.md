# reduce

### 🖤 arr.reduce(callback[, initialValue])

- 배열의 각 요소에 대해 주어진 리듀서(reducer) 함수를 실행한 후 하나의 결과값을 반환
- return : 배열의 순서대로, 각 요소에 callback 함수를 실행한 결과를 누적한 값

### callback function
- param 1) accumulator : callback 함수 반환값 누적. 콜백의 이전 반환값 또는 콜백의 첫 번째 호출이면서 initialValue를 제공한 경우에는 initialValue의 값
- param 2) currentValue : 배열의 현재 요소
- param 3) index : (optional) 배열 현재 요소의 인덱스. initialValue를 제공한 경우 0, 아니면 1부터 시작
- param 4) array : (optional) reduce()를 호출한 배열

### initialValue (optional)
- callback의 최초 호출에서 첫 번째 인수에 제공하는 값
- 초기값을 제공하지 않으면 배열의 첫 번째 요소를 사용
- 빈 배열에서 초기값 없이 reduce() 호출 시 TypeError 발생

Ref) https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce
