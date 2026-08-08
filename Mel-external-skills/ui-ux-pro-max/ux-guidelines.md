# UX Guidelines (source: UI/UX Pro Max skill)

Extracted from `.claude/skills/ui-ux-pro-max/data/ux-guidelines.csv` in the source repo. The repo's README advertises this as "98 UX Guidelines"; the actual data file contains 99 numbered rows (No. 1-99) across 18 categories. That discrepancy is noted here rather than silently corrected or silently reproduced.

## Categories

Navigation, Animation, Layout, Touch, Interaction, Accessibility, Performance, Forms, Responsive, Typography, Feedback, Content, Onboarding, Search, Data Entry, AI Interaction, Spatial UI, Sustainability

## Navigation

### 1. Smooth Scroll (Web) — Severity: High

- **Description:** Anchor links should scroll smoothly to target section
- **Do:** Use scroll-behavior: smooth on html element
- **Don't:** Jump directly without transition
- **Good example:** `html { scroll-behavior: smooth; }`
- **Bad example:** `<a href='#section'> without CSS`

### 2. Sticky Navigation (Web) — Severity: Medium

- **Description:** Fixed nav should not obscure content
- **Do:** Add padding-top to body equal to nav height
- **Don't:** Let nav overlap first section content
- **Good example:** `pt-20 (if nav is h-20)`
- **Bad example:** `No padding compensation`

### 3. Active State (All) — Severity: Medium

- **Description:** Current page/section should be visually indicated
- **Do:** Highlight active nav item with color/underline
- **Don't:** No visual feedback on current location
- **Good example:** `text-primary border-b-2`
- **Bad example:** `All links same style`

### 4. Back Button (Mobile) — Severity: High

- **Description:** Users expect back to work predictably
- **Do:** Preserve navigation history properly
- **Don't:** Break browser/app back button behavior
- **Good example:** `history.pushState()`
- **Bad example:** `location.replace()`

### 5. Deep Linking (All) — Severity: Medium

- **Description:** URLs should reflect current state for sharing
- **Do:** Update URL on state/view changes
- **Don't:** Static URLs for dynamic content
- **Good example:** `Use query params or hash`
- **Bad example:** `Single URL for all states`

### 6. Breadcrumbs (Web) — Severity: Low

- **Description:** Show user location in site hierarchy
- **Do:** Use for sites with 3+ levels of depth
- **Don't:** Use for flat single-level sites
- **Good example:** `Home > Category > Product`
- **Bad example:** `Only on deep nested pages`

## Animation

### 7. Excessive Motion (All) — Severity: High

- **Description:** Too many animations cause distraction and motion sickness
- **Do:** Animate 1-2 key elements per view maximum
- **Don't:** Animate everything that moves
- **Good example:** `Single hero animation`
- **Bad example:** `animate-bounce on 5+ elements`

### 8. Duration Timing (All) — Severity: Medium

- **Description:** Animations should feel responsive not sluggish
- **Do:** Use 150-300ms for micro-interactions
- **Don't:** Use animations longer than 500ms for UI
- **Good example:** `transition-all duration-200`
- **Bad example:** `duration-1000`

### 9. Reduced Motion (All) — Severity: High

- **Description:** Respect user's motion preferences
- **Do:** Check prefers-reduced-motion media query
- **Don't:** Ignore accessibility motion settings
- **Good example:** `@media (prefers-reduced-motion: reduce)`
- **Bad example:** `No motion query check`

### 10. Loading States (All) — Severity: High

- **Description:** Show feedback during async operations
- **Do:** Use skeleton screens or spinners
- **Don't:** Leave UI frozen with no feedback
- **Good example:** `animate-pulse skeleton`
- **Bad example:** `Blank screen while loading`

### 11. Hover vs Tap (All) — Severity: High

- **Description:** Hover effects don't work on touch devices
- **Do:** Use click/tap for primary interactions
- **Don't:** Rely only on hover for important actions
- **Good example:** `onClick handler`
- **Bad example:** `onMouseEnter only`

### 12. Continuous Animation (All) — Severity: Medium

- **Description:** Infinite animations are distracting
- **Do:** Use for loading indicators only
- **Don't:** Use for decorative elements
- **Good example:** `animate-spin on loader`
- **Bad example:** `animate-bounce on icons`

