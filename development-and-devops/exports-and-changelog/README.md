# Webflow exports and changelog

## 13/01/2023 - dynamic infrastructure link mobile

{% file src="../../.gitbook/assets/municipalmoney.webflow.zip" %}

## 12/01/2023 - calculation link to faq

{% file src="../../.gitbook/assets/municipalmoney.webflow (calc-link-faq-12012023).zip" %}

## 3/01/2023 - capital project link

{% file src="../../.gitbook/assets/municipalmoney.webflow_(Infra-projects-nav_03012023-2).zip" %}

## 1/09/2022 - tooltip showing below map for infra projects

{% file src="../../.gitbook/assets/muni-money-infra.webflow_(map-overlap-fix).zip" %}

## 14/04/2022 - cube version selector for indicator formula headings

{% file src="../../.gitbook/assets/municipalmoney.webflow (22).zip" %}

## 15/03/2022 - Dropdown overlap

{% file src="../../.gitbook/assets/muni-money-infra.webflow (overlap-fix).zip" %}

Dropdowns on the capital project filter dropdowns were covered by another element

## 07/02/2022 - Site notice

{% file src="../../.gitbook/assets/municipalmoney.webflow (site-notice).zip" %}

![](<../../.gitbook/assets/image (29).png>)

#### Added:

* High prominence `.site-notice` element that site below the `.nav` on all pages
* The `.site-notice` is `.hidden` by default
* `.site-notice` contains the following elements which can be adjusted
  * `.site-notice__row` can be duplicated to add another notice within the same element
  * `.site-notice__icon` contains a font awesome icon that can be adjusted
  * `.site-notice__text` can be adjusted&#x20;

## 21/01/2022 - Various updates

{% file src="../../.gitbook/assets/muni-money-infra.webflow (various-updates - 01212022).zip" %}

## 22/07/2021 - Fix video thumbnails

{% file src="../../.gitbook/assets/municipalmoney.webflow(8).zip" %}

## \[Infra] 05/14/2021 - Loading state on muni infrastructure

{% file src="../../.gitbook/assets/muni-money.webflow (infra-projects-loading - 05142021).zip" %}
Webflow export
{% endfile %}

<div align="left">

<img src="../../.gitbook/assets/image (37).png" alt="Loading state preview">

</div>

<div align="left">

<img src="../../.gitbook/assets/image (14).png" alt="custom classes for various headings">

</div>

#### Changes

* Removed all demo data from various fields.
* only one .breadcrumbs\_\_crumb (previously labelled "Municipal Infrastructure") is shown by default.
  * .breadcrumbs\_\_crumb.province and .breadcrumbs\_\_crumb.municipality are hidden by default
* Added .audited-outcome, .full-year-forecast, .budget-year-1, .budget-year-2, .budget-year-3
* Added .year as a span within the above headings where years should be inserted

## 08/04/2021 - Hidden components panel

{% file src="../../.gitbook/assets/municipalmoney.webflow (hidden-components - 04082021).zip" %}
Hidden components
{% endfile %}

#### Fixed:

* Added a `.hidden` class to the `.components` div on the municipality profile page

## 16/02/2021 - Similar Municipalities&#x20;

{% file src="../../.gitbook/assets/municipalmoney.webflow (similar-municipalities - 02162021).zip" %}
Similar municipalities
{% endfile %}

#### Changed:

#### **Tooltips:**

<div align="left">

<img src="../../.gitbook/assets/image (25).png" alt="">

</div>

* `.tooltip__description` is for the copy that describes the word with the tooltip.&#x20;
* `.tooltip__link` the `<a>` tag should reflect the desired link page&#x20;
* `.tooltip__link_text` is to change the default "learn more" text for the link button eg. explore
* Webflow has an interaction that shows the tooltip on hover of any element with the class `.hover-tooltip` eg. `.muni-type__wrapper.hover-tooltip`

####

#### **Similar municipalities in header:**

<div align="left">

<img src="../../.gitbook/assets/image (26).png" alt="Feature in default state">

</div>

<div align="left">

<img src="../../.gitbook/assets/image (8).png" alt="Muni info structure in default state">

</div>

* Modified the contents of `.page-heading__muni-info` to include the hover tooltip for muni-type so that we can show information about the types of muni and link to the FAQ "similar-munis" section for more information.
* By default there is a `.hidden` class on all of the `.page-heading__muni-info` blocks:&#x20;
  * `.page-heading__muni-info--local`
  * `.page-heading__muni-info--district`
  * `.page-heading__muni-info--metro`

<div align="left">

<img src="../../.gitbook/assets/image (1).png" alt="page-heading__muni-type">

</div>

* `.label.dotted-underline.page-heading__muni-type` is for displaying muni type eg. B4 local municipality
* `.page-heading__subtitle_link` is for parent district municipality
* `.page-heading__geo-parent-3` is for parent province

####

#### **Similar municipalities in indicator:**

![](<../../.gitbook/assets/image (39).png>)

* `.label.muni-type` is for the municipality type eg. B4 local municipality. It's default text is set to "loading..."

