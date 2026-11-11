# Cuneiform on the Surface, Metadata Beneath

**A Two-Layer Web Artwork and the Limits of Linguistic Resistance**

*Digital Epigraphy (SUX Markup)*

> *"Building the digital temple from the mud-bricks of antiquity."*

**Author:** Zeki Yahya, Independent Researcher (ORCID [0009-0009-8229-3946](https://orcid.org/0009-0009-8229-3946))
**Year:** 2026 • **Status:** Conceptual / Live Art; research article in manuscript
**Live edition:** <https://zekiyahya.github.io/sux/>

---

## Abstract

*Digital Epigraphy* is an experimental web artwork. Its Sumerian-script edition presents Unicode cuneiform characters to human visitors while declaring the language code `sux` (ISO 639-3) in its markup. The accompanying article inventories the page into a visible cuneiform surface and a machine-readable substrate, examines SUX Markup, an allegorical notation inspired by the Cylinders of Gudea, and reports descriptive Google Search Console data for the page over three months (47 clicks and 277 impressions, concentrated in the first two months). It finds that the substrate is written in English and enriched with structured data linking the author to more than thirty external identifiers, that Google does not use the language declaration to detect page language, and that the page therefore cannot be said to resist algorithmic data capture. The work is best understood as a **double address**: a surface that estranges human readers and a substrate that remains fully legible to machines. Read this way, the work does not escape the economy of legibility but exposes its architecture, and the use of an extinct language operates as an aesthetic of defamiliarisation rather than as a technical countermeasure.

**Keywords:** digital epigraphy; Sumerian; cuneiform; media archaeology; critical code studies; esoteric markup; structured data; surveillance capitalism; web art

## What this project is, and is not

- It **is** a conceptual artwork, an esoteric notation (SUX Markup), and a live website edition whose visible text is set in cuneiform characters.
- It **is not** a privacy tool. It does not prevent tracking or indexing, and it does not hide the author from search engines or other machines.
- It **is not** a verified Sumerian text. The strings of signs on the live edition carry no transliteration or translation and are offered as script and image.
- It **is not** a functional markup language for browsers.

## 1. Introduction

The commercial web is organised around legibility. Pages are written to be parsed by browsers, search crawlers and recommendation systems, and their language, authorship and subject matter are routinely declared in machine-readable form. Within this regime, an interface that is deliberately unreadable to most of its human visitors is an anomaly.

A familiar way of describing such work is as resistance to surveillance capitalism: a dead language, it is said, offers no monetisable data and therefore starves the systems that profile readers. The article tests that description against the page's source code and the available search data. It does not survive as a technical claim; a different reading does. The article is guided by three research questions:

1. How is the Sumerian-script edition constructed, and which of its components address human visitors and which address machines?
2. What can be said, on the evidence available, about the page's visibility in web search?
3. What do the answers imply for the claim that writing a page in an extinct language resists algorithmic data capture?

The study is a practice-based self-case study: the author created the work and owns the site.

## 2. Theoretical framework

| Strand | Sources | Use in the article |
| :--- | :--- | :--- |
| Media archaeology | Parikka (2012); Ernst (2013); Kittler (1997) | The crawler as a reader with its own temporality; suspicion toward the human-visible layer as the place where the work operates |
| Code as cultural text | Cox & McLean (2013); Marino (2020); Chun (2008) | Close reading of source; esoteric notation; code as fetish |
| Surveillance, obfuscation, legibility | Zuboff (2019); Brunton & Nissenbaum (2015); Galloway (2004); Berners-Lee et al. (2001); Guha et al. (2016) | Obfuscation versus disambiguation; protocol; structured data as legibility |
| Smoothness and defamiliarisation | Han (2018); Shklovsky (1965) | The cuneiform surface as friction |
| Standards for an ancient language | Unicode 15.0; ISO 639-3; ISO 15924; BCP 47; WHATWG HTML; WCAG 2.1; CDLI; Edzard (1997) | Unicode block U+12000–U+123FF; `sux` and `Xsux`; language tagging and accessibility |

## 3. Method and corpus

- **Close reading** of the HTML source of the live edition (examined on 10 November 2026) and of this repository.
- **Layer inventory**: every identifiable element classified as surface (addressed to humans), substrate (addressed to machines), or both.
- **Claims audit**: claims commonly made about works of this kind were tested against the source and against published platform documentation.
- **Search data**: Google Search Console, property `zekiyahya.github.io`, pages containing `/sux`, search type Web, three months to 10 November 2026. Only aggregate figures and the monthly chart were available. No inferential statistics are reported.
- No human participants; statements about visitor experience are interpretive.

## 4. The work: architecture of a two-layer page

### 4.1 Layer inventory

| Element | Content in the `/sux/` page | Layer | Language of content |
| :--- | :--- | :--- | :--- |
| Language declaration | `lang="sux"`; `inLanguage` "sux" in structured data | Substrate | Code (`sux`) |
| Document title | String of cuneiform characters | Both (tab and search result) | Cuneiform characters |
| Meta description and keywords | English prose; author's name, profession, film titles, theoretical terms | Substrate | English |
| Canonical and hreflang links | Self-canonical; twelve other language versions, the English root site, and `sux`, plus an `x-default` | Substrate | URLs and codes |
| Open Graph and social-card metadata | English title and description; portrait image | Substrate (link previews) | English |
| Structured data (JSON-LD) | Person, ProfilePage, WebSite, ImageObject, eight Movie entities, one ScholarlyArticle, two Article entities; more than thirty `sameAs` identifiers | Substrate | English and identifiers |
| Hero image | Author's portrait with English alt text | Surface (image) and substrate (alt text) | English (alt text) |
| Main heading and biography line | Cuneiform characters | Surface | Cuneiform characters |
| Manifesto block | Six lines of cuneiform characters | Surface | Cuneiform characters |
| Film cards | Posters with English alt text; titles and statements in cuneiform; links to external databases | Both | Mixed |
| Research cards | Links to PhilPapers and Zenodo records; titles and excerpts in cuneiform | Both | Mixed |
| Typeface | Stylesheet request to Google Fonts (Amiri) | Substrate (network request) | n/a |
| Scripts | No analytics or advertising scripts in the source examined | n/a | n/a |

The visible layer is not a cipher. A cipher hides a message; this page hides nothing, and ornaments the place where a message would ordinarily be read.

### 4.2 What the cuneiform strings are, and are not

The visible text is a sequence of cuneiform characters with no transliteration, translation or lexical annotation. Proper names and platform names have no attested Sumerian equivalents, so any cuneiform rendering of them can only be phonetic or symbolic, and long sign sequences recur across unrelated elements. The article therefore treats the visible layer as a **cuneiform-script surface** and makes no claim that it constitutes attested, grammatical or philologically verified Sumerian.

### 4.3 SUX Markup: a paper architecture

SUX Markup proposes four signs for the skeleton of a document. The allegory is inspired by the temple-building narrative of the **Cylinders of Gudea**, which describe the construction of a temple to the god Ningirsu from its foundation upward. A composite edition of Cylinder A is catalogued by the Cuneiform Digital Library Initiative as [P431881](https://cdli.earth/artifacts/431881) (RIME 3/1.01.07; Edzard 1997).

| Sign | Name | Unicode | HTML equivalent | Role in the allegory | Status |
| :---: | :---: | :---: | :---: | :--- | :--- |
| 𒋼 | TE | U+122FC | `<html>` | Foundation | Symbolic; relation to the lexeme *temen* unverified |
| 𒊕 | SAG | U+12295 | `<head>` | Head, metadata | Well-attested sign value |
| 𒂍 | E2 | U+1208D | `<body>` | House, main structure | Well-attested sign value |
| 𒋞 | SIG4 | U+122DE | `<div>` | Brick, structural block | Well-attested sign value |

```xml
<𒋼>
    <𒊕>
        <!-- metadata -->
    </𒊕>
    <𒂍>
        <𒋞>
            <!-- content block 1 -->
        </𒋞>
        <𒋞>
            <!-- content block 2 -->
        </𒋞>
    </𒂍>
</𒋼>
```

**Technical notes**

- **Not HTML.** Browsers parse HTML and do not recognise cuneiform characters as element names, so a document written literally in SUX Markup does not render as a web page.
- **Well-formed XML, parser permitting.** XML 1.0 (Fifth Edition) allows supplementary-plane characters in element names. The example is well-formed under libxml2-based parsers (tested with `lxml` and `xmllint`), while Python's built-in `expat` parser rejects it. A SUX Markup document could therefore be transformed into HTML by a script or stylesheet. **No converter is included in this project at present.**
- **Language and script codes.** `sux` is the ISO 639-3 code for the Sumerian *language*; `Xsux` is the ISO 15924 code for the Sumero-Akkadian cuneiform *script*. BCP 47 allows them to be combined, for example `lang="sux-Xsux"`.
- **Fonts.** Display of the characters depends on a cuneiform-capable font on the visitor's device (for example Noto Sans Cuneiform or Segoe UI Historic).
- The page at `/sux/` is ordinary HTML5 with cuneiform text content, not a SUX Markup document.

## 5. Search visibility: descriptive findings

**Table 1. Aggregate Search Console figures for the `/sux` page**

| Metric | Value and scope |
| :--- | :--- |
| Property and filter | `zekiyahya.github.io`; pages containing `/sux`; search type Web |
| Period | Three months to 10 November 2026 |
| Total clicks | 47 |
| Total impressions | 277 |
| Average click-through rate | 17% |
| Average position | 14 |

**Table 2. Approximate monthly distribution** (read from the Search Console chart; November is a partial month)

| Month (2026) | Clicks (approx.) | Impressions (approx.) |
| :--- | :---: | :---: |
| August | 29 | 175 |
| September | 18 | 72 |
| October | 0 | 24 |
| November (to 10th) | 0 | fewer than 5 |

**Reading.** The page was indexed, displayed, and received a small number of clicks; both clicks and impressions fell to near zero by October. A click-through rate of 17% at an average position of 14 is unusual and, in the author's reading, more characteristic of searches that already name the author or the site than of discovery by users searching for Sumerian content. This cannot be confirmed without query-level data. There is no control page, so nothing can be said about the effect of the `sux` declaration or of the cuneiform text as such.

## 6. Discussion

### 6.1 The resistance claim, tested

| Claim | Finding |
| :--- | :--- |
| The language declaration changes how crawlers treat the page | Google determines page language from visible content and does not use the HTML `lang` attribute ([Google Search Central](https://developers.google.com/search/docs/specialty/international/managing-multi-regional-sites); [Schwartz 2016](https://www.seroundtable.com/google-ignores-the-html-lang-attribute-22974.html)). Its [hreflang guidance](https://developers.google.com/search/docs/specialty/international/localized-versions) specifies two-letter ISO 639-1 codes, which `sux` is not. |
| The page contains nothing of value to systems that profile people | The substrate is English, names the author and his works, and links him to more than thirty external identifiers. The absence of analytics and advertising scripts is a real privacy property, but it would hold equally for an English page. |
| Tracking is starved | Tracking depends on identifiers and behaviour, not on the language of the text. The page requests a font stylesheet from a third party, is hosted on a centralised service (GitHub Pages), and is observed through Search Console. |

**Conclusion:** the work does not resist algorithmic data capture in any technically meaningful sense.

### 6.2 Obfuscation versus disambiguation

Obfuscation (Brunton & Nissenbaum 2015) adds ambiguous or misleading data to degrade surveillance. This page does the opposite: its substrate adds precise, cross-referenced identifiers. If the work operates on the data economy at all, it is **disambiguation under a mask**.

### 6.3 The double address

The page addresses two audiences with different competences and gives each a different message: an estranged typographic surface over a recognisable portrait for the human visitor, a dense and orderly statement of identity for the machine. The visible layer is epiphenomenal with respect to the substrate that does the identifying work (Kittler), the visible script is fetishised while the apparatus goes unremarked (Chun), and the crawler reads on a schedule unrelated to the contemplative time the surface invites (Ernst).

The most robust finding is Galloway's: **protocol is indifferent**. Unicode encodes cuneiform, ISO 639-3 registers Sumerian, BCP 47 and ISO 15924 allow a script to be tagged, and HTML accepts all of them without distinction. An extinct language can be made addressable, rendered, tagged and indexed as easily as any other.

### 6.4 The human visitor

Interpretively and without a user study: the surface can be read as defamiliarisation (Shklovsky), making the conventions of a portfolio page perceptible again. The effect is local rather than total; the portrait, card layout and link positions remain conventional. The surface also has an accessibility cost: for a language with no speech synthesis a correct language declaration cannot deliver access, so blind and low-vision visitors are excluded from the textual content.

### 6.5 Monument and mud-brick: durability

Clay tablets persisted because firing and burial happened to preserve them. A web page persists by replication and archiving, and depends on a host's continued service. Depositing a dated snapshot of the page and source in an independent repository such as Zenodo, with a persistent identifier, would give the work the durability its imagery promises.

### 6.6 Recommendations for tagging and access

- Declare language and script by element: `sux-Xsux` for cuneiform passages, `en` for English passages, and a root element that reflects the dominant language.
- Provide a transliteration and translation layer, visible on request or available to assistive technologies.
- Document how each cuneiform string was produced, with transliteration, translation and sources.
- Keep valid hreflang values for the language alternates; treat the `sux` alternate as descriptive metadata, not a search signal.
- Embed a cuneiform-capable, openly licensed font.
- Archive dated snapshots in an independent repository with a persistent identifier.

## 7. Limitations

1. Practice-based self-case study; proximity to the work cannot be fully separated from interest.
2. No query-level data.
3. No control condition; the data are purely descriptive.
4. Small sample, short window, approximate monthly values, incomplete final month.
5. The provenance of the cuneiform strings is not documented; no philological or Assyriological review; the sign-to-element mapping is not independently validated.
6. Google only.
7. No user study.
8. Search Console data are private to the account holder; exported data should be deposited with the article for independent reproduction.

## 8. Conclusion

The work places an extinct script on the surface of a living web page and thereby raises the question of what the web does with the past. It is better described as a double address than as resistance: it exposes the architecture of legibility rather than escaping it, and it makes visible the indifference of web protocols to the age and vitality of a language. Future work: a controlled comparison of matched pages on separate domains; a documented and philologically reviewed cuneiform layer; and a user study including participants who use assistive technology. Until then, the claim that an extinct language shields a page from the data economy should be regarded as an artistic proposition, not a technical finding.

## How to cite

Yahya, Z. (2026). *Cuneiform on the surface, metadata beneath: A two-layer web artwork and the limits of linguistic resistance* [Manuscript].

## Key references

Berners-Lee, T., Hendler, J., & Lassila, O. (2001). The Semantic Web. *Scientific American, 284*(5), 34–43. • Brunton, F., & Nissenbaum, H. (2015). *Obfuscation*. MIT Press. • Chun, W. H. K. (2008). On "sourcery," or code as fetish. *Configurations, 16*(3), 299–324. • Cox, G., & McLean, A. (2013). *Speaking code*. MIT Press. • Edzard, D. O. (1997). *Gudea and his dynasty* (RIME 3/1). University of Toronto Press. • Ernst, W. (2013). *Digital memory and the archive*. University of Minnesota Press. • Galloway, A. R. (2004). *Protocol*. MIT Press. • Guha, R. V., Brickley, D., & Macbeth, S. (2016). Schema.org: Evolution of structured data on the web. *Communications of the ACM, 59*(2), 44–51. • Han, B.-C. (2018). *Saving beauty*. Polity. • Kittler, F. (1997). There is no software. In J. Johnston (Ed.), *Literature, media, information systems* (pp. 147–155). • Marino, M. C. (2020). *Critical code studies*. MIT Press. • Parikka, J. (2012). *What is media archaeology?* Polity. • Shklovsky, V. (1965). Art as technique. In *Russian formalist criticism* (pp. 3–24). University of Nebraska Press. • Zuboff, S. (2019). *The age of surveillance capitalism*. PublicAffairs.

---

*Creative Direction: Zeki Yahya • © 2026 Zeki Yahya. All rights reserved.*

