## Fontbakery report

Fontbakery version: 0.8.6

<details>
<summary><b>[14] Solitreo-Regular.ttf</b></summary>
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
<summary>🔥 <b>FAIL:</b> Check `Google Fonts Latin Core` glyph coverage.</summary>

* [com.google.fonts/check/glyph_coverage](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/glyph_coverage)
<pre>--- Rationale ---
Google Fonts expects that fonts in its collection support at least the minimal
set of characters defined in the `GF-latin-core` glyph-set.</pre>

* 🔥 **FAIL** Missing required codepoints:

	- 0x00A4 (CURRENCY SIGN)

	- 0x00AD (SOFT HYPHEN)

	- 0x00C2 (LATIN CAPITAL LETTER A WITH CIRCUMFLEX)

	- 0x02BB (MODIFIER LETTER TURNED COMMA)

	- 0x2002 (EN SPACE)

	- 0x2009 (THIN SPACE)

	- 0x200B (ZERO WIDTH SPACE)

	- 0x2032 (PRIME)

	- 0x2033 (DOUBLE PRIME)

	- 0x2122 (TRADE MARK SIGN)
 
	- And 4 more.

Use -F or --full-lists to disable shortening of long lists. [code: missing-codepoints]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Checking OS/2 usWinAscent & usWinDescent.</summary>

* [com.google.fonts/check/family/win_ascent_and_descent](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/family/win_ascent_and_descent)
<pre>--- Rationale ---
A font&#x27;s winAscent and winDescent values should be greater than the head table&#x27;s
yMax, abs(yMin) values. If they are less than these values, clipping can occur
on Windows platforms (https://github.com/RedHatBrand/Overpass/issues/33).
If the font includes tall/deep writing systems such as Arabic or Devanagari, the
winAscent and winDescent can be greater than the yMax and abs(yMin) to
accommodate vowel marks.
When the win Metrics are significantly greater than the upm, the linespacing can
appear too loose. To counteract this, enabling the OS/2 fsSelection bit 7
(Use_Typo_Metrics), will force Windows to use the OS/2 typo values instead. This
means the font developer can control the linespacing with the typo values,
whilst avoiding clipping by setting the win values to values greater than the
yMax and abs(yMin).</pre>

* 🔥 **FAIL** OS/2.usWinDescent value should be equal or greater than 415, but got 307 instead. [code: descent]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Space and non-breaking space have the same width?</summary>

* [com.google.fonts/check/whitespace_widths](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/hmtx.html#com.google.fonts/check/whitespace_widths)

* 🔥 **FAIL** Space and non-breaking space have differing width: The space glyph named space is 211 font units wide, non-breaking space named (uni00A0) is 245 font units wide, and both should be positive and the same. GlyphsApp has "Sidebearing arithmetic" (https://glyphsapp.com/tutorials/spacing) which allows you to set the non-breaking space width to always equal the space width. [code: different-widths]

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
	- two.dnom
	- brevecombcy.case
	- brevecombcy
	- uni0326.case
	- uni0306.case
	- uni0304.case
	- four.dnom
	- five.numr
	- six.numr
	- uni0328.case 
	- And 21 more.

Use -F or --full-lists to disable shortening of long lists.
 [code: unreachable-glyphs]

</details>
<details>
<summary>⚠ <b>WARN:</b> Does GPOS table have kerning information? This check skips monospaced fonts as defined by post.isFixedPitch value</summary>

* [com.google.fonts/check/gpos_kerning_info](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/gpos.html#com.google.fonts/check/gpos_kerning_info)

* ⚠ **WARN** GPOS table lacks kerning information. [code: lacks-kern-info]

</details>
<details>
<summary>⚠ <b>WARN:</b> Are there any misaligned on-curve points?</summary>

* [com.google.fonts/check/outline_alignment_miss](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_alignment_miss)
<pre>--- Rationale ---
This check heuristically looks for on-curve points which are close to, but do
not sit on, significant boundary coordinates. For example, a point which has a
Y-coordinate of 1 or -1 might be a misplaced baseline point. As well as the
baseline, here we also check for points near the x-height (but only for lower
case Latin letters), cap-height, ascender and descender Y coordinates.
Not all such misaligned curve points are a mistake, and sometimes the design may
call for points in locations near the boundaries. As this check is liable to
generate significant numbers of false positives, it will pass if there are more
than 100 reported misalignments.</pre>

* ⚠ **WARN** The following glyphs have on-curve points which have potentially incorrect y coordinates:
	* parenleft (U+0028): X=308.0,Y=701.5 (should be at cap-height 700?)
	* parenright (U+0029): X=31.0,Y=701.5 (should be at cap-height 700?)
	* one (U+0031): X=265.0,Y=699.0 (should be at cap-height 700?)
	* bracketright (U+005D): X=33.5,Y=701.5 (should be at cap-height 700?)
	* asciicircum (U+005E): X=168.0,Y=701.0 (should be at cap-height 700?)
	* asciicircum (U+005E): X=264.0,Y=701.0 (should be at cap-height 700?)
	* grave (U+0060): X=72.0,Y=701.0 (should be at cap-height 700?)
	* section (U+00A7): X=71.0,Y=-2.0 (should be at baseline 0?)
	* acute (U+00B4): X=265.0,Y=701.0 (should be at cap-height 700?)
	* agrave (U+00E0): X=126.0,Y=701.0 (should be at cap-height 700?) and 63 more.

Use -F or --full-lists to disable shortening of long lists. [code: found-misalignments]

</details>
<br>
</details>

### Summary

| 💔 ERROR | 🔥 FAIL | ⚠ WARN | 💤 SKIP | ℹ INFO | 🍞 PASS | 🔎 DEBUG |
|:-----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 6 | 3 | 5 | 102 | 7 | 99 | 0 |
| 3% | 1% | 2% | 46% | 3% | 45% | 0% |

**Note:** The following loglevels were omitted in this report:
* **SKIP**
* **INFO**
* **PASS**
* **DEBUG**