### 13. Transform Performance (Web) — Severity: Medium

- **Description:** Some CSS properties trigger expensive repaints
- **Do:** Use transform and opacity for animations
- **Don't:** Animate width/height/top/left properties
- **Good example:** `transform: translateY()`
- **Bad example:** `top: 10px animation`

### 14. Easing Functions (All) — Severity: Low

- **Description:** Linear motion feels robotic
- **Do:** Use ease-out for entering ease-in for exiting
- **Don't:** Use linear for UI transitions
- **Good example:** `ease-out`
- **Bad example:** `linear`

## Layout

### 15. Z-Index Management (Web) — Severity: High

- **Description:** Stacking context conflicts cause hidden elements
- **Do:** Define z-index scale system (10 20 30 50)
- **Don't:** Use arbitrary large z-index values
- **Good example:** `z-10 z-20 z-50`
- **Bad example:** `z-[9999]`

### 16. Overflow Hidden (Web) — Severity: Medium

- **Description:** Hidden overflow can clip important content
- **Do:** Test all content fits within containers
- **Don't:** Blindly apply overflow-hidden
- **Good example:** `overflow-auto with scroll`
- **Bad example:** `overflow-hidden truncating content`

### 17. Fixed Positioning (Web) — Severity: Medium

- **Description:** Fixed elements can overlap or be inaccessible
- **Do:** Account for safe areas and other fixed elements
- **Don't:** Stack multiple fixed elements carelessly
- **Good example:** `Fixed nav + fixed bottom with gap`
- **Bad example:** `Multiple overlapping fixed elements`

### 18. Stacking Context (Web) — Severity: Medium

- **Description:** New stacking contexts reset z-index
- **Do:** Understand what creates new stacking context
- **Don't:** Expect z-index to work across contexts
- **Good example:** `Parent with z-index isolates children`
- **Bad example:** `z-index: 9999 not working`

### 19. Content Jumping (Web) — Severity: High

- **Description:** Layout shift when content loads is jarring
- **Do:** Reserve space for async content
- **Don't:** Let images/content push layout around
- **Good example:** `aspect-ratio or fixed height`
- **Bad example:** `No dimensions on images`

### 20. Viewport Units (Web) — Severity: Medium

- **Description:** 100vh can be problematic on mobile browsers
- **Do:** Use dvh or account for mobile browser chrome
- **Don't:** Use 100vh for full-screen mobile layouts
- **Good example:** `min-h-dvh or min-h-screen`
- **Bad example:** `h-screen on mobile`

### 21. Container Width (Web) — Severity: Medium

- **Description:** Content too wide is hard to read
- **Do:** Limit max-width for text content (65-75ch)
- **Don't:** Let text span full viewport width
- **Good example:** `max-w-prose or max-w-3xl`
- **Bad example:** `Full width paragraphs`

## Touch

### 22. Touch Target Size (Mobile) — Severity: High

- **Description:** Small buttons are hard to tap accurately
- **Do:** Minimum 44x44px touch targets
- **Don't:** Tiny clickable areas
- **Good example:** `min-h-[44px] min-w-[44px]`
- **Bad example:** `w-6 h-6 buttons`

### 23. Touch Spacing (Mobile) — Severity: Medium

- **Description:** Adjacent touch targets need adequate spacing
- **Do:** Minimum 8px gap between touch targets
- **Don't:** Tightly packed clickable elements
- **Good example:** `gap-2 between buttons`
- **Bad example:** `gap-0 or gap-1`

### 24. Gesture Conflicts (Mobile) — Severity: Medium

- **Description:** Custom gestures can conflict with system
- **Do:** Avoid horizontal swipe on main content
- **Don't:** Override system gestures
- **Good example:** `Vertical scroll primary`
- **Bad example:** `Horizontal swipe carousel only`

### 25. Tap Delay (Mobile) — Severity: Medium

- **Description:** 300ms tap delay feels laggy
- **Do:** Use touch-action CSS or fastclick
- **Don't:** Default mobile tap handling
- **Good example:** `touch-action: manipulation`
- **Bad example:** `No touch optimization`

### 26. Pull to Refresh (Mobile) — Severity: Low

