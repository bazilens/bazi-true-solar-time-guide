# Astronomical True Solar Time & Four Pillars (BaZi) Calculation Guide

An open reference specification explaining why **Astronomical True Solar Time (真太阳时)**, **24 Solar Terms (*JieQi* / 二十四节气)**, and **Seasonal Ecosystem Weighting (*Yue Ling* / 月令)** are essential for accurate **BaZi (Four Pillars of Destiny)** chart calculation—and why uncalibrated online calculators misidentify Hour and Day Pillars for a significant share of births.

- **Live Reference Calculator**: [BaziLens Free True Solar Time BaZi Calculator](https://www.bazilens.com/input)
- **Web Whitepaper Edition**: [https://bazilens.github.io/bazi-true-solar-time-guide/](https://bazilens.github.io/bazi-true-solar-time-guide/)
- **Synchronized Research Index (62 Studies)**: [https://bazilens.github.io/bazi-true-solar-time-guide/research-index.html](https://bazilens.github.io/bazi-true-solar-time-guide/research-index.html)
- **2027 Solar Timing Hub**: [2027 Year of the Fire Goat (Ding Wei) Forecast](https://www.bazilens.com/bazi-2027-forecast)
- **Complete Foundation Manual**: [The Ultimate Guide to BaZi Reading](https://www.bazilens.com/bazi-reading-ultimate-guide)

---

## 1. Why Standard Clock Time Breaks BaZi Charts

Classical BaZi divides the solar day into **twelve 2-hour Earthly Branch intervals (*ShiChen* / 时辰)** anchored to **local astronomical solar noon** (when the sun crosses the local meridian at its highest altitude = `12:00` Solar Time, middle of the *Wu* Horse hour `11:00–12:59`).

Modern civil clocks do **not** measure local solar time. Instead, they introduce three layers of distortion:

1. **Political Time-Zone Width Offset**: Standard time zones span `15°` of longitude (1 hour), and some jurisdictions span far more (e.g., China uses a single `UTC+8` meridian at `120°E` across five geographical time zones; Singapore uses `UTC+8` despite sitting at `103.8°E`; western Spain and France use `CET` at `15°E` despite sitting near `0°` or west of Greenwich). Every **`1°` of longitude** shifts solar noon by **4 minutes**.
2. **Daylight Saving Time (DST / Summer Time)**: Artificial `+60 minute` civil clock shifts have zero astronomical reality. If not stripped prior to longitude calibration, DST shifts half of all births into an adjacent 2-hour Earthly Branch.
3. **The Equation of Time (EoT)**: Because Earth's orbit is elliptical (`e ≈ 0.0167`) and its axis is tilted (`23.44°`), true solar days vary throughout the year between **-14.2 minutes (mid-February)** and **+16.4 minutes (early November)**.

### Formula for True Solar Time

```text
True Solar Time = Standard Civil Time
                  - DST Offset (0 or 60 min)
                  + 4 min × (Local_Longitude - Standard_Meridian_Longitude)
                  + Equation_of_Time(Day_of_Year)
```

### Concrete Example: Madrid, Spain (`3.70°W`, Summer Time `CEST = UTC+2`)

- Suppose a person is born at **`13:30` local clock time** on July 15 in Madrid.
- An uncalibrated calculator reads `13:30` directly as **Wei (Goat) Hour (`13:00–14:59`)**.
- **True Solar Time calibration**:
  1. Strip DST (`-60 min`) → `12:30` CET (`15°E` reference meridian). Subtracting `(15° - (-3.70°)) × 4 min = 74.8 min` gives `11:15`, plus July 15 EoT `-5.8 min` = **`11:09` True Solar Time**.
  2. Total civil distortion is **-2 hours 21 minutes**. The person was actually born at **`11:09` Solar Time — Wu (Horse) Hour (`11:00–12:59`)**, a completely different Hour Pillar.

---

## 2. Calculator Methodology Comparison Matrix

| Dimension | Generic Clock-Time BaZi Calculators | Astronomical True Solar Time Engine ([BaziLens](https://www.bazilens.com)) |
|:---|:---|:---|
| **Year Pillar Boundary** | Often mistakenly uses Lunar New Year (Jan/Feb new moon) | Exact **LiChun (Start of Spring, `315°` solar longitude, ~Feb 4)** to the minute |
| **Birth Time Calibration** | Raw wall-clock input (ignores longitude & EoT) | Strips historical DST + applies `4 min/deg` longitude & Equation of Time |
| **Unknown Birth Time Handling** | Forces arbitrary `00:00` midnight (corrupting Hour & sometimes Day Pillar) | Defaults to Solar Noon while flagging `~75–80%` 3-pillar structural confidence |
| **Five Elements Scoring** | Naive surface count (`0–8` visible characters) | Weighs **Month Branch seasonal command (*Yue Ling*)** + **Hidden Stems (*Cang Gan*)** |
| **Favorable Element (*Yong Shen*)** | Simplistic *"add whatever element is 0%"* rule | Evaluates **Structural Strength (*Fu Yi*)** + **Climate Regulation (*Tiao Hou*)** + **Bridge (*Tong Guan*)** |

---

## 3. Open Reference Notes & Empirical Index

- **Energy Diagnostics**: [True Solar Time Offset Reference: Singapore, Hawaii & North America](https://bazilens.github.io/bazi-true-solar-time-guide/notes/true-solar-time-singapore-north-america.html) · [Full Case Study](https://www.bazilens.com/blog/true-solar-time-bazi-singapore-north-america)
- **Relationships & Compatibility**: [Ji Earth & Ding Fire Spousal Palace Directional Flow Matrix](https://bazilens.github.io/bazi-true-solar-time-guide/notes/yin-earth-yin-fire-spousal-palace.html) · [Full Case Study](https://www.bazilens.com/blog/why-yin-earth-yin-fire-overgive-relationships)
- **Relationships & Compatibility**: [Hurting Officer (Shang Guan) & Seven Killings (Qi Sha) Mechanics](https://bazilens.github.io/bazi-true-solar-time-guide/notes/hurting-officer-seven-killings-ten-gods.html) · [Full Case Study](https://www.bazilens.com/blog/hurting-officer-seven-killings-women-bazi-myth)
- **System Architecture**: [Day Master Strength & Useful God (Yong Shen) Diagnostic Framework](https://bazilens.github.io/bazi-true-solar-time-guide/notes/day-master-strength-useful-god-guide.html) · [Full Case Study](https://www.bazilens.com/blog/bazi-calculator-favorable-element-trap)
- **Time & Cycles**: [2027 Fire Goat Year (Ding Wei): 10 Day Masters Timing Matrix](https://bazilens.github.io/bazi-true-solar-time-guide/notes/2027-fire-goat-ding-wei-timing-matrix.html) · [Full Case Study](https://www.bazilens.com/blog/2027-fire-goat-ding-wei-bazi-guide)
- **Relationships & Compatibility**: [Beyond Zodiac Animals: Spousal Palace & Branch Interaction Reference](https://bazilens.github.io/bazi-true-solar-time-guide/notes/spousal-palace-synastry-mechanics.html) · [Full Case Study](https://www.bazilens.com/blog/spousal-palace-compatibility)
- **Time & Cycles**: [10-Year Luck Pillars (Da Yun), Branch Clashes & Void Branches](https://bazilens.github.io/bazi-true-solar-time-guide/notes/luck-pillars-clashes-void-branches.html) · [Full Case Study](https://www.bazilens.com/blog/luck-pillars-climate)

### Latest Empirical Research Monographs
- [2027 Fire Goat Forecast for Bing and Ding Fire Charts](https://www.bazilens.com/blog/2027-fire-goat-bing-fire-ding-fire-bazi)
- [2027 Fire Goat Forecast for Ren and Gui Water Charts](https://www.bazilens.com/blog/2027-fire-goat-ren-water-gui-water-bazi)
- [2027 Fire Goat Forecast for Jia and Yi Wood Charts](https://www.bazilens.com/blog/2027-fire-goat-jia-wood-yi-wood-bazi)

---

## 4. The 12 Two-Hour Solar Branches (*ShiChen* / 时辰)

| Branch | Pinyin | Solar Window | Associated Animal | Primary Element | Hidden Stems (*Cang Gan*) |
|:---|:---|:---|:---|:---|:---|
| 子 | Zi | `23:00 – 00:59` | Rat | Yin/Yang Water | Gui (癸) |
| 丑 | Chou | `01:00 – 02:59` | Ox | Yin Earth (Wet) | Ji (己), Gui (癸), Xin (辛) |
| 寅 | Yin | `03:00 – 04:59` | Tiger | Yang Wood | Jia (甲), Bing (丙), Wu (戊) |
| 卯 | Mao | `05:00 – 06:59` | Rabbit | Yin Wood | Yi (乙) |
| 辰 | Chen | `07:00 – 08:59` | Dragon | Yang Earth (Reservoir) | Wu (戊), Yi (乙), Gui (癸) |
| 巳 | Si | `09:00 – 10:59` | Snake | Yin/Yang Fire | Bing (丙), Geng (庚), Wu (戊) |
| 午 | Wu | `11:00 – 12:59` | Horse | Yin/Yang Fire | Ding (丁), Ji (己) |
| 未 | Wei | `13:00 – 14:59` | Goat | Yin Earth (Dry/Warm) | Ji (己), Ding (丁), Yi (乙) |
| 申 | Shen | `15:00 – 16:59` | Monkey | Yang Metal | Geng (庚), Ren (壬), Wu (戊) |
| 酉 | You | `17:00 – 18:59` | Rooster | Yin Metal | Xin (辛) |
| 戌 | Xu | `19:00 – 20:59` | Dog | Yang Earth (Vault of Fire) | Wu (戊), Xin (辛), Ding (丁) |
| 亥 | Hai | `21:00 – 22:59` | Pig | Yang Water | Ren (壬), Jia (甲) |

---

## 5. The 10 Day Masters (*Ri Zhu* / 日主) Reference

| Day Master | Polarity & Element | Classical Nature Archetype | Core Strengths | Common Stress Pattern |
|:---|:---|:---|:---|:---|
| **Jia (甲)** | Yang Wood | Ancient Forest Tree | Principled leadership, long-term growth, protective | Rigidity; snapping rather than bending under sudden Geng Metal pressure |
| **Yi (乙)** | Yin Wood | Climbing Vine & Wildflower | Diplomatic adaptability, resilience, network intelligence | Over-accommodating others; losing directional anchor without support |
| **Bing (丙)** | Yang Fire | Radiant Sun | Generosity, clarity, magnetic presence, momentum | Over-extension and burnout when illuminating everyone without recovery |
| **Ding (丁)** | Yin Fire | Candlelight & Starlight | Focused insight, psychological warmth, precision craft | Internalized anxiety and overthinking when Wood resource runs dry |
| **Wu (戊)** | Yang Earth | Mountain Ridge | Unshakable reliability, containment, crisis poise | Stagnation and emotional opacity when lacking Wood/Water movement |
| **Ji (己)** | Yin Earth | Fertile Garden Soil | Nurturing synthesis, detail stewardship, resourcefulness | Over-giving in relationships; absorbing surrounding emotional clutter |
| **Geng (庚)** | Yang Metal | Raw Ore & Forged Sword | Decisive execution, loyalty, structural reform under heat | Bluntness and friction when lacking Ding Fire refinement |
| **Xin (辛)** | Yin Metal | Cut Gemstone & Frost | High aesthetic standards, articulate nuance, discernment | Perfectionism and sensitivity to harsh criticism or pressure |
| **Ren (壬)** | Yang Water | Ocean & Rushing River | Macro strategy, boundless adaptability, entrepreneurial drive | Restlessness and scattered focus without Wu Earth levees |
| **Gui (癸)** | Yin Water | Morning Dew & Rain Cloud | Quiet intuition, deep empathy, subtle strategic timing | Emotional overwhelm in overly arid or turbulent cycles |

---

## License

Released under the [MIT License](./LICENSE). Maintained by **Thomas** at [BaziLens](https://www.bazilens.com).
