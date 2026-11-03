# iOS 브라우저 화면녹화 오디오 지직거림 조사 기록

## 현상

- iOS의 Safari와 Chrome에서 Sauna Goyo 및 YouTube 웹페이지를 화면녹화하면 저장된 MP4의 오디오에 심한 지직거림이 발생함.
- YouTube 네이티브 앱을 화면녹화할 때는 같은 문제가 발생하지 않음.
- 녹화 당시 실시간으로 듣는 소리는 정상임.
- 저장된 화면녹화 MP4를 재생할 때만 지직거림이 들림.
- 이어폰을 사용한 녹음은 정상임.

## 첨부 MP4 기본 분석

| 파일 | 길이 | 오디오 형식 |
|---|---:|---|
| `RPReplay_Final1793348177.MP4` | 약 6.48초 | AAC, stereo, 44.1 kHz, 약 54.6 kbps |
| `RPReplay_Final1793347178.MP4` | 약 15.92초 | AAC, stereo, 44.1 kHz, 약 90.3 kbps |

두 파일 모두 iOS 화면녹화에서 일반적으로 생성되는 AAC 오디오 트랙을 포함하고 있음.

현재 분석 환경에서는 MP4 오디오를 PCM으로 디코딩할 도구가 없어 RMS, 클리핑률, 주파수 스펙트럼까지는 계산하지 못함.

## 현재 판단

가장 유력한 원인은 Sauna Goyo의 음원 파일이나 일반 재생 코드가 아니라, iOS가 브라우저 오디오를 화면녹화용 오디오로 캡처·믹싱·인코딩하는 과정의 문제임.

근거:

1. 녹화 중 실시간 청취는 정상임.
2. 저장된 MP4에서만 문제가 발생함.
3. 이어폰 녹음은 정상임.
4. Safari와 Chrome 모두에서 발생함. iOS용 Chrome도 WebKit 기반이므로 공통 엔진 문제가 가능함.
5. YouTube 네이티브 앱에서는 발생하지 않아 브라우저 오디오 경로와의 차이가 확인됨.

따라서 현재는 프로젝트의 오디오 파일을 재인코딩하거나 gain 값을 임의로 낮추는 수정의 우선순위가 낮음.

## 관련 외부 사례

- [WebKit bug 231191](https://bugs.webkit.org/show_bug.cgi?id=231191): iOS Safari 및 Chrome에서 `getUserMedia`와 echo cancellation 사용 시 crackle이 발생한 사례. 구형·저사양 기기에서 특히 재현됨.
- [WebKit bug 326286](https://bugs.webkit.org/show_bug.cgi?id=326286): iOS 26.2~27에서 마이크와 echo cancellation이 활성화된 웹페이지의 오디오 출력이 crackle되는 사례.
- [Apple Developer Forums 사례](https://developer.apple.com/forums/thread/818594): iOS 26에서 화면녹화 결과물의 오디오가 깨지는 문제와 `IOBufferDuration` 관련 가능성이 보고됨.

## 남은 확인 사항

다음 테스트 결과가 있으면 원인을 더 좁힐 수 있음.

1. 화면녹화 제어센터에서 마이크를 끈 상태와 켠 상태 비교
2. 같은 기기에서 내장 스피커와 이어폰으로 각각 녹화
3. Safari와 Chrome에서 동일한 짧은 순음 또는 YouTube 영상 녹화
4. 문제가 발생하는 iOS 버전과 기기 모델 기록
5. 페이지의 마이크 권한을 차단한 상태에서 재현 여부 확인
6. Sauna Goyo 페이지에서 `getUserMedia`, `echoCancellation`, `AudioContext`, `AudioWorklet` 사용 여부 확인

## 조치 결론

현재 증거만으로는 프로젝트 코드 수정이 필요하다고 보기 어려움.

우선은 현 상태를 유지하고, 문제가 발생한 기기·iOS 버전·브라우저·마이크 설정을 기록하는 것이 적절함. iOS 업데이트 후 동일 테스트를 다시 수행하고, 프로젝트 코드와 관련된 재현 조건이 확인될 때만 수정 검토.

이번 조사에서는 프로젝트 파일을 수정하지 않음.
