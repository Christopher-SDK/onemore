# OneMore Redesign Report [BETA]

**Files scanned:** 13
**HIG Score:** 0/100 (Grade: F)
**Violations:** 879 total (73 critical, 73 high, 397 medium, 336 low)

## Summary

| Category | Violations | Impact |
|----------|-----------|--------|
| Colors | 261 | Replace hardcoded colors with Apple semantic tokens |
| Touch | 249 | Increase touch targets to 44px minimum |
| Typography | 145 | Update font stack and sizes to Apple type scale |
| Spacing | 94 | Align to 4pt grid |
| Animation | 81 | Replace easing with Apple curves |
| Corners | 48 | Use Apple corner radii |
| Icons | 1 | Replace emoji icons with SF Symbols or SVG |

## Violations by File

### /Users/christopherarias/projects/onemore/showcase/demos/creative-tools.html

**[CRITICAL] TOUCH-001** (line 318)
```
Current:  height: 18px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 347)
```
Current:  height: 12px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 416)
```
Current:  height: 28px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 470)
```
Current:  height: 10px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 713)
```
Current:  height: 34px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 812)
```
Current:  height: 32px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 827)
```
Current:  height: 16px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 922)
```
Current:  height: 20px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 980)
```
Current:  height: 22px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 1118)
```
Current:  height: 18px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 1443)
```
Current:  <div class="channel-bar" style="height:40px; background:linear-gradient(to top, #FF9F0A, #ffb84d);" data-bar-delay="300"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 102)
```
Current:  @keyframes shimmer { from, to { background-position: 200% center; } }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 103)
```
Current:  @keyframes rotateBorder { from, to { --border-angle: 0deg; } }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 104)
```
Current:  @keyframes playheadMove { from, to { left: 4%; } }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] COLOR-002** (line 240)
```
Current:  background: linear-gradient(135deg, var(--purple) 0%, var(--pink) 40%, #fff 80%);
Fix:      Use '#fbfbfd' on web, Color.systemBackground in SwiftUI
Reason:   Pure white background — Apple uses slightly warm off-white
```

**[HIGH] ANIM-003** (line 283)
```
Current:  animation: shimmer 3s cubic-bezier(0.25, 0.1, 0.25, 1) infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 286)
```
Current:  @keyframes shimmer {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] CORNER-001** (line 358)
```
Current:  border-radius: 8px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 437)
```
Current:  border-radius: 5px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] ANIM-003** (line 461)
```
Current:  animation: playheadMove 8s cubic-bezier(0.25, 0.1, 0.25, 1) infinite alternate;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] CORNER-001** (line 472)
```
Current:  border-radius: 2px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] ANIM-003** (line 476)
```
Current:  @keyframes playheadMove {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] CORNER-001** (line 548)
```
Current:  border-radius: 8px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 565)
```
Current:  border-radius: 8px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 633)
```
Current:  border-radius: 8px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 699)
```
Current:  border-radius: 6px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 725)
```
Current:  border-radius: 8px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 747)
```
Current:  border-radius: 4px 4px 0 0;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 760)
```
Current:  border-radius: 8px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 813)
```
Current:  border-radius: 6px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 881)
```
Current:  border-radius: 8px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 908)
```
Current:  border-radius: 6px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 923)
```
Current:  border-radius: 4px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] COLOR-002** (line 1042)
```
Current:  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
Fix:      Use '#fbfbfd' on web, Color.systemBackground in SwiftUI
Reason:   Pure white background — Apple uses slightly warm off-white
```

**[HIGH] COLOR-002** (line 1043)
```
Current:  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
Fix:      Use '#fbfbfd' on web, Color.systemBackground in SwiftUI
Reason:   Pure white background — Apple uses slightly warm off-white
```

**[HIGH] ANIM-003** (line 1046)
```
Current:  animation: rotateBorder 4s linear infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 1055)
```
Current:  @keyframes rotateBorder {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] TYPO-002** (line 143)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 154)
```
Current:  color: #fbfbfd !important;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 160)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] SPACE-003** (line 219)
```
Current:  padding-bottom: 60px;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] COLOR-003** (line 265)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 331)
```
Current:  background: #1a1a1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 342)
```
Current:  background: #0d0d0f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 351)
```
Current:  .window-dot:nth-child(1) { background: #FF5F57; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 352)
```
Current:  .window-dot:nth-child(2) { background: #FFBD2E; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 353)
```
Current:  .window-dot:nth-child(3) { background: #28C840; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-003** (line 394)
```
Current:  padding: 8px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] COLOR-003** (line 459)
```
Current:  background: #FF375F;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 471)
```
Current:  background: #FF375F;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 487)
```
Current:  background: #0a0a0a;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 514)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 532)
```
Current:  background: #1a1a1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 564)
```
Current:  background: #111114;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 621)
```
Current:  background: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 632)
```
Current:  background: #0d0d0f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 681)
```
Current:  background: #1e1e22;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 698)
```
Current:  background: #141417;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 724)
```
Current:  background: #141417;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 759)
```
Current:  background: #141417;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 791)
```
Current:  background: #1a1a1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 801)
```
Current:  background: #111114;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-003** (line 805)
```
Current:  padding: 16px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] COLOR-003** (line 890)
```
Current:  background: #111114;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 954)
```
Current:  background: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 995)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 1015)
```
Current:  background: #111114;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] ANIM-001** (line 1046)
```
Current:  animation: rotateBorder 4s linear infinite;
Fix:      Use cubic-bezier(0.25, 0.1, 0.25, 1) or spring animations
Reason:   Non-Apple easing curve — avoid ease-in-out and linear
```

**[MEDIUM] COLOR-003** (line 1062)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 1073)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 1093)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 1111)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 1136)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 1189)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[LOW] ANIM-002** (line 57)
```
Current:  transition: opacity 600ms var(--ease-apple), transform 600ms var(--ease-apple);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 67)
```
Current:  transition: clip-path 1000ms var(--ease-apple);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] SPACE-002** (line 155)
```
Current:  padding: 6px 18px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 266)
```
Current:  padding: 14px 32px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 302)
```
Current:  padding: 14px 32px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 340)
```
Current:  padding: 14px 18px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 437)
```
Current:  border-radius: 5px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] ANIM-002** (line 440)
```
Current:  transition: transform 800ms var(--ease-apple);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] TYPO-003** (line 507)
```
Current:  font-size: 28px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] ANIM-002** (line 648)
```
Current:  transition: stroke-dashoffset 2000ms var(--ease-apple);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] CORNER-003** (line 699)
```
Current:  border-radius: 6px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] ANIM-002** (line 750)
```
Current:  transition: transform 800ms var(--ease-apple);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] CORNER-003** (line 813)
```
Current:  border-radius: 6px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] CORNER-003** (line 908)
```
Current:  border-radius: 6px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] TYPO-003** (line 1079)
```
Current:  font-size: 48px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 1125)
```
Current:  padding: 14px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 1266)
```
Current:  <li><a href="#video">Video</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1267)
```
Current:  <li><a href="#audio">Audio</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1268)
```
Current:  <li><a href="#design">Design</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1269)
```
Current:  <li><a href="#pricing">Pricing</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1270)
```
Current:  <li><a href="#" class="nav-cta">Try Free</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1282)
```
Current:  <button class="btn-primary">Start Creating</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1283)
```
Current:  <button class="btn-secondary">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1597)
```
Current:  <button class="pricing-btn pricing-btn-secondary">Get Started</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1612)
```
Current:  <button class="pricing-btn pricing-btn-primary">Get Started</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1626)
```
Current:  <button class="pricing-btn pricing-btn-secondary">Contact Sales</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1639)
```
Current:  <button class="btn-primary" style="font-size:19px; padding:16px 40px;">Try Prismix Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1652)
```
Current:  <li><a href="#">Privacy</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1653)
```
Current:  <li><a href="#">Terms</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1654)
```
Current:  <li><a href="#">Support</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1655)
```
Current:  <li><a href="#">Press</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

### /Users/christopherarias/projects/onemore/showcase/demos/crypto-web3.html

