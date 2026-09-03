---
layout: post
title: "HTML 기본 태그 개요와 실습 정리"
date: 2026-09-01 
categories: [이야기들]
---

오늘은 HTML 개요를 간단히 훑어보고, 실제로 자주 쓰이는 태그들을 카테고리별로 배우면서 실습했다.

## 배운 태그 카테고리

| 카테고리 | 설명 |
|---------|------|
| 글자 | 텍스트를 감싸고 의미를 부여하는 태그 |
| 목록 | 순서가 있거나 없는 목록을 표현하는 태그 |
| 표 | 행/열 구조의 데이터를 표현하는 태그 |
| 영역 | 페이지의 구조를 나누는 태그 |
| 이미지 | 사진 등 시각 자료를 삽입하는 태그 |
| 미디어 | 오디오, 비디오 등을 삽입하는 태그 |
| 하이퍼링크 | 페이지 간 이동을 위한 링크 태그 |
| 폼 | 사용자 입력을 받는 태그 |

강사님께서 이 중에서도 **하이퍼링크 관련 태그**와 **폼 관련 태그**가 정말 중요하다고 강조하셨다⭐⭐ 하이퍼링크 태그는 페이지 간 이동과 내비게이션의 기본이 되고, 폼 태그는 사용자와 상호 작용하는 대부분의 서비스(로그인, 검색, 회원가입 등)에서 핵심적으로 쓰이고 있다.

## 실습

나는 배운 태그들로 직접 실습을 해보았고, 간단한 자기소개서를 만들었다. 회원 이력서 양식처럼 왼쪽에 증명사진 칸이 있고 오른쪽에 정보가 채워지는 형태로 만들어 보았다.

```html
<p style="text-align: center; font-weight: bold; font-size: 1.15em;">자기소개</p>

<table style="border-collapse: collapse; width: 100%; max-width: 640px; margin: 0 auto; border: 3px double #888;">
  <tr>
    <td rowspan="3" style="width: 150px; border: 1px solid #888; text-align: center; vertical-align: middle;">
      <img src="/assets/img/id-photo.jpg" alt="증명사진" style="width: 100%; height: 150px; object-fit: cover;">
    </td>
    <td style="border: 1px solid #888; padding: 8px 12px; width: 110px;"><strong>이름</strong></td>
    <td style="border: 1px solid #888; padding: 8px 12px;">조성원</td>
  </tr>
  <tr>
    <td style="border: 1px solid #888; padding: 8px 12px;"><strong>생년월일</strong></td>
    <td style="border: 1px solid #888; padding: 8px 12px;">2002년 3월 16일</td>
  </tr>
  <tr>
    <td style="border: 1px solid #888; padding: 8px 12px;"><strong>좋아하는 것</strong></td>
    <td style="border: 1px solid #888; padding: 8px 12px;">운동</td>
  </tr>
  <tr>
    <td style="border: 1px solid #888; padding: 8px 12px;"><strong>인생 좌우명</strong></td>
    <td colspan="2" style="border: 1px solid #888; padding: 8px 12px;">좋아하는 것을 하면 그게 곧 성공이다</td>
  </tr>
</table>
```

실제로 렌더링하면 아래처럼 왼쪽 사진 칸에 증명사진이 들어간 이력서 형태의 표가 나타난다.

<p style="text-align: center; font-weight: bold; font-size: 1.15em;">자기소개</p>

<table style="border-collapse: collapse; width: 100%; max-width: 640px; margin: 0 auto; border: 3px double #888;">
<tr>
<td rowspan="3" style="width: 150px; border: 1px solid #888; text-align: center; vertical-align: middle;" markdown="1">

![증명사진](/assets/img/id-photo.jpg){: style="width: 100%; height: 150px; object-fit: cover;" }

</td>
<td style="border: 1px solid #888; padding: 8px 12px; width: 110px;"><strong>이름</strong></td>
<td style="border: 1px solid #888; padding: 8px 12px;">조성원</td>
</tr>
<tr>
<td style="border: 1px solid #888; padding: 8px 12px;"><strong>생년월일</strong></td>
<td style="border: 1px solid #888; padding: 8px 12px;">2002년 3월 16일</td>
</tr>
<tr>
<td style="border: 1px solid #888; padding: 8px 12px;"><strong>좋아하는 것</strong></td>
<td style="border: 1px solid #888; padding: 8px 12px;">운동</td>
</tr>
<tr>
<td style="border: 1px solid #888; padding: 8px 12px;"><strong>목표</strong></td>
<td colspan="2" style="border: 1px solid #888; padding: 8px 12px;">취업하고 하고 싶은거 하면서 살기</td>
</tr>
</table>

## 느낀 점

처음에는 태그마다 쓰이는 용어(속성 이름, 태그 이름)를 외우고 활용하는 게 조금 헷갈리고 어렵게 느껴졌다. 하지만 각 태그가 어떤 "기본 틀" 안에서 동작하는지(여는 태그-속성-닫는 태그 구조)를 이해하고 나니 훨씬 수월해졌다.

## 더 학습하면 좋은 개념

- **시맨틱 태그(Semantic HTML)** — `<header>`, `<nav>`, `<section>` 처럼 의미를 가진 태그를 쓰면 접근성과 SEO에 유리하다. 영역 태그를 배웠다면 다음 단계로 꼭 짚어볼 개념이다.
- **폼 접근성 (label과 input 연결)** — 폼 태그가 중요하다고 배운 만큼, `<label for="">`로 입력 요소와 라벨을 명확히 연결하는 방법을 익히면 실무 품질이 올라간다.
- **표 접근성 (`<th scope="">`, `<caption>`)** — 단순히 표를 그리는 것을 넘어, 스크린 리더가 표 구조를 이해하도록 돕는 속성들을 배우면 좋다.