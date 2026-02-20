# Hello! 안녕하세요! 🍊

Solving Problems with Open Source. [한글 프로젝트](#대한민국의-공휴일)

- [Email](mailto:contact@hyunb.in)
- [LinkedIn](https://www.linkedin.com/in/hyunbinseo)
- [홈페이지](https://hyunb.in/)

## REST API without ANY Dependencies

Supports [Twilio], [SendGrid], [Postmark], and [more](https://github.com/hyunbinseo/new-request#services).

[Twilio]: https://www.twilio.com/en-us/messaging
[SendGrid]: https://sendgrid.com/en-us
[Postmark]: https://postmarkapp.com/

```js
import { sendEmail } from 'new-request/email/send-grid/v3/POST';

const response = await sendEmail({}); // autocompleted and type-checked
```

## Bulk Download Zoom Cloud Recordings

Backup company recordings with a single command. [Learn more](https://github.com/hyunbinseo/zoom-rec-dl#readme)

```shell
# create a urls.txt file with the recording URLs
npx zoom-rec-dl@latest # then start the download
```

## CSS Optimized for Print and Screen

Display HTML similar to PDF viewers and word processors. [Demo](https://hyunb.in/print-friendly)

```html
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/print-friendly@0.4/index.css" />
</head>
<body>
  <div class="page-container">
    <div class="page">/* Add content */</div>
  </div>
</body>
```

## 대한민국의 공휴일

월력요항 기반의 오류 없는 공개 캘린더. [더 알아보기](https://github.com/hyunbinseo/holidays-kr#readme)

- `JSON`, `CSV`, `ICS` 파일 및 호스팅 제공
<!--- 구독용 캘린더 제공 (구글, 애플 캘린더 지원)-->

```js
import { isHoliday } from '@hyunbinseo/holidays-kr';
isHoliday(new Date('2025-01-01T00:00:00+0900')); // true - 공휴일입니다.
isHoliday(new Date('2025-01-02T00:00:00+0900')); // false - 공휴일이 아닙니다.
```

## 자모야 모여라

프로그램 설치 없는 파일명 자소 분리 해결. [웹페이지](https://jamo.hyunb.in/)

```diff
# 파일을 끌어다 놓으면 수정된 파일이 다운로드 됩니다.
- ㅍㅏㅇㅣㄹㅁㅕㅇ.hwp
+ 파일명.hwp
```

## 민방위.kr

전국에서 참여 가능한 민방위 훈련 일정 조회. [웹페이지](https://민방위.kr/)