- **Description:** Accidental refresh is frustrating
- **Do:** Disable where not needed
- **Don't:** Enable by default everywhere
- **Good example:** `overscroll-behavior: contain`
- **Bad example:** `Default overscroll`

### 27. Haptic Feedback (Mobile) — Severity: Low

- **Description:** Tactile feedback improves interaction feel
- **Do:** Use for confirmations and important actions
- **Don't:** Overuse vibration feedback
- **Good example:** `navigator.vibrate(10)`
- **Bad example:** `Vibrate on every tap`

## Interaction

### 28. Focus States (All) — Severity: High

- **Description:** Keyboard users need visible focus indicators
- **Do:** Use visible focus rings on interactive elements
- **Don't:** Remove focus outline without replacement
- **Good example:** `focus:ring-2 focus:ring-blue-500`
- **Bad example:** `outline-none without alternative`

### 29. Hover States (Web) — Severity: Medium

- **Description:** Visual feedback on interactive elements
- **Do:** Change cursor and add subtle visual change
- **Don't:** No hover feedback on clickable elements
- **Good example:** `hover:bg-gray-100 cursor-pointer`
- **Bad example:** `No hover style`

### 30. Active States (All) — Severity: Medium

- **Description:** Show immediate feedback on press/click
- **Do:** Add pressed/active state visual change
- **Don't:** No feedback during interaction
- **Good example:** `active:scale-95`
- **Bad example:** `No active state`

### 31. Disabled States (All) — Severity: Medium

- **Description:** Clearly indicate non-interactive elements
- **Do:** Reduce opacity and change cursor
- **Don't:** Confuse disabled with normal state
- **Good example:** `opacity-50 cursor-not-allowed`
- **Bad example:** `Same style as enabled`

### 32. Loading Buttons (All) — Severity: High

- **Description:** Prevent double submission during async actions
- **Do:** Disable button and show loading state
- **Don't:** Allow multiple clicks during processing
- **Good example:** `disabled={loading} spinner`
- **Bad example:** `Button clickable while loading`

### 33. Error Feedback (All) — Severity: High

- **Description:** Users need to know when something fails
- **Do:** Show clear error messages near problem
- **Don't:** Silent failures with no feedback
- **Good example:** `Red border + error message`
- **Bad example:** `No indication of error`

### 34. Success Feedback (All) — Severity: Medium

- **Description:** Confirm successful actions to users
- **Do:** Show success message or visual change
- **Don't:** No confirmation of completed action
- **Good example:** `Toast notification or checkmark`
- **Bad example:** `Action completes silently`

### 35. Confirmation Dialogs (All) — Severity: High

- **Description:** Prevent accidental destructive actions
- **Do:** Confirm before delete/irreversible actions
- **Don't:** Delete without confirmation
- **Good example:** `Are you sure modal`
- **Bad example:** `Direct delete on click`

## Accessibility

### 36. Color Contrast (All) — Severity: High

- **Description:** Text must be readable against background
- **Do:** Minimum 4.5:1 ratio for normal text
- **Don't:** Low contrast text
- **Good example:** `#333 on white (7:1)`
- **Bad example:** `#999 on white (2.8:1)`

### 37. Color Only (All) — Severity: High

- **Description:** Don't convey information by color alone
- **Do:** Use icons/text in addition to color
- **Don't:** Red/green only for error/success
- **Good example:** `Red text + error icon`
- **Bad example:** `Red border only for error`

### 38. Alt Text (All) — Severity: High

- **Description:** Images need text alternatives
- **Do:** Descriptive alt text for meaningful images
- **Don't:** Empty or missing alt attributes
- **Good example:** `alt='Dog playing in park'`
- **Bad example:** `alt='' for content images`

### 39. Heading Hierarchy (Web) — Severity: Medium

- **Description:** Screen readers use headings for navigation
- **Do:** Use sequential heading levels h1-h6
- **Don't:** Skip heading levels or misuse for styling
- **Good example:** `h1 then h2 then h3`
- **Bad example:** `h1 then h4`

### 40. ARIA Labels (All) — Severity: High

- **Description:** Interactive elements need accessible names
- **Do:** Add aria-label for icon-only buttons
- **Don't:** Icon buttons without labels
- **Good example:** `aria-label='Close menu'`
- **Bad example:** `<button><Icon/></button>`

