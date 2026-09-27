# Fonts

`inter-latin.woff2` is a self-hosted subset of Google Fonts' Inter (v20), a variable
font with a weight axis (used at 300/500/700). It replaces the Google Fonts CDN link
to remove third-party requests and shrink the payload.

Subset to Latin-1 (U+0000–00FF, covers Danish æøå) plus the punctuation the site uses
(curly quotes, en/em dash, ellipsis, bullet, ™, →). Regenerate with fontTools:

    # start from the Google-served latin woff2 for Inter:wght@300;500;700
    python3 -c "from fontTools import subset; from fontTools.ttLib import TTFont; \
    cps=list(range(0x00,0x100))+[0x2013,0x2014,0x2018,0x2019,0x201C,0x201D,0x2026,0x2022,0x2122,0x2192]; \
    f=TTFont('inter-google-latin.woff2'); o=subset.Options(); o.flavor='woff2'; o.layout_features='*'; o.name_IDs='*'; \
    s=subset.Subsetter(options=o); s.populate(unicodes=cps); s.subset(f); f.save('inter-latin.woff2')"

Keep `@font-face`'s `unicode-range` in `assets/css/main.css` in sync with this set.
