---
$title: 써드 파티 콘텐츠 가져오기
---
[TOC]


페이지에서 써드 파티 컴포넌트를 가져오는 법에 대해서 다룹니다.

## 트윗 가져오기

페이지에 트위터 트윗을 가져올 때
[`amp-twitter`](/ko/docs/reference/components/amp-twitter.html) 요소를 사용합니다.

트위터를 페이지에 추가하고자 할 때,
`<head>` 요소 안에 아래 스크립트를 먼저 가져와야 합니다.

[sourcecode:html]
<script async custom-element="amp-twitter"
  src="https://cdn.ampproject.org/v0/amp-twitter-0.1.js"></script>
[/sourcecode]

현재 트윗은 자동으로 제공된 사이즈에 비례하여 크기가 조정되지만, 원하는 크기에 미치지 않을 수도 있습니다.

수동으로 width와 height를 제공하여 조정하거나,
스크린 width에 기반한 해상도를 선택하는 media 속성을 사용할 수 있습니다.

<!-- embedded twitter example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.twitter.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div>
</amp-iframe>
</div>

도움말: [AMP By Example](https://ampbyexample.com/components/amp-twitter/)에서 더 많은 `amp-twitter` 예시를 확인하세요.

## 인스타그램 가져오기

페이지에 인스타그램을 가져올 때
[`amp-instagram`](/ko/docs/reference/components/amp-instagram.html) 요소를 사용합니다.

인스타그램을 페이지에 추가하고자 할 때,
`<head>` 요소 안에 아래 스크립트를 먼저 가져와야 합니다.

[sourcecode:html]
<script async custom-element="amp-instagram"
  src="https://cdn.ampproject.org/v0/amp-instagram-0.1.js"></script>
[/sourcecode]

인스타그램 사진 URL을 찾기 위해 인스타그램 data-shortcode를 추가해야합니다.
예를 들어, `https://instagram.com/p/fBwFP`에서 `fBwFP`가  data-shortcode 입니다.

또한 인스타그램은 반응형 레이아웃을 위한 고정 해상도를 사용하기 때문에,
width와 height 값은 전역으로 사용해야합니다.

<!-- embedded Instagram example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.instagram.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div>
</amp-iframe>
</div>

도움말: [AMP By Example](https://ampbyexample.com/components/amp-instagram/)에서 더 많은 `amp-instagram` 예시를 확인하세요.

## 페이스북 포스트나 비디오 보여주기

페이지에서 페이스북 포스트나 비디오를 보여줄 때는
[`amp-facebook`](/ko/docs/reference/components/amp-facebook.html) 요소를 사용합니다.

아래 스크립트를 `<head>` 안에 추가해야합니다:

[sourcecode:html]
<script async custom-element="amp-facebook"
  src="https://cdn.ampproject.org/v0/amp-facebook-0.1.js"></script>
[/sourcecode]

##### 예시 - 포스트 가져오기

출처:
```html
<amp-facebook width="486" height="657"
    layout="responsive"
    data-href="https://www.facebook.com/zuck/posts/10102593740125791">
</amp-facebook>
```
시사:
<amp-facebook width="486" height="657"
    layout="responsive"
    data-href="https://www.facebook.com/zuck/posts/10102593740125791">
</amp-facebook>

##### 예시 - 비디오 가져오기

출처:
```html
<amp-facebook width="476" height="316"
    layout="responsive"
    data-embed-as="video"
    data-href="https://www.facebook.com/nasaearth/videos/10155187938052139">
</amp-facebook>
```
시사:
<amp-facebook width="476" height="316"
    layout="responsive"
    data-embed-as="video"
    data-href="https://www.facebook.com/nasaearth/videos/10155187938052139">
</amp-facebook>

도움말: [AMP By Example](https://ampbyexample.com/components/amp-facebook/)에서 더 많은 `amp-facebook` 예시를 확인하세요.

## 유튜브 비디오 가져오기

페이지에 유튜브 비디오를 가져올 때는
[`amp-youtube`](/ko/docs/reference/components/amp-youtube.html) 요소를 사용합니다

아래 스크립트를 `<head>` 안에 추가해야합니다:

[sourcecode:html]
<script async custom-element="amp-youtube"
  src="https://cdn.ampproject.org/v0/amp-youtube-0.1.js"></script>
[/sourcecode]

유튜브 `data-videoid` 속성은 유튜브 비디오 페이지 URL을 찾게 해줍니다.
예를 들어, https://www.youtube.com/watch?v=Z1q71gFeRqM 에서
Z1q71gFeRqM가 video id입니다.

16:9 해상도 비디오의 정확한 레이아웃을 위해 `layout="responsive"`를 사용하길 바랍니다:

<!-- embedded youtube example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/responsive.youtube.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div>
</amp-iframe>
</div>

도움말: [AMP By Example](https://ampbyexample.com/components/amp-youtube/)에서 더 많은 `amp-youtube` 예시를 확인하세요.

## 광고 보여주기

페이지에서 광고를 보여줄 때는
[`amp-ad`](/ko/docs/reference/components/amp-ad.html) 요소를 사용합니다.
HTTPS로 제공한 광고만 지원합니다.

AMP 문서 내에서 자바스크립트로 제공하는 광고 네트워크는 허용하지 않습니다.
대신해 AMP 런타임은 다른 오리진(iframe sandbox)으로부터 iframe을 불러오며
해당 iframe sandbox 내에서 광고 네트워크 JS를 실행합니다.

광고에 반드시 width, height, 광고 네트워크 타입을 정의해야합니다.
`type` 식별자는 광고 네트워크의 템플릿입니다.
다른 광고 타입은 다른 `data-*` 속성을 필요로 합니다.

<!-- embedded ad example -->
<div>
<amp-iframe height="212"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.ad-basic.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div>
</amp-iframe>
</div>


만약 광고 네트워크가 지원한다면,
`placeholder`를 넣어서 광고가 불가한 경우에 보여줄 수 있습니다:

<!-- embedded ad example -->
<div>
<amp-iframe height="232"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.ad-placeholder.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div>
</amp-iframe>
</div>

AMP는 광범위한 광고 네트워크를 지원합니다.
[reference for a full list](/ko/docs/reference/components/amp-ad.html#supported-ad-networks)를 참고하시길 바랍니다.

읽어보기: [AMP에 광고 게재](/ko/docs/ads/monetization.html) 가이드에서 광고에 관해 자세히 알아보세요.
