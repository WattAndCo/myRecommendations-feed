# myBooks Cover Generation Guide

> Complete guide for generating cover illustrations for all free-in-store books.
> Two collections, two visual styles, one workflow.

---

## Collections

### myBooks: Classics (Japanese) — 53 books
Japanese literary canon from Aozora Bunko. All public domain under Japanese copyright law — every author died either before 1954 (life+50 rule), or died Feb 1955–Dec 1967 with PD vesting before the 2018 life+70 extension froze dates.
Elegant, painterly, atmospheric illustrations. Palette is locked by the collection's `--sref` reference (currently blue-toned) — do not override with colour instructions in individual prompts.

**Numbering scheme:**
- `C01`–`C53` — collection position, easiest → hardest across the whole myBooks Classics set
- `S1`/`S2`/`S3` — series position (only for books inside a named narrative series)

**Named series in this collection:**
| Series title (Japanese) | English | Members |
|---|---|---|
| 夏目漱石 前期三部作 | Natsume Sōseki's Early Trilogy | 三四郎 → それから → 門 |
| 夏目漱石 後期三部作 | Natsume Sōseki's Late Trilogy | 彼岸過迄 → 行人 → こころ |

**Explicitly excluded (still copyrighted):** 川端康成 (d.1972, PD 2043), 三島由紀夫 (d.1970, PD 2041), 志賀直哉 (d.1971, PD 2042).

### myBooks: African Folktales — 27 books
African folk tales translated into Japanese from Storybooks Japan (CC-BY 4.0).
Warm, inviting, picture book style. Separate colour palette TBD.

---

## Difficulty Tier Colours (for badges, NOT cover borders)

| Tier | Hex | Colour |
|------|-----|--------|
| Beginner | #B91C1C | Deep Red |
| Elementary | #C2620F | Burnt Orange |
| Intermediate | #A47B12 | Dark Gold |
| Upper Intermediate | #65A30D | Olive Green |
| Advanced | #4D7C0F | Forest Green |
| Proficiency | #0B5E5E | Teal |

---

## Workflow

### First Time Setup (per collection)
1. Generate one illustration for the first book in the collection
2. Run it 3-5 times (12-20 variations)
3. Pick your favourite, upscale it (U1/U2/U3/U4)
4. Copy the upscaled image URL → this is your `--sref` for the whole collection

### Generating Each Cover
1. Paste the prompt from this guide into Midjourney
2. Pick the best of 4 results, upscale it
3. Save as `{id}.png` in `covers/source_Images/` (raw illustration, no text)
4. Open Affinity template, drop in illustration, add title/author text
5. Export finished cover to `covers/{id}.png`

---

## Midjourney Settings (all prompts)

```
--ar 2:3              Portrait book proportions
--v 6.1               Latest model
--no text letters words writing typography kanji hiragana
--sref [URL]          Style reference (set per collection)
--sw 100              Style weight (how strongly to match reference)
```

---

## Cover Text Data

### myBooks: Classics (Japanese)

> ⚠️ **Removed:** `aozora-yukiguni` (雪国, 川端康成) — NOT PUBLIC DOMAIN. Kawabata d. 1972; caught by 2018 life+70 extension, PD in 2043. Delete the Affinity file for this book.

