## Fontbakery report

Fontbakery version: 0.8.6

<details>
<summary><b>[12] Solitreo-Regular.ttf</b></summary>
<details>
<summary>💔 <b>ERROR:</b> Check METADATA.pb includes production subsets.</summary>

* [com.google.fonts/check/metadata/includes_production_subsets](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/metadata/includes_production_subsets)
<pre>--- Rationale ---
Check METADATA.pb file includes the same subsets as the family in production.</pre>

* 💔 **ERROR** The condition <FontBakeryCondition:production_metadata> had an error: JSONDecodeError: Expecting value: line 1 column 1 (char 0)

</details>
<details>
<summary>💔 <b>ERROR:</b> Version number has increased since previous release on Google Fonts?</summary>

* [com.google.fonts/check/version_bump](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/version_bump)

* 💔 **ERROR** The condition <FontBakeryCondition:api_gfonts_ttFont> had an error: FailedConditionError: The condition <FontBakeryCondition:remote_styles> had an error: JSONDecodeError: Expecting value: line 1 column 1 (char 0)

</details>
<details>
<summary>💔 <b>ERROR:</b> Glyphs are similiar to Google Fonts version?</summary>

* [com.google.fonts/check/production_glyphs_similarity](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/production_glyphs_similarity)

* 💔 **ERROR** The condition <FontBakeryCondition:api_gfonts_ttFont> had an error: FailedConditionError: The condition <FontBakeryCondition:remote_styles> had an error: JSONDecodeError: Expecting value: line 1 column 1 (char 0)

</details>
<details>
<summary>💔 <b>ERROR:</b> Check if the vertical metrics of a family are similar to the same family hosted on Google Fonts.</summary>

* [com.google.fonts/check/vertical_metrics_regressions](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/vertical_metrics_regressions)
<pre>--- Rationale ---
If the family already exists on Google Fonts, we need to ensure that the checked
family&#x27;s vertical metrics are similar. This check will test the following schema
which was outlined in Fontbakery issue #1162 [1]:
- The family should visually have the same vertical metrics as the Regular style
hosted on Google Fonts.
- If the family on Google Fonts has differing hhea and typo metrics, the family
being checked should use the typo metrics for both the hhea and typo entries.
- If the family on Google Fonts has use typo metrics not enabled and the family
being checked has it enabled, the hhea and typo metrics should use the family on
Google Fonts winAscent and winDescent values.
- If the upms differ, the values must be scaled so the visual appearance is the
same.
[1] https://github.com/googlefonts/fontbakery/issues/1162</pre>

* 💔 **ERROR** The condition <FontBakeryCondition:regular_remote_style> had an error: FailedConditionError: The condition <FontBakeryCondition:remote_styles> had an error: JSONDecodeError: Expecting value: line 1 column 1 (char 0)

</details>
<details>
<summary>💔 <b>ERROR:</b> Check font follows the Google Fonts CJK vertical metric schema</summary>

* [com.google.fonts/check/cjk_vertical_metrics](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/cjk_vertical_metrics)
<pre>--- Rationale ---
CJK fonts have different vertical metrics when compared to Latin fonts. We
follow the schema developed by dr Ken Lunde for Source Han Sans and the Noto CJK
fonts.
Our documentation includes further information:
https://github.com/googlefonts/gf-docs/tree/main/Spec#cjk-vertical-metrics</pre>

* 💔 **ERROR** The condition <FontBakeryCondition:remote_styles> had an error: JSONDecodeError: Expecting value: line 1 column 1 (char 0)

</details>
<details>
<summary>💔 <b>ERROR:</b> Check if the vertical metrics of a CJK family are similar to the same family hosted on Google Fonts.</summary>

* [com.google.fonts/check/cjk_vertical_metrics_regressions](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/cjk_vertical_metrics_regressions)
<pre>--- Rationale ---
Check CJK family has the same vertical metrics as the same family hosted on
Google Fonts.</pre>

* 💔 **ERROR** The condition <FontBakeryCondition:regular_remote_style> had an error: FailedConditionError: The condition <FontBakeryCondition:remote_styles> had an error: JSONDecodeError: Expecting value: line 1 column 1 (char 0)

</details>
<details>
<summary>⚠ <b>WARN:</b> Checking OS/2 achVendID.</summary>