**[CRITICAL] TOUCH-001** (line 391)
```
Current:  height: 36px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 528)
```
Current:  height: 40px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 573)
```
Current:  height: 32px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 627)
```
Current:  height: 28px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 698)
```
Current:  height: 36px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 767)
```
Current:  height: 36px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 810)
```
Current:  height: 28px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 902)
```
Current:  height: 32px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 914)
```
Current:  height: 16px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 753)
```
Current:  animation: vaultPulse 3s var(--ease) infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 756)
```
Current:  @keyframes vaultPulse {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 762)
```
Current:  .vault-inner { animation: none; }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] TYPO-002** (line 153)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 165)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 173)
```
Current:  color: #1d1d1f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 214)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 264)
```
Current:  color: #1d1d1f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 396)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 398)
```
Current:  color: #1d1d1f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 401)
```
Current:  .asset-icon.btc { background: #F7931A; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 402)
```
Current:  .asset-icon.eth { background: #627EEA; color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 459)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 533)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 537)
```
Current:  .coin-circle.btc { background: #F7931A; color: #1d1d1f; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 538)
```
Current:  .coin-circle.eth { background: #627EEA; color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 539)
```
Current:  .coin-circle.sol { background: linear-gradient(135deg, #9945FF, #14F195); color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 540)
```
Current:  .coin-circle.avax { background: #E84142; color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 541)
```
Current:  .coin-circle.dot { background: #E6007A; color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 542)
```
Current:  .coin-circle.link { background: #2A5ADA; color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 642)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 712)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 844)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 852)
```
Current:  color: #1d1d1f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 925)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 935)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 960)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 981)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[LOW] ANIM-002** (line 77)
```
Current:  transition: opacity 0.6s var(--ease), transform 0.6s var(--ease);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 87)
```
Current:  transition: clip-path 0.8s var(--ease);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] TYPO-003** (line 316)
```
Current:  font-size: 42px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 426)
```
Current:  .dashboard-value { font-size: 32px; }
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 453)
```
Current:  font-size: 40px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 465)
```
Current:  .stat-number { font-size: 28px; }
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 560)
```
Current:  font-size: 24px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 636)
```
Current:  font-size: 24px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 828)
```
Current:  font-size: 32px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TOUCH-002** (line 1027)
```
Current:  <a href="#" class="nav-brand">Nexus</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1029)
```
Current:  <li><a href="#prices">Trade</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1030)
```
Current:  <li><a href="#features">Wallet</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1031)
```
Current:  <li><a href="#security">DeFi</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1032)
```
Current:  <li><a href="#app">Learn</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1034)
```
Current:  <a href="#cta" class="nav-cta">Start Trading</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1044)
```
Current:  <a href="#cta" class="btn-primary">Start Trading</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1045)
```
Current:  <a href="#features" class="btn-secondary">Explore DeFi</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1336)
```
Current:  <button class="phone-action-btn send">Send</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1337)
```
Current:  <button class="phone-action-btn receive">Receive</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 1388)
```
Current:  <a href="#" class="btn-primary" style="font-size: 19px; padding: 18px 40px;">Create Free Account</a>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 1388)
```
Current:  <a href="#" class="btn-primary" style="font-size: 19px; padding: 18px 40px;">Create Free Account</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1399)
```
Current:  <li><a href="#">Terms</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1400)
```
Current:  <li><a href="#">Privacy</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1401)
```
Current:  <li><a href="#">Security</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1402)
```
Current:  <li><a href="#">Status</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] ANIM-002** (line 1573)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25, 0.1, 0.25, 1), transform 0.6s cubic-bezier(0.25, 0.1, 0.25, 1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

### /Users/christopherarias/projects/onemore/showcase/demos/ecommerce.html

**[CRITICAL] TOUCH-001** (line 94)
```
Current:  width: 18px; height: 18px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 348)
```
Current:  .stars svg { width: 12px; height: 12px; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 448)
```
Current:  width: 28px; height: 28px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 551)
```
Current:  @keyframes fadeSlideIn {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] TYPO-002** (line 70)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 97)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 197)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 212)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 260)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 339)
```
Current:  .product-name { font-size: 15px; font-weight: 600; color: var(--text-light); margin-bottom: 8px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 361)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 399)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 410)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 437)
```
Current:  .showcase-brand { font-size: 14px; color: var(--secondary); margin-bottom: 16px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 466)
```
Current:  .swatch-label { font-size: 14px; color: var(--secondary); margin-left: 4px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 482)
```
Current:  .trust-label { font-size: 14px; color: var(--secondary); }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 517)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 519)
```
Current:  background: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 534)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 537)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 799)
```
Current:  <div style="font-size:14px;color:var(--secondary);margin-bottom:16px;">Color</div>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 801)
```
Current:  <div class="color-swatch active" data-color="midnight" data-bg="linear-gradient(135deg,#1a1a2e 0%,#16213e 50%,#533483 100%)" style="background:#1a1a2e;"></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 802)
```
Current:  <div class="color-swatch" data-color="rose" data-bg="linear-gradient(135deg,#c94b4b 0%,#4b134f 100%)" style="background:#c94b4b;"></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 803)
```
Current:  <div class="color-swatch" data-color="forest" data-bg="linear-gradient(135deg,#134e5e 0%,#71b280 100%)" style="background:#134e5e;"></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 804)
```
Current:  <div class="color-swatch" data-color="sand" data-bg="linear-gradient(135deg,#c79060 0%,#f7d794 100%)" style="background:#c79060;"></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 807)
```
Current:  <div style="font-size:15px;color:var(--secondary);line-height:1.7;margin-bottom:32px;">
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 811)
```
Current:  <button class="btn-accent add-to-cart" data-name="Aria Pro Headphones" data-price="$349" style="font-size:15px;padding:14px 28px;">Add to Cart</button>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 812)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Wishlist</button>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 853)
```
Current:  <button class="btn-accent" style="font-size:15px;padding:14px 24px;">Subscribe</button>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[LOW] SPACE-002** (line 145)
```
Current:  padding: 6px 16px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 438)
```
Current:  .showcase-price { font-size: 28px; font-weight: 700; color: var(--text-light); margin-bottom: 24px; }
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 514)
```
Current:  padding: 14px 20px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 535)
```
Current:  padding: 14px 24px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 579)
```
Current:  <li><a href="#">New Arrivals</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 580)
```
Current:  <li><a href="#">Collections</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 581)
```
Current:  <li><a href="#">Sale</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 582)
```
Current:  <li><a href="#">About</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 585)
```
Current:  <button class="cart-btn" id="cart-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 602)
```
Current:  <button class="btn-accent">Shop Now</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 603)
```
Current:  <button class="btn-primary">View Lookbook</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 638)
```
Current:  <button class="wishlist-btn" data-name="Merino Turtleneck">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 657)
```
Current:  <button class="add-to-cart" data-name="Merino Turtleneck" data-price="$289">Add to Cart</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 666)
```
Current:  <button class="wishlist-btn" data-name="Silk Midi Dress">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 685)
```
Current:  <button class="add-to-cart" data-name="Silk Midi Dress" data-price="$445">Add to Cart</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 694)
```
Current:  <button class="wishlist-btn" data-name="Italian Leather Bag">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 713)
```
Current:  <button class="add-to-cart" data-name="Italian Leather Bag" data-price="$695">Add to Cart</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 722)
```
Current:  <button class="wishlist-btn" data-name="Linen Blazer">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 741)
```
Current:  <button class="add-to-cart" data-name="Linen Blazer" data-price="$380">Add to Cart</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 756)
```
Current:  <button class="category-pill active" data-cat="all">All Items</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 757)
```
Current:  <button class="category-pill" data-cat="clothing">Clothing</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 758)
```
Current:  <button class="category-pill" data-cat="bags">Bags</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 759)
```
Current:  <button class="category-pill" data-cat="shoes">Shoes</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 760)
```
Current:  <button class="category-pill" data-cat="jewelry">Jewelry</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 761)
```
Current:  <button class="category-pill" data-cat="watches">Watches</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 762)
```
Current:  <button class="category-pill" data-cat="accessories">Accessories</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 763)
```
Current:  <button class="category-pill" data-cat="beauty">Beauty</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 811)
```
Current:  <button class="btn-accent add-to-cart" data-name="Aria Pro Headphones" data-price="$349" style="font-size:15px;padding:14px 28px;">Add to Cart</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 811)
```
Current:  <button class="btn-accent add-to-cart" data-name="Aria Pro Headphones" data-price="$349" style="font-size:15px;padding:14px 28px;">Add to Cart</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 812)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Wishlist</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 812)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Wishlist</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 853)
```
Current:  <button class="btn-accent" style="font-size:15px;padding:14px 24px;">Subscribe</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 853)
```
Current:  <button class="btn-accent" style="font-size:15px;padding:14px 24px;">Subscribe</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

### /Users/christopherarias/projects/onemore/showcase/demos/education.html

**[CRITICAL] TOUCH-001** (line 222)
```
Current:  .star { width: 14px; height: 14px; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 272)
```
Current:  width: 40px; height: 40px; border-radius: 50%;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 316)
```
Current:  .plan-features li::before { content: ''; width: 18px; height: 18px; border-radius: 50%; background: rgba(88,86,214,0.25); flex-shrink: 0; display: flex; align-items: center; justify-content: center; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 317)
```
Current:  .check-icon { width: 18px; height: 18px; flex-shrink: 0; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 90)
```
Current:  .badge-dot { width: 6px; height: 6px; background: var(--accent); border-radius: 50%; animation: pulse 2s infinite; }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 91)
```
Current:  @keyframes pulse { 0%,100% { opacity: 1; } 50% { opacity: 0.4; } }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 334)
```
Current:  *, .animate-ready { animation: none !important; transition: none !important; transform: none !important; opacity: 1 !important; }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] TYPO-002** (line 64)
```
Current:  .nav-links a { font-size: 14px; color: var(--text-secondary); text-decoration: none; transition: color 0.2s; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 67)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 69)
```
Current:  border-radius: var(--btn-radius); font-size: 14px; font-weight: 500;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 111)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 136)
```
Current:  .stat-label { font-size: 14px; color: var(--text-secondary); margin-top: 4px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 162)
```
Current:  .cat-section { background: #0c0c0e; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 164)
```
Current:  .cat-section .section-headline, .cat-section .section-tag { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 165)
```
Current:  .cat-section .section-sub { color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 166)
```
Current:  .cat-section .section-headline { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 183)
```
Current:  .cat-card h3 { font-size: 15px; font-weight: 600; color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 183)
```
Current:  .cat-card h3 { font-size: 15px; font-weight: 600; color: #f5f5f7; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 184)
```
Current:  .cat-card p { font-size: 13px; color: #86868b; margin-top: 4px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 192)
```
Current:  background: #fbfbfd; border: 1px solid rgba(0,0,0,0.07);
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 198)
```
Current:  .course-card { background: #1c1c1e; border-color: rgba(255,255,255,0.07); }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 213)
```
Current:  .course-card p { font-size: 14px; color: var(--text-secondary); line-height: 1.5; margin-bottom: 16px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 223)
```
Current:  .star-full { color: #FF9500; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 224)
```
Current:  .star-empty { color: #d2d2d7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 228)
```
Current:  @media (prefers-color-scheme: dark) { .timeline-section { background: #0c0c0e; } }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 229)
```
Current:  .timeline-section .section-headline { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 231)
```
Current:  .timeline-section .section-sub { color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 246)
```
Current:  color: #fbfbfd; font-weight: 700; font-size: 17px; position: relative; z-index: 1;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-003** (line 249)
```
Current:  .timeline-content { padding-bottom: 40px; }
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] COLOR-003** (line 250)
```
Current:  .timeline-content h3 { font-size: 20px; font-weight: 600; color: #f5f5f7; margin-bottom: 8px; margin-top: 10px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 251)
```
Current:  .timeline-content p { font-size: 15px; color: #86868b; line-height: 1.6; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 251)
```
Current:  .timeline-content p { font-size: 15px; color: #86868b; line-height: 1.6; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 259)
```
Current:  background: #fbfbfd; border: 1px solid rgba(0,0,0,0.07); border-radius: var(--card-radius);
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 264)
```
Current:  .testimonial-card { background: #1c1c1e; border-color: rgba(255,255,255,0.07); }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 268)
```
Current:  .tstar { font-size: 15px; color: #FF9500; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 268)
```
Current:  .tstar { font-size: 15px; color: #FF9500; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 269)
```
Current:  .testimonial-card blockquote { font-size: 15px; line-height: 1.7; color: var(--text-secondary); margin-bottom: 20px; font-style: italic; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 274)
```
Current:  font-size: 17px; font-weight: 700; color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 277)
```
Current:  .author-name { font-size: 14px; font-weight: 600; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 282)
```
Current:  @media (prefers-color-scheme: dark) { .pricing-section { background: #0c0c0e; } }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 283)
```
Current:  .pricing-section .section-headline { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 285)
```
Current:  .pricing-section .section-sub { color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 307)
```
Current:  background: var(--accent); color: #fbfbfd; font-size: 12px; font-weight: 600;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 310)
```
Current:  .plan-name { font-size: 13px; font-weight: 600; color: #86868b; text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 12px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 311)
```
Current:  .plan-price { font-size: 52px; font-weight: 700; letter-spacing: -2px; color: #f5f5f7; margin-bottom: 6px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 313)
```
Current:  .plan-period { font-size: 14px; color: #86868b; margin-bottom: 28px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 313)
```
Current:  .plan-period { font-size: 14px; color: #86868b; margin-bottom: 28px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 315)
```
Current:  .plan-features li { font-size: 15px; color: #f5f5f7; display: flex; align-items: center; gap: 10px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 315)
```
Current:  .plan-features li { font-size: 15px; color: #f5f5f7; display: flex; align-items: center; gap: 10px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 320)
```
Current:  background: #1d1d1f; color: #86868b; text-align: center;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 324)
```
Current:  .footer-brand { font-size: 18px; font-weight: 600; color: #f5f5f7; margin-bottom: 8px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 472)
```
Current:  <span class="course-level" style="background: rgba(255,149,0,0.1); color: #FF9500;">Beginner</span>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 496)
```
Current:  <span class="course-level" style="background: rgba(52,199,89,0.1); color: #34C759;">Advanced</span>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 521)
```
Current:  <h2 class="section-headline animate-ready" style="color: #f5f5f7;">How Learning Paths Work</h2>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 595)
```
Current:  <h2 class="section-headline animate-ready" style="color: #f5f5f7;">Simple, Transparent Pricing</h2>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[LOW] SPACE-002** (line 86)
```
Current:  color: var(--accent); padding: 6px 14px; border-radius: 100px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 112)
```
Current:  padding: 14px 28px; border-radius: var(--btn-radius); font-size: 17px; font-weight: 500;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 119)
```
Current:  padding: 14px 28px; border-radius: var(--btn-radius); font-size: 17px; font-weight: 500;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 130)
```
Current:  border-radius: 18px; padding: 28px 36px; text-align: center;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 130)
```
Current:  border-radius: 18px; padding: 28px 36px; text-align: center;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] CORNER-003** (line 180)
```
Current:  width: 52px; height: 52px; margin: 0 auto 16px; border-radius: 14px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] TYPO-003** (line 203)
```
Current:  font-size: 48px; position: relative; overflow: hidden;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 208)
```
Current:  font-size: 12px; font-weight: 600; padding: 3px 10px; border-radius: 100px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 260)
```
Current:  padding: 28px; opacity: 0; transform: translateY(30px);
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] ANIM-002** (line 330)
```
Current:  transition: opacity 0.6s cubic-bezier(0.25, 0.1, 0.25, 1), transform 0.6s cubic-bezier(0.25, 0.1, 0.25, 1);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] TOUCH-002** (line 343)
```
Current:  <li><a href="#">Courses</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 344)
```
Current:  <li><a href="#">Paths</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 345)
```
Current:  <li><a href="#">For Teams</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 346)
```
Current:  <li><a href="#">Pricing</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 348)
```
Current:  <button class="nav-cta">Start Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 360)
```
Current:  <button class="btn-primary">Start Learning Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 361)
```
Current:  <button class="btn-ghost">Browse Courses</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 607)
```
Current:  <button class="btn-ghost" style="width: 100%;">Get Started</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 621)
```
Current:  <button class="btn-primary" style="width: 100%;">Start Pro</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 633)
```
Current:  <button class="btn-ghost" style="width: 100%;">Contact Sales</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] ANIM-002** (line 666)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 680)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