| # | Filename | JP Title | Author | EN Title | Series |
|---|----------|----------|--------|----------|--------|
| C01 | aozora-tebukuro-wo-kai-ni.png | 手袋を買いに | 新美南吉 | Buying Mittens | |
| C02 | aozora-gon-gitsune.png | ごん狐 | 新美南吉 | Gon, the Fox | |
| C03 | aozora-kumo-no-ito.png | 蜘蛛の糸 | 芥川龍之介 | The Spider's Thread | |
| C04 | aozora-hana.png | 鼻 | 芥川龍之介 | The Nose | |
| C05 | aozora-mikan.png | 蜜柑 | 芥川龍之介 | Mandarin Oranges | |
| C06 | aozora-torokko.png | トロッコ | 芥川龍之介 | The Trolley | |
| C07 | aozora-toshishun.png | 杜子春 | 芥川龍之介 | Tu Tze-chun | |
| C08 | aozora-yodaka-no-hoshi.png | よだかの星 | 宮沢賢治 | The Nighthawk Star | |
| C09 | aozora-cello-hiki-no-goshu.png | セロ弾きのゴーシュ | 宮沢賢治 | Gauche the Cellist | |
| C10 | aozora-chumon-no-ooi-ryouriten.png | 注文の多い料理店 | 宮沢賢治 | The Restaurant of Many Orders | |
| C11 | aozora-yuki-watari.png | 雪渡り | 宮沢賢治 | Crossing the Snow | |
| C12 | aozora-hashire-melos.png | 走れメロス | 太宰治 | Run, Melos! | |
| C13 | aozora-joseito.png | 女生徒 | 太宰治 | Schoolgirl | |
| C14 | aozora-yume-juya.png | 夢十夜 | 夏目漱石 | Ten Nights of Dreams | |
| C15 | aozora-botchan.png | 坊っちゃん | 夏目漱石 | Botchan | |
| C16 | aozora-ginga-tetsudou-no-yoru.png | 銀河鉄道の夜 | 宮沢賢治 | Night on the Galactic Railroad | |
| C17 | aozora-kaze-no-matasaburo.png | 風の又三郎 | 宮沢賢治 | Matasaburō of the Wind | |
| C18 | aozora-otsuberu-to-zou.png | オツベルと象 | 宮沢賢治 | Ozbel and the Elephant | |
| C19 | aozora-lemon.png | 檸檬 | 梶井基次郎 | Lemon | |
| C20 | aozora-rashomon.png | 羅生門 | 芥川龍之介 | Rashomon | |
| C21 | aozora-yabu-no-naka.png | 藪の中 | 芥川龍之介 | In a Grove | |
| C22 | aozora-takasebune.png | 高瀬舟 | 森鷗外 | The Boat on the Takase River | |
| C23 | aozora-sansho-dayu.png | 山椒大夫 | 森鷗外 | Sanshō the Steward | |
| C24 | aozora-maihime.png | 舞姫 | 森鷗外 | The Dancing Girl | |
| C25 | aozora-sangetsuki.png | 山月記 | 中島敦 | The Moon Over the Mountain | |
| C26 | aozora-meijinden.png | 名人伝 | 中島敦 | The Master | |
| C27 | aozora-fugaku-hyakkei.png | 富嶽百景 | 太宰治 | One Hundred Views of Mount Fuji | |
| C28 | aozora-koya-hijiri.png | 高野聖 | 泉鏡花 | The Holy Man of Mount Kōya | |
| C29 | aozora-musashino.png | 武蔵野 | 国木田独歩 | Musashino | |
| C30 | aozora-kaze-tachinu.png | 風立ちぬ | 堀辰雄 | The Wind Has Risen | |
| C31 | aozora-gin-no-saji.png | 銀の匙 | 中勘助 | The Silver Spoon | |
| C32 | aozora-sanshiro.png | 三四郎 | 夏目漱石 | Sanshirō | 夏目漱石 前期三部作 (Early Trilogy) S1/3 |
| C33 | aozora-sorekara.png | それから | 夏目漱石 | And Then | 夏目漱石 前期三部作 (Early Trilogy) S2/3 |
| C34 | aozora-mon.png | 門 | 夏目漱石 | The Gate | 夏目漱石 前期三部作 (Early Trilogy) S3/3 |
| C35 | aozora-higan-sugi-made.png | 彼岸過迄 | 夏目漱石 | To the Spring Equinox and Beyond | 夏目漱石 後期三部作 (Late Trilogy) S1/3 |
| C36 | aozora-kojin.png | 行人 | 夏目漱石 | The Wayfarer | 夏目漱石 後期三部作 (Late Trilogy) S2/3 |
| C37 | aozora-kokoro.png | こころ | 夏目漱石 | Kokoro | 夏目漱石 後期三部作 (Late Trilogy) S3/3 |
| C38 | aozora-jigokuhen.png | 地獄変 | 芥川龍之介 | Hell Screen | |
| C39 | aozora-kappa.png | 河童 | 芥川龍之介 | Kappa | |
| C40 | aozora-ningen-shikkaku.png | 人間失格 | 太宰治 | No Longer Human | |
| C41 | aozora-shayo.png | 斜陽 | 太宰治 | The Setting Sun | |
| C42 | aozora-villon-no-tsuma.png | ヴィヨンの妻 | 太宰治 | Villon's Wife | |
| C43 | aozora-otogi-zoshi.png | お伽草紙 | 太宰治 | Tales | |
| C44 | aozora-riryou.png | 李陵 | 中島敦 | Li Ling | |
| C45 | aozora-kaidan.png | 怪談 | 小泉八雲 | Kwaidan: Ghost Stories | |
| C46 | aozora-sakura-no-mori.png | 桜の森の満開の下 | 坂口安吾 | Under the Cherry Blossoms | |
| C47 | aozora-kani-kosen.png | 蟹工船 | 小林多喜二 | The Crab Cannery Ship | |
| C48 | aozora-darakuron.png | 堕落論 | 坂口安吾 | On Decadence | |
| C49 | aozora-kusamakura.png | 草枕 | 夏目漱石 | Kusamakura | |
| C50 | aozora-wagahai-wa-neko-de-aru.png | 吾輩は猫である | 夏目漱石 | I Am a Cat | |
| C51 | aozora-takekurabe.png | たけくらべ | 樋口一葉 | Child's Play | |
| C52 | aozora-shunkinshow.png | 春琴抄 | 谷崎潤一郎 | A Portrait of Shunkin | |
| C53 | aozora-aru-onna.png | 或る女 | 有島武郎 | A Certain Woman | |

