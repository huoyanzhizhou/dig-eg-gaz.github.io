---
layout: page
title: Elements
permalink: /elements/
header:
  image_fullwidth: front-page.jpg
---
The Egyptian Gazette features a large number of recurring elements, which this project identifies using the `element=` attribute. Some of this material is captured in [templates](https://dig-eg-gaz.github.io/templates/), and others are [advertisements](https://dig-eg-gaz.github.io/advertisements). This pages lists recurring free-text elements, which are described using terms from the [Digital Egyptian Gazette schema](https://dig-eg-gaz.github.io/schema/). Many of the elements listed (ought to) contain sub-items with their own headlines, often also bylines and datelines.

Section name|element (or deprecated xml:id)|Usual page(s)|Frequency|Notes
---|---|---|---|---
**[Advertisements](https://dig-eg-gaz.github.io/advertisements/)** |various|1,2|daily|Use [templates](https://dig-eg-gaz.github.io/advertisements/)
**[Daily Weather Report](https://dig-eg-gaz.github.io/templates/#daily-weather-report)** |"weather"|2|daily|[tempate](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/daily-weather-report.xml) [alternate tempate](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/daily-weather-report-02.xml)
**Telegrams / Wire Reports** (international news)|"wire"|2,3|daily|Sometimes appears as "To-day's telegrams", but typically there is no heading for this section. Treat wire reports as individual divs (`type="wireReport"`), each with its own `<dateline>` and `<title>`. This section is sometimes spread over two pages; when this is the case, you can use the `next` and `prev` attributes.
**Local and General** |"local"|3|daily|Treat individual paragraphs as individual divs (`type="item"`), each with its own `<head>`.
**Sport and Play** |"sport"|3|daily?|Treat contents as items, each with own headline.
**Personal and Social** |"social"|3|daily?|Treat contents as paragraphs
**The Khedive** |"khedive"|3|daily?|
**Council of Ministers** |"councilMinisters"|3||
**Letters to the Editor** |"letters"|3||Treat each letter as an item, with `<byline>` and `<dateline>`
**Native Press Comments** |"nativePress"|3||
**Naval Notes** |"navalNotes"|3||
**Esbekieh Gardens** |"esbekieh"|3||Format concert program as a `list`
**Passenger List** |"passList"|3,4,5,6,7||Treat arrivals and departures as items.
**Steamer Movements** |"steamerMovements"|3||Treat contents as paragraphs.
**Shipping Movements** |"shippingMovements"|4,6||Begins November 13, 1905?
**[Mouvement Maritime](https://dig-eg-gaz.github.io/templates/#mouvement-maritime)** |"mouvementMaritime"|4||French language. see [template](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/mouvement-maritime.xml) for format. none after October 17, 1905?
**Army and Navy / Army of Occupation / Egyptian Army** |"army"|3,4,5,7||
**[Calendar of Coming Events](https://dig-eg-gaz.github.io/templates/#calendar-of-coming-events)** |"comingEvents"|5||see [template](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/calendar-of-coming-events.xml) for format
**[Cheap Prepaid Advertisements](https://dig-eg-gaz.github.io/templates/#cheap-prepaid-advertisements)** |"prepaidAdvertisements"|2,5,7||Section template [here](https://dig-eg-gaz.github.io/templates/#cheap-prepaid-advertisements). Treat each advertisement as an item.
**Visitors' List** |"visitList"|3,5||Treat each hotel as an item.
**Matters of Moment. Pith of the Press Comments.** |"mattersMoment"|5||
**Legal Notes / Chronique Judiciare** |"legal"|3,4,6||French language
**Our London Letter** |"londonLetter"|7||
**Our Paris Letter** |"parisLetter"|7||
**Egyptian Share Market** |"shareMarket"|3,5||contains items (Egyptians, Mining, Consols, Rails, etc.) with own heads; often closes with a table.
**Bulletin de la bourse** |"bulletinBourse"|3,4,6||French language
**Chronique Financiere** |"chroniqueFinanciere"|3,4||French language
**[Export Manifests](https://dig-eg-gaz.github.io/templates/#export-manifests)** |"exportManifests"|||See [template](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/export-manifests.xml) for format

## "Notes from" section:
These notes typically appear on page 3. They are sourced to "Our Own Correspondent". Treat individual stories as `<div type="item">`, each with its own `<head>`. It is not always clear how many stories belong to the section.

Place|element|Notes
---|---|---
Constantinople|"notesConstantinople"|also appears as Constantinople Notes
Port Said|"notesPortSaid"|
Suez|"notesSuez"
Fayoum|"notesFayoum"|also appears as Fayoum Notes
Cyprus|"notesCyprus"
The Sudan|"notesSudan"
Suakin|"notesSuakin"
Khartoum|"notesKhartoum"
Assiout|"notesAssiout"
Luxor|"notesLuxor"|also appears as Luxor Notes
Other|"notesOther"|Notes from Akhmin, Keneh, Kafr Zayat, Minet el Gamh, Wadi Medani, and other places in Egypt

Others infrequently occuring elements, not yet assigned an `element` value:
- Questions municipales
- Egyptological Notes