### /Users/christopherarias/projects/onemore/showcase/demos/finance-banking.html

**[CRITICAL] TOUCH-001** (line 271)
```
Current:  height: 30px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 326)
```
Current:  height: 28px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 400)
```
Current:  .feat-icon svg { width: 24px; height: 24px; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 493)
```
Current:  width: 40px; height: 40px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] CORNER-001** (line 272)
```
Current:  border-radius: 5px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 454)
```
Current:  border-radius: 6px 6px 0 0;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 468)
```
Current:  border-radius: 6px 6px 0 0;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] ANIM-003** (line 621)
```
Current:  @keyframes fadeSlideIn {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] COLOR-003** (line 78)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 178)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 196)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 298)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 312)
```
Current:  .card-name { font-size: 15px; font-weight: 600; color: rgba(255,255,255,0.9); margin-top: 2px; letter-spacing: 0.5px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 314)
```
Current:  .card-expiry { font-size: 14px; color: rgba(255,255,255,0.8); margin-top: 2px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 391)
```
Current:  .feat-cell:hover { background: #252528; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 402)
```
Current:  .feat-desc { font-size: 15px; color: var(--secondary); line-height: 1.6; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 428)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] SPACE-003** (line 484)
```
Current:  padding: 14px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] TYPO-002** (line 500)
```
Current:  .txn-name { font-size: 15px; font-weight: 500; color: var(--text-light); }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 533)
```
Current:  .sec-desc { font-size: 14px; color: var(--secondary); line-height: 1.6; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 587)
```
Current:  .tier-price { font-size: 32px; font-weight: 700; color: #fbfbfd; margin-bottom: 20px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 588)
```
Current:  .tier-price small { font-size: 14px; font-weight: 400; opacity: 0.7; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] SPACE-003** (line 594)
```
Current:  padding: 6px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] TYPO-002** (line 687)
```
Current:  <div style="font-size:14px;color:var(--accent);font-weight:600;margin-bottom:24px;">+$1,240 this month</div>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 770)
```
Current:  <button style="background:var(--accent);color:#fbfbfd;border:none;padding:10px 20px;min-height:44px;display:inline-flex;align-items:center;border-radius:10px;font-size:14px;font-weight:600;cursor:pointer;font-family:var(--font);">Send Money</button>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 770)
```
Current:  <button style="background:var(--accent);color:#fbfbfd;border:none;padding:10px 20px;min-height:44px;display:inline-flex;align-items:center;border-radius:10px;font-size:14px;font-weight:600;cursor:pointer;font-family:var(--font);">Send Money</button>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 771)
```
Current:  <button style="background:rgba(0,0,0,0.06);color:var(--text-light);border:none;padding:10px 20px;min-height:44px;display:inline-flex;align-items:center;border-radius:10px;font-size:14px;font-weight:600;cursor:pointer;font-family:var(--font);">Add Funds</button>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[LOW] SPACE-002** (line 125)
```
Current:  padding: 6px 16px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 244)
```
Current:  padding: 28px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 272)
```
Current:  border-radius: 5px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] TYPO-003** (line 420)
```
Current:  font-size: 52px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] CORNER-003** (line 454)
```
Current:  border-radius: 6px 6px 0 0;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] CORNER-003** (line 468)
```
Current:  border-radius: 6px 6px 0 0;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 484)
```
Current:  padding: 14px 0;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] ANIM-002** (line 580)
```
Current:  transition: left 600ms;
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] TYPO-003** (line 587)
```
Current:  .tier-price { font-size: 32px; font-weight: 700; color: #fbfbfd; margin-bottom: 20px; }
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 594)
```
Current:  padding: 6px 0;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 641)
```
Current:  <li><a href="#">Personal</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 642)
```
Current:  <li><a href="#">Business</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 643)
```
Current:  <li><a href="#">Cards</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 644)
```
Current:  <li><a href="#">Security</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 646)
```
Current:  <button class="nav-cta">Open Account</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 655)
```
Current:  <button class="btn-accent">Open Free Account</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 656)
```
Current:  <button class="btn-primary">View Pricing</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 770)
```
Current:  <button style="background:var(--accent);color:#fbfbfd;border:none;padding:10px 20px;min-height:44px;display:inline-flex;align-items:center;border-radius:10px;font-size:14px;font-weight:600;cursor:pointer;font-family:var(--font);">Send Money</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 771)
```
Current:  <button style="background:rgba(0,0,0,0.06);color:var(--text-light);border:none;padding:10px 20px;min-height:44px;display:inline-flex;align-items:center;border-radius:10px;font-size:14px;font-weight:600;cursor:pointer;font-family:var(--font);">Add Funds</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 961)
```
Current:  <button class="btn-accent">Open Free Account</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] ANIM-002** (line 1111)
```
Current:  card.style.transition = 'transform 600ms cubic-bezier(0.25, 0.1, 0.25, 1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

### /Users/christopherarias/projects/onemore/showcase/demos/food-delivery.html

**[CRITICAL] TOUCH-001** (line 122)
```
Current:  width: 40px; height: 40px; background: rgba(255,149,0,0.12); border-radius: 12px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 307)
```
Current:  *, .animate-ready { animation: none !important; transition: none !important; transform: none !important; opacity: 1 !important; }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] TYPO-002** (line 59)
```
Current:  .nav-links a { font-size: 14px; color: var(--text-secondary); text-decoration: none; transition: color 0.2s; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 62)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 64)
```
Current:  border-radius: var(--btn-radius); font-size: 14px; font-weight: 600;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 100)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 131)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 133)
```
Current:  border-radius: 12px; font-size: 15px; font-weight: 600;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 150)
```
Current:  font-size: 22px; font-weight: 700; color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 198)
```
Current:  background: rgba(0,0,0,0.65); color: #fbfbfd; font-size: 12px; font-weight: 600;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 203)
```
Current:  background: var(--accent); color: #fbfbfd; font-size: 11px; font-weight: 700;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 215)
```
Current:  .free-delivery { font-size: 13px; font-weight: 600; color: #34C759; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 219)
```
Current:  @media (prefers-color-scheme: dark) { .how-section { background: #0a0a0c; } }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 220)
```
Current:  .how-section .section-headline { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 222)
```
Current:  .how-section .section-sub { color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 242)
```
Current:  font-size: 26px; font-weight: 700; color: #fbfbfd; margin: 0 auto 24px;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 245)
```
Current:  .step-item h3 { font-size: 19px; font-weight: 600; color: #f5f5f7; margin-bottom: 10px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 246)
```
Current:  .step-item p { font-size: 15px; color: #86868b; line-height: 1.6; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 246)
```
Current:  .step-item p { font-size: 15px; color: #86868b; line-height: 1.6; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 263)
```
Current:  .dish-name { font-size: 15px; font-weight: 600; margin-bottom: 4px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 266)
```
Current:  .dish-price { font-size: 15px; font-weight: 700; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 268)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 274)
```
Current:  .add-btn:hover { transform: scale(1.1); background: #e68900; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 276)
```
Current:  .add-btn.added { background: #34C759; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 283)
```
Current:  .app-section h2 { font-size: clamp(36px,5vw,56px); font-weight: 700; letter-spacing: -1.5px; color: #fbfbfd; margin-bottom: 16px; opacity: 0; transform: translateY(30px); }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 288)
```
Current:  background: rgba(0,0,0,0.25); color: #fbfbfd; border: 1.5px solid rgba(255,255,255,0.4);
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 298)
```
Current:  background: #1d1d1f; color: #86868b; text-align: center;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 470)
```
Current:  <h2 class="section-headline animate-ready" style="color: #f5f5f7;">From Craving to Doorstep</h2>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[LOW] SPACE-002** (line 80)
```
Current:  color: var(--accent); padding: 6px 14px; border-radius: 100px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 101)
```
Current:  padding: 14px 28px; border-radius: var(--btn-radius); font-size: 17px; font-weight: 600;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 108)
```
Current:  padding: 14px 28px; border-radius: var(--btn-radius); font-size: 17px; font-weight: 500;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 117)
```
Current:  border-radius: 18px; padding: 16px 20px; margin-bottom: 48px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 132)
```
Current:  padding: 10px 22px; min-height: 44px; display: inline-flex; align-items: center;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 194)
```
Current:  font-size: 52px; position: relative;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 206)
```
Current:  .restaurant-body { padding: 18px 20px; }
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 242)
```
Current:  font-size: 26px; font-weight: 700; color: #fbfbfd; margin: 0 auto 24px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 261)
```
Current:  .dish-thumb { height: 140px; display: flex; align-items: center; justify-content: center; font-size: 44px; }
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 262)
```
Current:  .dish-body { padding: 14px 16px; }
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 269)
```
Current:  width: 44px; height: 44px; border-radius: 14px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] CORNER-003** (line 289)
```
Current:  padding: 12px 24px; border-radius: 14px; cursor: pointer;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] TOUCH-002** (line 316)
```
Current:  <li><a href="#">Restaurants</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 317)
```
Current:  <li><a href="#">Groceries</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 318)
```
Current:  <li><a href="#">Deals</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 319)
```
Current:  <li><a href="#">Track Order</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 321)
```
Current:  <button class="nav-cta">Order Now</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 333)
```
Current:  <button class="btn-primary">Order Now</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 334)
```
Current:  <button class="btn-ghost">See Restaurants</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 341)
```
Current:  <button class="search-btn">Find Food</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TYPO-003** (line 382)
```
Current:  <span style="font-size: 52px;">&#127829;</span>
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 403)
```
Current:  <span style="font-size: 52px;">&#127843;</span>
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 423)
```
Current:  <span style="font-size: 52px;">&#127828;</span>
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 444)
```
Current:  <span style="font-size: 52px;">&#127798;</span>
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TOUCH-002** (line 509)
```
Current:  <button class="add-btn" onclick="addToCart(this)">+</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 520)
```
Current:  <button class="add-btn" onclick="addToCart(this)">+</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 531)
```
Current:  <button class="add-btn" onclick="addToCart(this)">+</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 542)
```
Current:  <button class="add-btn" onclick="addToCart(this)">+</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 553)
```
Current:  <button class="add-btn" onclick="addToCart(this)">+</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 564)
```
Current:  <button class="add-btn" onclick="addToCart(this)">+</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 578)
```
Current:  <button class="app-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 585)
```
Current:  <button class="app-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] ANIM-002** (line 635)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 649)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

### /Users/christopherarias/projects/onemore/showcase/demos/health-fitness.html

**[CRITICAL] TOUCH-001** (line 275)
```
Current:  height: 12px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 370)
```
Current:  .metric-icon svg { width: 24px; height: 24px; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 389)
```
Current:  height: 40px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 523)
```
Current:  height: 28px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 653)
```
Current:  height: 40px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 819)
```
Current:  <div class="sleep-wave-bar" style="height:12px;animation-delay:0s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 820)
```
Current:  <div class="sleep-wave-bar" style="height:28px;animation-delay:0.1s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 821)
```
Current:  <div class="sleep-wave-bar" style="height:20px;animation-delay:0.2s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 822)
```
Current:  <div class="sleep-wave-bar" style="height:35px;animation-delay:0.3s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 823)
```
Current:  <div class="sleep-wave-bar" style="height:18px;animation-delay:0.4s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 824)
```
Current:  <div class="sleep-wave-bar" style="height:38px;animation-delay:0.5s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 825)
```
Current:  <div class="sleep-wave-bar" style="height:22px;animation-delay:0.6s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 826)
```
Current:  <div class="sleep-wave-bar" style="height:30px;animation-delay:0.7s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 827)
```
Current:  <div class="sleep-wave-bar" style="height:15px;animation-delay:0.8s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 828)
```
Current:  <div class="sleep-wave-bar" style="height:25px;animation-delay:0.9s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 829)
```
Current:  <div class="sleep-wave-bar" style="height:32px;animation-delay:1.0s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 830)
```
Current:  <div class="sleep-wave-bar" style="height:40px;animation-delay:1.1s;"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 397)
```
Current:  animation: heartbeat-scroll 2s linear infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 400)
```
Current:  @keyframes heartbeat-scroll {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 631)
```
Current:  animation: fadeSlideIn 600ms cubic-bezier(0.25, 0.1, 0.25, 1) forwards;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 634)
```
Current:  @keyframes fadeSlideIn {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] CORNER-001** (line 658)
```
Current:  border-radius: 2px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] ANIM-003** (line 660)
```
Current:  animation: wavePulse 1.5s cubic-bezier(0.25, 0.1, 0.25, 1) infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 663)
```
Current:  @keyframes wavePulse {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] COLOR-003** (line 78)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 173)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-001** (line 193)
```
Current:  padding: 15px 32px;
Fix:      Align to 4pt grid: use 4/8/12/16/20/24/32/48 values
Reason:   Odd spacing value — not aligned to 4pt grid
```

**[MEDIUM] ANIM-001** (line 397)
```
Current:  animation: heartbeat-scroll 2s linear infinite;
Fix:      Use cubic-bezier(0.25, 0.1, 0.25, 1) or spring animations
Reason:   Non-Apple easing curve — avoid ease-in-out and linear
```

**[MEDIUM] COLOR-003** (line 507)
```
Current:  background: #1c1c1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 524)
```
Current:  background: #1c1c1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 532)
```
Current:  background: #1d1d1f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 608)
```
Current:  background: #1c1c1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 659)
```
Current:  background: #0CD4F5;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 670)
```
Current:  color: #30D158;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 733)
```
Current:  <div style="font-size:13px;font-weight:700;color:#f5f5f7;">Activity</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 740)
```
Current:  <div class="ring-dot" style="background:#FF2D55;"></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 743)
```
Current:  <div class="ring-stat-val" style="color:#FF2D55;"><span class="counter" data-target="680">0</span> <small style="font-size:14px;">cal</small></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 743)
```
Current:  <div class="ring-stat-val" style="color:#FF2D55;"><span class="counter" data-target="680">0</span> <small style="font-size:14px;">cal</small></div>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 747)
```
Current:  <div class="ring-dot" style="background:#30D158;"></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 750)
```
Current:  <div class="ring-stat-val" style="color:#30D158;"><span class="counter" data-target="42">0</span> <small style="font-size:14px;">min</small></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 750)
```
Current:  <div class="ring-stat-val" style="color:#30D158;"><span class="counter" data-target="42">0</span> <small style="font-size:14px;">min</small></div>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 754)
```
Current:  <div class="ring-dot" style="background:#0CD4F5;"></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 757)
```
Current:  <div class="ring-stat-val" style="color:#0CD4F5;"><span class="counter" data-target="10">0</span> <small style="font-size:14px;">hrs</small></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 757)
```
Current:  <div class="ring-stat-val" style="color:#0CD4F5;"><span class="counter" data-target="10">0</span> <small style="font-size:14px;">hrs</small></div>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 779)
```
Current:  <div class="metric-value" style="color:#FF2D55;"><span class="counter" data-target="72">0</span></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 797)
```
Current:  <div class="metric-value" style="color:#30D158;"><span class="counter" data-target="8432">0</span></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 816)
```
Current:  <div class="metric-value" style="color:#0CD4F5;">7<small style="font-size:20px;">h</small> 42<small style="font-size:20px;">m</small></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 904)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Get VitalFlow Free</button>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 929)
```
Current:  <div class="phone-stat-value" style="color:#FF2D55;">72 BPM</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 933)
```
Current:  <div class="phone-stat-value" style="color:#30D158;">8,432</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 939)
```
Current:  <div class="phone-stat-value" style="color:#0CD4F5;">7h 42m</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 943)
```
Current:  <div class="phone-stat-value" style="color:#FF9F0A;">680 cal</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[LOW] SPACE-002** (line 125)
```
Current:  padding: 6px 16px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 193)
```
Current:  padding: 15px 32px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 373)
```
Current:  font-size: 36px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 468)
```
Current:  font-size: 32px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] CORNER-003** (line 565)
```
Current:  border-radius: 14px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] TOUCH-002** (line 688)
```
Current:  <li><a href="#">Health</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 689)
```
Current:  <li><a href="#">Fitness</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 690)
```
Current:  <li><a href="#">Nutrition</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 691)
```
Current:  <li><a href="#">Sleep</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 693)
```
Current:  <button class="nav-cta">Download Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 705)
```
Current:  <button class="btn-primary">Download on the App Store</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 706)
```
Current:  <button class="btn-secondary">Watch the Demo</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 904)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Get VitalFlow Free</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 904)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Get VitalFlow Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 963)
```
Current:  <a class="store-badge" href="#">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 972)
```
Current:  <a class="store-badge" href="#">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

