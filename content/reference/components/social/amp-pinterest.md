---
$title: "amp-pinterest"
$order: 68
toc: true
---

<!---
Copyright 2015 The AMP HTML Authors.

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
    <td>Displays a Pinterest widget, Pin It button, or Follow button.</td>
  </tr>
  <tr>
    <td width="40%"><strong>Required Script</strong></td>
    <td><code>&lt;script async custom-element="amp-pinterest" src="https://cdn.ampproject.org/v0/amp-pinterest-0.1.js">&lt;/script></code></td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Supported Layouts</a></strong></td>
    <td>fill, fixed, fixed-height, flex-item, nodisplay, responsive</td>
  </tr>
  <tr>
    <td width="40%"><strong>Examples</strong></td>
    <td><a href="https://ampbyexample.com/components/amp-pinterest/">Annotated code example for amp-pinterest</a></td>
  </tr>
</table>

[TOC]

## Examples

Use the `amp-pinterest` component to display a Pin It button, Pin widget, or Follow button.

**Example: Pin It button**

[sourcecode:html]
<amp-pinterest
  height=20
  width=40
  data-do="buttonPin"
  data-url="http://www.flickr.com/photos/kentbrew/6851755809/"
  data-media="http://farm8.staticflickr.com/7027/6851755809_df5b2051c9_z.jpg"
  data-description="Next stop: Pinterest">
</amp-pinterest>
[/sourcecode]

**Example: Pin widget**

[sourcecode:html]
<amp-pinterest
  width=245
  height=330
  data-do="embedPin"
  data-url="https://www.pinterest.com/pin/99360735500167749/">
</amp-pinterest>
[/sourcecode]

**Example: Follow button**

[sourcecode:html]
<amp-pinterest
    height=20
    width=94
    data-do="buttonFollow"
    data-href="https://www.pinterest.com/kentbrew/"
    data-label="Kent Brewster">
</amp-pinterest>
[/sourcecode]

## Pin It Button

##### data-do (required)

Must be set to `buttonPin`.

##### data-url (required)

Contains the fully-qualified URL intended to be pinned or re-made into a widget.

##### data-media (required)

Contains the fully-qualified URL of the image intended to be pinned. If the pin will eventually contain multimedia (such as YouTube), it should point to a high-resolution thumbnail.

##### data-description (required)

Contains the default description that appears in the pin create form; please choose carefully, since many Pinners will close the form without pinning if it doesn't make sense.

### Sizing the Pin It button

Default small rectangular button:

[sourcecode:html]
height=20 width=40
[/sourcecode]

Small rectangular button with pin count to the right, using `data-count="beside"`:

[sourcecode:html]
height=20 width=85
[/sourcecode]

Small rectangular button with pin count on top, using `data-count="above"`:

[sourcecode:html]
height=50 width=40
[/sourcecode]

Large rectangular button using `data-tall="true"`:

[sourcecode:html]
height=28 width=56
[/sourcecode]

Large rectangular button with pin count to the right, using `data-tall="true"` and `data-count="beside"`:

[sourcecode:html]
height=28 width=107
[/sourcecode]

Large rectangular button with pin count on top, using `data-tall="true"` and `data-count="above"`:

[sourcecode:html]
height=66 width=56
[/sourcecode]

Small circular button using `data-round="true"`:

[sourcecode:html]
height=16 width=16
[/sourcecode]

Large circular button using `data-round="true"` and `data-tall="true"`:

[sourcecode:html]
height=32 width=32
[/sourcecode]

## Follow Button

##### data-do (required)

Must be set to `buttonFollow`.

##### data-href (required)

Contains the fully qualified Pinterest user profile url to follow.

##### data-label (required)

Contains the text to display on the follow button.

## Embedded Pin Widget

##### data-do (required)

Must be set to `embedPin`.

##### data-url (required)

Must contain the fully-qualified URL of the Pinterest resource to be shown as a widget.

[sourcecode:html]
data-url="https://www.pinterest.com/pin/99360735500167749/"
[/sourcecode]

##### alt

This property like the the `alt` attribute on an `<img>` tag specifies the alternate text. If not provided it will be infered from the pin data provided by the Pinterest API.

## Validation

See [amp-pinterest rules](https://github.com/ampproject/amphtml/blob/master/extensions/amp-pinterest/validator-amp-pinterest.protoascii) in the AMP validator specification.