* [com.google.fonts/check/vendor_id](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/vendor_id)
<pre>--- Rationale ---
Microsoft keeps a list of font vendors and their respective contact info. This
list is updated regularly and is indexed by a 4-char &quot;Vendor ID&quot; which is stored
in the achVendID field of the OS/2 table.
Registering your ID is not mandatory, but it is a good practice since some
applications may display the type designer / type foundry contact info on some
dialog and also because that info will be visible on Microsoft&#x27;s website:
https://docs.microsoft.com/en-us/typography/vendors/
This check verifies whether or not a given font&#x27;s vendor ID is registered in
that list or if it has some of the default values used by the most common font
editors.
Each new FontBakery release includes a cached copy of that list of vendor IDs.
If you registered recently, you&#x27;re safe to ignore warnings emitted by this
check, since your ID will soon be included in one of our upcoming releases.</pre>

* ⚠ **WARN** OS/2 VendorID value 'NONE' is not yet recognized. If you registered it recently, then it's safe to ignore this warning message. Otherwise, you should set it to your own unique 4 character code, and register it with Microsoft at https://www.microsoft.com/typography/links/vendorlist.aspx
 [code: unknown]

</details>
<details>
<summary>⚠ <b>WARN:</b> Are there caret positions declared for every ligature?</summary>

* [com.google.fonts/check/ligature_carets](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/ligature_carets)
<pre>--- Rationale ---
All ligatures in a font must have corresponding caret (text cursor) positions
defined in the GDEF table, otherwhise, users may experience issues with caret
rendering.
If using GlyphsApp or UFOs, ligature carets can be defined as anchors with names
starting with &#x27;caret_&#x27;. These can be compiled with fontmake as of version
v2.4.0.</pre>

* ⚠ **WARN** This font lacks caret position values for ligature glyphs on its GDEF table. [code: lacks-caret-pos]

</details>
<details>
<summary>⚠ <b>WARN:</b> Is there kerning info for non-ligated sequences?</summary>

* [com.google.fonts/check/kerning_for_non_ligated_sequences](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/kerning_for_non_ligated_sequences)
<pre>--- Rationale ---
Fonts with ligatures should have kerning on the corresponding non-ligated
sequences for text where ligatures aren&#x27;t used (eg
https://github.com/impallari/Raleway/issues/14).</pre>

* ⚠ **WARN** GPOS table lacks kerning info for the following non-ligated sequences:
	- uni05D1 + uni05F3
	- uni05F3 + quoteright
	- quoteright + quotesingle
	- uni05D2 + uni05F3
	- uni05F3 + uni05D5
	- uni05D5 + uni05F3
	- uni05F3 + uni05D9
	- uni05D9 + quoteright
	- quoteright + uni05D5
	- uni05D5 + quoteright
	- quoteright + uni05D9
	- uni05D9 + quotesingle
	- quotesingle + uni05D5
	- uni05D5 + quotesingle
	- quotesingle + uni05D9
	- uni05D9 + uni05F3
	- uni05D5 + uni05D9
	- uni05D3 + uni05F3
	- uni05D9 + uni05D9
	- uni05D9 + uni05D5
	- uni05D4 + uni05F3
	- uni05D6 + uni05F3
	- uni05DF + uni05F3
	- uni05E1 + uni05F3
	- uni05E4 + uni05F3
	- uni05E8 + uni05D1
	- uni05F3 + uni05D1
	- uni05D1 + quoteright
	- quoteright + uni05D1
	- uni05D1 + quotesingle
	- uni05E9 + uni05F3
	- uni05D2.alt + uni05F3
	- uni05D3.alt + uni05F3
	- quotedblleft + quotedblleft
	- quotedblright + quotedblright
	- quotedbl + quotedbl
	- quotedbl + quotedblright
	- quotedblright + quotedbl
	- greater + greater
	- less + less
	- comma + comma

   [code: lacks-kern-info]

</details>
<details>
<summary>⚠ <b>WARN:</b> Ensure fonts have ScriptLangTags declared on the 'meta' table.</summary>

