# Exports and changelog

### 16/02/2021 - Similar Municipalities 

{% file src="../.gitbook/assets/municipalmoney.webflow-similar-municipalities-02162021- \(1\).zip" caption="Similar municipalities" %}

### Changed:

#### **Tooltips:**

![](../.gitbook/assets/image.png)

* `.tooltip__description` is for the copy that describes the word with the tooltip. 
* `.tooltip__link` the `<a>` tag should reflect the desired link page 
* `.tooltip__link_text` is to change the default "learn more" text for the link button eg. explore
* Webflow has an interaction that shows the tooltip on hover of any element with the class `.hover-tooltip` eg. `.muni-type__wrapper.hover-tooltip`

#### \*\*\*\*

#### **Similar municipalities in header:**

![Feature in default state](../.gitbook/assets/image%20%281%29.png)

![Muni info structure in default state](../.gitbook/assets/image%20%282%29.png)

* Modified the contents of `.page-heading__muni-info` to include the hover tooltip for muni-type so that we can show information about the types of muni and link to the FAQ "similar-munis" section for more information.
* By default there is a `.hidden` class on all of the `.page-heading__muni-info` blocks: 
  * `.page-heading__muni-info--local`
  * `.page-heading__muni-info--district`
  * `.page-heading__muni-info--metro`

![page-heading\_\_muni-type](../.gitbook/assets/image%20%287%29.png)

* `.label.dotted-underline.page-heading__muni-type` is for displaying muni type eg. B4 local municipality
* `.page-heading__subtitle_link` is for parent district municipality
* `.page-heading__geo-parent-3` is for parent province

#### \*\*\*\*

#### **Similar municipalities in indicator:**

![](../.gitbook/assets/image%20%285%29.png)

* `.label.muni-type` is for the municipality type eg. B4 local municipality. It's default text is set to "loading..."