### 41. Keyboard Navigation (Web) — Severity: High

- **Description:** All functionality accessible via keyboard
- **Do:** Tab order matches visual order
- **Don't:** Keyboard traps or illogical tab order
- **Good example:** `tabIndex for custom order`
- **Bad example:** `Unreachable elements`

### 42. Screen Reader (All) — Severity: Medium

- **Description:** Content should make sense when read aloud
- **Do:** Use semantic HTML and ARIA properly
- **Don't:** Div soup with no semantics
- **Good example:** `<nav> <main> <article>`
- **Bad example:** `<div> for everything`

### 43. Form Labels (All) — Severity: High

- **Description:** Inputs must have associated labels
- **Do:** Use label with for attribute or wrap input
- **Don't:** Placeholder-only inputs
- **Good example:** `<label for='email'>`
- **Bad example:** `placeholder='Email' only`

### 44. Error Messages (All) — Severity: High

- **Description:** Error messages must be announced
- **Do:** Use aria-live or role=alert for errors
- **Don't:** Visual-only error indication
- **Good example:** `role='alert'`
- **Bad example:** `Red border only`

### 45. Skip Links (Web) — Severity: Medium

- **Description:** Allow keyboard users to skip navigation
- **Do:** Provide skip to main content link
- **Don't:** No skip link on nav-heavy pages
- **Good example:** `Skip to main content link`
- **Bad example:** `100 tabs to reach content`

### 99. Motion Sensitivity (All) — Severity: High

- **Description:** Parallax/Scroll-jacking causes nausea
- **Do:** Respect prefers-reduced-motion
- **Don't:** Force scroll effects
- **Good example:** `@media (prefers-reduced-motion)`
- **Bad example:** `ScrollTrigger.create()`

## Performance

### 46. Image Optimization (All) — Severity: High

- **Description:** Large images slow page load
- **Do:** Use appropriate size and format (WebP)
- **Don't:** Unoptimized full-size images
- **Good example:** `srcset with multiple sizes`
- **Bad example:** `4000px image for 400px display`

### 47. Lazy Loading (All) — Severity: Medium

- **Description:** Load content as needed
- **Do:** Lazy load below-fold images and content
- **Don't:** Load everything upfront
- **Good example:** `loading='lazy'`
- **Bad example:** `All images eager load`

### 48. Code Splitting (Web) — Severity: Medium

- **Description:** Large bundles slow initial load
- **Do:** Split code by route/feature
- **Don't:** Single large bundle
- **Good example:** `dynamic import()`
- **Bad example:** `All code in main bundle`

### 49. Caching (Web) — Severity: Medium

- **Description:** Repeat visits should be fast
- **Do:** Set appropriate cache headers
- **Don't:** No caching strategy
- **Good example:** `Cache-Control headers`
- **Bad example:** `Every request hits server`

### 50. Font Loading (Web) — Severity: Medium

- **Description:** Web fonts can block rendering
- **Do:** Use font-display swap or optional
- **Don't:** Invisible text during font load
- **Good example:** `font-display: swap`
- **Bad example:** `FOIT (Flash of Invisible Text)`

### 51. Third Party Scripts (Web) — Severity: Medium

- **Description:** External scripts can block rendering
- **Do:** Load non-critical scripts async/defer
- **Don't:** Synchronous third-party scripts
- **Good example:** `async or defer attribute`
- **Bad example:** `<script src='...'> in head`

### 52. Bundle Size (Web) — Severity: Medium

- **Description:** Large JavaScript slows interaction
- **Do:** Monitor and minimize bundle size
- **Don't:** Ignore bundle size growth
- **Good example:** `Bundle analyzer`
- **Bad example:** `No size monitoring`

### 53. Render Blocking (Web) — Severity: Medium

- **Description:** CSS/JS can block first paint
- **Do:** Inline critical CSS defer non-critical
- **Don't:** Large blocking CSS files
- **Good example:** `Critical CSS inline`
- **Bad example:** `All CSS in head`

## Forms

### 54. Input Labels (All) — Severity: High

