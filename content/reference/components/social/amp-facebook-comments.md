---
$title: "amp-facebook-comments"
$order: 30
toc: true
---

<!---
Copyright 2015 The AMP HTML Authors. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS-IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->



<table>
  <tr>
    <td width="40%"><strong>Description</strong></td>
    <td>Embeds the Facebook comments plugin.</td>
  </tr>
  <tr>
    <td width="40%"><strong>Required Script</strong></td>
    <td><code>&lt;script async custom-element="amp-facebook-comments" src="https://cdn.ampproject.org/v0/amp-facebook-comments-0.1.js">&lt;/script></code></td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Supported Layouts</a></strong></td>
    <td>fill, fixed, fixed-height, flex-item, nodisplay, responsive</td>
  </tr>
  <tr>
    <td><strong>Examples</strong></td>
    <td>See AMP By Example's <a href="https://ampbyexample.com/components/amp-facebook-comments/">amp-facebook-comments example</a>.</td>
  </tr>
</table>

[TOC]

## Overview

You can use the `amp-facebook-comments` component to embed the [Facebook comments plugin](https://developers.facebook.com/docs/plugins/comments).

**Example**

[sourcecode:html]
<amp-facebook-comments width=486 height=657
    layout="responsive"
    data-numposts="5"
    data-href="http://www.directlyrics.com/adele-25-complete-album-lyrics-news.html">
</amp-facebook-comments>
[/sourcecode]
## Attributes

##### data-href (required)

The URL of the comments page. For example, `http://www.directlyrics.com/adele-25-complete-album-lyrics-news.html`.

##### data-locale (optional)

By default, the locale is set to user's system language; however, you can specify a locale as well.

For details on strings accepted here please visit the [Facebook API Localization page](https://developers.facebook.com/docs/internationalization)

##### data-numposts (optional)

The number of comments to show.  For details, see the [Facebook comments documentation](https://developers.facebook.com/docs/plugins/comments).

##### data-order-by (optional)

The order to use when displaying comments. For details, see the [Facebook comments documentation](https://developers.facebook.com/docs/plugins/comments).

##### data-colorscheme (optional)

The color scheme. For details, see the [Facebook comments documentation](https://developers.facebook.com/docs/plugins/comments).

##### common attributes

This element includes [common attributes](https://www.ampproject.org/docs/reference/common_attributes) extended to AMP components.

## Validation

See [amp-facebook-comments rules](https://github.com/ampproject/amphtml/blob/master/extensions/amp-facebook-comments/validator-amp-facebook-comments.protoascii) in the AMP validator specification.
