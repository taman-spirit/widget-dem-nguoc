# Event countdown

A countdown to any date you set: an opening, a launch, a founding anniversary.

*[Đọc bản tiếng Việt](README.md)*

**See it running:** https://nhatnguyet.org/widget/dem-nguoc

## Paste these two lines

```html
<div data-widget="dem-nguoc"></div>
<script async src="https://nhatnguyet.org/embed/w.js"></script>
```

No account, no API key, nothing to pay.

## What it gives your page

The general form of the Tết countdown: instead of being fixed to the lunar New Year, you set any date through data-ngay-den. The widget knows three states, counting, the day itself, and afterwards, so it never counts to zero and then sits there.

## Worth knowing before you embed

- Two attributes are required: the target date and the event name. Leave either out and the widget says which is missing rather than inventing a number.
- Once the day has passed, the widget switches to a line saying so instead of removing itself from your page.
- Days are counted on the calendar date in Vietnam time, so every visitor on a given day sees the same number.

## The steps

1. Set data-ngay-den in year-month-day form, for example 2027-03-15.
2. Set data-ten-su-kien to the name shown beside the count, up to 60 characters.
3. After the day, remove it or leave it as you prefer; the widget will not vanish on its own.

## Where to paste it

**WordPress.** Add a *Custom HTML* block to the post, or a *Text* widget in
the sidebar, and paste both lines there. Do not paste into the ordinary
editor: it will show the code as text instead of running it.

**Wix, Squarespace, Shopify.** Use the *Embed HTML* / *Custom HTML* block.

**Hand-written sites.** Paste it straight where you want the widget. If you
embed several widgets, the `<script>` line only needs to appear once on the
page.

**A note on width.** The widget fits the width of wherever you put it. If that is narrower than 280px, add
`data-size="compact"`; if it is a wide horizontal strip, use
`data-size="wide"`.

## Make it match your page

| Attribute | Values | Meaning |
|---|---|---|
| `data-widget` | `dem-nguoc` | Required |
| `data-theme` | light or dark | Defaults to light |
| `data-accent` | #b3341f | Accent colour as a 6-digit hex value, to match your own branding |
| `data-lang` | vi or en | Defaults to vi |
| `data-size` | compact, standard or wide | Level of detail for the width you have: compact drops secondary detail, wide lays out horizontally. Defaults to standard |
| `data-ngay-den` | 2027-03-15 | Target date for the event countdown, in year-month-day form. Required for that widget |
| `data-ten-su-kien` | Branch 2 opening | The name shown beside the count, up to 60 characters. Required for the event countdown |

With every attribute this widget accepts, it looks like this:

```html
<div data-widget="dem-nguoc" data-theme="dark" data-accent="#1f6f5c" data-lang="en" data-size="compact" data-ngay-den="2027-03-15" data-ten-su-kien="Khai truong chi nhanh 2"></div>
<script async src="https://nhatnguyet.org/embed/w.js"></script>
```

Want to see it for yourself before it goes near your real page? Open
[`vi-du/index.html`](vi-du/index.html) in a browser, nothing to install.

## A few things we ask

- Free for personal and business websites, with no display limit.
- Keep the attribution line at the foot of the widget. That is what you give
  in return for free use.
- Do not embed on gambling, adult, fraudulent sites or anything unlawful
  under Vietnamese law.
- The content is folk knowledge and cultural convention, offered as
  reference, not as health, financial or legal advice.

Full text: [`TERMS.md`](TERMS.md) · [https://nhatnguyet.org/widget/dieu-khoan](https://nhatnguyet.org/widget/dieu-khoan)

## Who we are

Nhat Nguyet (https://nhatnguyet.org) is a Vietnamese reference site for calendrical and
cultural knowledge: the lunar calendar computed for Vietnam's own time zone,
the sexagenary cycle, solar terms, auspicious hours, astrology, feng shui,
and a glossary of terms.

There is one thing we try hard to keep clear, even inside a 300px frame:
which parts are computed, and which are folk convention.

Lunar dates, sexagenary names and solar terms are **computed**. Run the same
calculation and you get the same answer, and we publish the underlying
datasets under CC BY 4.0 so you can check for yourself.

Auspicious hours, Bat Trach directions and Lo Ban rule bands are **cultural
convention**. There are real lookup tables behind them, but they are not
measurements. The widget tells you what the table says; how much weight to
give it is yours to decide.

Where the schools disagree, we say so, rather than quietly picking a side and
presenting it as the only reading.

Open data: [GitHub](https://github.com/taman-spirit/du-lieu-am-lich) ·
[Hugging Face](https://huggingface.co/datasets/nhatnguyet)

## Something not right?

Open an issue in this repository. We do read them.

The whole widget library: [https://nhatnguyet.org/widget](https://nhatnguyet.org/widget)