### /Users/christopherarias/projects/onemore/showcase/demos/logo-design.html

**[CRITICAL] TOUCH-001** (line 223)
```
Current:  height: 36px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 67)
```
Current:  animation: fadeUp 0.6s 0.2s both;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 71)
```
Current:  animation: fadeUp 0.8s 0.3s both;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 79)
```
Current:  animation: fadeUp 0.8s 0.5s both;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 91)
```
Current:  animation: fadeUp 0.8s 0.7s both;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 280)
```
Current:  @keyframes fadeUp {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] COLOR-003** (line 138)
```
Current:  .v-card.dark { background: #1d1d1f; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 144)
```
Current:  .v-card.light .wm { color: #1d1d1f; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 145)
```
Current:  .v-card.dark .wm { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 181)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 228)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 232)
```
Current:  .review-name { font-size: 15px; font-weight: 600; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 235)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[LOW] SPACE-002** (line 59)
```
Current:  padding: 6px 16px 6px 8px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 251)
```
Current:  font-size: 120px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TOUCH-002** (line 454)
```
Current:  <p>Designed with <a href="https://github.com/JubaKitiashvili/onemore" target="_blank" rel="noopener">OneMore</a> — Apple HIG Design Intelligence</p>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

### /Users/christopherarias/projects/onemore/showcase/demos/media-entertainment.html

**[CRITICAL] TOUCH-001** (line 179)
```
Current:  width: 28px; height: 28px; border-radius: 50%;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 186)
```
Current:  width: 10px; height: 10px; border-radius: 50%; background: rgba(255,255,255,0.3);
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 403)
```
Current:  content: ''; width: 18px; height: 18px; border-radius: 50%; flex-shrink: 0;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 426)
```
Current:  @keyframes fadeSlideIn {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 432)
```
Current:  @keyframes progressGrow {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] COLOR-003** (line 50)
```
Current:  background: var(--accent); color: #fbfbfd; border: none;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 99)
```
Current:  background: var(--accent); color: #fbfbfd; border: none;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-001** (line 108)
```
Current:  padding: 15px 32px; border-radius: 12px; font-size: 17px; font-weight: 600;
Fix:      Align to 4pt grid: use 4/8/12/16/20/24/32/48 values
Reason:   Odd spacing value — not aligned to 4pt grid
```

