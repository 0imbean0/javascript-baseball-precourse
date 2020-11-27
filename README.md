# ⚾ 미션 - 숫자 야구 게임

## 📝 스토리보드

1.  게임 시작
      1. 컴퓨터 랜덤 값 세팅
            1.  서로 다른 세 개의 랜덤 숫자 생성
      2. 유저 입력 값 받기
            1. 서로 다른 세 개의 숫자인지 확인
            2. 아닐 경우 `alert` 메세지를 띄우고 입력 값 다시 받기 
2.  게임 진행
       1.  컴퓨터 랜덤 값과 유저 입력 값 비교
             1. 유저 입력 값의 각 자리 수를 컴퓨터 랜덤 값과 비교
             2. 값과 인덱스가 같으면 스트라이크 ++1
             3. 값만 같으면 볼 ++1
       2.  결과 출력
             1. 두 값이 모두 0이면, "낫싱" 출력.  (1 - 2)로 이동
             2. 스트라이크 값이 3이면,  "정답을 맟추셨습니다." 출력. (3 - 1)로 이동
             3. "{$볼}볼과 {$스트라이크}스트라이크" 출력.  (1 - 2)로 이동
3.  게임 종료
       1.  `게임 재시작` 버튼과 "게임을 새로 시작하시겠습니까?" 출력.
       2.   `게임 재시작` 버튼을 누르면,  (1 - 1)로 이동

## 💻 기능 구현 

**컴퓨터 랜덤 값 세팅(setTargetNumber)** ✅

- `Math.floor()` , `Math.random()`, `indexOf()` 를 사용하여 로또 번호 뽑기와 같은 방식으로 구현하였다.

**유저 입력 값 받기(getInputNumber)** ✅

- `document.getElementById()` 와  `addEventListener()` 를 사용하여 유저의 입력 값을 가져온다.

- 유저가 값을 입력하면 `isNaN()`,  `userInput.length !== 3`, `isDuplication()` 세 가지 검증을 진행한다. 

  (값이 숫자가 아닐 경우에는 `userInput` 을 `''` 로 초기화시키지만, 숫자일 경우 실수로 입력된 경우를 고려하여 초기화하지 않기로 하였다.)

- 하나의 함수로 구현하기에는 가독성이 좋지않아서 `isDuplication()` 기능(중복 숫자 검사)을 추가로 구현하였다.

**게임 진행(play - 프로그래밍 요구사항)** ✅

- `compareNumbers()` 와 `printResult()` 를 사용하여 "결과 값 String"을 `return` 한다.

**컴퓨터 랜덤 값과 유저 입력 값 비교(compareNumbers)** ✅

- `indexOf` 를 사용하여 값을 비교한다

  (for문의 `i` 와 `indexOf` 의 `index` 값이 같으면 스트라이크, 다르면서 -1이 아니면 볼)

- 처음에는 이중 for문으로 구현하였는데, depth가 깊어져서 수정하였다.

**결과 출력(printResult)** ✅

- 조건문을 사용하여 볼과 스트라이크의 값에 따라 네 가지로 분기하였다.

  (볼과 스트라이크 모두 0이면 "낫싱", 스트라이크가 3이면 "🎉정답을 맞추셨습니다!🎉", 볼이 0이 아니면 "${ball}볼", 스트라이크가 0이 아니면 "${strike}스트라이크" 추가)

**게임 재시작(replay)**

