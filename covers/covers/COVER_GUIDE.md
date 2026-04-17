# myBooks Cover Generation Guide

> Complete guide for generating cover illustrations for all free-in-store books.
> Two collections, two visual styles, one workflow.

---

## Collections

### myBooks: Classics (Japanese) — 23 books
Japanese literary canon from Aozora Bunko. Public domain.
Elegant, painterly, atmospheric illustrations. Raspberry colour palette (Japanese language accent).

### myBooks: African Folktales — 27 books
African folk tales translated into Japanese from Storybooks Japan (CC-BY 4.0).
Warm, inviting, picture book style. Separate colour palette TBD.

---

## Language Colour Palettes

Each language in the myWords platform has an accent colour. Covers use the language colour as the primary palette for the border/frame and should influence the illustration tone.

| Language | Light Accent | Dark Accent | Cover Palette Direction |
|----------|-------------|-------------|------------------------|
| **Japanese** | #8D0048 (raspberry) | #C70066 (bright raspberry) | Warm reds, crimsons, deep pinks |
| French | TBD | TBD | TBD |
| German | TBD | TBD | TBD |

### Difficulty Tier Colours (for badges, NOT cover borders)

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

### Changing Colour Palette on Existing Images

To shift an existing blue-toned illustration to raspberry/red:

**Option A — Regenerate with colour direction:**
Add colour instructions to the prompt and use a new `--sref` that's already in the target palette:
```
[existing prompt], warm raspberry and crimson colour palette, deep red tones, no blue no teal --sref [NEW RED-TONED REFERENCE URL]
```

**Option B — Regenerate from existing with Vary:**
1. Open the existing image in Midjourney
2. Click **Vary (Subtle)** or **Vary (Strong)**
3. Add a remaster prompt: `--no blue teal cyan` and add `warm crimson raspberry red tones`

**Option C — Recolour in Affinity:**
1. Open the source illustration in Affinity Photo
2. Adjustment Layer → HSL (Hue/Saturation/Lightness)
3. Shift the Blues/Cyans hue towards Red/Magenta
4. Adjust saturation to match the raspberry palette
5. This preserves the composition while changing the colour mood

**Option D — Generate a new reference image first:**
1. Take the prompt for 手袋を買いに and add: `warm crimson and raspberry colour palette, deep red and pink tones, no blue no teal`
2. Generate until you get one you like in the red palette
3. Upscale it → use as the new `--sref` for all remaining books
4. This is the cleanest approach — one new reference, then batch the rest

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

| Filename | Japanese Title | Author | English Title |
|----------|---------------|--------|---------------|
| aozora-tebukuro-wo-kai-ni.png | 手袋を買いに | 新美南吉 | Buying Mittens |
| aozora-gon-gitsune.png | ごん狐 | 新美南吉 | Gon, the Fox |
| aozora-kumo-no-ito.png | 蜘蛛の糸 | 芥川龍之介 | The Spider's Thread |
| aozora-hana.png | 鼻 | 芥川龍之介 | The Nose |
| aozora-yodaka-no-hoshi.png | よだかの星 | 宮沢賢治 | The Nighthawk Star |
| aozora-cello-hiki-no-goshu.png | セロ弾きのゴーシュ | 宮沢賢治 | Gauche the Cellist |
| aozora-chumon-no-ooi-ryouriten.png | 注文の多い料理店 | 宮沢賢治 | The Restaurant of Many Orders |
| aozora-toshishun.png | 杜子春 | 芥川龍之介 | Tu Tze-chun |
| aozora-hashire-melos.png | 走れメロス | 太宰治 | Run, Melos! |
| aozora-rashomon.png | 羅生門 | 芥川龍之介 | Rashomon |
| aozora-ginga-tetsudou-no-yoru.png | 銀河鉄道の夜 | 宮沢賢治 | Night on the Galactic Railroad |
| aozora-lemon.png | 檸檬 | 梶井基次郎 | Lemon |
| aozora-yabu-no-naka.png | 藪の中 | 芥川龍之介 | In a Grove |
| aozora-botchan.png | 坊っちゃん | 夏目漱石 | Botchan |
| aozora-takasebune.png | 高瀬舟 | 森鷗外 | The Boat on the Takase River |
| aozora-sangetsuki.png | 山月記 | 中島敦 | The Moon Over the Mountain |
| aozora-ningen-shikkaku.png | 人間失格 | 太宰治 | No Longer Human |
| aozora-kokoro.png | こころ | 夏目漱石 | Kokoro |
| aozora-yukiguni.png | 雪国 | 川端康成 | Snow Country |
| aozora-shayo.png | 斜陽 | 太宰治 | The Setting Sun |
| aozora-wagahai-wa-neko-de-aru.png | 吾輩は猫である | 夏目漱石 | I Am a Cat |
| aozora-shunkinshow.png | 春琴抄 | 谷崎潤一郎 | A Portrait of Shunkin |
| aozora-aru-onna.png | 或る女 | 有島武郎 | A Certain Woman |

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