### myBooks: African Folktales

| Filename | Japanese Title | English Title |
|----------|---------------|---------------|
| sbj-0087.png | 本を読むのが好き！ | I Like to Read! |
| sbj-0030.png | いろんな気持ち | Feelings |
| sbj-0302.png | 火 | Fire |
| sbj-0156.png | はらぺこのワニ | The Hungry Crocodile |
| sbj-0002.png | 動物たちを見てごらん | Look at the Animals |
| sbj-0003.png | 学校の制服 | School Clothes |
| sbj-0120.png | 髪 | Hair |
| sbj-0231.png | お天気の本 | Weather Book |
| sbj-0129.png | 働かない弟 | Lazy Little Brother |
| sbj-0067.png | 料理 | Cooking |
| sbj-0009.png | わたしのネコちゃんはどこ？ | Where Is My Cat? |
| sbj-0112.png | 僕の体 | My Body |
| sbj-0111.png | カバに毛がない訳 | Why Hippos Have No Hair |
| sbj-0210.png | ティンギと牛たち | Tingi and the Cows |
| sbj-0296.png | バナナ売りのトム | Tom the Banana Seller |
| sbj-0342.png | お仕置き | Punishment |
| sbj-0089.png | 草木に話しかけるカライ | Khalai Talks to Plants |
| sbj-0095.png | ザーマはすごいよ！ | Zama Is Great! |
| sbj-0004.png | ヤギと犬と牛 | Goat, Dog, and Cow |
| sbj-0110.png | 小さな種 | A Tiny Seed |
| sbj-0294.png | おばあちゃんのバナナ | Grandma's Bananas |
| sbj-0158.png | メンドリとワシ | Hen and Eagle |
| sbj-0066.png | ノジベレと三本の髪の毛 | Nozibele and the Three Hairs |
| sbj-0324.png | 僕が街に向けて家を出た日 | The Day I Left Home for the City |
| sbj-0072.png | ミツオシエの仕返し | The Honeyguide's Revenge |
| sbj-0291.png | ブーシーのお姉さんが言ったこと | What Vusi's Sister Said |
| sbj-0052.png | シンベグィレ | Simbegwire |

---

## Illustration Prompts

### myBooks: Classics (Japanese)

Style reference: `--sref https://cdn.midjourney.com/83d250ce-f069-412d-92fa-f2b291b17814/0_0.png` (blue-toned master — do not override in prompts).

> ⚠️ **`aozora-yukiguni` removed** — NOT PUBLIC DOMAIN (Kawabata d. 1972, PD 2043). Delete any Affinity file for this book.

#### Intermediate (C01–C13)