* [com.google.fonts/check/meta/script_lang_tags](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/meta/script_lang_tags)
<pre>--- Rationale ---
The OpenType &#x27;meta&#x27; table originated at Apple. Microsoft added it to OT with
just two DataMap records:
- dlng: comma-separated ScriptLangTags that indicate which scripts, or languages
and scripts, with possible variants, the font is designed for
- slng: comma-separated ScriptLangTags that indicate which scripts, or languages
and scripts, with possible variants, the font supports
The slng structure is intended to describe which languages and scripts the font
overall supports. For example, a Traditional Chinese font that also contains
Latin characters, can indicate Hant,Latn, showing that it supports Hant, the
Traditional Chinese variant of the Hani script, and it also supports the Latn
script
The dlng structure is far more interesting. A font may contain various glyphs,
but only a particular subset of the glyphs may be truly &quot;leading&quot; in the design,
while other glyphs may have been included for technical reasons. Such a
Traditional Chinese font could only list Hant there, showing that it’s designed
for Traditional Chinese, but the font would omit Latn, because the developers
don’t think the font is really recommended for purely Latin-script use.
The tags used in the structures can comprise just script, or also language and
script. For example, if a font has Bulgarian Cyrillic alternates in the locl
feature for the cyrl BGR OT languagesystem, it could also indicate in dlng
explicitly that it supports bul-Cyrl. (Note that the scripts and languages in
meta use the ISO language and script codes, not the OpenType ones).
This check ensures that the font has the meta table containing the slng and dlng
structures.
All families in the Google Fonts collection should contain the &#x27;meta&#x27; table.
Windows 10 already uses it when deciding on which fonts to fall back to. The
Google Fonts API and also other environments could use the data for smarter
filtering. Most importantly, those entries should be added to the Noto fonts.
In the font making process, some environments store this data in external files
already. But the meta table provides a convenient way to store this inside the
font file, so some tools may add the data, and unrelated tools may read this
data. This makes the solution much more portable and universal.</pre>

* ⚠ **WARN** This font file does not have a 'meta' table. [code: lacks-meta-table]

</details>
<details>
<summary>⚠ <b>WARN:</b> Check font contains no unreachable glyphs</summary>

* [com.google.fonts/check/unreachable_glyphs](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/unreachable_glyphs)
<pre>--- Rationale ---
Glyphs are either accessible directly through Unicode codepoints or through
substitution rules. Any glyphs not accessible by either of these means are
redundant and serve only to increase the font&#x27;s file size.</pre>

* ⚠ **WARN** The following glyphs could not be reached by codepoint or substitution rules:
	- brevecombcy
	- uni030C.alt
	- uni05D3.alt 
	- And uni05D2.alt
 [code: unreachable-glyphs]

</details>
<details>
<summary>⚠ <b>WARN:</b> Check if each glyph has the recommended amount of contours.</summary>

* [com.google.fonts/check/contour_count](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/contour_count)
<pre>--- Rationale ---
Visually QAing thousands of glyphs by hand is tiring. Most glyphs can only be
constructured in a handful of ways. This means a glyph&#x27;s contour count will only
differ slightly amongst different fonts, e.g a &#x27;g&#x27; could either be 2 or 3
contours, depending on whether its double story or single story.
However, a quotedbl should have 2 contours, unless the font belongs to a display
family.
This check currently does not cover variable fonts because there&#x27;s plenty of
alternative ways of constructing glyphs with multiple outlines for each feature
in a VarFont. The expected contour count data for this check is currently
optimized for the typical construction of glyphs in static fonts.</pre>

* ⚠ **WARN** This font has a 'Soft Hyphen' character (codepoint 0x00AD) which is supposed to be zero-width and invisible, and is used to mark a hyphenation possibility within a word in the absence of or overriding dictionary hyphenation. It is mostly an obsolete mechanism now, and the character is only included in fonts for legacy codepage coverage. [code: softhyphen]
* ⚠ **WARN** This check inspects the glyph outlines and detects the total number of contours in each of them. The expected values are infered from the typical ammounts of contours observed in a large collection of reference font families. The divergences listed below may simply indicate a significantly different design on some of your glyphs. On the other hand, some of these may flag actual bugs in the font such as glyphs mapped to an incorrect codepoint. Please consider reviewing the design and codepoint assignment of these to make sure they are correct.

The following glyphs do not have the recommended number of contours:

	- Glyph name: percent	Contours detected: 4	Expected: 5
	- Glyph name: Q	Contours detected: 3	Expected: 2
	- Glyph name: q	Contours detected: 1	Expected: 2
	- Glyph name: Q	Contours detected: 3	Expected: 2
	- Glyph name: percent	Contours detected: 4	Expected: 5 
	- And Glyph name: q	Contours detected: 1	Expected: 2
 [code: contour-count]

</details>
<br>
</details>

### Summary

| 💔 ERROR | 🔥 FAIL | ⚠ WARN | 💤 SKIP | ℹ INFO | 🍞 PASS | 🔎 DEBUG |
|:-----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 6 | 0 | 6 | 100 | 7 | 103 | 0 |
| 3% | 0% | 3% | 45% | 3% | 46% | 0% |

**Note:** The following loglevels were omitted in this report:
* **SKIP**
* **INFO**
* **PASS**
* **DEBUG**