- **Description:** Every input needs a visible label
- **Do:** Always show label above or beside input
- **Don't:** Placeholder as only label
- **Good example:** `<label>Email</label><input>`
- **Bad example:** `placeholder='Email' only`

### 55. Error Placement (All) — Severity: Medium

- **Description:** Errors should appear near the problem
- **Do:** Show error below related input
- **Don't:** Single error message at top of form
- **Good example:** `Error under each field`
- **Bad example:** `All errors at form top`

### 56. Inline Validation (All) — Severity: Medium

- **Description:** Validate as user types or on blur
- **Do:** Validate on blur for most fields
- **Don't:** Validate only on submit
- **Good example:** `onBlur validation`
- **Bad example:** `Submit-only validation`

### 57. Input Types (All) — Severity: Medium

- **Description:** Use appropriate input types
- **Do:** Use email tel number url etc
- **Don't:** Text input for everything
- **Good example:** `type='email'`
- **Bad example:** `type='text' for email`

### 58. Autofill Support (Web) — Severity: Medium

- **Description:** Help browsers autofill correctly
- **Do:** Use autocomplete attribute properly
- **Don't:** Block or ignore autofill
- **Good example:** `autocomplete='email'`
- **Bad example:** `autocomplete='off' everywhere`

### 59. Required Indicators (All) — Severity: Medium

- **Description:** Mark required fields clearly
- **Do:** Use asterisk or (required) text
- **Don't:** No indication of required fields
- **Good example:** `* required indicator`
- **Bad example:** `Guess which are required`

### 60. Password Visibility (All) — Severity: Medium

- **Description:** Let users see password while typing
- **Do:** Toggle to show/hide password
- **Don't:** No visibility toggle
- **Good example:** `Show/hide password button`
- **Bad example:** `Password always hidden`

### 61. Submit Feedback (All) — Severity: High

- **Description:** Confirm form submission status
- **Do:** Show loading then success/error state
- **Don't:** No feedback after submit
- **Good example:** `Loading -> Success message`
- **Bad example:** `Button click with no response`

### 62. Input Affordance (All) — Severity: Medium

- **Description:** Inputs should look interactive
- **Do:** Use distinct input styling
- **Don't:** Inputs that look like plain text
- **Good example:** `Border/background on inputs`
- **Bad example:** `Borderless inputs`

### 63. Mobile Keyboards (Mobile) — Severity: Medium

- **Description:** Show appropriate keyboard for input type
- **Do:** Use inputmode attribute
- **Don't:** Default keyboard for all inputs
- **Good example:** `inputmode='numeric'`
- **Bad example:** `Text keyboard for numbers`

## Responsive

### 64. Mobile First (Web) — Severity: Medium

- **Description:** Design for mobile then enhance for larger
- **Do:** Start with mobile styles then add breakpoints
- **Don't:** Desktop-first causing mobile issues
- **Good example:** `Default mobile + md: lg: xl:`
- **Bad example:** `Desktop default + max-width queries`

### 65. Breakpoint Testing (Web) — Severity: Medium

- **Description:** Test at all common screen sizes
- **Do:** Test at 320 375 414 768 1024 1440
- **Don't:** Only test on your device
- **Good example:** `Multiple device testing`
- **Bad example:** `Single device development`

### 66. Touch Friendly (Web) — Severity: High

- **Description:** Mobile layouts need touch-sized targets
- **Do:** Increase touch targets on mobile
- **Don't:** Same tiny buttons on mobile
- **Good example:** `Larger buttons on mobile`
- **Bad example:** `Desktop-sized targets on mobile`

### 67. Readable Font Size (All) — Severity: High

- **Description:** Text must be readable on all devices
- **Do:** Minimum 16px body text on mobile
- **Don't:** Tiny text on mobile
- **Good example:** `text-base or larger`
- **Bad example:** `text-xs for body text`

### 68. Viewport Meta (Web) — Severity: High

- **Description:** Set viewport for mobile devices
- **Do:** Use width=device-width initial-scale=1
- **Don't:** Missing or incorrect viewport
- **Good example:** `<meta name='viewport'...>`
- **Bad example:** `No viewport meta tag`

### 69. Horizontal Scroll (Web) — Severity: High