**[MEDIUM] TYPO-002** (line 191)
```
Current:  .player-artist { font-size: 15px; color: var(--secondary); margin-bottom: 8px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] ANIM-001** (line 216)
```
Current:  transition: width 0.1s linear;
Fix:      Use cubic-bezier(0.25, 0.1, 0.25, 1) or spring animations
Reason:   Non-Apple easing curve — avoid ease-in-out and linear
```

**[MEDIUM] COLOR-003** (line 239)
```
Current:  background: var(--accent); color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 271)
```
Current:  font-size: 14px; font-weight: 500; cursor: pointer;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 276)
```
Current:  .cat-pill:hover, .cat-pill.active { background: var(--accent); border-color: var(--accent); color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 319)
```
Current:  .album-title { font-size: 14px; font-weight: 700; color: var(--text-light); margin-bottom: 2px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 338)
```
Current:  .feat-block:hover { background: #252528; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 342)
```
Current:  .feat-desc { font-size: 15px; color: var(--secondary); line-height: 1.7; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 367)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 374)
```
Current:  background: var(--accent-pink); color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 379)
```
Current:  .pricing-tier { font-size: 14px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 8px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 389)
```
Current:  .pricing-period { font-size: 14px; margin-bottom: 28px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 395)
```
Current:  padding: 8px 0; font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] SPACE-003** (line 395)
```
Current:  padding: 8px 0; font-size: 15px;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] COLOR-003** (line 417)
```
Current:  background: var(--text-light); color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 421)
```
Current:  background: #fbfbfd; color: var(--accent);
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 469)
```
Current:  <div style="font-size:12px;font-weight:700;color:#fbfbfd;opacity:0.9;">Neon Dreams</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 475)
```
Current:  <div style="font-size:12px;font-weight:700;color:#fbfbfd;opacity:0.9;">Midnight Low</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 481)
```
Current:  <div style="font-size:12px;font-weight:700;color:#fbfbfd;opacity:0.9;">Sunrise Drive</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 487)
```
Current:  <div style="font-size:12px;font-weight:700;color:#fbfbfd;opacity:0.9;">Forest Rain</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] ANIM-001** (line 862)
```
Current:  bar.style.transition = 'width 0.5s linear';
Fix:      Use cubic-bezier(0.25, 0.1, 0.25, 1) or spring animations
Reason:   Non-Apple easing curve — avoid ease-in-out and linear
```

**[LOW] SPACE-002** (line 75)
```
Current:  border: 1px solid rgba(175,82,222,0.25); padding: 6px 16px; border-radius: 980px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 108)
```
Current:  padding: 15px 32px; border-radius: 12px; font-size: 17px; font-weight: 600;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 196)
```
Current:  padding: 3px 10px; border-radius: 980px; font-size: 11px; font-weight: 600; color: var(--accent);
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] ANIM-002** (line 216)
```
Current:  transition: width 0.1s linear;
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] SPACE-002** (line 268)
```
Current:  padding: 10px 20px; min-height: 44px; display: inline-flex; align-items: center;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 318)
```
Current:  .album-body { padding: 14px; }
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 340)
```
Current:  .feat-accent { width: 48px; height: 48px; border-radius: 14px; display: flex; align-items: center; justify-content: center; margin-bottom: 20px; }
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 411)
```
Current:  width: 100%; padding: 14px; border-radius: 12px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 448)
```
Current:  <li><a href="#">Listen Now</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 449)
```
Current:  <li><a href="#">Browse</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 450)
```
Current:  <li><a href="#">Radio</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 451)
```
Current:  <li><a href="#">Plans</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 453)
```
Current:  <button class="nav-cta">Try Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 462)
```
Current:  <button class="btn-primary">Try 3 Months Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 463)
```
Current:  <button class="btn-secondary">Hear the Difference</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 468)
```
Current:  <div style="position:absolute;inset:0;display:flex;flex-direction:column;justify-content:flex-end;padding:14px;">
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 474)
```
Current:  <div style="position:absolute;inset:0;display:flex;flex-direction:column;justify-content:flex-end;padding:14px;">
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 480)
```
Current:  <div style="position:absolute;inset:0;display:flex;flex-direction:column;justify-content:flex-end;padding:14px;">
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 486)
```
Current:  <div style="position:absolute;inset:0;display:flex;flex-direction:column;justify-content:flex-end;padding:14px;">
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 517)
```
Current:  <button class="player-heart">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 535)
```
Current:  <button class="ctrl-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 541)
```
Current:  <button class="ctrl-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 546)
```
Current:  <button class="ctrl-btn play-btn" id="play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 551)
```
Current:  <button class="ctrl-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 556)
```
Current:  <button class="ctrl-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 586)
```
Current:  <button class="cat-pill active">All</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 587)
```
Current:  <button class="cat-pill">Pop</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 588)
```
Current:  <button class="cat-pill">Hip-Hop</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 589)
```
Current:  <button class="cat-pill">Electronic</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 590)
```
Current:  <button class="cat-pill">Jazz</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 591)
```
Current:  <button class="cat-pill">Indie</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 592)
```
Current:  <button class="cat-pill">Classical</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 593)
```
Current:  <button class="cat-pill">R&amp;B</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 599)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 607)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 615)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 623)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 631)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 639)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 647)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 655)
```
Current:  <button class="album-play-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 733)
```
Current:  <button class="pricing-btn">Start Free Trial</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 748)
```
Current:  <button class="pricing-btn">Try 3 Months Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 762)
```
Current:  <button class="pricing-btn">Start Free Trial</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] ANIM-002** (line 862)
```
Current:  bar.style.transition = 'width 0.5s linear';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

### /Users/christopherarias/projects/onemore/showcase/demos/productivity.html