**C01 · aozora-tebukuro-wo-kai-ni** ✅ DONE — 手袋を買いに (Buying Mittens) — 新美南吉
```
Illustration only, no title, no words, a small fox cub standing in falling snow outside a warmly lit shop window in a rural Japanese village at dusk, the cub holds out one small paw towards the shopkeeper, warm golden lamplight against cold blue snow, intimate and tender mood, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C02 · aozora-gon-gitsune** ✅ DONE — ごん狐 (Gon, the Fox) — 新美南吉
```
Illustration only, no title, no words, a lone red fox carrying chestnuts through tall autumn grass towards a thatched farmhouse, late afternoon golden light, rural Japanese countryside, bittersweet melancholy atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C03 · aozora-kumo-no-ito** ✅ DONE — 蜘蛛の糸 (The Spider's Thread) — 芥川龍之介
```
Illustration only, no title, no words, view from above looking down, golden heavenly light at the top of the image, a thin silver spider thread descending downward into a dark lotus pond far below, a tiny figure clinging to the thread above the dark water, the thread stretches between heaven and hell, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C04 · aozora-hana** ✅ DONE — 鼻 (The Nose) — 芥川龍之介
```
Illustration only, no title, no words, a Buddhist monk in traditional robes looking at his reflection in a still pond, his comically long nose almost touching the water surface, a serene temple garden setting, wry humour mixed with contemplation, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C05 · aozora-mikan** — 蜜柑 (Mandarin Oranges) — 芥川龍之介
```
Illustration only, no title, no words, a country girl leaning out of a steam train window throwing bright mandarin oranges into the air, her younger brothers waving from a railway crossing below, winter afternoon golden light, a poignant tender moment, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C06 · aozora-torokko** — トロッコ (The Trolley) — 芥川龍之介
```
Illustration only, no title, no words, a young boy clinging to a wooden rail cart rolling down a mountain track, two workmen pushing from behind, forest shadows deepening into dusk, childhood fear and wonder, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C07 · aozora-toshishun** ✅ DONE — 杜子春 (Tu Tze-chun) — 芥川龍之介
```
Illustration only, no title, no words, a young man in ancient Chinese robes standing at a crossroads between a bustling golden city and a misty mountain peak where an old hermit waits, twilight sky, a choice between wealth and wisdom, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C08 · aozora-yodaka-no-hoshi** ✅ DONE — よだかの星 (The Nighthawk Star) — 宮沢賢治
```
Illustration only, no title, no words, a small brown nighthawk bird soaring upward into a vast starry night sky, growing smaller and more luminous as it rises, the earth far below, transcendent and lonely atmosphere, elegant painterly style, deep blues and silvers, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C09 · aozora-cello-hiki-no-goshu** ✅ DONE — セロ弾きのゴーシュ (Gauche the Cellist) — 宮沢賢治
```
Illustration only, no title, no words, a dishevelled young man playing a cello in a small cluttered room at night, a cat and a cuckoo bird sitting before him listening intently, warm candlelight, whimsical and earnest atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C10 · aozora-chumon-no-ooi-ryouriten** ✅ DONE — 注文の多い料理店 (The Restaurant of Many Orders) — 宮沢賢治
```
Illustration only, no title, no words, two hunters in Western-style hunting clothes standing before an ornate door deep in a dark mountain forest, eerie golden light from within, darkly comic and unsettling mood, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C11 · aozora-yuki-watari** — 雪渡り (Crossing the Snow) — 宮沢賢治
```
Illustration only, no title, no words, two children in kimono walking across a vast moonlit crusted snowfield, several young foxes watching from the tree line, a distant magic lantern's warm glow, northern Japan winter wonder, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C12 · aozora-hashire-melos** ✅ DONE — 走れメロス (Run, Melos!) — 太宰治
```
Illustration only, no title, no words, a young man running desperately along a rocky path at sunset, torn clothes and bare feet, a distant city on the horizon, storm clouds breaking to reveal golden light, heroic determination and urgency, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C13 · aozora-joseito** — 女生徒 (Schoolgirl) — 太宰治
```
Illustration only, no title, no words, a young woman in a 1930s Japanese schoolgirl uniform gazing at her faint reflection in a mirror, soft morning light through a Tokyo window, introspective and private mood, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

#### Upper Intermediate (C14–C31)

**C14 · aozora-yume-juya** — 夢十夜 (Ten Nights of Dreams) — 夏目漱石
```
Illustration only, no title, no words, a man kneeling in vigil beside a dying woman on a futon in a dim room, a single cherry blossom petal suspended mid-air between them, dreamlike stillness and quiet foreboding, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C15 · aozora-botchan** — 坊っちゃん (Botchan) — 夏目漱石
```
Illustration only, no title, no words, a cocky young man in Meiji-era clothing stepping off a train into a small coastal town in Shikoku, looking unimpressed at the provincial surroundings, fishing boats in the harbour behind him, humorous and energetic, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C16 · aozora-ginga-tetsudou-no-yoru** — 銀河鉄道の夜 (Night on the Galactic Railroad) — 宮沢賢治
```
Illustration only, no title, no words, a small steam train crossing a luminous bridge among the stars of the Milky Way, two boys visible through a lit window, cosmic wonder and gentle sadness, deep indigo sky with brilliant stars, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C17 · aozora-kaze-no-matasaburo** — 風の又三郎 (Matasaburō of the Wind) — 宮沢賢治
```
Illustration only, no title, no words, a red-haired boy in rural school uniform standing alone at the gate of a mountain village schoolhouse, autumn wind scattering yellow leaves, other children peering from behind bamboo, supernatural and uncanny mood, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C18 · aozora-otsuberu-to-zou** — オツベルと象 (Ozbel and the Elephant) — 宮沢賢治
```
Illustration only, no title, no words, a large white elephant standing in chains inside a crude farm courtyard at sunset, a stern-looking master counting coins nearby, darkening fable atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C19 · aozora-lemon** — 檸檬 (Lemon) — 梶井基次郎
```
Illustration only, no title, no words, a single bright yellow lemon placed on top of a stack of colourful art books in a dimly lit bookshop, the lemon glowing as if lit from within, quiet rebellion and unexpected beauty, Kyoto atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C20 · aozora-rashomon** — 羅生門 (Rashomon) — 芥川龍之介
```
Illustration only, no title, no words, a crumbling ancient Japanese gate in heavy rain at dusk, a lone figure sheltering beneath the massive wooden structure, crows circling above, ominous and atmospheric, Heian period Japan, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C21 · aozora-yabu-no-naka** — 藪の中 (In a Grove) — 芥川龍之介
```
Illustration only, no title, no words, a dense bamboo grove with shafts of light breaking through, a samurai sword abandoned on the ground, multiple translucent figures visible at different angles suggesting conflicting testimonies, mysterious and unsettling, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C22 · aozora-takasebune** — 高瀬舟 (The Boat on the Takase River) — 森鷗外
```
Illustration only, no title, no words, a small wooden boat drifting down a moonlit river at night, a guard and a prisoner sitting together in quiet conversation, Edo period Kyoto, serene and contemplative despite the solemn journey, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C23 · aozora-sansho-dayu** — 山椒大夫 (Sanshō the Steward) — 森鷗外
```
Illustration only, no title, no words, two ragged children a sister and younger brother walking barefoot along a dark coastal path in medieval Japan, moonlit sea beyond, deep sorrow and resilience, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C24 · aozora-maihime** — 舞姫 (The Dancing Girl) — 森鷗外
```
Illustration only, no title, no words, a Japanese gentleman in Meiji Western formal dress walking beneath a gaslamp in rainy 1880s Berlin, a pale young dancer watching from a doorway, cross-cultural melancholy, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C25 · aozora-sangetsuki** — 山月記 (The Moon Over the Mountain) — 中島敦
```
Illustration only, no title, no words, a tiger crouching on a moonlit mountain path, its eyes reflecting human intelligence and sorrow, a faint ghostly figure of a scholar visible within its form, ancient Chinese landscape, haunting and poetic, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C26 · aozora-meijinden** — 名人伝 (The Master) — 中島敦
```
Illustration only, no title, no words, an elderly archery master seated meditating on a windswept cliff in ancient China, an unstrung bow resting across his knees, mythic mastery transcending form, distant peaks and drifting clouds, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C27 · aozora-fugaku-hyakkei** — 富嶽百景 (One Hundred Views of Mount Fuji) — 太宰治
```
Illustration only, no title, no words, Mount Fuji seen through the open shoji doors of a mountain teahouse at dawn, a figure in a yukata standing on the veranda with a cup in hand, contemplative solitude, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C28 · aozora-koya-hijiri** — 高野聖 (The Holy Man of Mount Kōya) — 泉鏡花
```
Illustration only, no title, no words, a young monk in traveller's robes pausing at a forested mountain crossroads at twilight, a beautiful woman barely visible among the mist between cedars, supernatural undercurrent, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C29 · aozora-musashino** — 武蔵野 (Musashino) — 国木田独歩
```
Illustration only, no title, no words, a wandering scholar walking through an oak forest on the Musashino plain at autumn dusk, golden leaves drifting through slanting light, quiet solitude of nature writing, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C30 · aozora-kaze-tachinu** — 風立ちぬ (The Wind Has Risen) — 堀辰雄
```
Illustration only, no title, no words, a young man and young woman sitting on the veranda of an alpine sanatorium overlooking a pine valley, 1930s clothing, a gentle breeze moving her hair, fragile beauty and foreknowledge of loss, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C31 · aozora-gin-no-saji** — 銀の匙 (The Silver Spoon) — 中勘助
```
Illustration only, no title, no words, a small tarnished silver spoon held delicately in a child's hand, a Meiji-era parlour blurred softly in background, firelight on lacquered surfaces, bittersweet childhood memory, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

#### Advanced (C32–C48)

**C32 · aozora-sanshiro** — 三四郎 (Sanshirō) — 夏目漱石 — Series: **夏目漱石 前期三部作 (Early Trilogy) · S1/3**
```
Illustration only, no title, no words, a young provincial man in Meiji student uniform stepping off a steam train onto a Tokyo platform, suitcases at his feet, the modern city rising beyond the tracks, beginnings and uncertainty, scene framed by an architectural threshold (doorway, gate, or window), elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C33 · aozora-sorekara** — それから (And Then) — 夏目漱石 — Series: **夏目漱石 前期三部作 (Early Trilogy) · S2/3**
```
Illustration only, no title, no words, a well-dressed Meiji gentleman sitting alone in a tatami study at dusk, a framed portrait of a woman visible on the shelf behind him, moral crisis and quiet longing, scene framed by an architectural threshold (doorway, gate, or window), elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C34 · aozora-mon** — 門 (The Gate) — 夏目漱石 — Series: **夏目漱石 前期三部作 (Early Trilogy) · S3/3**
```
Illustration only, no title, no words, a middle-aged couple sitting quietly across from each other in a small Tokyo house on a grey winter afternoon, the timbered gate of a Zen temple visible through an open paper door, restrained intimacy, scene framed by an architectural threshold (doorway, gate, or window), elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C35 · aozora-higan-sugi-made** — 彼岸過迄 (To the Spring Equinox and Beyond) — 夏目漱石 — Series: **夏目漱石 後期三部作 (Late Trilogy) · S1/3**
```
Illustration only, no title, no words, a young man standing on a narrow Meiji Tokyo street during a spring equinox festival, figures blurred in motion around him, watching intently as if collecting stories, cool evening light, two figures with visible physical distance between them one observing the other, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C36 · aozora-kojin** — 行人 (The Wayfarer) — 夏目漱石 — Series: **夏目漱石 後期三部作 (Late Trilogy) · S2/3**
```
Illustration only, no title, no words, a husband and wife standing at the rail of a small wooden ferry on a misty lake, a third man watching from the distant shore, late Meiji, unspoken distance between the figures, two figures with visible physical distance between them one observing the other, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C37 · aozora-kokoro** — こころ (Kokoro) — 夏目漱石 — Series: **夏目漱石 後期三部作 (Late Trilogy) · S3/3**
```
Illustration only, no title, no words, two men walking along a beach in Meiji-era Japan, one young and one older, the older man's shadow stretching long behind him, a sense of unspoken secrets and generational divide, two figures with visible physical distance between them one observing the other, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C38 · aozora-jigokuhen** — 地獄変 (Hell Screen) — 芥川龍之介
```
Illustration only, no title, no words, a Heian court painter feverishly painting a hellscape on a folding screen by lantern light, a flame-lit carriage silhouetted through the window behind him, disturbing artistic obsession, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C39 · aozora-kappa** — 河童 (Kappa) — 芥川龍之介
```
Illustration only, no title, no words, a human traveller sitting in conversation with several kappa water creatures in a dimly lit underwater chamber of carved stone, strange surreal Taishō satire, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C40 · aozora-ningen-shikkaku** — 人間失格 (No Longer Human) — 太宰治
```
Illustration only, no title, no words, a young man sitting alone at a bar counter in 1940s Tokyo, his face partially obscured by shadow, a mask lying on the counter beside a drink, deep isolation despite the urban setting, noir atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C41 · aozora-shayo** — 斜陽 (The Setting Sun) — 太宰治
```
Illustration only, no title, no words, a grand but decaying Japanese manor house at sunset, a woman in a faded kimono standing in the overgrown garden looking at the sinking sun, aristocratic decline and quiet defiance, warm dying light on cold shadows, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C42 · aozora-villon-no-tsuma** — ヴィヨンの妻 (Villon's Wife) — 太宰治
```
Illustration only, no title, no words, a young mother carrying a baby through a narrow post-war Tokyo alley at dusk, wooden houses leaning overhead, a distant izakaya lantern visible, quiet resilience, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C43 · aozora-otogi-zoshi** — お伽草紙 (Tales) — 太宰治
```
Illustration only, no title, no words, a father reading aloud to children in an underground air-raid shelter, folk-tale characters a tanuki a hare a crane half-visible as shadows on the walls, candlelit wartime tenderness, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C44 · aozora-riryou** — 李陵 (Li Ling) — 中島敦
```
Illustration only, no title, no words, a lone Han dynasty general in military dress standing on a vast Mongolian steppe at twilight, snow blowing across bare grass, honour and exile, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C45 · aozora-kaidan** — 怪談 (Kwaidan: Ghost Stories) — 小泉八雲
```
Illustration only, no title, no words, a willow tree in mist by a lantern-lit garden path at night, a pale female figure barely visible among the hanging branches, traditional Japanese ghost story atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C46 · aozora-sakura-no-mori** — 桜の森の満開の下 (Under the Cherry Blossoms) — 坂口安吾
```
Illustration only, no title, no words, a figure walking slowly beneath a vast grove of cherry trees in full bloom, petals falling like snow, a shadowy second figure trailing behind, ancient Japan, haunting beauty and dread, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C47 · aozora-kani-kosen** — 蟹工船 (The Crab Cannery Ship) — 小林多喜二
```
Illustration only, no title, no words, a massive steel crab-cannery ship labouring through a stormy northern sea, exhausted workers huddled under tarpaulins on deck, harsh industrial grey and black, proletarian struggle, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C48 · aozora-darakuron** — 堕落論 (On Decadence) — 坂口安吾
```
Illustration only, no title, no words, a lone figure standing in the ruined streets of post-war Tokyo, broken buildings smouldering, a single fresh plant growing through rubble, philosophical reckoning, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

#### Proficiency (C49–C53)

**C49 · aozora-kusamakura** — 草枕 (Kusamakura) — 夏目漱石
```
Illustration only, no title, no words, an artist sitting on the veranda of a mountain hot-spring ryokan, mist rolling through distant valleys, a woman's silhouette through a paper screen, haiku-like stillness, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C50 · aozora-wagahai-wa-neko-de-aru** — 吾輩は猫である (I Am a Cat) — 夏目漱石
```
Illustration only, no title, no words, a dignified cat sitting on a stack of books in a cluttered Meiji-era study, observing a group of intellectuals arguing over tea through a sliding door, the cat's expression is one of amused contempt, satirical and witty, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C51 · aozora-takekurabe** — たけくらべ (Child's Play) — 樋口一葉
```
Illustration only, no title, no words, two children standing at the narrow wooden gate of the Meiji-era Yoshiwara pleasure quarter at dusk, paper lanterns lit beyond, youth on the edge of a hard adult world, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C52 · aozora-shunkinshow** — 春琴抄 (A Portrait of Shunkin) — 谷崎潤一郎
```
Illustration only, no title, no words, a beautiful blind woman playing a shamisen in a traditional Japanese room, a devoted man kneeling behind her in shadow, cherry blossoms drifting through an open screen, obsessive devotion and fragile beauty, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**C53 · aozora-aru-onna** — 或る女 (A Certain Woman) — 有島武郎
```
Illustration only, no title, no words, a woman in Meiji-era Western dress standing at the railing of a steamship, looking out at the open sea with fierce determination, her hair and dress caught by the wind, independence and defiance against convention, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

---

### myBooks: African Folktales

Style: warmer, brighter, playful picture book aesthetic. Generate a new `--sref` from the first story (sbj-0087).

Prompt template:
```
Children's book cover illustration, [SCENE], warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [FOLKTALE STYLE URL] --no text letters words writing typography
```

#### Beginner (19 stories, A-Z)

**sbj-0067.png** — 料理 (Cooking)
```
Children's book cover illustration, a cheerful kitchen scene with pots vegetables and someone cooking, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0030.png** — いろんな気持ち (Feelings)
```
Children's book cover illustration, a child's face shown in multiple expressions happy sad angry surprised like a collage, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0302.png** — 火 (Fire)
```
Children's book cover illustration, a warm campfire with orange flames people sitting around it night sky, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0004.png** — ヤギと犬と牛 (Goat, Dog, and Cow)
```
Children's book cover illustration, a goat a dog and a cow travelling together on a road, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0120.png** — 髪 (Hair)
```
Children's book cover illustration, different hairstyles on different people braids afro straight curly, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0087.png** — 本を読むのが好き！ (I Like to Read!)
```
Children's book cover illustration, a happy child sitting cross-legged reading a colourful book surrounded by floating open books, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --no text letters words writing typography
```