- **Description:** Avoid horizontal scrolling
- **Do:** Ensure content fits viewport width
- **Don't:** Content wider than viewport
- **Good example:** `max-w-full overflow-x-hidden`
- **Bad example:** `Horizontal scrollbar on mobile`

### 70. Image Scaling (Web) — Severity: Medium

- **Description:** Images should scale with container
- **Do:** Use max-width: 100% on images
- **Don't:** Fixed width images overflow
- **Good example:** `max-w-full h-auto`
- **Bad example:** `width='800' fixed`

### 71. Table Handling (Web) — Severity: Medium

- **Description:** Tables can overflow on mobile
- **Do:** Use horizontal scroll or card layout
- **Don't:** Wide tables breaking layout
- **Good example:** `overflow-x-auto wrapper`
- **Bad example:** `Table overflows viewport`

## Typography

### 72. Line Height (All) — Severity: Medium

- **Description:** Adequate line height improves readability
- **Do:** Use 1.5-1.75 for body text
- **Don't:** Cramped or excessive line height
- **Good example:** `leading-relaxed (1.625)`
- **Bad example:** `leading-none (1)`

### 73. Line Length (Web) — Severity: Medium

- **Description:** Long lines are hard to read
- **Do:** Limit to 65-75 characters per line
- **Don't:** Full-width text on large screens
- **Good example:** `max-w-prose`
- **Bad example:** `Full viewport width text`

### 74. Font Size Scale (All) — Severity: Medium

- **Description:** Consistent type hierarchy aids scanning
- **Do:** Use consistent modular scale
- **Don't:** Random font sizes
- **Good example:** `Type scale (12 14 16 18 24 32)`
- **Bad example:** `Arbitrary sizes`

### 75. Font Loading (Web) — Severity: Medium

- **Description:** Fonts should load without layout shift
- **Do:** Reserve space with fallback font
- **Don't:** Layout shift when fonts load
- **Good example:** `font-display: swap + similar fallback`
- **Bad example:** `No fallback font`

### 76. Contrast Readability (All) — Severity: High

- **Description:** Body text needs good contrast
- **Do:** Use darker text on light backgrounds
- **Don't:** Gray text on gray background
- **Good example:** `text-gray-900 on white`
- **Bad example:** `text-gray-400 on gray-100`

### 77. Heading Clarity (All) — Severity: Medium

- **Description:** Headings should stand out from body
- **Do:** Clear size/weight difference
- **Don't:** Headings similar to body text
- **Good example:** `Bold + larger size`
- **Bad example:** `Same size as body`

## Feedback

### 78. Loading Indicators (All) — Severity: High

- **Description:** Show system status during waits
- **Do:** Show spinner/skeleton for operations > 300ms
- **Don't:** No feedback during loading
- **Good example:** `Skeleton or spinner`
- **Bad example:** `Frozen UI`

### 79. Empty States (All) — Severity: Medium

- **Description:** Guide users when no content exists
- **Do:** Show helpful message and action
- **Don't:** Blank empty screens
- **Good example:** `No items yet. Create one!`
- **Bad example:** `Empty white space`

### 80. Error Recovery (All) — Severity: Medium

- **Description:** Help users recover from errors
- **Do:** Provide clear next steps
- **Don't:** Error without recovery path
- **Good example:** `Try again button + help link`
- **Bad example:** `Error message only`

### 81. Progress Indicators (All) — Severity: Medium

- **Description:** Show progress for multi-step processes
- **Do:** Step indicators or progress bar
- **Don't:** No indication of progress
- **Good example:** `Step 2 of 4 indicator`
- **Bad example:** `No step information`

### 82. Toast Notifications (All) — Severity: Medium

- **Description:** Transient messages for non-critical info
- **Do:** Auto-dismiss after 3-5 seconds
- **Don't:** Toasts that never disappear
- **Good example:** `Auto-dismiss toast`
- **Bad example:** `Persistent toast`

### 83. Confirmation Messages (All) — Severity: Medium

- **Description:** Confirm successful actions
- **Do:** Brief success message
- **Don't:** Silent success
- **Good example:** `Saved successfully toast`
- **Bad example:** `No confirmation`

## Content

### 84. Truncation (All) — Severity: Medium