**[CRITICAL] TOUCH-001** (line 136)
```
Current:  width: 22px; height: 22px; border-radius: 50%; border: 2px solid #d2d2d7;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 211)
```
Current:  width: 24px; height: 24px; border-radius: 50%; background: var(--accent);
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 254)
```
Current:  .int-icon { width: 36px; height: 36px; border-radius: 10px; display: flex; align-items: center; justify-content: center; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 284)
```
Current:  .check-icon { width: 18px; height: 18px; flex-shrink: 0; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 318)
```
Current:  *, .animate-ready { animation: none !important; transition: none !important; transform: none !important; opacity: 1 !important; }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] TYPO-002** (line 59)
```
Current:  .nav-links a { font-size: 14px; color: var(--text-secondary); text-decoration: none; transition: color 0.2s; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 62)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 64)
```
Current:  border-radius: var(--btn-radius); font-size: 14px; font-weight: 500;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 102)
```
Current:  background: var(--accent); color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 125)
```
Current:  .mockup-title { font-size: 15px; font-weight: 600; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] SPACE-003** (line 131)
```
Current:  display: flex; align-items: center; gap: 14px; padding: 12px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] TYPO-002** (line 146)
```
Current:  .task-text { font-size: 14px; flex: 1; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 149)
```
Current:  .p-high { background: #FF3B30; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 150)
```
Current:  .p-med { background: #FF9500; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 151)
```
Current:  .p-low { background: #34C759; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 173)
```
Current:  @media (prefers-color-scheme: dark) { .kanban-section { background: #0a0a0c; } }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 174)
```
Current:  .kanban-section .section-headline { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 176)
```
Current:  .kanban-section .section-sub { color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 191)
```
Current:  .kanban-col-title { font-size: 13px; font-weight: 600; color: #86868b; text-transform: uppercase; letter-spacing: 0.05em; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 193)
```
Current:  background: rgba(255,255,255,0.08); color: #86868b;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 207)
```
Current:  .kcard-title { font-size: 14px; font-weight: 500; color: #f5f5f7; margin-bottom: 10px; line-height: 1.4; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 207)
```
Current:  .kcard-title { font-size: 14px; font-weight: 500; color: #f5f5f7; margin-bottom: 10px; line-height: 1.4; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 209)
```
Current:  .kcard-due { font-size: 12px; color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 213)
```
Current:  font-size: 11px; font-weight: 700; color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 234)
```
Current:  .feature-card p { font-size: 15px; color: var(--text-secondary); line-height: 1.6; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 238)
```
Current:  @media (prefers-color-scheme: dark) { .integrations-section { background: #0a0a0c; } }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 239)
```
Current:  .integrations-section .section-headline { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 241)
```
Current:  .integrations-section .section-sub { color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 255)
```
Current:  .int-name { font-size: 15px; font-weight: 600; color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 255)
```
Current:  .int-name { font-size: 15px; font-weight: 600; color: #f5f5f7; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 256)
```
Current:  .int-type { font-size: 12px; color: #86868b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 277)
```
Current:  .pricing-card.featured .plan-price { color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 279)
```
Current:  .plan-period { font-size: 14px; color: var(--text-secondary); margin-bottom: 28px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 282)
```
Current:  .plan-features li { font-size: 15px; display: flex; align-items: center; gap: 10px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 283)
```
Current:  .pricing-card.featured .plan-features li { color: #fbfbfd; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 288)
```
Current:  .cta-section h2 { font-size: clamp(36px, 5vw, 56px); font-weight: 700; letter-spacing: -1.5px; color: #fbfbfd; margin-bottom: 20px; opacity: 0; transform: translateY(30px); }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 292)
```
Current:  background: #fbfbfd; color: var(--accent); border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 298)
```
Current:  background: transparent; color: #fbfbfd; border: 1.5px solid rgba(255,255,255,0.6); cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 305)
```
Current:  background: #1d1d1f; color: #86868b; text-align: center;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 309)
```
Current:  .footer-brand { font-size: 18px; font-weight: 700; color: #007AFF; margin-bottom: 8px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 392)
```
Current:  <h2 class="section-headline animate-ready" style="color: #f5f5f7;">Your Work, Visualized</h2>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 402)
```
Current:  <div class="kcard-tag" style="background: rgba(255,149,0,0.15); color: #FF9500;">Design</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 407)
```
Current:  <div class="kcard-tag" style="background: rgba(175,82,222,0.15); color: #AF52DE;">Research</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 409)
```
Current:  <div class="kcard-meta"><span class="kcard-due">Apr 2</span><div class="kcard-avatar" style="background: #FF9500;">M</div></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 412)
```
Current:  <div class="kcard-tag" style="background: rgba(0,122,255,0.15); color: #007AFF;">Dev</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 414)
```
Current:  <div class="kcard-meta"><span class="kcard-due">Apr 5</span><div class="kcard-avatar" style="background: #34C759;">J</div></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 423)
```
Current:  <div class="kcard-tag" style="background: rgba(0,122,255,0.15); color: #007AFF;">Dev</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 428)
```
Current:  <div class="kcard-tag" style="background: rgba(255,59,48,0.15); color: #FF3B30;">Urgent</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 430)
```
Current:  <div class="kcard-meta"><span class="kcard-due" style="color: #FF3B30;">Today</span><div class="kcard-avatar" style="background: #FF3B30;">S</div></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 433)
```
Current:  <div class="kcard-tag" style="background: rgba(52,199,89,0.15); color: #34C759;">Content</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 435)
```
Current:  <div class="kcard-meta"><span class="kcard-due">Mar 26</span><div class="kcard-avatar" style="background: #AF52DE;">L</div></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 444)
```
Current:  <div class="kcard-tag" style="background: rgba(52,199,89,0.12); color: #34C759;">Completed</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 445)
```
Current:  <div class="kcard-title" style="text-decoration: line-through; color: #86868b;">Mobile app v2.3 release</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 446)
```
Current:  <div class="kcard-meta"><span class="kcard-due">Mar 20</span><div class="kcard-avatar" style="background: #34C759;">R</div></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 449)
```
Current:  <div class="kcard-tag" style="background: rgba(52,199,89,0.12); color: #34C759;">Completed</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 450)
```
Current:  <div class="kcard-title" style="text-decoration: line-through; color: #86868b;">User interview synthesis</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 454)
```
Current:  <div class="kcard-tag" style="background: rgba(52,199,89,0.12); color: #34C759;">Completed</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 455)
```
Current:  <div class="kcard-title" style="text-decoration: line-through; color: #86868b;">Q1 retrospective doc</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 456)
```
Current:  <div class="kcard-meta"><span class="kcard-due">Mar 15</span><div class="kcard-avatar" style="background: #AF52DE;">M</div></div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 507)
```
Current:  <h2 class="section-headline animate-ready" style="color: #f5f5f7;">Works With Your Stack</h2>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 580)
```
Current:  <button class="btn-white" style="background: #fbfbfd; color: #007AFF; border: none; cursor: pointer; padding: 14px 26px; border-radius: 12px; font-size: 16px; font-weight: 600; width: 100%; transition: transform 0.2s;" onmouseover="this.style.transform='translateY(-2px)'" onmouseout="this.style.transform='none'">Start Pro Trial</button>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[LOW] SPACE-002** (line 84)
```
Current:  color: var(--accent); padding: 6px 14px; border-radius: 100px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 103)
```
Current:  padding: 14px 26px; border-radius: var(--btn-radius); font-size: 16px; font-weight: 500;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 110)
```
Current:  padding: 14px 26px; border-radius: var(--btn-radius); font-size: 16px; font-weight: 500;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 118)
```
Current:  border-radius: 20px; padding: 28px; box-shadow: 0 24px 80px rgba(0,0,0,0.12);
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 128)
```
Current:  font-size: 12px; font-weight: 600; padding: 3px 10px; border-radius: 100px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 185)
```
Current:  border-radius: 18px; padding: 20px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 198)
```
Current:  border-radius: 12px; padding: 14px; margin-bottom: 10px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 229)
```
Current:  width: 52px; height: 52px; border-radius: 14px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 293)
```
Current:  padding: 14px 28px; border-radius: var(--btn-radius); font-size: 16px; font-weight: 600;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 299)
```
Current:  padding: 14px 28px; border-radius: var(--btn-radius); font-size: 16px; font-weight: 500;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] ANIM-002** (line 314)
```
Current:  transition: opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] TOUCH-002** (line 327)
```
Current:  <li><a href="#">Features</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 328)
```
Current:  <li><a href="#">Boards</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 329)
```
Current:  <li><a href="#">Integrations</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 330)
```
Current:  <li><a href="#">Pricing</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 332)
```
Current:  <button class="nav-cta">Get Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 345)
```
Current:  <button class="btn-primary">Start for Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 346)
```
Current:  <button class="btn-ghost">See How It Works</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 567)
```
Current:  <button class="btn-ghost" style="width: 100%;">Get Started</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 580)
```
Current:  <button class="btn-white" style="background: #fbfbfd; color: #007AFF; border: none; cursor: pointer; padding: 14px 26px; border-radius: 12px; font-size: 16px; font-weight: 600; width: 100%; transition: transform 0.2s;" onmouseover="this.style.transform='translateY(-2px)'" onmouseout="this.style.transform='none'">Start Pro Trial</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 591)
```
Current:  <button class="btn-white">Download for Mac</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 592)
```
Current:  <button class="btn-outline-white">Get iOS App</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] ANIM-002** (line 630)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 644)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

### /Users/christopherarias/projects/onemore/showcase/demos/saas-dashboard.html

**[CRITICAL] TOUCH-001** (line 495)
```
Current:  height: 12px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 560)
```
Current:  height: 16px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 1044)
```
Current:  height: 18px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 1482)
```
Current:  <svg viewBox="0 0 120 30" width="100%" preserveAspectRatio="none" style="height:30px">
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 1494)
```
Current:  <svg viewBox="0 0 120 30" width="100%" preserveAspectRatio="none" style="height:30px">
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 1506)
```
Current:  <svg viewBox="0 0 120 30" width="100%" preserveAspectRatio="none" style="height:30px">
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 1518)
```
Current:  <svg viewBox="0 0 120 30" width="100%" preserveAspectRatio="none" style="height:30px">
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 99)
```
Current:  animation: iconPulse 3s cubic-bezier(0.25, 0.1, 0.25, 1) infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 102)
```
Current:  @keyframes iconPulse {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 131)
```
Current:  animation: glow-rotate 4s cubic-bezier(0.25, 0.1, 0.25, 1) infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 135)
```
Current:  @keyframes glow-rotate {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 185)
```
Current:  animation: none;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 196)
```
Current:  animation: none;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] CORNER-001** (line 507)
```
Current:  border-radius: 6px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 774)
```
Current:  border-radius: 6px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 794)
```
Current:  border-radius: 6px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 843)
```
Current:  border-radius: 4px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 892)
```
Current:  border-radius: 4px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[HIGH] CORNER-001** (line 933)
```
Current:  border-radius: 2px;
Fix:      Use borderRadius: 12 for buttons, 10/16/24 for other elements
Reason:   Button border-radius too small — Apple buttons use 12px
```

