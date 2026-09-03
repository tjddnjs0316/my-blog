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
| 글자 관련 | 텍스트를 감싸고 의미를 부여하는 태그 |
| 목록 관련 | 순서가 있거나 없는 목록을 표현하는 태그 |
| 표 관련 | 행/열 구조의 데이터를 표현하는 태그 |
| 영역 | 페이지의 구조를 나누는 태그 |
| 이미지 | 사진 등 시각 자료를 삽입하는 태그 |
| 미디어 | 오디오, 비디오 등을 삽입하는 태그 |
| 하이퍼링크 | 페이지 간 이동을 위한 링크 태그 |
| 폼 관련 | 사용자 입력을 받는 태그 |

이 중에서도 **하이퍼링크**와 **폼 관련 태그**가 정말 중요하다고 강조받았다⭐⭐ 하이퍼링크는 페이지 간 이동과 내비게이션의 기본이 되고, 폼 태그는 사용자와 상호 작용하는 대부분의 서비스(로그인, 검색, 회원가입 등)에서 핵심적으로 쓰이기 때문이다.

## 실습

표(table)와 미디어(media) 태그를 직접 사용해 실습했다.

### 표 태그로 자기소개 만들기

```html
<table>
  <tr>
    <th>이름</th>
    <td>조성원</td>
  </tr>
  <tr>
    <th>관심 분야</th>
    <td>서비스 기획, 홍보</td>
  </tr>
  <tr>
    <th>좋아하는 노래</th>
    <td>성시경 - 거리에서</td>
  </tr>
</table>
```

| 이름 | 조성원 |
|------|--------|
| 관심 분야 | 서비스 기획, 홍보 |
| 좋아하는 노래 | 성시경 - 거리에서 |

### 미디어 태그로 좋아하는 노래 삽입하기

가장 좋아하는 노래인 성시경의 "거리에서"를 유튜브 영상으로 삽입해봤다.

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/qx4xDFP2WDU" title="성시경 - 거리에서" frameborder="0" allowfullscreen></iframe>
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/qx4xDFP2WDU" title="성시경 - 거리에서" frameborder="0" allowfullscreen></iframe>

## 느낀 점

처음에는 태그마다 쓰이는 용어(속성 이름, 태그 이름)를 외우고 활용하는 게 조금 헷갈렸다. 하지만 각 태그가 어떤 "기본 틀" 안에서 동작하는지(여는 태그-속성-닫는 태그 구조)를 이해하고 나니 훨씬 수월해졌다. 처음 보는 용어는 어렵게 느껴져도, 기본 구조만 이해하고 나면 응용은 오히려 쉬워진다는 걸 체감했다.

## 더 학습하면 좋은 개념

- **시맨틱 태그(Semantic HTML)** — `<header>`, `<nav>`, `<section>` 처럼 의미를 가진 태그를 쓰면 접근성과 SEO에 유리하다. 영역 태그를 배웠다면 다음 단계로 꼭 짚어볼 개념이다.
- **폼 접근성 (label과 input 연결)** — 폼 태그가 중요하다고 배운 만큼, `<label for="">`로 입력 요소와 라벨을 명확히 연결하는 방법을 익히면 실무 품질이 올라간다.
- **표 접근성 (`<th scope="">`, `<caption>`)** — 단순히 표를 그리는 것을 넘어, 스크린 리더가 표 구조를 이해하도록 돕는 속성들을 배우면 좋다.

## 참고 자료

- [MDN - HTML 기본 개념](https://developer.mozilla.org/ko/docs/Learn/HTML/Introduction_to_HTML)
- [MDN - 하이퍼링크(a 태그)](https://developer.mozilla.org/ko/docs/Web/HTML/Element/a)
- [MDN - 폼 관련 태그](https://developer.mozilla.org/ko/docs/Learn/Forms)
