# postMessage
- postMessage를 통해서 iframe(youTube) 제어

## 유튜브

#### func
- postMessage로 전달할 함수(명령)

  - playVideo: 동영상 시작
  - pauseVideo: 동영상 일시정지
  - stopVideo: 동영상 정지
  - mute: 음소거
  - unMute: 소리 있음
  
#### args
- func의 인자(전달할 값)
- [ ]로 전달

```
var message = JSON.stringify({
  event: "command"
  ,func: "playVideo"
  ,args: []
});
$("#youtube-iframe")[0].contentWindow.postMessage(message, "*");
```
```
$("#youtube-iframe")[0].contentWindow.postMessage('{"event":"command","func":"playVideo","args":""}', "*");
```

## 비메오

#### method
- postMessage로 전달할 함수(명령)

  - play: 동영상 시작
  - pause: 동영상 일시정지
  - unload: 동영상 정지
  - setVolume: 소리 설정(value: 0 ~ 1 설정 필요!)

#### value
- method의 인자(전달할 값)

```
var message = JSON.stringify({
  method: "setVolume"
  ,value: "0.5"
});
$("#youtube-iframe")[0].contentWindow.postMessage(message, "*");
```
```
$("#youtube-iframe")[0].contentWindow.postMessage('{"method":"setVolume","value":"0.5"}', "*");
```