**sbj-0089.png** — 草木に話しかけるカライ (Khalai Talks to Plants)
```
Children's book cover illustration, a girl kneeling in a garden whispering to flowers and plants, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0129.png** — 働かない弟 (Lazy Little Brother)
```
Children's book cover illustration, a lazy boy lying under a tree while his sister works in a garden, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0002.png** — 動物たちを見てごらん (Look at the Animals)
```
Children's book cover illustration, African savanna animals gathered together elephant giraffe monkey bird, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0112.png** — 僕の体 (My Body)
```
Children's book cover illustration, a child pointing to different body parts hands feet eyes ears, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0342.png** — お仕置き (Punishment)
```
Children's book cover illustration, a mischievous child caught red-handed an adult looking stern, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0003.png** — 学校の制服 (School Clothes)
```
Children's book cover illustration, children in different school uniforms walking to school together, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0156.png** — はらぺこのワニ (The Hungry Crocodile)
```
Children's book cover illustration, a green crocodile with its mouth wide open looking hungry near a river, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0210.png** — ティンギと牛たち (Tingi and the Cows)
```
Children's book cover illustration, a boy herding cows across an African grassland, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0296.png** — バナナ売りのトム (Tom the Banana Seller)
```
Children's book cover illustration, a boy carrying a large bunch of bananas on his head at a market, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0231.png** — お天気の本 (Weather Book)
```
Children's book cover illustration, weather scenes in quadrants sun rain wind clouds, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0009.png** — わたしのネコちゃんはどこ？ (Where Is My Cat?)
```
Children's book cover illustration, a child looking under furniture and behind curtains searching for a hiding cat, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0111.png** — カバに毛がない訳 (Why Hippos Have No Hair)
```
Children's book cover illustration, a hippo standing embarrassed next to a fire other animals watching, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0095.png** — ザーマはすごいよ！ (Zama Is Great!)
```
Children's book cover illustration, a confident girl standing proudly with hands on hips, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

#### Elementary (7 stories, A-Z)

**sbj-0110.png** — 小さな種 (A Tiny Seed)
```
Children's book cover illustration, a woman planting a tiny seed in African soil a forest growing behind her, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0294.png** — おばあちゃんのバナナ (Grandma's Bananas)
```
Children's book cover illustration, a grandmother handing bananas to children under a banana tree, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0158.png** — メンドリとワシ (Hen and Eagle)
```
Children's book cover illustration, a hen and an eagle facing each other one on the ground one in a tree, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0066.png** — ノジベレと三本の髪の毛 (Nozibele and the Three Hairs)
```
Children's book cover illustration, a girl holding three glowing hairs a river and a bridge in the background, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0324.png** — 僕が街に向けて家を出た日 (The Day I Left Home for the City)
```
Children's book cover illustration, a boy with a small bag walking away from a rural village towards a distant city skyline, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0072.png** — ミツオシエの仕返し (The Honeyguide's Revenge)
```
Children's book cover illustration, a honeyguide bird leading a man through the bush bees in the distance, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

**sbj-0291.png** — ブーシーのお姉さんが言ったこと (What Vusi's Sister Said)
```
Children's book cover illustration, an older sister speaking seriously to her younger brother, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

