# SCRAPING PLAYBOOK — techno-optimism.xyz Photo Gallery

> **Automated Image Discovery & Collection Guidelines**
> Gallery: [techno-optimism.xyz](https://techno-optimism.xyz) · Repo: [jzone3/techno-optimism](https://github.com/jzone3/techno-optimism)
> Current count: **212 tiles** across 30+ categories

---

## Table of Contents

1. [Image Quality Criteria](#1-image-quality-criteria)
2. [Themes & Keywords](#2-themes--keywords)
3. [Source Priority List](#3-source-priority-list)
4. [Twitter/X Accounts to Monitor](#4-twitterx-accounts-to-monitor)
5. [Search Queries](#5-search-queries)
6. [People to Track](#6-people-to-track)
7. [Events to Watch](#7-events-to-watch)
8. [Deduplication Rules](#8-deduplication-rules)
9. [Image Requirements](#9-image-requirements)
10. [Categories & Tags](#10-categories--tags)
11. [Scraping Schedule](#11-scraping-schedule)
12. [Example Workflow — Daily Scraping Run](#12-example-workflow--daily-scraping-run)
13. [Emerging Topics](#13-emerging-topics)

---

## 1. Image Quality Criteria

### Gallery-Worthy (YES)

| Signal | Examples |
|--------|----------|
| **Candid & unscripted** | Jensen signing a fan's leather jacket; Zuckerberg in a jiu-jitsu match; Musk carrying a sink into Twitter HQ |
| **Iconic moment** | Jobs holding the first iPhone; Kasparov vs Deep Blue; the Dartmouth Workshop lawn photo |
| **Beautiful hardware** | Die-shot macro photography; wafer close-ups; fiber-optic server aisles with vivid color |
| **Humanizing / unexpected** | Gates jumping a chair; Nadella with his parents; Karpathy holding Tesla Tequila |
| **Historical significance** | ENIAC operators 1946; Apollo guidance code stacks; Traitorous Eight at Fairchild |
| **"Dripped out" aesthetic** | Tech personalities looking cool, fashionable, or in culturally unexpected contexts (Peter Thiel wearing a crown, Linus Torvalds casual candid) |
| **Emotional resonance** | Photos that tell a story — triumph, intensity, humor, humility |
| **Founding-team energy** | PayPal Mafia Fortune cover; Microsoft 1978; Facebook kitchen table 2004 |

### NOT Gallery-Worthy (NO)

| Signal | Why it fails |
|--------|-------------|
| **Corporate headshot / PR portrait** | Posed, sterile, no story |
| **Marketing render / CGI** | We only use real photos — no product renders, no 3D mockups |
| **Stock photography** | Watermarked, generic, soulless |
| **Low-resolution / blurry** | Anything under ~800px on the long edge |
| **Illustrations / infographics** | Not a photograph |
| **Screenshots of tweets / articles** | Not a photo |
| **Duplicate angle of existing photo** | We already have 10 Jensen shots — a new one needs to be meaningfully different |
| **Conference speaker at generic podium** | Unless the moment itself is iconic (e.g., iPhone reveal) |
| **Group photo where everyone is posed** | Unless historically significant (e.g., OpenAI founding team) |

### The "TechBroDrip Test"

Before adding any image, ask: *"Would @TechBroDrip post this?"* The bar is:
- Real, candid, surprising, or visually stunning
- Shows personality, not just status
- Has meme potential or cultural resonance
- Makes you stop scrolling

---

## 2. Themes & Keywords

### Primary Themes

| Theme | Keywords for Search |
|-------|-------------------|
| **Silicon & Chips** | `die shot`, `wafer close-up`, `chip macro photography`, `semiconductor fab`, `NVIDIA H100 die`, `TSMC wafer`, `silicon art`, `CPU die photo`, `chip photography` |
| **Data Centers** | `data center interior`, `server room`, `fiber optic data center`, `hyperscale`, `Google data center`, `liquid cooling server`, `data center night` |
| **Robots & Autonomous** | `Boston Dynamics Atlas`, `humanoid robot`, `Tesla Optimus`, `Figure robot`, `Waymo self-driving`, `robot walking`, `industrial robot arm` |
| **Consumer AI Hardware** | `Neuralink implant`, `AI wearable`, `smart glasses AI`, `brain-computer interface` |
| **Historical Computing** | `ENIAC 1946`, `Xerox Alto`, `PDP-11`, `mainframe computer`, `punch card operator`, `early computer room`, `vintage computing` |
| **Computing Pioneers** | `Alan Turing portrait`, `Grace Hopper UNIVAC`, `Margaret Hamilton Apollo`, `Claude Shannon`, `John von Neumann`, `Ada Lovelace`, `Ken Thompson Dennis Ritchie` |
| **AI Researchers** | `Geoffrey Hinton`, `Yann LeCun`, `Ilya Sutskever candid`, `Andrej Karpathy`, `Fei-Fei Li`, `Demis Hassabis`, `Dario Amodei`, `Yoshua Bengio` |
| **Tech Founders Candid** | `Jensen Huang candid`, `Zuckerberg jiu-jitsu`, `Elon Musk smoking`, `Bill Gates young`, `Steve Jobs garage`, `Jeff Bezos early Amazon`, `Sam Altman candid` |
| **TechBroDrip** | `tech founder drip`, `silicon valley fashion`, `tech CEO casual`, `founder candid photo`, `tech billionaire style` |
| **Founding Teams** | `PayPal mafia`, `Microsoft 1978`, `Apple garage`, `Facebook dorm room`, `Google Stanford`, `founding team photo tech` |
| **Women in Tech** | `Lisa Su AMD`, `Gwynne Shotwell SpaceX`, `Fei-Fei Li Stanford`, `Reshma Saujani`, `Joy Buolamwini`, `Susan Wojcicki` |
| **International Founders** | `Morris Chang TSMC`, `Jack Ma Alibaba`, `Masayoshi Son`, `Daniel Ek Spotify`, `Jan Koum WhatsApp` |
| **Tech Crossovers** | `tech CEO meeting`, `Obama Silicon Valley`, `tech summit`, `Davos tech`, `tech founder together` |
| **Infamous / Rise & Fall** | `Elizabeth Holmes trial`, `Sam Bankman-Fried`, `Travis Kalanick`, `Adam Neumann WeWork`, `Theranos` |
| **Product Launches** | `iPhone reveal 2007`, `Macintosh 1984`, `product launch tech`, `Tesla unveiling`, `first demo` |
| **Military / Defense Tech** | `FPV drone military`, `Anduril`, `defense tech`, `Palantir`, `military robotics` |
| **Space Tech** | `SpaceX Starship landing`, `rocket launch`, `Falcon Heavy`, `Blue Origin`, `space tech` |

### Aesthetic Keywords (Cross-cutting)

These can be combined with any theme:
- `candid`, `behind the scenes`, `rare photo`, `vintage`, `iconic moment`
- `close-up`, `macro`, `night shot`, `long exposure`, `aerial`
- `viral`, `meme`, `funny tech`, `unexpected`, `dripped out`

---

## 3. Source Priority List

Sources ranked by signal quality and reliability:

### Tier 1 — High Signal, Check Daily

| Source | Why | URL / How to Access |
|--------|-----|---------------------|
| **Twitter/X (curated accounts)** | Highest-signal source for candid tech photos, viral moments, TechBroDrip content | See [Section 4](#4-twitterx-accounts-to-monitor) |
| **Reddit r/hardware, r/chipdesign, r/homelab** | Stunning hardware close-ups, die shots, fab photos | reddit.com/r/hardware, /r/chipdesign, /r/homelab |
| **Reddit r/retrobattlestations, r/vintagecomputing** | Historical computing photos, rare finds | reddit.com/r/retrobattlestations |
| **Wikimedia Commons** | High-res, freely licensed historical photos | commons.wikimedia.org |
| **Google Images (time-filtered)** | Broad sweep for recent candid photos of tracked people | images.google.com with `tbs=qdr:d` (past 24h) |
| **Getty Images editorial** | Professional event photography (GTC, CES, WWDC) — use for reference/discovery, respect licensing | gettyimages.com |

### Tier 2 — High Signal, Check Weekly

| Source | Why | URL / How to Access |
|--------|-----|---------------------|
| **Flickr (Creative Commons)** | Conference photography, tech events, hardware shots | flickr.com/search/?license=2%2C3%2C4%2C5%2C6%2C9 |
| **The Verge / Wired / Ars Technica** | High-quality editorial photography from product launches and events | theverge.com, wired.com, arstechnica.com |
| **IEEE Spectrum** | Engineering and hardware photography | spectrum.ieee.org |
| **Computer History Museum** | Historical photos, archive collections | computerhistory.org |
| **NVIDIA Blog / Newsroom** | Official but sometimes candid Jensen photos, hardware beauty shots | nvidianews.nvidia.com, blogs.nvidia.com |
| **Google AI Blog / DeepMind Blog** | Researcher photos, lab shots | blog.google/technology/ai, deepmind.google |
| **AnandTech / Tom's Hardware archives** | Hardware die shots and close-ups | anandtech.com (archived), tomshardware.com |
| **TechCrunch / Bloomberg** | Founder candid photos, conference coverage | techcrunch.com, bloomberg.com/technology |
| **r/MachineLearning** | AI researcher candid shots, conference photos | reddit.com/r/MachineLearning |

### Tier 3 — Periodic Deep Dives (Monthly)

| Source | Why |
|--------|-----|
| **YouTube thumbnails / video stills** | Conference talks, interviews — extract compelling frames |
| **LinkedIn (public posts)** | Founders occasionally post personal/candid photos |
| **Instagram** | Tech personalities' personal accounts |
| **Documentary stills** | Films like *AlphaGo*, *General Magic*, *Steve Jobs: The Man in the Machine* |
| **Book cover / interior photography** | Biographies often contain rare candid photos |
| **University archives** | Stanford, MIT, CMU — historical AI lab photos |
| **Photographer portfolios** | Photographers who specialize in tech events (e.g., those who shoot GTC, CES) |
| **Stock agencies (for reference)** | AP Images, Reuters, AFP — use to identify photos, then find originals or free alternatives |
| **Hacker News (Show HN / front page)** | Occasionally surfaces incredible hardware or historical photos |
| **National Archives / Library of Congress** | Early computing, ARPANET, government tech programs |
| **Museum digital collections** | Science Museum London, Deutsches Museum, Smithsonian |

---

## 4. Twitter/X Accounts to Monitor

### Must-Follow (Daily Check)

| Account | Content Type | Signal Level |
|---------|-------------|--------------|
| **@TechBroDrip** | Candid tech founder photos, dripped-out aesthetic | 🔴 Highest |
| **@TechEmails** | Historical internal emails often paired with candid photos | 🟠 High |
| **@TechMemesFun** | Viral tech moments, meme-worthy photos | 🟠 High |
| **@historyinmemes** | Historical photos of tech pioneers | 🟠 High |
| **@oldpicsarchive** | Rare historical photos including computing pioneers | 🟡 Medium |
| **@HistoryHit** | Historical moments, occasionally tech history | 🟡 Medium |

### Tech Industry / Hardware Accounts

| Account | Content Type |
|---------|-------------|
| **@IanCutress** | Semiconductor die shots, chip analysis with stunning visuals |
| **@chilodasern** / **@FritzchensFritz** | Die-shot macro photography — artistic chip close-ups |
| **@RealSiliconAge** | Historical semiconductor industry photos |
| **@erikbryn** | Historical tech economy observations with photos |
| **@hardaboratory** | Hardware teardowns and close-ups |
| **@anikitatech** | Chip architecture visuals |

### Founder / CEO Personal Accounts

| Account | What to Watch For |
|---------|-------------------|
| **@elonmusk** | Candid factory tours, SpaceX moments, viral antics |
| **@faborules** (Mark Zuckerberg) | MMA training, surfing, product demos |
| **@JensenHuang** (not very active — use fan accounts) | GTC moments, fan interactions |
| **@sataborasu** (Satya Nadella) | Personal reflections, rare candid moments |
| **@sama** (Sam Altman) | Candid moments, OpenAI milestones |
| **@kaborarpathy** (Andrej Karpathy) | AI researcher life, candid shots |
| **@Dr_LiSu** (Lisa Su) | AMD keynotes, chip reveals |
| **@demaboris_hassabis** (Demis Hassabis) | Nobel Prize, DeepMind milestones |

### Journalist / Photographer Accounts

| Account | Content Type |
|---------|-------------|
| **@ashaborlee** (Ashley Vance) | Tech biographies, founder candid access |
| **@Walt_Mossberg** | Historical tech industry photos |
| **@karaswisher** | Behind-the-scenes tech industry |
| **@stevesi** (Steven Sinofsky) | Historical Microsoft, early PC era |
| **@benedictevans** | Tech industry analysis with archival photos |

### AI/ML Community

| Account | Content Type |
|---------|-------------|
| **@ylecun** (Yann LeCun) | AI research candids, conference photos |
| **@GaboroffHinton** (Geoffrey Hinton) | Nobel Prize, historical deep learning |
| **@hardmaru** (David Ha) | AI research community, conference shots |
| **@EMostaque** | AI community gatherings |
| **@ClementDelangue** | Hugging Face events, AI community |

---

## 5. Search Queries

### Twitter/X Search Queries

Run these via X Advanced Search (`x.com/search`) or X API:

```
# TechBroDrip-style content
from:TechBroDrip filter:images min_faves:500
"tech founder" (candid OR rare OR drip) filter:images min_faves:100
(Jensen OR Zuckerberg OR "Elon Musk") (candid OR rare OR behind) filter:images min_faves:200
"silicon valley" (drip OR fashion OR style) filter:images

# Hardware beauty shots
(die shot OR "die photo" OR wafer) (NVIDIA OR AMD OR Intel OR TSMC) filter:images min_faves:50
"data center" (tour OR interior OR beautiful) filter:images min_faves:100
(H100 OR H200 OR B200 OR GB200) (photo OR close-up OR die) filter:images

# Historical computing
(ENIAC OR UNIVAC OR "Xerox Alto" OR PDP) (photo OR rare OR original) filter:images
("Grace Hopper" OR "Margaret Hamilton" OR "Alan Turing") (photo OR rare) filter:images
"computing history" (photo OR rare OR archive) filter:images

# AI researchers
("Geoffrey Hinton" OR "Yann LeCun" OR "Ilya Sutskever") (photo OR candid) filter:images min_faves:50
("Demis Hassabis" OR "Dario Amodei" OR "Fei-Fei Li") filter:images

# Founding teams & moments
("PayPal mafia" OR "founding team" OR "early days") (tech OR startup) filter:images
(Microsoft OR Apple OR Google OR Amazon OR Facebook) (1978 OR 1984 OR 1998 OR garage OR "early days") filter:images

# Product launches
("iPhone reveal" OR "Macintosh 1984" OR "product launch") filter:images
"first demo" (tech OR AI OR computer) filter:images

# Viral tech moments
(Zuckerberg OR Musk OR Gates) (funny OR viral OR meme OR awkward) filter:images min_faves:500

# Women in tech
("Lisa Su" OR "Gwynne Shotwell" OR "Fei-Fei Li") (candid OR keynote OR photo) filter:images
"women in tech" (pioneer OR founder OR history) filter:images

# Robots
("Boston Dynamics" OR "Figure robot" OR "Tesla Optimus" OR Waymo) filter:images min_faves:100
```

### Reddit Search Queries

```
# r/hardware, r/chipdesign
site:reddit.com/r/hardware "die shot" OR "wafer" OR "fab" OR "close-up"
site:reddit.com/r/chipdesign die shot macro

# r/retrobattlestations
site:reddit.com/r/retrobattlestations ENIAC OR mainframe OR PDP OR VAX

# r/MachineLearning
site:reddit.com/r/MachineLearning photo OR candid OR conference

# r/EngineeringPorn
site:reddit.com/r/EngineeringPorn semiconductor OR chip OR "data center" OR robot
```

### Google Image Search Queries

Use `tbs=qdr:d` for past 24 hours, `tbs=qdr:w` for past week:

```
# Time-filtered for recent candid photos
"Jensen Huang" candid -headshot -official -press
"Sam Altman" candid OR behind the scenes 2026
"Mark Zuckerberg" MMA OR surfing OR training 2026
tech CEO candid viral

# Hardware photography
NVIDIA die shot macro photography -render -diagram
"silicon wafer" close-up photography -stock
data center interior photography fiber optic -illustration

# Historical
"computing history" rare photograph -painting -illustration
"AI history" photograph archive

# Large size filter
Add &tbs=isz:l to URL for large images only
```

### Wikimedia Commons Queries

Search at `commons.wikimedia.org/w/index.php?search=`:

```
# Categories to browse
Category:NVIDIA_graphics_processing_units
Category:Supercomputers
Category:History_of_artificial_intelligence
Category:Robotics
Category:Computer_hardware_history
Category:Silicon_wafers
Category:Semiconductor_fabrication_plants
Category:Grace_Hopper
Category:Alan_Turing
Category:Computer_pioneers

# Full-text search
ENIAC photograph
"data center" interior
semiconductor wafer close-up
artificial intelligence researcher
computer history museum
```

### Exa AI Search Queries

Use the Exa API for neural/semantic search (available via `$EXA_API_KEY`):

```python
# High-signal semantic searches
"candid photo of tech CEO at conference, not posed headshot"
"stunning macro photography of computer chip die shot"
"rare historical photo of early computing pioneers"
"behind the scenes at AI research lab"
"tech founder in unexpected casual setting"
```

---

## 6. People to Track

### Tier 1 — Always Grab New Candid Photos

These are the gallery's core personalities. Any new candid, viral, or historically significant photo should be collected.

| Person | Existing Count | What We Want More Of |
|--------|---------------|---------------------|
| **Jensen Huang** | ~10 | GTC moments, fan interactions, casual candids, signing sessions |
| **Mark Zuckerberg** | ~5 | MMA/jiu-jitsu, surfing, gold chain moments, Meta events |
| **Elon Musk** | ~4 | Factory tours, SpaceX launches, viral/meme moments |
| **Sam Altman** | ~3 | OpenAI events, candid meetings, Worldcoin |
| **Bill Gates** | ~3 | Historical candids, philanthropy, young Gates |
| **Steve Jobs** (historical) | ~3 | Rare photos, Apple events, NeXT era, candid with Woz |
| **Jeff Bezos** | ~2 | Early Amazon, space, Day 1 era |
| **Satya Nadella** | ~2 | Personal moments, keynotes, with team |
| **Andrej Karpathy** | ~2 | Teaching, Tesla days, candid tech moments |
| **Lisa Su** | ~2 | AMD keynotes, chip reveals, leadership moments |
| **Ilya Sutskever** | ~1 | OpenAI departure, Safe Superintelligence, early Google Brain |
| **Demis Hassabis** | ~1 | Nobel Prize, AlphaFold, DeepMind milestones |

### Tier 2 — Actively Seek

| Person | Notes |
|--------|-------|
| **Linus Torvalds** | Rare candids, Linux conferences |
| **Peter Thiel** | Unusual photos, chess, Founders Fund events |
| **Dario Amodei** | Anthropic events, candid moments |
| **Fei-Fei Li** | Stanford AI Lab, World Labs, speaking events |
| **Yann LeCun** | Meta AI, conferences, candid debates |
| **Geoffrey Hinton** | Nobel Prize ceremony, historical lab photos |
| **Morris Chang** | TSMC founding, retirement, semiconductor history |
| **Jan Koum** | WhatsApp founding, rare candids |
| **Jack Ma** | Alibaba era, post-retirement appearances |
| **Sundar Pichai** | Google events, AI keynotes |
| **Tim Cook** | Apple events, candid moments |
| **Larry Page & Sergey Brin** | Google garage era, rare recent sightings |
| **Gwynne Shotwell** | SpaceX launches, leadership |
| **Susan Wojcicki** (memorial) | YouTube era, Google early days |
| **Patrick & John Collison** | Stripe, candid brothers |

### Tier 3 — Opportunistic

| Person | Notes |
|--------|-------|
| **Palmer Luckey** | Anduril, Oculus, defense tech |
| **Daniel Ek** | Spotify founder |
| **Brian Chesky** | Airbnb, design thinking |
| **Travis Kalanick** | Rise & fall narrative |
| **Elizabeth Holmes** | Trial photos, Theranos era |
| **Adam Neumann** | WeWork, comeback attempts |
| **Sam Bankman-Fried** | Trial, FTX collapse |
| **Timnit Gebru** | AI ethics, Google firing |
| **Joy Buolamwini** | AI bias research, Algorithmic Justice League |
| **Reshma Saujani** | Girls Who Code |
| **Jack Dorsey** | Twitter/Square era |
| **Masayoshi Son** | SoftBank, Vision Fund |
| **Ratan Tata** (memorial) | Tata Group, Indian tech |
| **Pony Ma** | Tencent |
| **Niklas Zennström** | Skype founder |

### Rising Stars — Watch Closely

| Person | Why |
|--------|-----|
| **Alexandr Wang** (Scale AI) | Youngest self-made billionaire, defense tech |
| **Aravind Srinivas** (Perplexity) | AI search, rising profile |
| **Mustafa Suleyman** (Microsoft AI) | DeepMind co-founder, Microsoft AI CEO |
| **Mira Murati** | OpenAI CTO departure, next venture |
| **Leopold Aschenbrenner** | AI safety → AI acceleration |
| **Guillaume Verdon** (Extropic) | Thermodynamic computing, emerging founder |
| **Dylan Field** (Figma) | Design tool founder |
| **Connor Leahy** (Conjecture) | AI safety researcher |

---

## 7. Events to Watch

### Annual Conferences — Mark Your Calendar

| Event | Typical Date | What to Look For | Priority |
|-------|-------------|-----------------|----------|
| **NVIDIA GTC** | March | Jensen keynotes, new GPU reveals, fan interactions, DGX deliveries | 🔴 Critical |
| **CES** | January | Product reveals, concept devices, weird gadgets, CEO appearances | 🔴 Critical |
| **Apple WWDC** | June | Tim Cook on stage, new product reveals, developer energy | 🔴 Critical |
| **Google I/O** | May | Sundar Pichai, AI demos, Gemini reveals | 🟠 High |
| **Meta Connect** | September/October | Zuckerberg VR/AR demos, Meta hardware | 🟠 High |
| **Microsoft Build** | May | Satya Nadella keynotes, AI integration demos | 🟠 High |
| **AWS re:Invent** | November/December | Andy Jassy, cloud infrastructure, data center tours | 🟠 High |
| **Computex** | June | Jensen in Taiwan, TSMC, AMD Lisa Su | 🟠 High |
| **MWC (Mobile World Congress)** | February/March | Mobile/AI convergence, global tech leaders | 🟡 Medium |
| **NeurIPS** | December | AI researcher candids, poster sessions, hallway conversations | 🟠 High |
| **ICML** | July | ML research community, candid researcher shots | 🟡 Medium |
| **ICLR** | May | Deep learning community, emerging researchers | 🟡 Medium |
| **CVPR** | June | Computer vision community, demo day | 🟡 Medium |
| **Hot Chips** | August | Semiconductor deep dives, chip die shots | 🟡 Medium |
| **IEDM** | December | Semiconductor manufacturing, fab photos | 🟡 Medium |
| **Tesla AI Day / Shareholder Meeting** | Varies | Optimus robot demos, Elon candids | 🟡 Medium |
| **TED / TED AI** | Varies | Polished but sometimes candid founder appearances | 🟡 Medium |

### One-Time / Irregular Events to Watch For

| Event Type | Examples | What to Capture |
|-----------|---------|-----------------|
| **Nobel Prize** | Hinton (2024 Physics), Hassabis (2024 Chemistry) | Ceremony photos, reactions, press conferences |
| **IPOs / Listings** | Any major tech IPO | Bell-ringing photos, founding team celebrations |
| **Congressional Hearings** | AI regulation hearings | Tech CEOs testifying, intense moments |
| **Acquisitions** | Major tech M&A | Handshake photos, signing ceremonies |
| **Product Failures** | Humane AI Pin flop, Cybertruck window | The memorable failure moments |
| **Departures / Firings** | CEO changes, high-profile exits | The "last day" or "new beginning" photos |
| **Factory / Fab Openings** | New TSMC fabs, NVIDIA facilities | Ribbon cutting, clean room tours |
| **Space Launches** | SpaceX Starship milestones | Launch and landing photography |
| **Robot Demos** | Boston Dynamics, Figure, Agility | New capability demonstrations |

---

## 8. Deduplication Rules

### Pre-Scrape Check

Before downloading any image, check against the existing gallery:

1. **Filename match**: Check if any existing image in `images/` has a similar descriptive filename
   ```bash
   ls images/ | grep -i "<person_name_or_keyword>"
   ```

2. **Visual similarity**: Compare the candidate image against existing images of the same person/subject
   - Same event + same angle = **DUPLICATE — skip**
   - Same event + different angle/moment = **MAYBE — include if meaningfully different**
   - Different event + similar pose = **INCLUDE — if the new context adds value**

3. **Content overlap rules**:
   - Do NOT add another generic "Jensen at GTC" unless it captures a genuinely different moment
   - Do NOT add another "Zuckerberg headshot" — we want candids
   - Do NOT add a cropped/filtered version of an existing photo
   - DO add the same person in a meaningfully different context (e.g., Jensen signing fans vs Jensen cooking)

### The "Would Someone Notice?" Test

If you placed the new image next to the most similar existing image, would a viewer say:
- *"These are the same photo"* → **SKIP**
- *"These are from the same moment"* → **SKIP** (unless the new one is significantly better quality)
- *"Oh cool, different moment"* → **INCLUDE**

### Existing Image Manifest

Maintain awareness of the current gallery by parsing `index.html` for:
- Person names in tile titles
- Category tags
- Image descriptions
- Source attributions

Before each scraping run, generate a quick inventory:
```bash
# Extract all tile titles from the gallery
grep -oP '<h3>[^<]*</h3>' index.html | sed 's/<[^>]*>//g' | sort > /tmp/existing_tiles.txt
```

---

## 9. Image Requirements

### Technical Requirements

| Requirement | Minimum | Preferred |
|-------------|---------|-----------|
| **Resolution** | 800px on longest edge | 1200px+ on longest edge |
| **Format** | JPEG, PNG, WebP | JPEG (for photos), PNG (for graphics/die shots) |
| **File size** | No minimum | Under 500KB preferred (optimize before adding) |
| **Aspect ratio** | Any (masonry layout handles all ratios) | Portrait and landscape both work; square is fine |
| **Color depth** | 8-bit | 8-bit |
| **Compression** | No visible artifacts | Clean, sharp |

### Image Optimization Pipeline

Before adding to the gallery, process each image:

```bash
# Resize if over 2000px wide (preserve aspect ratio)
convert input.jpg -resize '2000x2000>' -quality 85 output.jpg

# Or use sharp/squoosh for better compression
npx @squoosh/cli --mozjpeg '{quality:82}' -d output/ input.jpg
```

### Naming Convention

Follow the existing pattern:
```
{index}_{Descriptive_Title_With_Underscores}.{ext}
```

Examples from the current gallery:
- `042_time-AI-Jensen-Huang-homepage-social.jpg`
- `202_Peter_Thiel_Crown___Chess_Match.jpg`
- `215_Karpathy___Tesla_Tequila.jpg`

Rules:
- Increment the index from the highest existing number
- Use descriptive names with underscores (or hyphens — match nearby files)
- Triple underscore `___` separates multiple subjects/concepts
- Include the person's name when applicable
- Include the context (event, year, location) when known

### Licensing Considerations

| License Type | Can We Use? | Notes |
|-------------|-------------|-------|
| **Public Domain** | ✅ Yes | Wikimedia, government archives, expired copyrights |
| **Creative Commons (CC-BY, CC-BY-SA)** | ✅ Yes | Attribute the source in the tile metadata |
| **Creative Commons (CC-BY-NC)** | ⚠️ Check | OK if gallery is non-commercial |
| **Fair Use (editorial)** | ⚠️ Case-by-case | Historical/newsworthy photos, criticism, commentary — document rationale |
| **Getty/AP/Reuters** | ❌ No direct use | Use for discovery/reference only; find alternative sources |
| **Stock photo (watermarked)** | ❌ Never | Absolutely not |
| **Personal social media posts** | ⚠️ Generally OK | Photos posted publicly by the subject themselves are usually fine for editorial use |

**Always record the source URL for every image** in the tile's HTML metadata for attribution.

---

## 10. Categories & Tags

### Primary Categories (from current gallery)

These are the categories currently used in the gallery's navigation and tile overlays:

| Category | Slug | Count | Description |
|----------|------|-------|-------------|
| **AI Personalities** | `ai-personalities` | 20 | AI researchers and leaders in candid/notable settings |
| **TechBroDrip** | `techbro-drip` | 20 | The aesthetic — tech people looking unexpectedly cool |
| **Tech Founders** | `tech-founders` | 14 | Major tech company founders and CEOs |
| **Computing Pioneers** | `computing-pioneers` | 12 | Historical figures in computing |
| **AI Researchers** | `ai-researchers` | 11 | Academic and industry AI researchers |
| **Women in Tech** | `women-in-tech` | 10 | Women leaders, pioneers, and founders |
| **Jensen Huang** | `jensen-huang` | 10 | Jensen-specific shots (he earns his own category) |
| **Viral Moments** | `viral-moments` | 8 | Meme-worthy, internet-famous tech moments |
| **Robots** | `robots` | 8 | Humanoid robots, Boston Dynamics, Figure, etc. |
| **Tech Icons** | `tech-icons` | 7 | Legendary figures in tech |
| **Historical AI** | `historical-ai` | 7 | Historical moments in AI development |
| **Founding Teams** | `founding-teams` | 7 | Group photos of founding teams |
| **Data Centers** | `data-centers` | 7 | Beautiful data center interiors |
| **Tech Bro Culture** | `techbro-culture` | 6 | Silicon Valley culture moments |
| **Product Launches** | `product-launches` | 6 | Iconic product reveal moments |
| **Infamous** | `infamous` | 6 | Rise-and-fall figures |
| **Chips** | `chips` | 6 | Semiconductor die shots and close-ups |
| **Hackers** | `hackers` | 5 | Hacker culture, cyberpunk aesthetic |
| **Rise & Fall** | `rise-and-fall` | 4 | Dramatic career arcs |
| **Crossovers** | `crossovers` | 4 | Tech leaders meeting non-tech contexts |
| **Consumer Hardware** | `consumer-hardware` | 4 | Consumer AI/tech devices |
| **Candid Moments** | `candid-moments` | 4 | Unscripted personal moments |
| **Young Founders** | `young-founders` | 3 | Founders in their early days |
| **International Founders** | `international-founders` | 6 | Non-US tech founders |
| **Founding Moments** | `founding-moments` | 3 | The specific moment of founding |
| **Fabs** | `fabs` | 3 | Semiconductor fabrication facilities |
| **Bonus** | `bonus` | 3 | Miscellaneous stunning photos |
| **Autonomous** | `autonomous` | 3 | Self-driving cars, autonomous systems |
| **Supercomputers** | `supercomputers` | 1 | Supercomputer installations |

### Category Assignment Rules

Each image gets **one primary category** (shown on the tile) and optionally mentioned in the description for cross-referencing.

Priority order for category assignment:
1. If the image is quintessentially "TechBroDrip" aesthetic → `TechBroDrip`
2. If it's Jensen Huang → `Jensen Huang` (he's special)
3. If it's a historical computing photo (pre-2000) → `Computing Pioneers` or `Historical AI`
4. If it features a woman in tech prominently → `Women in Tech`
5. If it's hardware/chip/die shot → `Chips` or `Data Centers` or `Fabs`
6. If it's a founding team group photo → `Founding Teams`
7. If it's a robot → `Robots`
8. If it's a product launch → `Product Launches`
9. If it's an infamous/controversial figure → `Infamous`
10. If it's a viral/meme moment → `Viral Moments`
11. Otherwise → `Tech Founders`, `AI Researchers`, `AI Personalities`, etc.

### Proposing New Categories

If a batch of 3+ images doesn't fit existing categories, propose a new category. Possible future categories:
- **AI Art & Creativity** — AI-generated art exhibitions, creative AI tools
- **Quantum Computing** — quantum chip close-ups, cryogenic setups, IBM/Google quantum labs
- **Biotech x AI** — AlphaFold visualizations, lab robotics, computational biology
- **Climate Tech** — fusion reactors, solar farms, carbon capture
- **Open Source Heroes** — Linus Torvalds, Guido van Rossum, Brendan Eich, DHH

---

## 11. Scraping Schedule

### Daily (Automated)

| Task | Source | Method | Time |
|------|--------|--------|------|
| Check @TechBroDrip + Tier 1 Twitter accounts for new posts | Twitter/X | X API or Exa search | Morning |
| Google Image search for tracked people (past 24h) | Google Images | Exa API with date filter | Morning |
| Check r/hardware, r/chipdesign top posts (past 24h) | Reddit | Reddit API or web scrape | Morning |
| Review any new photos from tech news (Verge, Wired, etc.) | News sites | Exa API | Morning |

**Expected yield**: 0-3 new images per day

### Weekly (Automated, More Thorough)

| Task | Source | Method | Day |
|------|--------|--------|-----|
| Full Twitter sweep of all monitored accounts | Twitter/X | X API | Monday |
| Reddit deep dive (r/retrobattlestations, r/EngineeringPorn, etc.) | Reddit | Reddit API | Monday |
| Flickr Creative Commons search for hardware + tech events | Flickr | Flickr API | Wednesday |
| Wikimedia Commons new uploads in tech categories | Wikimedia | MediaWiki API | Wednesday |
| News roundup — any viral tech moments from the week | Multiple | Exa API | Friday |

**Expected yield**: 3-8 new images per week

### Monthly (Manual Review Recommended)

| Task | Notes |
|------|-------|
| Deep dive into photographer portfolios | Look for new conference photographers |
| Check for new documentary stills | New tech documentaries, YouTube originals |
| University archive check | Stanford, MIT, CMU digital collections |
| Review "Emerging Topics" list and update | Add new people, events, trends |
| Gallery curation pass | Remove low-quality images, re-categorize, update metadata |
| Category rebalancing | Ensure no category is over-represented or starved |

### Event-Driven (Triggered by Calendar)

| Trigger | Action | Timing |
|---------|--------|--------|
| Major conference starts (GTC, CES, WWDC, etc.) | Intensive daily scraping of conference hashtags and photographer feeds | Day 1-3 of conference |
| Nobel Prize announcements | Search for ceremony photos if tech-related | Within 24 hours |
| Major product launch | Search for launch event photos | Within 24 hours |
| Viral tech moment trending | Real-time scraping of the moment | Within hours |
| CEO departure / major tech news | Search for relevant candid photos | Within 24 hours |

---

## 12. Example Workflow — Daily Scraping Run

### Step 1: Prepare Environment

```bash
# Navigate to repo
cd ~/repos/jzone3/techno-optimism

# Ensure on the latest gallery branch
git checkout devin/1779487914-gallery-v7
git pull origin devin/1779487914-gallery-v7

# Generate current inventory
grep -oP '<h3>[^<]*</h3>' index.html | sed 's/<[^>]*>//g' | sort > /tmp/existing_titles.txt
NEXT_INDEX=$(ls images/ | grep -oP '^\d+' | sort -n | tail -1)
NEXT_INDEX=$((NEXT_INDEX + 1))
echo "Next image index: $NEXT_INDEX"
```

### Step 2: Run Source Checks

```bash
# 1. Check @TechBroDrip and Tier 1 Twitter accounts (via Exa API)
# Search for recent tech candid photos
curl -s "https://api.exa.ai/search" \
  -H "x-api-key: $EXA_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "query": "candid photo tech CEO founder viral 2026",
    "type": "auto",
    "numResults": 20,
    "startPublishedDate": "'$(date -d "yesterday" +%Y-%m-%dT00:00:00Z)'"
  }' | jq '.results[] | {title, url}'

# 2. Check Reddit hardware/chip photography
curl -s "https://api.exa.ai/search" \
  -H "x-api-key: $EXA_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "query": "die shot chip macro photography semiconductor",
    "type": "auto",
    "numResults": 10,
    "includeDomains": ["reddit.com"],
    "startPublishedDate": "'$(date -d "7 days ago" +%Y-%m-%dT00:00:00Z)'"
  }' | jq '.results[] | {title, url}'

# 3. Check for new photos of tracked people
for person in "Jensen Huang" "Sam Altman" "Mark Zuckerberg" "Elon Musk" "Lisa Su"; do
  echo "=== Checking: $person ==="
  curl -s "https://api.exa.ai/search" \
    -H "x-api-key: $EXA_API_KEY" \
    -H "Content-Type: application/json" \
    -d '{
      "query": "'$person' candid photo 2026",
      "type": "auto",
      "numResults": 5,
      "startPublishedDate": "'$(date -d "yesterday" +%Y-%m-%dT00:00:00Z)'"
    }' | jq '.results[] | {title, url}'
done
```

### Step 3: Evaluate Candidates

For each candidate image found:

1. **Quality check**: Does it meet the criteria in [Section 1](#1-image-quality-criteria)?
2. **Dedup check**: Does it already exist? (See [Section 8](#8-deduplication-rules))
3. **Resolution check**: Is it at least 800px on the longest edge?
4. **Licensing check**: Can we use it? (See [Section 9](#9-image-requirements))
5. **TechBroDrip test**: Would @TechBroDrip post this?

### Step 4: Download & Process

```bash
# Download the image
wget -O /tmp/candidate.jpg "IMAGE_URL_HERE"

# Check dimensions
identify /tmp/candidate.jpg  # ImageMagick

# Optimize if needed (resize to max 2000px, compress to ~82% quality)
convert /tmp/candidate.jpg -resize '2000x2000>' -quality 82 \
  "images/${NEXT_INDEX}_Descriptive_Title.jpg"

NEXT_INDEX=$((NEXT_INDEX + 1))
```

### Step 5: Add to Gallery HTML

Add a new tile to `index.html` following this template:

```html
<a class="tile" href="images/218_New_Image_Title.jpg" data-full="images/218_New_Image_Title.jpg">
  <img src="images/218_New_Image_Title.jpg" alt="Description" width="800" height="600" loading="lazy" onload="this.classList.add('loaded')">
  <div class="label">Short Label</div>
  <div class="overlay">
    <div class="cat">Category Name</div>
    <h3>Full Title</h3>
    <div class="sub">Year or Context</div>
    <div class="desc">A one or two sentence description of why this photo is significant or interesting.</div>
    <div class="src">Source: <a href="SOURCE_URL" target="_blank">Source Name</a></div>
  </div>
</a>
```

### Step 6: Commit & Deploy

```bash
# Stage only the new images and updated HTML
git add images/218_New_Image_Title.jpg index.html
git commit -m "Add N new images: brief description of what was added"
git push origin devin/1779487914-gallery-v7

# Create PR if needed, or push directly to deploy via Vercel
```

### Step 7: Log Results

Create a brief log entry:

```
=== Scraping Run: 2026-05-23 ===
Sources checked: Twitter (TechBroDrip, TechEmails), Reddit (r/hardware), Exa
Candidates found: 12
Passed quality filter: 4
Passed dedup check: 3
Added to gallery: 3
  - 218_New_Chip_Die_Shot.jpg (Chips)
  - 219_Jensen_Cooking_Demo.jpg (Jensen Huang)
  - 220_Young_Jeff_Bezos.jpg (Young Founders)
New total: 215 tiles
```

---

## 13. Emerging Topics

### Near-Term (Next 3 Months)

| Topic | Why | Photo Opportunities |
|-------|-----|-------------------|
| **NVIDIA Blackwell Ultra / Rubin architecture** | Next-gen GPU launch | Die shots, Jensen keynote with new chip, rack installations |
| **GPT-5 / Claude 4 / Gemini 2.5 launches** | Major model releases | Launch events, CEO reactions, demo moments |
| **Humanoid robot deployments** | Figure, Tesla Optimus in factories | Robots working alongside humans — iconic images |
| **Apple AI glasses** | Rumored smart glasses launch | Product reveal moments, Tim Cook demo |
| **OpenAI hardware device** | Jony Ive + OpenAI collaboration | Design reveal, Altman + Ive candid |
| **EU AI Act enforcement begins** | Regulatory milestone | Hearing photos, protest/support imagery |
| **Anthropic growth** | Dario Amodei rising profile | Candid photos, office/lab shots |

### Medium-Term (3-12 Months)

| Topic | Photo Opportunities |
|-------|-------------------|
| **Quantum computing milestones** | Quantum chip close-ups, cryogenic setups, IBM/Google quantum labs |
| **Brain-computer interface trials** | Neuralink patient photos, medical breakthroughs |
| **Autonomous vehicle expansion** | Waymo/Cruise in new cities, first rider reactions |
| **AI-generated movies / music** | Creative AI moments, filmmaker reactions |
| **TSMC Arizona / Japan / Germany fabs** | Clean room construction, first wafers |
| **Space tech milestones** | Starship orbital, Artemis missions |
| **Defense tech growth** | Anduril, Shield AI, autonomous drones |

### People to Watch (Rising Influence)

| Person | Why They'll Be Photographed More |
|--------|----------------------------------|
| **Alexandr Wang** (Scale AI) | Defense contracts, youngest billionaire narratives |
| **Aravind Srinivas** (Perplexity) | Google Search disruptor, media darling |
| **Mustafa Suleyman** (Microsoft AI) | Running Microsoft's AI division |
| **Arthur Mensch** (Mistral) | European AI champion |
| **Daniela Amodei** (Anthropic) | President of Anthropic, sister of Dario |
| **Sarah Friar** (OpenAI CFO) | OpenAI's business leadership |
| **Dylan Field** (Figma) | Post-Adobe saga, independent Figma |
| **David Luan** (Adept → Amazon) | AI agent companies |
| **Noam Brown** (OpenAI) | o1/reasoning research, rising star |
| **Tri Dao** (Together AI) | Flash Attention creator, Stanford |

### Hardware to Photograph

| Hardware | Why |
|----------|-----|
| **NVIDIA B200 / GB300** | Next-gen die shots will be gallery centerpieces |
| **AMD MI400** | Lisa Su's counter to NVIDIA |
| **Intel 18A process** | Intel's comeback attempt — fab photos |
| **Google TPU v6** | Custom AI silicon |
| **Cerebras WSE-3** | Wafer-scale chip — the largest chip ever made |
| **Groq LPU** | Inference-optimized chip |
| **TSMC N2 (2nm) first chips** | Next node milestone |
| **Quantum processors** | IBM Condor, Google Willow |

### Events Calendar (Upcoming)

| Event | Date | Priority |
|-------|------|----------|
| **Computex 2026** | June 2026 | 🔴 Jensen in Taiwan, TSMC, AMD |
| **WWDC 2026** | June 2026 | 🔴 Apple AI announcements |
| **ICML 2026** | July 2026 | 🟡 ML researcher candids |
| **Hot Chips 2026** | August 2026 | 🟡 Chip die shots galore |
| **Tesla AI Day 2026** | TBD | 🟡 Optimus, FSD demos |
| **Meta Connect 2026** | Sept/Oct 2026 | 🟠 Zuckerberg AR/VR demos |
| **NeurIPS 2026** | December 2026 | 🟠 AI researcher community |
| **CES 2027** | January 2027 | 🔴 Consumer tech reveals |
| **GTC 2027** | March 2027 | 🔴 Jensen's annual show |

---

## Appendix A: Gallery Architecture Quick Reference

- **Repo**: `github.com/jzone3/techno-optimism`
- **Branch**: `devin/1779487914-gallery-v7` (active gallery)
- **Hosting**: Vercel, auto-deployed from repo
- **Domain**: techno-optimism.xyz
- **Layout**: Pinterest-style masonry grid (CSS columns, 6→2 columns responsive)
- **Image directory**: `images/` (all images stored locally in repo)
- **Gallery file**: `index.html` (single-file gallery with inline CSS/JS)
- **Current image count**: 202 files, 212 tiles (some tiles share images)
- **Image format**: Mixed JPEG/PNG/WebP, locally stored
- **Interaction**: Click-to-expand modal with full-resolution view

## Appendix B: Quality Scoring Rubric

Rate each candidate image 1-5 on these criteria. **Include if total score ≥ 15/25.**

| Criterion | 1 (Poor) | 3 (Average) | 5 (Excellent) |
|-----------|----------|-------------|---------------|
| **Candid/Iconic** | Posed corporate headshot | Standard event photo | Truly candid or iconic moment |
| **Visual Quality** | Blurry, low-res, poorly lit | Decent quality, adequate lighting | Stunning composition, perfect lighting |
| **Historical Significance** | No particular significance | Mildly interesting context | Captures a pivotal moment in tech |
| **Emotional Resonance** | Feels generic | Mildly interesting | Tells a story, evokes feeling |
| **Gallery Fit** | Doesn't match aesthetic | Fits but doesn't stand out | Perfect for the gallery, fills a gap |

## Appendix C: Anti-Patterns — What NOT to Add

1. **No corporate PR photos** — the kind companies put in press kits
2. **No stock photos** — nothing from Shutterstock, iStock, etc.
3. **No AI-generated images** — the entire point is REAL photography
4. **No screenshots** — of tweets, articles, code, apps
5. **No renders** — product renders, architectural renders, concept art
6. **No infographics** — charts, diagrams, flowcharts
7. **No heavily filtered/edited photos** — unless the edit IS the story (like a viral meme edit)
8. **No watermarked images** — ever
9. **No photos where the subject is clearly uncomfortable** — paparazzi ambush shots, invasive moments
10. **No photos primarily about politics** — unless it's a tech-politics crossover (e.g., Senate hearing)

---

*Last updated: 2026-05-22*
*Gallery: [techno-optimism.xyz](https://techno-optimism.xyz)*
*Maintained by: Devin (automated) + Human curation review*
