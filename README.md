# 궤도 — 우주 탐험 퀴즈

열 개의 질문으로 우주를 탐험하는 한국어 퀴즈 앱이당. 답변 직후 정답과 해설을 확인하고, 탐험을 마치면 점수·정답률과 함께 틀린 문제를 복습할 수 있당. 결과 복사와 다시하기, 숫자키·키보드 조작, 라이트·다크 테마 및 모션 감소 설정을 지원한당.

## 로컬 실행

저장소를 내려받은 뒤 프로젝트 루트에서 다음 명령을 실행하면 된당.

```sh
open index.html
```

macOS 이외의 환경에서는 `index.html`을 브라우저로 직접 열면 된당. 통합 브라우저에서도 현재 작업 폴더의 `index.html`을 `file://` URL로 열 수 있당.

앱은 CSS·JavaScript·SVG를 모두 포함한 `index.html` 하나로 실행되며, 설치·빌드·서버·외부 네트워크 요청이 필요하지 않당. 숫자키 `1`–`4`로 답을 선택하거나 Tab으로 버튼을 이동한 뒤 Enter·Space로 조작할 수 있당. 브라우저가 자동 복사를 지원하지 않거나 권한을 거부하면 읽기 전용 공유 문구에서 직접 복사할 수 있당.

## GitHub Pages 배포

사이트 주소: [https://rsh0770.github.io/space-quiz/](https://rsh0770.github.io/space-quiz/)

`.github/workflows/pages.yml`은 `main`을 대상으로 하는 PR과 `main` 푸시에서 인라인 JavaScript 구문을 검사한당. `main` 푸시 또는 `main`에서의 수동 실행은 검사가 통과하면 `index.html`만 배포 아티팩트에 담아 GitHub Pages에 게시한당. README나 저장소 설정 파일은 게시하지 않당.

저장소 **Settings → Pages → Build and deployment → Source**는 **GitHub Actions**로 설정해야 한당. 배포 결과는 **Actions → GitHub Pages**에서 확인할 수 있당.

## 기능 확인

페이지를 새로고침하고 `3`을 누르면 첫 문항 정답으로 10점과 `1 / 10 완료`가 표시된당. 열 문항을 완료하면 결과 화면에서 틀린 문제 복습을 펼쳐 질문·선택한 답·정답·해설을 읽을 수 있고, 모두 맞히면 별도 안내가 표시된당. 다시하기는 점수와 답변 기록을 초기화한당.

상세한 상태 흐름과 브라우저 검증 시나리오는 [저장소 지침](.github/copilot-instructions.md)에 정리되어 있당.
