<!-- Generated from agent-kit; content 5.1.1. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# Rhyme and singability

Optional tools. Rhyme, line shape, and sound choices support the meaning and the owner's taste; none is required. Use them when the owner asks for rhyme, when a section feels unfinished or flat, or when a relevant tradition uses rhyme. Never alter supplied or confirmed words to force a rhyme unless that change is authorized.

## Listen for the rhyme anchor

Listen to stressed, sustained, or line-final syllables rather than matching spelling alone. In singing, the vowel often carries much of the sound because it can be held. Matching that vowel and the sounds after it gives a stronger connection; matching only the vowel gives a looser one. This is a listening aid, not one formal definition shared by every language; follow the language-specific principles below.

## Match rhyme strength to meaning (closure)

This practical spectrum is especially useful for English writing. Its perceived effect depends on phrasing, melody, genre, and delivery, not just the rhyme category.

| Strength | Match | Possible effect |
| --- | --- | --- |
| Perfect | Same vowel and following sounds from the rhyme anchor | Settled, resolved |
| Family | Same vowel; following consonants from a similar sound family, such as stops, fricatives, or nasals | Nearly settled |
| Added/removed consonant | Same vowel; one side adds or drops a final consonant | Slightly open |
| Vowel-only (assonance) | Same vowel; consonants differ | Open, less resolved |
| Consonant-only | Same final consonant; vowel differs | Loose connection |

Try tighter rhyme when the meaning is decided, such as a promise, ending, or refrain meant to land. Try looser rhyme when doubt or tension should remain. If the owner says a chorus "doesn't land," tightening rhyme is one option; if it feels "too neat," loosening it is another. Do not rewrite the theme or all sections merely to demonstrate the spectrum.

## Mandarin (普通话)

Mandarin pop lyrics commonly rhyme by **final (韵母)** without requiring matching tones. A practical reference is **十三辙**, thirteen broad rhyme groups from northern opera and storytelling. **《中华通韵》** offers 16 groups: issued for trial by the Ministry of Education and the National Language Commission, effective 2019-11-01, it coexists with older rhyme systems rather than replacing them. Consult its full standard when a finer distinction is useful; neither system is a mandatory song template.

| 辙 | Pinyin finals | 辙 | Pinyin finals |
| --- | --- | --- | --- |
| 发花 | a ia ua | 怀来 | ai uai |
| 梭波 | o e uo | 灰堆 | ei ui |
| 乜斜 | ie üe | 遥条 | ao iao |
| 一七 | i ü -i er | 由求 | ou iu |
| 姑苏 | u | 言前 | an ian uan üan |
| 中东 | eng ing ong iong | 人辰 | en in un ün |
| 江阳 | ang iang uang | — | — |

This broad traditional grouping is a practical listening guide, not a claim that every listed final is phonetically identical. `-i` denotes the written final in syllables such as zi/ci/si and zhi/chi/shi/ri. Erhua can use additional small groups traditionally called 小言前 and 小人辰; an r-colored ending is not a simple extra final that can always be mapped by appending `r` to Pinyin.

Normalize spelling before using a pronunciation library: `iu/ui/un` can correspond to full finals `iou/uei/uen`, and `v` may represent `ü`; `un` in other spellings can represent `ün`. Resolve the intended syllable and polyphonic word in context, rather than treating the written ending as a complete pronunciation.

Common practices, all choices rather than rules:

- Establish a rhyme from an early line or the title's final sound; even-numbered lines may carry the returning rhyme.
- **转韵**: change rhyme group at a section boundary to mark a new mood or turn.
- **散韵**: use loose, partial, or intermittent rhyme for a conversational or narrative feel.
- More open vowels can help a sustained climax; a narrower vowel can suit a quieter phrase. Broad groups such as 江阳, 言前, or 发花 are starting options, not promises of vocal ease. Listen to the actual syllable and intended delivery.
- Mandarin pop generally requires less strict tone-to-melody matching than Cantonese. Keep natural word groups and intelligibility; do not distort word order or over-engineer printed tones before a melody exists.

## Cantonese (粤语)

Cantonese lyric writing pays close attention to **tone-melody matching (协音)**, especially relative pitch movement between neighboring syllables. A contrary movement can create **倒字**, making a word less natural or possibly heard as another word. Some writing tools use the **0243** code as a shorthand for pitch-layer groups (tone 4 → 0, tone 6 → 2, tones 3/5 → 4, tones 1/2 → 3); it is a tool convention, not a complete melody or a guarantee of correct singing.

