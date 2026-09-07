# DevKin — Raycast 익스텐션

Raycast에서 DevKin의 원하는 기능 탭을 바로 열 수 있습니다.  
각 커맨드는 `devkin://...` 딥링크를 트리거하는 **no-view** 액션이며,
DevKin macOS 앱이 이를 인터셉트해 해당 화면으로 바로 라우팅합니다.

## 사전 조건

- macOS에 Raycast 설치
- DevKin 앱 설치 (최초 실행 시 URL 스킴이 자동 등록됩니다)

## 개발 모드로 직접 사용하기

```sh
cd raycast-devkin
npm install
npm run dev
```

`npm run dev`가 실행 중인 상태에서 Raycast가 익스텐션을 자동으로 인식합니다.  
`⌘ Space`를 누르고 아래 커맨드 이름 중 하나를 입력하면 됩니다.

## 커맨드 목록

| Raycast에서 입력 | 열리는 기능 |
| --- | --- |
| `Byte Converter` | 바이트/SI/IEC 단위 변환기 |
| `Length Converter` | 길이 단위 변환기 (mm/cm/m/km · in/ft/yd/mi) |
| `Base Converter` | 진수 변환기 (2 · 8 · 10 · 16진수) |
| `JSON Converter` | JSON 트리 뷰어 |
| `Base64 String Converter` | Base64 문자열 인코드/디코드 |
| `Base64 Image Converter` | Base64 이미지 인코드/디코드 |
| `JWT Converter` | JWT 디코더 & 시그니처 검증/생성기 |
| `SQL Formatter` | SQL 포매터 |
| `Text Diff` | 좌우 비교 텍스트 디프 |
| `Text Inspector` | 실시간 글자/단어/바이트 카운터 |
| `Markdown Preview` | 실시간 마크다운 렌더러 |
| `Markdown Preview (md)` | 위와 동일 — `md` 단축 입력용 별칭 |
| `HTML Preview` | 샌드박스 HTML 미리보기 |
| `QR Code Converter` | QR 코드 생성기 & 디코더 (URL · Wi-Fi · vCard 등) |
| `Regex Tester` | 정규식 테스터 (라이브 매칭 하이라이트) |
| `Time Converter` | 타임스탬프/날짜 변환기 (epoch · ISO · UTC · KST) |

키워드도 등록되어 있어서 `kb`, `decode`, `query` 등 부분 입력으로도 원하는 커맨드를
찾을 수 있습니다.

## Raycast Store 배포 (선택)

```sh
cd raycast-devkin
npm run publish
```

Raycast 심사 대기열을 통해 배포됩니다. Homebrew tap과는 독립적인 절차입니다.