#### Intermediate (1 story)

**sbj-0052.png** — シンベグィレ (Simbegwire)
```
Children's book cover illustration, a young girl finding comfort under a tree a kind woman's spirit watching over her, warm and inviting, simple bold shapes, friendly atmosphere, picture book style --ar 2:3 --sref [URL] --no text letters words writing typography
```

---

## Progress Tracker

### myBooks: Classics (Japanese) — 9/53 done

**Intermediate (C01–C13)**
- [x] C01 aozora-tebukuro-wo-kai-ni
- [x] C02 aozora-gon-gitsune
- [x] C03 aozora-kumo-no-ito
- [x] C04 aozora-hana
- [ ] C05 aozora-mikan
- [ ] C06 aozora-torokko
- [x] C07 aozora-toshishun
- [x] C08 aozora-yodaka-no-hoshi
- [x] C09 aozora-cello-hiki-no-goshu
- [x] C10 aozora-chumon-no-ooi-ryouriten
- [ ] C11 aozora-yuki-watari
- [x] C12 aozora-hashire-melos
- [ ] C13 aozora-joseito

**Upper Intermediate (C14–C31)**
- [ ] C14 aozora-yume-juya
- [ ] C15 aozora-botchan
- [ ] C16 aozora-ginga-tetsudou-no-yoru
- [ ] C17 aozora-kaze-no-matasaburo
- [ ] C18 aozora-otsuberu-to-zou
- [ ] C19 aozora-lemon
- [ ] C20 aozora-rashomon
- [ ] C21 aozora-yabu-no-naka
- [ ] C22 aozora-takasebune
- [ ] C23 aozora-sansho-dayu
- [ ] C24 aozora-maihime
- [ ] C25 aozora-sangetsuki
- [ ] C26 aozora-meijinden
- [ ] C27 aozora-fugaku-hyakkei
- [ ] C28 aozora-koya-hijiri
- [ ] C29 aozora-musashino
- [ ] C30 aozora-kaze-tachinu
- [ ] C31 aozora-gin-no-saji

