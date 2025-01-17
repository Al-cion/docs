---
$title: Integrating with AMP to serve display ads
$order: 4
toc: true
---

[TOC]

This guide is for ad networks that want to integrate with AMP to serve display ads to AMP pages.

## Overview

As an ad server, you can integrate with AMP to serve traditional HTML ads to AMP pages, as well as serving [AMPHTML](/docs/ads/amphtml_ads.html) ads.

##### Want to serve traditional HTML ads?

1.  [Create an amp-ad implementation](#creating-an-amp-ad-implementation)

##### Want to serve AMPHTML ads?

1. [Create an amp-ad implementation](#creating-an-amp-ad-implementation) (i.e., if you haven't already created one to serve traditional HTML ads).
2. [Create a Fast Fetch integration to serve AMPHTML ads](#creating-a-fast-fetch-integration).


## Creating an amp-ad implementation

As an ad server, publishers you support include a JavaScript library provided by you and place various "ad snippets" that rely on the JavaScript library to fetch ads and render them on the publisher's website. Because AMP doesn't allow publishers to execute arbitrary JavaScript, you will need to contribute to the AMP open-source code to allow the [`amp-ad`](/docs/reference/components/amp-ad.html)  tag to request ads from your ad server.

Note: You can use this amp-ad implementation to display traditional HTML ads **and** AMPHTML ads.

For example, the Amazon A9 server can be invoked by using following syntax:

```html
<amp-ad width="300" height="250"
    type="a9"
    data-aax_size="300x250"
    data-aax_pubname="test123"
    data-aax_src="302">
</amp-ad>
```

In the above code, the `type` attribute specifies the ad network, which in this case is A9. The `data-*` attributes are dependent on the parameters that the Amazon's A9 server expects to deliver an ad. The [`a9.js`](https://github.com/ampproject/amphtml/blob/master/ads/a9.js) file shows you how the parameters are mapped to making a JavaScript call to the A9 server's URL. The corresponding parameters passed by the amp-ad tag are appended to the URL to return an ad.

For instructions on creating an `amp-ad` integration, see [Integrating ad networks into AMP](https://github.com/ampproject/amphtml/blob/master/ads/README.md).

## Creating a Fast Fetch integration

[Fast Fetch](https://www.ampproject.org/latest/blog/even-faster-loading-ads-in-amp/) is an AMP mechanism that separates the ad request from the ad response, allowing ad requests to occur earlier in the page lifecycle, and rendering ads only when they are likely to be viewed by users. Fast Fetch provides preferential treatment to verified AMPHTML ads over traditional HTML ads. Within Fast Fetch, if an ad fails validation, that ad is wrapped in a cross-domain iframe to sandbox it from the rest of the AMP document. Conversely, an AMPHTML ad passing validation is written directly into the page. Fast Fetch handles both AMP and non-AMP ads; no additional ad requests are required for ads that fail validation.

{{ image('/static/img/docs/ads/amphtml-ad-flow.svg', 843, 699, alt='Fast Fetch Integration flow', caption='Fast Fetch Integration flow' ) }}

To serve AMPHTML ads from your ad server, you must provide a Fast Fetch integration that includes:

1.  Supporting SSL network communication.
1.  Providing JavaScript to build the ad request (example implementations: [AdSense](https://github.com/ampproject/amphtml/tree/master/extensions/amp-ad-network-adsense-impl) & [DoubleClick](https://github.com/ampproject/amphtml/tree/master/extensions/amp-ad-network-doubleclick-impl)).
1.  Validating and signing the creative through a validation service. [Cloudflare](https://blog.cloudflare.com/firebolt/) provides an AMP ad verification service, enabling any independent ad provider to deliver faster, lighter, and more engaging ads.

For instructions on creating a Fast Fetch integration, see the [Fast Fetch Network Implementation Guide](https://github.com/ampproject/amphtml/blob/master/ads/google/a4a/docs/Network-Impl-Guide.md).


## Related resources

*   [GitHub directory for all amp-ad extensions](https://github.com/ampproject/amphtml/tree/master/ads)
*   [List of supported ad vendors](/docs/ads/ads_vendors.html)
*   [Blog entry describing launch of Fast Fetch](https://www.ampproject.org/latest/blog/even-faster-loading-ads-in-amp/)
