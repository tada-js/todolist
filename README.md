# To-do-list

<br>

## 바닐라JS 첫 도전!

### 무엇을 구현 했나요?

- 실시간 시계
- 로컬 스토리지를 사용한 로그인
- 로컬 스토리지를 사용한 todolist
- 랜덤 배경 이미지
- 날씨와 위치 (geolocation)

<br>

### 어떻게 구현 했나요?

- ES6 문법으로 라이브러리 사용 없이 바닐라JS로 구현

<br>

⏳
.
.
.
.
.
⌛

##### 완성(구현)을 끝으로 두지 않고 앞으로 꾸준한 학습을 통해 리팩토링을 지속적으로 할 예정입니다. 그동안 무엇을 배웠고 무엇을 몰랐는지 확인할 것입니다!

<br><br><br>

## 완성 이후 진행 상황

### 무엇이 바뀌었나요?
- `parcel-bundler`로 개발 서버 오픈!
- css를 보다 효율적인 코드로 작성하기 위해 scss 학습 시작!

### 어떤 문제들이 발생하였나요?
- `index.html` 파일이 `parcel-bundler`로 인해 변환돼서 `dist` 폴더에 삽입되는지를 인지하지 못했습니다. 그 결과로 `background image`가 출력이 안 되었습니다.

### 어떻게 해결 방법으로 접근 하였나요?
- 해결 방안을 좁히기 위해 어떤 변화 이후에 문제가 발생하였는지 생각해 보았습니다.
- 첫 번째로는 `scss` 파일 생성이었고, 두 번째는 `parcle-bundler` 설치였습니다.
- 제일 쉬운 `scss` 파일 연결 방식, 연결 코드들을 확인해 보았으나 이상이 없어 보였습니다.
- `parcle-bundler` 문제로 추측되어 한참 찾아보다 `index.html`이 변환돼서  `dist` 폴더로 삽입된다는 것을 알게 되었고 이때 `JavaScript` 파일 뿐만 아니라 `img` 파일도 앞에 기호들이 붙게 되는데 여기서 문제가 발생했던 겁니다. 즉, 파일이 `img.go3fg0z.jpg` 로 바뀌었는데 `img.jpg` 로 불러오려 했으니 출력이 안되었죠.
- `parcel plugin static files copy`를 통해 정적 파일 연결 패키지를 설치해 주고 `package.json` 파일에 `staticFiles`를 추가해주어 정적 파일 연결이 되었고 그 결과로 `background image`가 정상적으로 출력 되었습니다!🎉
