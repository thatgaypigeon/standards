# CSS
> *This page is up-to-date as of 6 Nov, 2023.*

## Property order
1. General
2. Content
3. Meta / Other
4. Display
5. Size
6. Position
7. Margins
8. Placement
9.  Padding
10. Layout
11. Style
   1. Background
   2. Border
   3. Text
      1. Size
      2. Style (bold, italic, etc.)
      3. Colour
      4. Decoration
12. Transform
13. Transition
14. Animation
15. Custom variables
16. Layers
   1.  Z-Index
   2.  Overflow
17. Other

Properties should then be ordered alphabetically.

### Prefixed properties
All prefixed properties should precede their corresponding property in alphabetical order, all indented so the property values line up.

### Example
```css
element.style {
    /* General */
    all: initial | inherit | unset | revert | revert-layer;

    /* Content */
    content: normal | none | [ <content-replacement> | <content-list> ] [ / [ <string> | <counter> ]+ ]? | element( );

    /* Meta / Other */
    appearance: none | auto | <compat-auto> | <compat-special>;
    caret-color: auto | <color>;
    color-scheme: normal | [ light | dark | <custom-ident> ]+ && only?;
    cursor: [ [ <url> | <url-set> ] [ <x> <y> ]? ]#? [ auto | default | none | context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | grab | grabbing | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll | zoom-in | zoom-out ];
    direction: ltr | rtl;
    
    /* Display */
    display: [ <display-outside> || <display-inside> ] | <display-listitem> | <display-internal> | <display-box> | <display-legacy> | <display-outside> || [ <display-inside> | math ];
        /* Flex */
        flex: none | [ [ <number> <number>? ] || [ content | <width> ] ];
        flex-basis: content | <width>;
        flex-direction: row | row-reverse | column | column-reverse;
        flex-flow: [ row | row-reverse | column | column-reverse ] || [ nowrap | wrap | wrap-reverse ];
        flex-grow: <number>;
        flex-shrink: <number>;
        flex-wrap: nowrap | wrap | wrap-reverse;
        
        /* Grid */

    /* Size */
    block-size: <width>;
    aspect-ratio: auto || [ <number> [ / <number> ]? ];

    /* Position */
    position: ;
    top: auto | <length-percentage>;
    left: auto | <length-percentage>;
    right: auto | <length-percentage>;
    bottom: auto | <length-percentage>;

    clear: inline-start | inline-end | block-start | block-end | left | right | top | bottom | none;
    float: block-start | block-end | inline-start | inline-end | snap-block | <snap-block()> | snap-inline | <snap-inline()> | left | right | top | bottom | none | footnote;

    /* Placement */
    align-self: auto | normal | stretch | <baseline-position> | <overflow-position>? <self-position>;

    /* Layout */
    align-content: normal | <baseline-position> | <content-distribution> | <overflow-position>? <content-position>;
    align-items: normal | stretch | <baseline-position> | [<overflow-position>? <self-position>];

    /* Layout */
    box-sizing: content-box | border-box;

        /* Break */
        break-before: auto | avoid | always | all | avoid-page | page | left | right | recto | verso | avoid-column | column | avoid-region | region;
        break-inside: auto | avoid | avoid-page | avoid-column | avoid-region;
        break-after: auto | avoid | always | all | avoid-page | page | left | right | recto | verso | avoid-column | column | avoid-region | region;
    
    caption-side: top | bottom;
    gap: <row-gap> <column-gap>?;

        /* Column */
        columns: [ auto | <length> | min-content | max-content | fit-content( <length-percentage> ) ] || [ auto | <integer> ];
        column-count: auto | <integer>;
        column-fill: auto | balance | balance-all;
        column-gap: normal | <length-percentage>;
        
            /* Column Rule */
            column-rule: <line-width> || <line-style> || <color>;
            column-rule-color: <color>;
            column-rule-style: <line-style>;
            column-rule-width: <line-width>;
        
        column-span: none | all;
        column-width: auto | <length> | min-content | max-content | fit-content( <length-percentage> );

        /* Contain */
        contain: none | strict | content | [ size || layout || style || paint ];
        contain-intrinsic-size: [ none | <length> | auto <length> ]{1,2};
        contain-intrinsic-block-size: none | <length> | auto <length>;
        contain-intrinsic-inline-size: none | <length> | auto <length>;
        contain-intrinsic-width: none | <length> | auto <length>;
        contain-intrinsic-height: none | <length> | auto <length>;

    /* Style */
    accent-color: auto | <color>;

        /* Background */
        background: [ <bg-layer># , ]? <final-bg-layer>;
        background-attachment: [ scroll | fixed | local ]#;
        background-blend-mode: <mix-blend-mode>#;
        background-clip: [ border-box | padding-box | content-box ]#;
        background-color: <color>;
        background-image: <image> | none;
        background-origin: [ border-box | padding-box | content-box ]#;
        background-position: <bg-position>#;
        background-position-x: [ center | [ [ left | right | x-start | x-end ]? <length-percentage>? ]! ]#;
        background-position-y: [ center | [ [ top | bottom | y-start | y-end ]? <length-percentage>? ]! ]#;
        background-repeat: [ repeat-x | repeat-y | [ repeat | space | round | no-repeat ]{1,2} ]#;
        background-size: [ [ <length-percentage> | auto ]{1,2} | cover | contain ]#;

        /* Border */
        border: <line-width> || <line-style> || <color>;

            /* Block */
            border-block: <line-width> || <line-style> || <color>;
            border-block-color: <color>{1,2};
            border-block-style: <line-style>{1,2};
            border-block-width: <line-width>{1,2};

                /* Block Start */
                border-block-start: <line-width> || <line-style> || <color>;
                border-block-start-color: <color>;
                border-block-start-style: <line-style>;
                border-block-start-width: <line-width>;

                /* Block End */
                border-block-end: <line-width> || <line-style> || <color>;
                border-block-end-color: <color>;
                border-block-end-style: <line-style>;
                border-block-end-width: <line-width>;
            
            /* Inline */
            border-inline: <line-width> || <line-style> || <color>;
            border-inline-color: <color>{1,2};
            border-inline-style: <line-style>{1,2};
            border-inline-width: <line-width>{1,2};

                /* Block Start */
                border-inline-start: <line-width> || <line-style> || <color>;
                border-inline-start-color: <color>;
                border-inline-start-style: <line-style>;
                border-inline-start-width: <line-width>;

                /* Block End */
                border-inline-end: <line-width> || <line-style> || <color>;
                border-inline-end-color: <color>;
                border-inline-end-style: <line-style>;
                border-inline-end-width: <line-width>;

            /* Top */
            border-top: <line-width> || <line-style> || <color>;
            border-top-color: <color>;
            border-top-style: <line-style>;
            border-top-width: <line-width>;

            /* Left */
            border-left: <line-width> || <line-style> || <color>;
            border-left-color: <color>;
            border-left-style: <line-style>;
            border-left-width: <line-width>;

            /* Right */
            border-right: <line-width> || <line-style> || <color>;
            border-right-color: <color>;
            border-right-style: <line-style>;
            border-right-width: <line-width>;

            /* Bottom */
            border-bottom: <line-width> || <line-style> || <color>;
            border-bottom-color: <color>;
            border-bottom-style: <line-style>;
            border-bottom-width: <line-width>;
        
        border-collapse: collapse | separate;
        border-color: <color>{1,4};

            /* Border Image */
            border-image: <border-image>;
            border-image-outset: [ <length> | <number> ]{1,4};
            border-image-repeat: [ stretch | repeat | round | space ]{1,2};
            border-image-slice: [ <number> | <percentage> ]{1,4} && fill?;
            border-image-source: none | <image>;
            border-image-width: [ <length-percentage> | <number> | auto ]{1,4};

        border-radius: <length-percentage>{1,4} [ / <length-percentage>{1,4} ]?;
            /* Start */
            border-start-end-radius: <length-percentage>;
            border-start-start-radius: <length-percentage>;
            
            /* End */
            border-end-end-radius: <length-percentage>;
            border-end-start-radius: <length-percentage>;

            /* Top */
            border-top-left-radius: <length-percentage>;
            border-top-right-radius: <length-percentage>;
            
            /* Bottom */
            border-bottom-left-radius: <length-percentage>;
            border-bottom-right-radius: <length-percentage>;

        border-spacing: <length>{1,2};
        border-style: <line-style>{1,4};
        border-width: <line-width>{1,4};

    box-shadow: none | <shadow>#;
    color: <color>;
    filter: none | <filter-value-list>;

        /* Font */
        font: ;
        font-family: ;
        font-size: ;
        font-weight: ;
        font-style: ;

        font-feature-settings: ;
        font-kerning: ;
        font-language-override: ;
        font-optical-sizing: ;
        font-palette: ;
        font-size-adjust: ;
        font-stretch: ;

            /* Synthesis */
            font-synthesis: ;
            font-synthesis-position: ;
            font-synthesis-small-caps: ;
            font-synthesis-style: ;
            font-synthesis-weight: ;

            /* Variant */
            font-variant: ;
            font-variant-alternates: ;
            font-variant-caps: ;
            font-variant-east-asian: ;
            font-variant-emoji: ;
            font-variant-ligatures: ;
            font-variant-numeric: ;
            font-variant-position: ;

        font-variation-settings: ;

        /* Other */
        backdrop-filter: none | <filter-value-list>;
        backface-visibility: visible | hidden;
        box-decoration-break: slice | clone;
        clip-path: <clip-source> | [ <basic-shape> || <geometry-box> ] | none;
        forced-color-adjust: auto | none | preserve-parent-color;

    /* Animation */
    animation: <single-animation>#;
    animation-composition: [ replace | add | accumulate ]#;
    animation-delay: [ <animation-delay-start> <animation-delay-end>? | <timeline-range-name> ]#;
    animation-direction: [ normal | reverse | alternate | alternate-reverse ]#;
    animation-duration: <time>#;
    animation-fill-mode: [ none | forwards | backwards | both ]#;
    animation-iteration-count: [ infinite | <number> ]#;
    animation-name: [ none | [ <custom-ident> | <string> ] ]#;
    animation-play-state: [ running | paused ]#;
    animation-timing-function: [ linear | <linear-easing-function> | <cubic-bezier-easing-function> | <step-easing-function> ]#;

    /* Other */
        /* Container */
        container: none | <custom-ident>+ [ / normal | size | inline-size ]?;
        container-name: none | <custom-ident>+;
        container-type: normal | size | inline-size;

        /* Counter */
        counter-increment: [ <counter-name> <integer>? ]+ | none;
        counter-reset: [ <counter-name> <integer>? | reversed( <counter-name> ) <integer>? ]+ | none;
        counter-set: [ <counter-name> <integer>? ]+ | none;
    
    empty-cells: show | hide;
}
```