- **Description:** Handle long content gracefully
- **Do:** Truncate with ellipsis and expand option
- **Don't:** Overflow or broken layout
- **Good example:** `line-clamp-2 with expand`
- **Bad example:** `Overflow or cut off`

### 85. Date Formatting (All) — Severity: Low

- **Description:** Use locale-appropriate date formats
- **Do:** Use relative or locale-aware dates
- **Don't:** Ambiguous date formats
- **Good example:** `2 hours ago or locale format`
- **Bad example:** `01/02/03`

### 86. Number Formatting (All) — Severity: Low

- **Description:** Format large numbers for readability
- **Do:** Use thousand separators or abbreviations
- **Don't:** Long unformatted numbers
- **Good example:** `1.2K or 1,234`
- **Bad example:** `1234567`

### 87. Placeholder Content (All) — Severity: Low

- **Description:** Show realistic placeholders during dev
- **Do:** Use realistic sample data
- **Don't:** Lorem ipsum everywhere
- **Good example:** `Real sample content`
- **Bad example:** `Lorem ipsum`

## Onboarding

### 88. User Freedom (All) — Severity: Medium

- **Description:** Users should be able to skip tutorials
- **Do:** Provide Skip and Back buttons
- **Don't:** Force linear unskippable tour
- **Good example:** `Skip Tutorial button`
- **Bad example:** `Locked overlay until finished`

## Search

### 89. Autocomplete (Web) — Severity: Medium

- **Description:** Help users find results faster
- **Do:** Show predictions as user types
- **Don't:** Require full type and enter
- **Good example:** `Debounced fetch + dropdown`
- **Bad example:** `No suggestions`

### 90. No Results (Web) — Severity: Medium

- **Description:** Dead ends frustrate users
- **Do:** Show 'No results' with suggestions
- **Don't:** Blank screen or '0 results'
- **Good example:** `Try searching for X instead`
- **Bad example:** `No results found.`

## Data Entry

### 91. Bulk Actions (Web) — Severity: Low

- **Description:** Editing one by one is tedious
- **Do:** Allow multi-select and bulk edit
- **Don't:** Single row actions only
- **Good example:** `Checkbox column + Action bar`
- **Bad example:** `Repeated actions per row`

## AI Interaction

### 92. Disclaimer (All) — Severity: High

- **Description:** Users need to know they talk to AI
- **Do:** Clearly label AI generated content
- **Don't:** Present AI as human
- **Good example:** `AI Assistant label`
- **Bad example:** `Fake human name without label`

### 93. Streaming (All) — Severity: Medium

- **Description:** Waiting for full text is slow
- **Do:** Stream text response token by token
- **Don't:** Show loading spinner for 10s+
- **Good example:** `Typewriter effect`
- **Bad example:** `Spinner until 100% complete`

### 98. Feedback Loop (All) — Severity: Low

- **Description:** AI needs user feedback to improve
- **Do:** Thumps up/down or 'Regenerate'
- **Don't:** Static output only
- **Good example:** `Feedback component`
- **Bad example:** `Read-only text`

## Spatial UI

### 94. Gaze Hover (VisionOS) — Severity: High

- **Description:** Elements should respond to eye tracking before pinch
- **Do:** Scale/highlight element on look
- **Don't:** Static element until pinch
- **Good example:** `hoverEffect()`
- **Bad example:** `onTap only`

### 95. Depth Layering (VisionOS) — Severity: Medium

- **Description:** UI needs Z-depth to separate content from environment
- **Do:** Use glass material and z-offset
- **Don't:** Flat opaque panels blocking view
- **Good example:** `.glassBackgroundEffect()`
- **Bad example:** `bg-white`

## Sustainability

### 96. Auto-Play Video (Web) — Severity: Medium

- **Description:** Video consumes massive data and energy
- **Do:** Click-to-play or pause when off-screen
- **Don't:** Auto-play high-res video loops
- **Good example:** `playsInline muted preload='none'`
- **Bad example:** `autoplay loop`

### 97. Asset Weight (Web) — Severity: Medium

- **Description:** Heavy 3D/Image assets increase carbon footprint
- **Do:** Compress and lazy load 3D models
- **Don't:** Load 50MB textures
- **Good example:** `Draco compression`
- **Bad example:** `Raw .obj files`
