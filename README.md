# Hello! 안녕하세요! 🍊

![Svelte](https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white) ![Firefox](https://img.shields.io/badge/Firefox-FF7139?style=for-the-badge&logo=Firefox-Browser&logoColor=white) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)

Solving Problems with Open Source. [한글 프로젝트](#대한민국의-공휴일)

Contact: [LinkedIn], [Email]

[LinkedIn]: https://www.linkedin.com/in/hyunbinseo
[Email]: mailto:contact@hyunb.in

## Self-host Svelte Applications

Almost as simple as Vercel and Cloudflare Pages. [Learn more](https://github.com/hyunbinseo/svelte-kitty#readme)

```shell
npm create svelte-kitty # setup project and database
npm run deploy # build and deploy to a Linux server
```

- 🔒 Includes email based authentication, user and role management.
- 📦 Fully configured [Drizzle ORM], [Tailwind CSS], [Valibot] out-of-the box.

[Drizzle ORM]: https://orm.drizzle.team/
[Tailwind CSS]: https://tailwindcss.com/
[Valibot]: https://valibot.dev/

## Better DX for Svelte Form and Modal

Form state management. Disable buttons during submission. [Learn more](https://github.com/hyunbinseo/svelte-form-enhanced#readme)

```svelte
<script>
  import { enhance } from '$app/forms';
  import { createFormHelper } from 'svelte-form-enhanced';
  const f = createFormHelper();
</script>

<form method="post" use:enhance={f.submitFunction}>
  <button disabled={f.state === 'submitting'}>
    {f.state === 'submitting' ? 'Submitting' : 'Submit'}
  </button>
</form>
```

Open and close an HTML [modal](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement/showModal) by toggling a boolean state. [Demo](https://svelte.dev/playground/7ffaea50f0c0466ea2b4be8e0aee20dd?version=5.2.7)

```svelte
<script>
  import { Modal } from 'svelte-html-modal';
  let isOpen = $state(false);
</script>

<button type="button" onclick={() => (isOpen = true)}>Open Modal</button>

<div class="modal-wrapper">
  <Modal bind:isOpen closeOnBackdropClick={true}>
    <button type="button" onclick={() => (isOpen = false)}>Close</button>
  </Modal>
</div>
```

## REST API without ANY Dependencies

Supports [Twilio] SMS, [SendGrid] and [Postmark] email, and [more](https://github.com/hyunbinseo/new-request#services).

[Twilio]: https://www.twilio.com/en-us/messaging
[SendGrid]: https://sendgrid.com/en-us
[Postmark]: https://postmarkapp.com/

```js
import { sendEmail } from 'new-request/email/send-grid/v3/POST/index.js';

const response = await sendEmail({
  // Utilizes the Fetch API and TypeScript types.
  // Everything is autocompleted and type-checked.
});
```

## Bulk Download Zoom Cloud Recordings

Backup company recordings with a single command. [Learn more](https://github.com/hyunbinseo/zoom-rec-dl#readme)

```shell
# create a urls.txt file with the recording URLs
npx zoom-rec-dl@latest # then start the download
```

## CSS Optimized for Print and Screen

Pages are displayed like PDF viewers and word processors. [Demo](https://hyunb.in/print-friendly)

```html
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/print-friendly@0.3/index.css" />
  </head>
  <body>
    <div>
      <div class="page">/* Add content */</div>
    </div>
  </body>
</html>
```

## 대한민국의 공휴일

월력요항 기반의 오류 없는 공개 캘린더. [더 알아보기](https://github.com/hyunbinseo/holidays-kr#readme)

- `JSON`, `CSV`, `ICS` 파일 및 호스팅 제공
- 캘린더 구독 제공 (구글, 애플 캘린더 지원)

```js
import { isHoliday } from '@hyunbinseo/holidays-kr';
isHoliday(new Date('2025-01-01T00:00:00+0900')); // true - 공휴일입니다.
isHoliday(new Date('2025-01-02T00:00:00+0900')); // false - 공휴일이 아닙니다.
```

## 자모야 모여라

프로그램 설치 없는 파일명 자소 분리 해결. [웹페이지](https://jamoya.one/)

```diff
# 파일을 끌어다 놓으면 수정된 파일이 다운로드 됩니다.
- ㅍㅏㅇㅣㄹㅁㅕㅇ.hwp
+ 파일명.hwp
```

## 민방위.kr

전국에서 참여 가능한 민방위 훈련 일정 조회. [웹페이지](https://민방위.kr/)