**[MEDIUM] TYPO-002** (line 251)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] SPACE-001** (line 266)
```
Current:  padding: 7px 18px;
Fix:      Align to 4pt grid: use 4/8/12/16/20/24/32/48 values
Reason:   Odd spacing value — not aligned to 4pt grid
```

**[MEDIUM] COLOR-003** (line 268)
```
Current:  color: #fbfbfd !important;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 270)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 306)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 345)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 485)
```
Current:  background: #1c1c1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 499)
```
Current:  .traffic-light.red { background: #ff5f57; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 500)
```
Current:  .traffic-light.yellow { background: #febc2e; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 501)
```
Current:  .traffic-light.green { background: #28c840; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-001** (line 508)
```
Current:  padding: 5px 14px;
Fix:      Align to 4pt grid: use 4/8/12/16/20/24/32/48 values
Reason:   Odd spacing value — not aligned to 4pt grid
```

**[MEDIUM] COLOR-003** (line 514)
```
Current:  background: #111113;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 525)
```
Current:  background: #0d0d0f;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 534)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 555)
```
Current:  color: #a5a4f3;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 612)
```
Current:  .kpi-change.up { color: #32d74b; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 613)
```
Current:  .kpi-change.down { color: #ff453a; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 633)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 671)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 727)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 784)
```
Current:  color: #a5a4f3;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 848)
```
Current:  color: #32d74b;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 853)
```
Current:  color: #ff453a;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-003** (line 912)
```
Current:  padding: 8px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] SPACE-003** (line 922)
```
Current:  padding: 10px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] COLOR-003** (line 985)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 1015)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 1020)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 1038)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 1055)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 1066)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 1103)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 1120)
```
Current:  font-size: 14px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 1152)
```
Current:  background: #111113;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 1158)
```
Current:  background: #111113;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 1167)
```
Current:  background: #111113;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 1170)
```
Current:  background: #1c1c1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 1186)
```
Current:  color: #a5a4f3;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[LOW] ANIM-002** (line 62)
```
Current:  transition: opacity 0.6s var(--ease),
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 111)
```
Current:  transition: transform 0.6s var(--ease), opacity 0.6s var(--ease);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 153)
```
Current:  transition: left 0.6s ease;
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] SPACE-002** (line 266)
```
Current:  padding: 7px 18px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 343)
```
Current:  padding: 14px 32px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 367)
```
Current:  padding: 14px 32px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] ANIM-002** (line 395)
```
Current:  transition: opacity 0.6s var(--ease), transform 0.6s var(--ease);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 418)
```
Current:  transition: opacity 1.2s var(--ease) 0.8s;
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 426)
```
Current:  transition: stroke-dasharray 1.5s var(--ease) 0.5s;
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 434)
```
Current:  transition: opacity 0.6s var(--ease) 1s;
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 449)
```
Current:  transition: opacity 0.5s var(--ease), transform 0.5s var(--ease);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 456)
```
Current:  transition: transform 0.8s var(--ease);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 477)
```
Current:  transition: transform 0.8s var(--ease);
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] SPACE-002** (line 487)
```
Current:  padding: 14px 18px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 507)
```
Current:  border-radius: 6px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 508)
```
Current:  padding: 5px 14px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 545)
```
Current:  padding: 10px 12px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 590)
```
Current:  padding: 18px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 600)
```
Current:  font-size: 24px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 664)
```
Current:  font-size: 36px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 773)
```
Current:  padding: 6px 14px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 774)
```
Current:  border-radius: 6px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 793)
```
Current:  padding: 6px 14px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 794)
```
Current:  border-radius: 6px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 891)
```
Current:  padding: 3px 10px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 922)
```
Current:  padding: 10px 0;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 1008)
```
Current:  font-size: 48px;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 1053)
```
Current:  padding: 14px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 1260)
```
Current:  <li><a href="#features">Features</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1261)
```
Current:  <li><a href="#dashboard">Dashboard</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1262)
```
Current:  <li><a href="#pricing">Pricing</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1263)
```
Current:  <li><a href="#cta" class="nav-cta">Start Free</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1274)
```
Current:  <button class="hero-btn-primary shimmer-btn">Start Free Trial</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1275)
```
Current:  <a href="#dashboard" class="hero-btn-secondary">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1666)
```
Current:  <button class="pricing-btn secondary">Get Started</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1700)
```
Current:  <button class="pricing-btn primary shimmer-btn">Get Started</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1732)
```
Current:  <button class="pricing-btn secondary">Contact Sales</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1741)
```
Current:  <button class="final-btn shimmer-btn">Get Started Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1750)
```
Current:  <a href="#">Privacy</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1751)
```
Current:  <a href="#">Terms</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 1752)
```
Current:  <a href="#">Status</a>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

### /Users/christopherarias/projects/onemore/showcase/demos/social-communication.html

**[CRITICAL] TOUCH-001** (line 130)
```
Current:  width: 36px; height: 36px; border-radius: 50%;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 145)
```
Current:  width: 28px; height: 28px; border-radius: 50%;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 275)
```
Current:  .feat6-icon svg { width: 22px; height: 22px; }
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 297)
```
Current:  width: 110px; height: 26px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 313)
```
Current:  width: 28px; height: 28px; border-radius: 50%;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 349)
```
Current:  width: 36px; height: 36px; border-radius: 10px;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 396)
```
Current:  width: 36px; height: 36px; border-radius: 50%;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[CRITICAL] TOUCH-001** (line 640)
```
Current:  <div style="width:24px;height:24px;border-radius:50%;background:linear-gradient(135deg,#007AFF,#5AC8FA);"></div>
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] ANIM-003** (line 215)
```
Current:  animation: typingBounce 1.2s cubic-bezier(0.25, 0.1, 0.25, 1) infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 221)
```
Current:  @keyframes typingBounce {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 407)
```
Current:  animation: voicePulse 1.5s cubic-bezier(0.25, 0.1, 0.25, 1) infinite;
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 410)
```
Current:  @keyframes voicePulse {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 444)
```
Current:  @keyframes fadeSlideIn {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[HIGH] ANIM-003** (line 449)
```
Current:  @keyframes bubbleIn {
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] COLOR-003** (line 49)
```
Current:  background: var(--accent); color: #fbfbfd; border: none;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 98)
```
Current:  background: var(--accent); color: #fbfbfd; border: none;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 115)
```
Current:  background: #1c1c1e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 133)
```
Current:  font-size: 14px; font-weight: 700; color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 133)
```
Current:  font-size: 14px; font-weight: 700; color: #fbfbfd;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 136)
```
Current:  .chat-name { font-size: 15px; font-weight: 600; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 137)
```
Current:  .chat-status { font-size: 12px; color: #30D158; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 154)
```
Current:  font-size: 15px;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 159)
```
Current:  background: #2c2c2e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 167)
```
Current:  color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 172)
```
Current:  background: #2c2c2e;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 209)
```
Current:  background: #2c2c2e; border-radius: 18px; border-bottom-left-radius: 4px;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 277)
```
Current:  .feat6-desc { font-size: 14px; color: var(--secondary); line-height: 1.6; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 288)
```
Current:  background: #1c1c1e; border-radius: 44px;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 298)
```
Current:  background: #1c1c1e; border-radius: 0 0 18px 18px; z-index: 2;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 303)
```
Current:  background: #1d1d1f; padding: 36px 12px 16px;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-001** (line 320)
```
Current:  font-size: 11px; padding: 7px 10px; border-radius: 13px;
Fix:      Align to 4pt grid: use 4/8/12/16/20/24/32/48 values
Reason:   Odd spacing value — not aligned to 4pt grid
```