**Advanced (C32–C48)**
- [ ] C32 aozora-sanshiro — 夏目漱石 前期三部作 (Early Trilogy) S1/3
- [ ] C33 aozora-sorekara — 夏目漱石 前期三部作 (Early Trilogy) S2/3
- [ ] C34 aozora-mon — 夏目漱石 前期三部作 (Early Trilogy) S3/3
- [ ] C35 aozora-higan-sugi-made — 夏目漱石 後期三部作 (Late Trilogy) S1/3
- [ ] C36 aozora-kojin — 夏目漱石 後期三部作 (Late Trilogy) S2/3
- [ ] C37 aozora-kokoro — 夏目漱石 後期三部作 (Late Trilogy) S3/3
- [ ] C38 aozora-jigokuhen
- [ ] C39 aozora-kappa
- [ ] C40 aozora-ningen-shikkaku
- [ ] C41 aozora-shayo
- [ ] C42 aozora-villon-no-tsuma
- [ ] C43 aozora-otogi-zoshi
- [ ] C44 aozora-riryou
- [ ] C45 aozora-kaidan
- [ ] C46 aozora-sakura-no-mori
- [ ] C47 aozora-kani-kosen
- [ ] C48 aozora-darakuron

**Proficiency (C49–C53)**
- [ ] C49 aozora-kusamakura
- [ ] C50 aozora-wagahai-wa-neko-de-aru
- [ ] C51 aozora-takekurabe
- [ ] C52 aozora-shunkinshow
- [ ] C53 aozora-aru-onna

**Removed:** ~~aozora-yukiguni~~ — not PD (Kawabata d. 1972, PD 2043)

### myBooks: African Folktales — 0/27 done
- [ ] All 27 stories (generate style reference first from sbj-0087)
