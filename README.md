🧭 [Overview](https://github.com/mrk214)

| abbr | name | lang | first<br>chapter |
| --- | --- | :---: | :---: |
| `CSB` | Christian Standard Bible | **eng** | [json](https://mrk214.github.io/snapshots-by-chapter/en___eng___eng/CSB_vid_1713/GEN.1.json) |
| `ESV` | English Standard Version 2016 | **eng** | [json](https://mrk214.github.io/snapshots-by-chapter/en___eng___eng/ESV_vid_59/GEN.1.json) |
| `KJV` | King James Version | **eng** | [json](https://mrk214.github.io/snapshots-by-chapter/en___eng___eng/KJV_vid_1/GEN.1.json) |
| `NASB2020` | New American Standard Bible - NASB | **eng** | [json](https://mrk214.github.io/snapshots-by-chapter/en___eng___eng/NASB2020_vid_2692/GEN.1.json) |
| `NIV` | New International Version | **eng** | [json](https://mrk214.github.io/snapshots-by-chapter/en___eng___eng/NIV_vid_111/GEN.1.json) |
| `NKJV` | New King James Version | **eng** | [json](https://mrk214.github.io/snapshots-by-chapter/en___eng___eng/NKJV_vid_114/GEN.1.json) |
| `NLT` | New Living Translation | **eng** | [json](https://mrk214.github.io/snapshots-by-chapter/en___eng___eng/NLT_vid_116/GEN.1.json) |

---

| abbr | name | lang | first<br>chapter |
| --- | --- | :---: | :---: |
| `DHH94I` | Biblia Dios Habla Hoy | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/DHH94I_vid_52/GEN.1.json) |
| `DHHS94` | Dios habla Hoy Estándar | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/DHHS94_vid_1846/GEN.1.json) |
| `LBLA` | La Biblia de las Américas | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/LBLA_vid_89/GEN.1.json) |
| `NBLA` | Nueva Biblia de las Américas | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/NBLA_vid_103/GEN.1.json) |
| `NTV` | Nueva Traducción Viviente | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/NTV_vid_127/GEN.1.json) |
| `NVI` | Nueva Versión Internacional - Español | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/NVI_vid_128/GEN.1.json) |
| `RVA2015` | Reina Valera Actualizada | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/RVA2015_vid_1782/GEN.1.json) |
| `RVC` | Reina Valera Contemporánea | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/RVC_vid_146/GEN.1.json) |
| `RVR1960` | Biblia Reina Valera 1960 | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/RVR1960_vid_149/GEN.1.json) |
| `TLAI` | Traducción en Lenguaje Actual Interconfesional | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/TLAI_vid_178/GEN.1.json) |
| `TLA` | Traducción en Lenguaje Actual | **spa** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa/TLA_vid_176/GEN.1.json) |
| `NVI` | Nueva Versión Internacional - Castellano | **spa_es** | [json](https://mrk214.github.io/snapshots-by-chapter/es___spa___spa_es/NVI_vid_1637/GEN.1.json) |

---

| abbr | name | lang | first<br>chapter |
| --- | --- | :---: | :---: |
| `A21` | Biblia Almeida Século 21 | **por** | [json](https://mrk214.github.io/snapshots-by-chapter/pt___por___por/A21_vid_2645/GEN.1.json) |
| `ARA` | Almeida Revista e Atualizada | **por** | [json](https://mrk214.github.io/snapshots-by-chapter/pt___por___por/ARA_vid_1608/GEN.1.json) |
| `ARC` | Almeida Revista e Corrigida | **por** | [json](https://mrk214.github.io/snapshots-by-chapter/pt___por___por/ARC_vid_212/GEN.1.json) |
| `NAA` | Nova Almeida Atualizada | **por** | [json](https://mrk214.github.io/snapshots-by-chapter/pt___por___por/NAA_vid_1840/GEN.1.json) |
| `NTLH` | Nova Tradução na Linguagem de Hoje | **por** | [json](https://mrk214.github.io/snapshots-by-chapter/pt___por___por/NTLH_vid_211/GEN.1.json) |
| `NVI` | Nova Versão Internacional 2011 | **por** | [json](https://mrk214.github.io/snapshots-by-chapter/pt___por___por/NVI_vid_4360/GEN.1.json) |
| `ARC` | Almeida Revista e Corrigida (Portugal) | **por_pt** | [json](https://mrk214.github.io/snapshots-by-chapter/pt___por___por_pt/ARC_vid_215/GEN.1.json) |

---

## 👉 TypeScript Types

Every JSON file uses the following TypeScript definitions:

```typescript
export type Root = {
  _links: {
    prev_usfm: string | null
    next_usfm: string | null
    book_first_usfm: string
    book_last_usfm: string
    prev: string | null
    next: string | null
    book_first: string
    book_last: string
  }
  book: {
    book_usfm: string
    name: string
  }
  chapter: {
    chapter_usfm: string
    current: CurrPrevNext
    previous: CurrPrevNext | null
    next: CurrPrevNext | null
    items: ChapterItem[]
  }
  version: {
    version_id: number
    local_abbreviation: string
    local_title: string
    language: Language
    repository: string
    publisher: Publisher
    copyright: Copyright
  }
}

export type CurrPrevNext = {
  usfm: string
  human: string
}

export type ChapterItem = {
  type: ChapterItemType
  verse_numbers: number[]
  lines: string[]
  rlw_lines: RedLetterWordsSection[][]
}

// Depending on the version, some ChapterItemTypes may appear more or less.
// The essential ChapterItemTypes are: 'heading1' and 'verse'.
// I have added comments that can be used as a reference for styles. 👇👇👇
// (This is only a reference; you can apply any styles you want.)
export type ChapterItemType =
  | 'section1' // rare        - weight: 900 - h1
  | 'section2' // rare        - weight: 800 - h2
  | 'heading1' // very common - weight: 700 - h3
  | 'heading2' // common      - weight: 600 - h4
  | 'label' //    common      - weight: 500 - italic
  | 'verse' //    very common - weight: 400 - regular text

export type RedLetterWordsSection = {
  text: string
  rl: boolean
}

export type Language = {
  iso_639_1: string
  iso_639_3: string
  language_tag: string
  local_name: string
  text_direction: string
}

export type Publisher = {
  name: string
}

export type Copyright = {
  html: string
  text: string
}
```