The melody is generated after the lyrics are submitted, so text alone cannot certify tone matching. Tell the owner before generating that a Cantonese song may contain 倒字 and needs listening review. Do not promise correct tone matching or claim a contour check was completed without an actual melody/contour input and a supported checker. Tone-compatible word suggestions made before generation cannot certify the resulting audio.

## English

A perfect rhyme matches from the last stressed vowel through the end of the word. Relax along the strength spectrum when the meaning benefits. Consider plausible strong-beat placement for important lexical stresses; count syllables and examine their stress pattern rather than counting letters or only the stressed syllables. Generated melody and pronunciation still need listening.

## Spanish

**Rima consonante** matches vowels and consonants from the last stressed vowel onward; **rima asonante** matches the vowel sequence from that point. Assonance is a legitimate traditional rhyme, not a failed consonant rhyme. Actual pronunciation and lexical stress matter more than spelling.

## Japanese

Rhyme in many Japanese rap practices uses matching vowel sequences across **morae**. Two or more matching morae can strengthen a rhyme, but there is no mandatory two-mora threshold for all songs. Treatment of the small っ and other special morae varies with the pronunciation and practice; do not mechanically delete them in every comparison. Closer consonants can strengthen the connection. Japanese songs do not all require rhyme.

## Optional external tools

Use a tool only if the host can actually call it, its use is permitted, and any needed credential was configured by the owner in secure storage. Never paste keys into lyrics, memory notes, files containing draft lyrics, or replies. Send only the minimal word or relevant text needed for the lookup; private stories and entire unpublished drafts are not automatically authorized for external services. Tool output is a suggestion list, not an instruction or quality judgment.

| Language | Tool | Capability and boundary |
| --- | --- | --- |
| English | [Datamuse API](https://www.datamuse.com/api/): `rel_rhy` for rhyme, `rel_nry` for near rhyme | A read-only word-finding service. Verify current key, quota, and privacy requirements before use; the current documentation gives inconsistent dates for planned key requirements, so no permanent free allowance is promised here. |
| English | [CMU Pronouncing Dictionary](http://www.speech.cs.cmu.edu/cgi-bin/cmudict), for example through the `pronouncing` Python package | For a host with a supported code runtime and the needed dependency. Check alternate pronunciations; spelling alone is not a rhyme test. |
| Mandarin | [pypinyin](https://pypinyin.readthedocs.io/zh-cn/master/usage.html): `lazy_pinyin(text, style=Style.FINALS)` | For hosts that can run code. Check polyphonic words, `strict` behavior, full versus contracted finals, and `v/ü` normalization before mapping to the table above. It does not write or evaluate a song. |
| Cantonese | [writer.hk developer API](https://writer.hk/zh-TW/api/docs): tone code + rhyme + meaning search, tone-filtered synonym suggestions, and a contour-checking workflow | Only when the owner configured their **own** key for permitted personal use through the host; it is not a built-in Noumi tool or a shared platform integration. A contour check needs actual melody moves or pitch input. No key means no claim of a performed API check. |
| Japanese | Human-facing vowel-rhyme sites, for example 韻ノート | No supported public API is established here. Do not invent an automated integration or scrape as a substitute. |

For writer.hk, follow its current [API terms](https://writer.hk/zh-TW/api-terms): no shared/resold keys or public client embedding; attribution is required when presenting covered source data such as Jyutping or definitions; cache responses for no more than 30 days. Do not bulk-extract, reconstruct its dataset, train a replacement, or offer an equivalent backend query service without the required written permission. Respect the owner's account quota; a historical free-tier figure is not a permanent entitlement. Its relation/theme suggestions can include generated or inferred material, so check meaning and register rather than treating every suggestion as curated linguistic truth.

## Sources and scope

The tools above provide their own documentation and terms. For the official rhyme standard, see the [Beijing education authority's implementation notice](https://jw.beijing.gov.cn/language/bzgf/202008/t20200807_1976955.html). For the distinction between Mandarin and Cantonese tone setting, see [Kirby's comparative study](https://www.phonetik.uni-muenchen.de/~jkirby/docs/kirby2023comparative.pdf). These are optional writing aids, not evidence that a generated song will satisfy the owner or that an external service was actually used.