Style reference: `--sref https://cdn.midjourney.com/83d250ce-f069-412d-92fa-f2b291b17814/0_0.png`
Colour palette note: Current reference is blue-toned. To shift to Japanese raspberry palette, regenerate reference with `warm crimson and raspberry colour palette, deep red and pink tones, no blue no teal` added to the prompt (see "Changing Colour Palette" section above).

#### Intermediate

**aozora-tebukuro-wo-kai-ni.png** ✅ DONE — 手袋を買いに (Buying Mittens)
```
Illustration only, no title, no words, a small fox cub standing in falling snow outside a warmly lit shop window in a rural Japanese village at dusk, the cub holds out one small paw towards the shopkeeper, warm golden lamplight against cold blue snow, intimate and tender mood, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-gon-gitsune.png** ✅ DONE — ごん狐 (Gon, the Fox)
```
Illustration only, no title, no words, a lone red fox carrying chestnuts through tall autumn grass towards a thatched farmhouse, late afternoon golden light, rural Japanese countryside, bittersweet melancholy atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-kumo-no-ito.png** ✅ DONE — 蜘蛛の糸 (The Spider's Thread)
```
Illustration only, no title, no words, view from above looking down, golden heavenly light at the top of the image, a thin silver spider thread descending downward into a dark lotus pond far below, a tiny figure clinging to the thread above the dark water, the thread stretches between heaven and hell, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-hana.png** ✅ DONE — 鼻 (The Nose)
```
Illustration only, no title, no words, a Buddhist monk in traditional robes looking at his reflection in a still pond, his comically long nose almost touching the water surface, a serene temple garden setting, wry humour mixed with contemplation, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-yodaka-no-hoshi.png** ✅ DONE — よだかの星 (The Nighthawk Star)
```
Illustration only, no title, no words, a small brown nighthawk bird soaring upward into a vast starry night sky, growing smaller and more luminous as it rises, the earth far below, transcendent and lonely atmosphere, elegant painterly style, deep blues and silvers, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-cello-hiki-no-goshu.png** ✅ DONE — セロ弾きのゴーシュ (Gauche the Cellist)
```
Illustration only, no title, no words, a dishevelled young man playing a cello in a small cluttered room at night, a cat and a cuckoo bird sitting before him listening intently, warm candlelight, whimsical and earnest atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-chumon-no-ooi-ryouriten.png** ✅ DONE — 注文の多い料理店 (The Restaurant of Many Orders)
```
Illustration only, no title, no words, two hunters in Western-style hunting clothes standing before an ornate door deep in a dark mountain forest, eerie golden light from within, darkly comic and unsettling mood, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-toshishun.png** ✅ DONE — 杜子春 (Tu Tze-chun)
```
Illustration only, no title, no words, a young man in ancient Chinese robes standing at a crossroads between a bustling golden city and a misty mountain peak where an old hermit waits, twilight sky, a choice between wealth and wisdom, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-hashire-melos.png** ✅ DONE — 走れメロス (Run, Melos!)
```
Illustration only, no title, no words, a young man running desperately along a rocky path at sunset, torn clothes and bare feet, a distant city on the horizon, storm clouds breaking to reveal golden light, heroic determination and urgency, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

#### Upper Intermediate

**aozora-botchan.png** — 坊っちゃん (Botchan)
```
Illustration only, no title, no words, a cocky young man in Meiji-era clothing stepping off a train into a small coastal town in Shikoku, looking unimpressed at the provincial surroundings, fishing boats in the harbour behind him, humorous and energetic, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-ginga-tetsudou-no-yoru.png** — 銀河鉄道の夜 (Night on the Galactic Railroad)
```
Illustration only, no title, no words, a small steam train crossing a luminous bridge among the stars of the Milky Way, two boys visible through a lit window, cosmic wonder and gentle sadness, deep indigo sky with brilliant stars, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-lemon.png** — 檸檬 (Lemon)
```
Illustration only, no title, no words, a single bright yellow lemon placed on top of a stack of colourful art books in a dimly lit bookshop, the lemon glowing as if lit from within, quiet rebellion and unexpected beauty, Kyoto atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-rashomon.png** — 羅生門 (Rashomon)
```
Illustration only, no title, no words, a crumbling ancient Japanese gate in heavy rain at dusk, a lone figure sheltering beneath the massive wooden structure, crows circling above, ominous and atmospheric, Heian period Japan, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-sangetsuki.png** — 山月記 (The Moon Over the Mountain)
```
Illustration only, no title, no words, a tiger crouching on a moonlit mountain path, its eyes reflecting human intelligence and sorrow, a faint ghostly figure of a scholar visible within its form, ancient Chinese landscape, haunting and poetic, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-takasebune.png** — 高瀬舟 (The Boat on the Takase River)
```
Illustration only, no title, no words, a small wooden boat drifting down a moonlit river at night, a guard and a prisoner sitting together in quiet conversation, Edo period Kyoto, serene and contemplative despite the solemn journey, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-yabu-no-naka.png** — 藪の中 (In a Grove)
```
Illustration only, no title, no words, a dense bamboo grove with shafts of light breaking through, a samurai sword abandoned on the ground, multiple translucent figures visible at different angles suggesting conflicting testimonies, mysterious and unsettling, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

#### Advanced

**aozora-kokoro.png** — こころ (Kokoro)
```
Illustration only, no title, no words, two men walking along a beach in Meiji-era Japan, one young and one older, the older man's shadow stretching long behind him, a sense of unspoken secrets and generational divide, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-ningen-shikkaku.png** — 人間失格 (No Longer Human)
```
Illustration only, no title, no words, a young man sitting alone at a bar counter in 1940s Tokyo, his face partially obscured by shadow, a mask lying on the counter beside a drink, deep isolation despite the urban setting, noir atmosphere, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-shayo.png** — 斜陽 (The Setting Sun)
```
Illustration only, no title, no words, a grand but decaying Japanese manor house at sunset, a woman in a faded kimono standing in the overgrown garden looking at the sinking sun, aristocratic decline and quiet defiance, warm dying light on cold shadows, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-yukiguni.png** — 雪国 (Snow Country)
```
Illustration only, no title, no words, a train emerging from a long tunnel into a snow-covered mountain landscape, a woman's face faintly reflected in the dark train window overlaid on the white landscape, ethereal and melancholy, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

#### Proficiency

**aozora-aru-onna.png** — 或る女 (A Certain Woman)
```
Illustration only, no title, no words, a woman in Meiji-era Western dress standing at the railing of a steamship, looking out at the open sea with fierce determination, her hair and dress caught by the wind, independence and defiance against convention, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-shunkinshow.png** — 春琴抄 (A Portrait of Shunkin)
```
Illustration only, no title, no words, a beautiful blind woman playing a shamisen in a traditional Japanese room, a devoted man kneeling behind her in shadow, cherry blossoms drifting through an open screen, obsessive devotion and fragile beauty, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
```

**aozora-wagahai-wa-neko-de-aru.png** — 吾輩は猫である (I Am a Cat)
```
Illustration only, no title, no words, a dignified cat sitting on a stack of books in a cluttered Meiji-era study, observing a group of intellectuals arguing over tea through a sliding door, the cat's expression is one of amused contempt, satirical and witty, elegant painterly style, muted sophisticated palette --ar 2:3 --sref [URL] --no text letters words writing typography kanji hiragana
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

### myBooks: Classics (Japanese) — 9/23 done
- [x] aozora-tebukuro-wo-kai-ni (Intermediate)
- [x] aozora-gon-gitsune (Intermediate)
- [x] aozora-kumo-no-ito (Intermediate)
- [x] aozora-hana (Intermediate)
- [x] aozora-yodaka-no-hoshi (Intermediate)
- [x] aozora-cello-hiki-no-goshu (Intermediate)
- [x] aozora-chumon-no-ooi-ryouriten (Intermediate)
- [x] aozora-toshishun (Intermediate)
- [x] aozora-hashire-melos (Intermediate)
- [ ] aozora-botchan (Upper Intermediate)
- [ ] aozora-ginga-tetsudou-no-yoru (Upper Intermediate)
- [ ] aozora-lemon (Upper Intermediate)
- [ ] aozora-rashomon (Upper Intermediate)
- [ ] aozora-sangetsuki (Upper Intermediate)
- [ ] aozora-takasebune (Upper Intermediate)
- [ ] aozora-yabu-no-naka (Upper Intermediate)
- [ ] aozora-kokoro (Advanced)
- [ ] aozora-ningen-shikkaku (Advanced)
- [ ] aozora-shayo (Advanced)
- [ ] aozora-yukiguni (Advanced)
- [ ] aozora-aru-onna (Proficiency)
- [ ] aozora-shunkinshow (Proficiency)
- [ ] aozora-wagahai-wa-neko-de-aru (Proficiency)

### myBooks: African Folktales — 0/27 done
- [ ] All 27 stories (generate style reference first from sbj-0087)
