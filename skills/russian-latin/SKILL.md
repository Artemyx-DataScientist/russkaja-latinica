---
name: russian-latin
description: Write and understand Russian using the Russian Latin ASCII orthography defined in this skill. Use when the user asks for Russian Latin, provides text in this orthography, or asks to continue in it.
---

# Russian Latin — writing skill

## Core instruction

Write Russian in the project's Latin orthography. This is Russian written in Latin characters, not English and not conventional ISO transliteration.

When the user asks for Russian Latin or writes to you in Russian Latin:
- understand the text as Russian;
- answer in the same orthography;
- preserve the user's meaning, tone, register and formatting;
- output only the requested text by default.

Do not add explanations, introductions, transliteration notes, a Cyrillic duplicate, or a table unless the user explicitly asks for them. Do not explain the rules while performing ordinary writing.

If the user asks a question in Russian Latin, answer the question in Russian Latin. If they explicitly request Cyrillic or another language, follow that request.

## ASCII inventory

Use ASCII letters only; do not use diacritics or non-ASCII Latin characters.

Single-letter values:
- a, b, v, g, d, e, f, i, j, k, l, m, n, o, p, r, s, t, u, x, y, z, c

Consonant graphemes:
- zh = Ж
- ch = Ч
- sh = Ш
- hsc = Щ

Important vowel assignments:
- y = У
- u = Ы

Never reverse these two values.

## Contextual vowels

The forms depend on pronunciation and the preceding consonant.

| Russian vowel | Pronounced [j] | Softening a paired consonant, without [j] | No added softening marker |
|---|---|---|---|
| Я | ja | ia | a |
| Е | je | ie | e |
| Ё | jo | io | o |
| Ю | jy | iy | y |

Use j only when [j] is actually pronounced.

## Softness

Use silent i as a softness marker only for Russian consonants that have a hard/soft opposition:

b, v, g, d, z, k, l, m, n, p, r, s, t, f, x.

The marker is combined with the following vowel:
- ia = soft consonant + А;
- ie = soft consonant + Е;
- io = soft consonant + Ё;
- iy = soft consonant + Ю.

The marker i is not pronounced as a separate vowel in these combinations.

Do not add a softness marker after:
- always-hard Ж zh, Ш sh, Ц c;
- always-soft Ч ch, Щ hsc.

Examples:
- dielat' — делать;
- miaso — мясо;
- liydi — люди;
- zhena — жена;
- zhelezo — железо;
- shest' — шесть;
- cena — цена;
- chelovek — человек;
- hscotka — щётка.

## Full vowel I versus silent marker I

The letter i can be either:
1. the fully pronounced Russian vowel И; or
2. a silent softness marker in ia, ie, io, iy.

Do not confuse these functions.

- dijeta means диета: i is the pronounced vowel И and j is the pronounced [j] before Е.
- d'iakritiki means диакритики: d' marks the soft Д; the following i is the pronounced vowel И. The apostrophe prevents the sequence from being misread as a silent softness marker.

A pronounced i can itself indicate softness in ordinary contexts. If it is followed by another vowel and the reading could be confused with the silent marker, use the apostrophe to make the intended soft consonant and full И clear.

## Apostrophe and hard sign

Use ':
- for a soft consonant before another consonant;
- at the end of a word for final softness;
- where needed to distinguish a soft consonant followed by a pronounced И from a silent i marker;
- to represent Cyrillic Ь.

Examples:
- mat' — мать;
- kon' — конь;
- ban'ka — банька;
- sem'ja — семья;
- d'iakritiki — диакритики.

Do not treat the apostrophe as a mere visual separator. It carries orthographic information.

Cyrillic Ъ has no separate Latin sign. Preserve a pronounced [j] after it:
- podjezd — подъезд;
- objom — объём.

## Morphological spelling

Preserve the project's morphological spelling when it is explicitly used. Confirmed example:

- bezsmuslienno = безсмысленно, preserving the з of the prefix без- before с.

Do not silently normalize this to the modern assimilated spelling. Other restored prefix spellings are not yet fully specified; do not invent them.

## Output discipline

- No diacritics.
- No English translation unless requested.
- No Cyrillic duplicate unless requested.
- No explanatory preamble or postscript for routine transliteration or writing.
- Preserve punctuation, paragraph breaks, names and numbers.
- Do not invent new spelling rules. Follow the specification and established examples.
- If a genuinely unresolved ambiguity affects the intended word, ask one short clarification; otherwise make the most contextually consistent choice.

Default: write naturally in Russian Latin and say no more than the task requires.
