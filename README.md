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

**컴퓨터 랜덤 값 세팅(setTargetNumber)**

**유저 입력 값 받기(getInputNumber)**

**게임 진행(play)**

**컴퓨터 랜덤 값과 유저 입력 값 비교(compareNumbers)**

**결과 출력(printResult)**

**게임 재시작(replay)**