**[MEDIUM] COLOR-003** (line 324)
```
Current:  .phone-bubble.recv { background: #2c2c2e; color: var(--text-dark); align-self: flex-start; border-bottom-left-radius: 3px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 325)
```
Current:  .phone-bubble.sent { background: var(--accent); color: #fbfbfd; align-self: flex-end; border-bottom-right-radius: 3px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 354)
```
Current:  .priv-title { font-size: 15px; font-weight: 700; color: var(--text-light); margin-bottom: 2px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 355)
```
Current:  .priv-desc { font-size: 14px; color: var(--secondary); line-height: 1.5; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] SPACE-003** (line 379)
```
Current:  display: flex; align-items: center; gap: 10px; padding: 8px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] TYPO-002** (line 384)
```
Current:  .channel-hash { color: var(--secondary); font-size: 15px; font-weight: 700; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 385)
```
Current:  .channel-name { font-size: 14px; color: var(--text-dark); }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 386)
```
Current:  .channel-badge { margin-left: auto; background: var(--accent); color: #fbfbfd; font-size: 10px; font-weight: 700; padding: 2px 6px; border-radius: 980px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 398)
```
Current:  font-size: 13px; font-weight: 700; color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] SPACE-003** (line 416)
```
Current:  padding: 8px 0;
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] TYPO-002** (line 418)
```
Current:  font-size: 14px; color: var(--secondary);
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 434)
```
Current:  background: #1c1c1e; border: 1px solid rgba(255,255,255,0.1); border-radius: 12px;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] ICON-001** (line 504)
```
Current:  <button class="reaction-chip">❤️ 1</button>
Fix:      Replace emoji with SF Symbols (iOS/macOS) or SVG/icon-font icons
Reason:   Emoji used as UI icon — use SF Symbols or SVG icons instead
```

**[MEDIUM] SPACE-003** (line 639)
```
Current:  <div style="display:flex;align-items:center;gap:6px;padding:8px 0;">
Fix:      Use minimum 100px (py-24 in Tailwind) vertical section padding for Apple-quality spacing
Reason:   Section padding less than 100px — Apple uses 100-120px section padding minimum
```

**[MEDIUM] COLOR-003** (line 647)
```
Current:  <div style="margin-top:auto;background:#1c1c1e;border-radius:18px;padding:8px 12px;display:flex;align-items:center;gap:8px;">
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 658)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Download on iOS</button>
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[LOW] SPACE-002** (line 74)
```
Current:  border: 1px solid rgba(0,122,255,0.25); padding: 6px 16px; border-radius: 980px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 152)
```
Current:  padding: 10px 14px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 153)
```
Current:  border-radius: 18px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] CORNER-003** (line 173)
```
Current:  border-radius: 14px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 184)
```
Current:  .link-preview-body { padding: 10px 12px; }
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 209)
```
Current:  background: #2c2c2e; border-radius: 18px; border-bottom-left-radius: 4px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 261)
```
Current:  border-radius: 20px; padding: 28px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 320)
```
Current:  font-size: 11px; padding: 7px 10px; border-radius: 13px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 320)
```
Current:  font-size: 11px; padding: 7px 10px; border-radius: 13px;
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] TOUCH-002** (line 466)
```
Current:  <li><a href="#">Features</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 467)
```
Current:  <li><a href="#">Teams</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 468)
```
Current:  <li><a href="#">Privacy</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 469)
```
Current:  <li><a href="#">Pricing</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 471)
```
Current:  <button class="nav-cta">Download App</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 480)
```
Current:  <button class="btn-primary">Download Free</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 481)
```
Current:  <button class="btn-secondary">See How It Works</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 503)
```
Current:  <button class="reaction-chip">👍 3</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 504)
```
Current:  <button class="reaction-chip">❤️ 1</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] SPACE-002** (line 641)
```
Current:  <div class="typing-indicator" style="padding:6px 10px;">
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] CORNER-003** (line 647)
```
Current:  <div style="margin-top:auto;background:#1c1c1e;border-radius:18px;padding:8px 12px;display:flex;align-items:center;gap:8px;">
Fix:      Use Apple corner radii: 10px (small), 16px (medium), 24px (large)
Reason:   Generic border-radius on cards — use Apple-standard radii
```

**[LOW] SPACE-002** (line 658)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Download on iOS</button>
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 658)
```
Current:  <button class="btn-primary" style="font-size:15px;padding:14px 28px;">Download on iOS</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 797)
```
Current:  <a class="store-badge" href="#">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 804)
```
Current:  <a class="store-badge" href="#">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

### /Users/christopherarias/projects/onemore/showcase/demos/travel.html

**[CRITICAL] TOUCH-001** (line 204)
```
Current:  width: 36px; height: 36px; border-radius: 50%;
Fix:      Set minimum height to 44px for all interactive elements
Reason:   Touch target too small — minimum 44px per Apple HIG
```

**[HIGH] COLOR-002** (line 89)
```
Current:  background: linear-gradient(135deg, #fff 0%, var(--accent) 60%, var(--accent-deep) 100%);
Fix:      Use '#fbfbfd' on web, Color.systemBackground in SwiftUI
Reason:   Pure white background — Apple uses slightly warm off-white
```

**[HIGH] ANIM-003** (line 307)
```
Current:  *, .animate-ready { animation: none !important; transition: none !important; transform: none !important; opacity: 1 !important; }
Fix:      Add @media (prefers-reduced-motion: reduce) to disable or simplify animations
Reason:   Missing prefers-reduced-motion — must respect user accessibility settings
```

**[MEDIUM] TYPO-002** (line 52)
```
Current:  .nav-links a { font-size: 14px; color: rgba(255,255,255,0.6); text-decoration: none; transition: color 0.2s; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 53)
```
Current:  .nav-links a:hover { color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 55)
```
Current:  background: var(--accent); color: #1d1d1f; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 57)
```
Current:  border-radius: var(--btn-radius); font-size: 14px; font-weight: 700;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 117)
```
Current:  font-family: inherit; font-size: 15px; color: #fbfbfd; width: 100%;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 117)
```
Current:  font-family: inherit; font-size: 15px; color: #fbfbfd; width: 100%;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 122)
```
Current:  color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 148)
```
Current:  .destinations-section { background: #0a0a0f; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 172)
```
Current:  background: rgba(0,0,0,0.4); color: #fbfbfd; font-size: 13px; font-weight: 600;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 176)
```
Current:  .dest-city { font-size: 24px; font-weight: 700; color: #fbfbfd; margin-bottom: 2px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 177)
```
Current:  .dest-country { font-size: 14px; color: rgba(255,255,255,0.7); margin-bottom: 12px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] TYPO-002** (line 178)
```
Current:  .dest-price { font-size: 15px; font-weight: 600; color: var(--accent); }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 182)
```
Current:  .experiences-section { background: #050508; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 206)
```
Current:  font-size: 15px; font-weight: 700; color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 206)
```
Current:  font-size: 15px; font-weight: 700; color: #fbfbfd;
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 211)
```
Current:  .exp-title { font-size: 20px; font-weight: 600; color: #f5f5f7; margin-bottom: 8px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 212)
```
Current:  .exp-desc { font-size: 14px; color: rgba(255,255,255,0.5); line-height: 1.6; margin-bottom: 18px; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 215)
```
Current:  .exp-price { font-size: 19px; font-weight: 700; color: #f5f5f7; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 219)
```
Current:  .trust-section { background: #0a0a0f; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 232)
```
Current:  .trust-item h3 { font-size: 19px; font-weight: 600; color: #f5f5f7; margin-bottom: 10px; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 233)
```
Current:  .trust-item p { font-size: 15px; color: rgba(255,255,255,0.45); line-height: 1.6; }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 236)
```
Current:  .testimonials-section { background: #050508; }
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 255)
```
Current:  font-size: 18px; font-weight: 700; color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] TYPO-002** (line 257)
```
Current:  .t-name { font-size: 15px; font-weight: 600; color: rgba(255,255,255,0.9); }
Fix:      Apple body text is 17px (iOS) or 13px (macOS). Use 17px for mobile, 13px for desktop
Reason:   Body text size not aligned with Apple type scale
```

**[MEDIUM] COLOR-003** (line 278)
```
Current:  color: #fbfbfd; border: none; cursor: pointer;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 285)
```
Current:  background: rgba(255,255,255,0.08); color: #fbfbfd;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 294)
```
Current:  background: #1d1d1f; color: rgba(255,255,255,0.3); text-align: center;
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 371)
```
Current:  <div class="dest-rating"><span style="color:#FF9500;">&#9733;</span> 4.9</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 381)
```
Current:  <div class="dest-rating"><span style="color:#FF9500;">&#9733;</span> 4.8</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 391)
```
Current:  <div class="dest-rating"><span style="color:#FF9500;">&#9733;</span> 4.9</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[MEDIUM] COLOR-003** (line 401)
```
Current:  <div class="dest-rating"><span style="color:#FF9500;">&#9733;</span> 4.7</div>
Fix:      Use --apple-* CSS custom properties or semantic color tokens
Reason:   Hardcoded hex color that should be a CSS variable / semantic token
```

**[LOW] SPACE-002** (line 82)
```
Current:  color: var(--accent); padding: 6px 16px; border-radius: 100px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 110)
```
Current:  border-radius: 16px; padding: 14px 20px; min-width: 180px;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TYPO-003** (line 176)
```
Current:  .dest-city { font-size: 24px; font-weight: 700; color: #fbfbfd; margin-bottom: 2px; }
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] TYPO-003** (line 197)
```
Current:  font-size: 60px; position: relative; overflow: hidden;
Fix:      Apple uses tight tracking on headlines. Add letter-spacing: -0.02em for 24px+
Reason:   Missing letter-spacing on large/headline text
```

**[LOW] SPACE-002** (line 279)
```
Current:  padding: 14px 32px; border-radius: var(--btn-radius); font-size: 17px; font-weight: 700;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] SPACE-002** (line 287)
```
Current:  padding: 14px 32px; border-radius: var(--btn-radius); font-size: 17px; font-weight: 500;
Fix:      Use 4pt-grid values: 4/8/12/16/20/24/32/48
Reason:   Non-grid spacing value on padding/margin
```

**[LOW] TOUCH-002** (line 316)
```
Current:  <li><a href="#">Destinations</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 317)
```
Current:  <li><a href="#">Experiences</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 318)
```
Current:  <li><a href="#">Stays</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 319)
```
Current:  <li><a href="#">About</a></li>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 321)
```
Current:  <button class="nav-cta">Book Now</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 351)
```
Current:  <button class="search-btn">
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 562)
```
Current:  <button class="btn-teal">Download for iOS</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] TOUCH-002** (line 563)
```
Current:  <button class="btn-glass">Get on Android</button>
Fix:      Add cursor: pointer to all clickable elements
Reason:   Missing cursor: pointer on clickable element
```

**[LOW] ANIM-002** (line 593)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

**[LOW] ANIM-002** (line 607)
```
Current:  el.style.transition = 'opacity 0.6s cubic-bezier(0.25,0.1,0.25,1), transform 0.6s cubic-bezier(0.25,0.1,0.25,1)';
Fix:      Apple uses 200-400ms transitions. Use 0.2s-0.4s or 200ms-400ms
Reason:   Transition duration outside Apple range (200-400ms)
```

## Quick Fix Guide

To apply these changes, ask your AI agent:
"Read the redesign report at ./redesign-report.md and apply all fixes"

---
*Generated by OneMore [BETA] — Apple HIG Design Intelligence*
