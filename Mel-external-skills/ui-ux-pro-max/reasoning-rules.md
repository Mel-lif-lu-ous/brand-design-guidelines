# Industry Reasoning Rules (source: UI/UX Pro Max skill)

Extracted from `.claude/skills/ui-ux-pro-max/data/ui-reasoning.csv` in the source repo — 161 numbered rows (No. 1-161), matching the README's claim of "161 Industry-Specific Reasoning Rules." Each rule captures, per industry/product category: the recommended structural pattern, a style-priority pairing, a color-mood descriptor, a typography-mood descriptor, key motion/effects, machine-readable decision rules, and anti-patterns to avoid.

**Important for LKI use:** the `Style_Priority`, `Color_Mood`, and `Typography_Mood` fields below are directional descriptors from the source skill's own style/palette/font system (the part Lara asked to exclude from generation). They are kept here only as context for *why* a given industry pattern is recommended — never as inputs to pick colors or type. LKI color and typography always come from `Design Guidelines/colors_and_type.css`.

## Index

| No | Category | Severity |
|----|----------|----------|
| 1 | SaaS (General) | HIGH |
| 2 | Micro SaaS | HIGH |
| 3 | E-commerce | HIGH |
| 4 | E-commerce Luxury | HIGH |
| 5 | B2B Service | HIGH |
| 6 | Financial Dashboard | HIGH |
| 7 | Analytics Dashboard | HIGH |
| 8 | Healthcare App | HIGH |
| 9 | Educational App | MEDIUM |
| 10 | Creative Agency | HIGH |
| 11 | Portfolio/Personal | MEDIUM |
| 12 | Gaming | HIGH |
| 13 | Government/Public Service | HIGH |
| 14 | Fintech/Crypto | HIGH |
| 15 | Social Media App | MEDIUM |
| 16 | Productivity Tool | HIGH |
| 17 | Design System/Component Library | HIGH |
| 18 | AI/Chatbot Platform | HIGH |
| 19 | NFT/Web3 Platform | HIGH |
| 20 | Creator Economy Platform | MEDIUM |
| 21 | Remote Work/Collaboration Tool | HIGH |
| 22 | Mental Health App | HIGH |
| 23 | Pet Tech App | MEDIUM |
| 24 | Smart Home/IoT Dashboard | HIGH |
| 25 | EV/Charging Ecosystem | HIGH |
| 26 | Subscription Box Service | HIGH |
| 27 | Podcast Platform | HIGH |
| 28 | Dating App | HIGH |
| 29 | Micro-Credentials/Badges Platform | MEDIUM |
| 30 | Knowledge Base/Documentation | HIGH |
| 31 | Hyperlocal Services | HIGH |
| 32 | Beauty/Spa/Wellness Service | HIGH |
| 33 | Luxury/Premium Brand | HIGH |
| 34 | Restaurant/Food Service | HIGH |
| 35 | Fitness/Gym App | HIGH |
| 36 | Real Estate/Property | HIGH |
| 37 | Travel/Tourism Agency | HIGH |
| 38 | Hotel/Hospitality | HIGH |
| 39 | Wedding/Event Planning | HIGH |
| 40 | Legal Services | HIGH |
| 41 | Insurance Platform | HIGH |
| 42 | Banking/Traditional Finance | HIGH |
| 43 | Online Course/E-learning | HIGH |
| 44 | Non-profit/Charity | HIGH |
| 45 | Music Streaming | HIGH |
| 46 | Video Streaming/OTT | HIGH |
| 47 | Job Board/Recruitment | HIGH |
| 48 | Marketplace (P2P) | HIGH |
| 49 | Logistics/Delivery | HIGH |
| 50 | Agriculture/Farm Tech | MEDIUM |
| 51 | Construction/Architecture | HIGH |
| 52 | Automotive/Car Dealership | HIGH |
| 53 | Photography Studio | HIGH |
| 54 | Coworking Space | MEDIUM |
| 55 | Home Services (Plumber/Electrician) | HIGH |
| 56 | Childcare/Daycare | HIGH |
| 57 | Senior Care/Elderly | HIGH |
| 58 | Medical Clinic | HIGH |
| 59 | Pharmacy/Drug Store | HIGH |
| 60 | Dental Practice | HIGH |
| 61 | Veterinary Clinic | MEDIUM |
| 62 | Florist/Plant Shop | MEDIUM |
| 63 | Bakery/Cafe | HIGH |
| 64 | Brewery/Winery | HIGH |
| 65 | Airline | HIGH |
| 66 | News/Media Platform | HIGH |
| 67 | Magazine/Blog | HIGH |
| 68 | Freelancer Platform | HIGH |
| 69 | Marketing Agency | HIGH |
| 70 | Event Management | HIGH |
| 71 | Membership/Community | HIGH |
| 72 | Newsletter Platform | MEDIUM |
| 73 | Digital Products/Downloads | HIGH |
| 74 | Church/Religious Organization | MEDIUM |
| 75 | Sports Team/Club | HIGH |
| 76 | Museum/Gallery | HIGH |
| 77 | Theater/Cinema | HIGH |
| 78 | Language Learning App | HIGH |
| 79 | Coding Bootcamp | HIGH |
| 80 | Cybersecurity Platform | HIGH |
| 81 | Developer Tool / IDE | HIGH |
| 82 | Biotech / Life Sciences | HIGH |
| 83 | Space Tech / Aerospace | HIGH |
| 84 | Architecture / Interior | HIGH |
| 85 | Quantum Computing Interface | HIGH |
| 86 | Biohacking / Longevity App | HIGH |
| 87 | Autonomous Drone Fleet Manager | HIGH |
| 88 | Generative Art Platform | HIGH |
| 89 | Spatial Computing OS / App | HIGH |
| 90 | Sustainable Energy / Climate Tech | HIGH |
| 91 | Personal Finance Tracker | HIGH |
| 92 | Chat & Messaging App | HIGH |
| 93 | Notes & Writing App | HIGH |
| 94 | Habit Tracker | HIGH |
| 95 | Food Delivery / On-Demand | HIGH |
| 96 | Ride Hailing / Transportation | HIGH |
| 97 | Recipe & Cooking App | HIGH |
| 98 | Meditation & Mindfulness | HIGH |
| 99 | Weather App | HIGH |
| 100 | Diary & Journal App | HIGH |
| 101 | CRM & Client Management | HIGH |
| 102 | Inventory & Stock Management | HIGH |
| 103 | Flashcard & Study Tool | HIGH |
| 104 | Booking & Appointment App | HIGH |
| 105 | Invoice & Billing Tool | HIGH |
| 106 | Grocery & Shopping List | HIGH |
| 107 | Timer & Pomodoro | HIGH |
| 108 | Parenting & Baby Tracker | HIGH |
| 109 | Scanner & Document Manager | HIGH |
| 110 | Calendar & Scheduling App | HIGH |
| 111 | Password Manager | HIGH |
| 112 | Expense Splitter / Bill Split | HIGH |
| 113 | Voice Recorder & Memo | HIGH |
| 114 | Bookmark & Read-Later | HIGH |
| 115 | Translator App | HIGH |
| 116 | Calculator & Unit Converter | HIGH |
| 117 | Alarm & World Clock | HIGH |
| 118 | File Manager & Transfer | HIGH |
| 119 | Email Client | HIGH |
| 120 | Casual Puzzle Game | HIGH |
| 121 | Trivia & Quiz Game | HIGH |
| 122 | Card & Board Game | HIGH |
| 123 | Idle & Clicker Game | HIGH |
| 124 | Word & Crossword Game | HIGH |
| 125 | Arcade & Retro Game | HIGH |
| 126 | Photo Editor & Filters | HIGH |
| 127 | Short Video Editor | HIGH |
| 128 | Drawing & Sketching Canvas | HIGH |
| 129 | Music Creation & Beat Maker | HIGH |
| 130 | Meme & Sticker Maker | HIGH |
| 131 | AI Photo & Avatar Generator | HIGH |
| 132 | Link-in-Bio Page Builder | HIGH |
| 133 | Wardrobe & Outfit Planner | HIGH |
| 134 | Plant Care Tracker | HIGH |
| 135 | Book & Reading Tracker | HIGH |
| 136 | Couple & Relationship App | HIGH |
| 137 | Family Calendar & Chores | HIGH |
| 138 | Mood Tracker | HIGH |
| 139 | Gift & Wishlist | HIGH |
| 140 | Running & Cycling GPS | HIGH |
| 141 | Yoga & Stretching Guide | HIGH |
| 142 | Sleep Tracker | HIGH |
| 143 | Calorie & Nutrition Counter | HIGH |
| 144 | Period & Cycle Tracker | HIGH |
| 145 | Medication & Pill Reminder | HIGH |
| 146 | Water & Hydration Reminder | HIGH |
| 147 | Fasting & Intermittent Timer | HIGH |
| 148 | Anonymous Community / Confession | HIGH |
| 149 | Local Events & Discovery | HIGH |
| 150 | Study Together / Virtual Coworking | HIGH |
| 151 | Coding Challenge & Practice | HIGH |
| 152 | Kids Learning (ABC & Math) | HIGH |
| 153 | Music Instrument Learning | HIGH |
| 154 | Parking Finder | HIGH |
| 155 | Public Transit Guide | HIGH |
| 156 | Road Trip Planner | HIGH |
| 157 | VPN & Privacy Tool | HIGH |
| 158 | Emergency SOS & Safety | HIGH |
| 159 | Wallpaper & Theme App | HIGH |
| 160 | White Noise & Ambient Sound | HIGH |
| 161 | Home Decoration & Interior Design | HIGH |

## Full Rules

### 1. SaaS (General) — Severity: HIGH

- **Recommended pattern:** Hero + Features + CTA
- **Style priority:** Glassmorphism + Flat Design
- **Color mood:** Trust blue + Accent contrast
- **Typography mood:** Professional + Hierarchy
- **Key effects:** Subtle hover (200-250ms) + Smooth transitions
- **Decision rules:** `{"if_ux_focused": "prioritize-minimalism", "if_data_heavy": "add-glassmorphism"}`
- **Anti-patterns:** Excessive animation + Dark mode by default

### 2. Micro SaaS — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Trust
- **Style priority:** Motion-Driven + Vibrant & Block
- **Color mood:** Bold primaries + Accent contrast
- **Typography mood:** Modern + Energetic typography
- **Key effects:** Scroll-triggered animations + Parallax
- **Decision rules:** `{"if_pre_launch": "use-waitlist-pattern", "if_video_ready": "add-hero-video"}`
- **Anti-patterns:** Static design + No video + Poor mobile

### 3. E-commerce — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Vibrant & Block-based
- **Color mood:** Brand primary + Success green
- **Typography mood:** Engaging + Clear hierarchy
- **Key effects:** Card hover lift (200ms) + Scale effect
- **Decision rules:** `{"if_luxury": "switch-to-liquid-glass", "if_conversion_focused": "add-urgency-colors"}`
- **Anti-patterns:** Flat design without depth + Text-heavy pages

### 4. E-commerce Luxury — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Liquid Glass + Glassmorphism
- **Color mood:** Premium colors + Minimal accent
- **Typography mood:** Elegant + Refined typography
- **Key effects:** Chromatic aberration + Fluid animations (400-600ms)
- **Decision rules:** `{"if_checkout": "emphasize-trust", "if_hero_needed": "use-3d-hyperrealism"}`
- **Anti-patterns:** Vibrant & Block-based + Playful colors

### 5. B2B Service — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Trust
- **Style priority:** Trust & Authority + Minimalism
- **Color mood:** Professional blue + Neutral grey
- **Typography mood:** Formal + Clear typography
- **Key effects:** Section transitions + Feature reveals
- **Decision rules:** `{"must_have": "case-studies", "must_have": "roi-messaging"}`
- **Anti-patterns:** Playful design + Hidden credentials + AI purple/pink gradients

### 6. Financial Dashboard — Severity: HIGH

- **Recommended pattern:** Data-Dense Dashboard
- **Style priority:** Dark Mode (OLED) + Data-Dense
- **Color mood:** Dark bg + Red/Green alerts + Trust blue
- **Typography mood:** Clear + Readable typography
- **Key effects:** Real-time number animations + Alert pulse
- **Decision rules:** `{"must_have": "real-time-updates", "must_have": "high-contrast"}`
- **Anti-patterns:** Light mode default + Slow rendering

### 7. Analytics Dashboard — Severity: HIGH

- **Recommended pattern:** Data-Dense + Drill-Down
- **Style priority:** Data-Dense + Heat Map
- **Color mood:** Cool→Hot gradients + Neutral grey
- **Typography mood:** Clear + Functional typography
- **Key effects:** Hover tooltips + Chart zoom + Filter animations
- **Decision rules:** `{"must_have": "data-export", "if_large_dataset": "virtualize-lists"}`
- **Anti-patterns:** Ornate design + No filtering

### 8. Healthcare App — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused
- **Style priority:** Neumorphism + Accessible & Ethical
- **Color mood:** Calm blue + Health green
- **Typography mood:** Readable + Large type (16px+)
- **Key effects:** Soft box-shadow + Smooth press (150ms)
- **Decision rules:** `{"must_have": "wcag-aaa-compliance", "if_medication": "red-alert-colors"}`
- **Anti-patterns:** Bright neon colors + Motion-heavy animations + AI purple/pink gradients

### 9. Educational App — Severity: MEDIUM

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Claymorphism + Micro-interactions
- **Color mood:** Playful colors + Clear hierarchy
- **Typography mood:** Friendly + Engaging typography
- **Key effects:** Soft press (200ms) + Fluffy elements
- **Decision rules:** `{"if_gamification": "add-progress-animation", "if_children": "increase-playfulness"}`
- **Anti-patterns:** Dark modes + Complex jargon

### 10. Creative Agency — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven
- **Style priority:** Brutalism + Motion-Driven
- **Color mood:** Bold primaries + Artistic freedom
- **Typography mood:** Bold + Expressive typography
- **Key effects:** CRT scanlines + Neon glow + Glitch effects
- **Decision rules:** `{"must_have": "case-studies", "if_boutique": "increase-artistic-freedom"}`
- **Anti-patterns:** Corporate minimalism + Hidden portfolio

### 11. Portfolio/Personal — Severity: MEDIUM

- **Recommended pattern:** Storytelling-Driven
- **Style priority:** Motion-Driven + Minimalism
- **Color mood:** Brand primary + Artistic
- **Typography mood:** Expressive + Variable typography
- **Key effects:** Parallax (3-5 layers) + Scroll-triggered reveals
- **Decision rules:** `{"if_creative_field": "add-brutalism", "if_minimal_portfolio": "reduce-motion"}`
- **Anti-patterns:** Corporate templates + Generic layouts

### 12. Gaming — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** 3D & Hyperrealism + Retro-Futurism
- **Color mood:** Vibrant + Neon + Immersive
- **Typography mood:** Bold + Impactful typography
- **Key effects:** WebGL 3D rendering + Glitch effects
- **Decision rules:** `{"if_competitive": "add-real-time-stats", "if_casual": "increase-playfulness"}`
- **Anti-patterns:** Minimalist design + Static assets

### 13. Government/Public Service — Severity: HIGH

- **Recommended pattern:** Minimal & Direct
- **Style priority:** Accessible & Ethical + Minimalism
- **Color mood:** Professional blue + High contrast
- **Typography mood:** Clear + Large typography
- **Key effects:** Clear focus rings (3-4px) + Skip links
- **Decision rules:** `{"must_have": "wcag-aaa", "must_have": "keyboard-navigation"}`
- **Anti-patterns:** Ornate design + Low contrast + Motion effects + AI purple/pink gradients

### 14. Fintech/Crypto — Severity: HIGH

- **Recommended pattern:** Trust & Authority
- **Style priority:** Minimalism + Accessible & Ethical
- **Color mood:** Navy + Trust Blue + Gold
- **Typography mood:** Professional + Trustworthy
- **Key effects:** Smooth state transitions + Number animations
- **Decision rules:** `{"must_have": "security-first", "if_dashboard": "use-dark-mode"}`
- **Anti-patterns:** Playful design + Unclear fees + AI purple/pink gradients

### 15. Social Media App — Severity: MEDIUM

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Vibrant + Engagement colors
- **Typography mood:** Modern + Bold typography
- **Key effects:** Large scroll animations + Icon animations
- **Decision rules:** `{"if_engagement_metric": "add-motion", "if_content_focused": "minimize-chrome"}`
- **Anti-patterns:** Heavy skeuomorphism + Accessibility ignored

### 16. Productivity Tool — Severity: HIGH

- **Recommended pattern:** Interactive Demo + Feature-Rich
- **Style priority:** Flat Design + Micro-interactions
- **Color mood:** Clear hierarchy + Functional colors
- **Typography mood:** Clean + Efficient typography
- **Key effects:** Quick actions (150ms) + Task animations
- **Decision rules:** `{"must_have": "keyboard-shortcuts", "if_collaboration": "add-real-time-cursors"}`
- **Anti-patterns:** Complex onboarding + Slow performance

### 17. Design System/Component Library — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Documentation
- **Style priority:** Minimalism + Accessible & Ethical
- **Color mood:** Clear hierarchy + Code-like structure
- **Typography mood:** Monospace + Clear typography
- **Key effects:** Code copy animations + Component previews
- **Decision rules:** `{"must_have": "search", "must_have": "code-examples"}`
- **Anti-patterns:** Poor documentation + No live preview

### 18. AI/Chatbot Platform — Severity: HIGH

- **Recommended pattern:** Interactive Demo + Minimal
- **Style priority:** AI-Native UI + Minimalism
- **Color mood:** Neutral + AI Purple (#6366F1)
- **Typography mood:** Modern + Clear typography
- **Key effects:** Streaming text + Typing indicators + Fade-in
- **Decision rules:** `{"must_have": "conversational-ui", "must_have": "context-awareness"}`
- **Anti-patterns:** Heavy chrome + Slow response feedback

### 19. NFT/Web3 Platform — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Cyberpunk UI + Glassmorphism
- **Color mood:** Dark + Neon + Gold (#FFD700)
- **Typography mood:** Bold + Modern typography
- **Key effects:** Wallet connect animations + Transaction feedback
- **Decision rules:** `{"must_have": "wallet-integration", "must_have": "gas-fees-display"}`
- **Anti-patterns:** Light mode default + No transaction status

### 20. Creator Economy Platform — Severity: MEDIUM

- **Recommended pattern:** Social Proof + Feature-Rich
- **Style priority:** Vibrant & Block-based + Bento Box Grid
- **Color mood:** Vibrant + Brand colors
- **Typography mood:** Modern + Bold typography
- **Key effects:** Engagement counter animations + Profile reveals
- **Decision rules:** `{"must_have": "creator-profiles", "must_have": "monetization-display"}`
- **Anti-patterns:** Generic layout + Hidden earnings

### 21. Remote Work/Collaboration Tool — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Real-Time
- **Style priority:** Soft UI Evolution + Minimalism
- **Color mood:** Calm Blue + Neutral grey
- **Typography mood:** Clean + Readable typography
- **Key effects:** Real-time presence indicators + Notification badges
- **Decision rules:** `{"must_have": "status-indicators", "must_have": "video-integration"}`
- **Anti-patterns:** Cluttered interface + No presence

### 22. Mental Health App — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused
- **Style priority:** Neumorphism + Accessible & Ethical
- **Color mood:** Calm Pastels + Trust colors
- **Typography mood:** Calming + Readable typography
- **Key effects:** Soft press + Breathing animations
- **Decision rules:** `{"must_have": "privacy-first", "if_meditation": "add-breathing-animation"}`
- **Anti-patterns:** Bright neon + Motion overload

### 23. Pet Tech App — Severity: MEDIUM

- **Recommended pattern:** Storytelling + Feature-Rich
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Playful + Warm colors
- **Typography mood:** Friendly + Playful typography
- **Key effects:** Pet profile animations + Health tracking charts
- **Decision rules:** `{"must_have": "pet-profiles", "if_health": "add-vet-integration"}`
- **Anti-patterns:** Generic design + No personality

### 24. Smart Home/IoT Dashboard — Severity: HIGH

- **Recommended pattern:** Real-Time Monitoring
- **Style priority:** Glassmorphism + Dark Mode (OLED)
- **Color mood:** Dark + Status indicator colors
- **Typography mood:** Clear + Functional typography
- **Key effects:** Device status pulse + Quick action animations
- **Decision rules:** `{"must_have": "real-time-controls", "must_have": "energy-monitoring"}`
- **Anti-patterns:** Slow updates + No automation

### 25. EV/Charging Ecosystem — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Minimalism + Aurora UI
- **Color mood:** Electric Blue (#009CD1) + Green
- **Typography mood:** Modern + Clear typography
- **Key effects:** Range estimation animations + Map interactions
- **Decision rules:** `{"must_have": "charging-map", "must_have": "range-calculator"}`
- **Anti-patterns:** Poor map UX + Hidden costs

### 26. Subscription Box Service — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Conversion
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Brand + Excitement colors
- **Typography mood:** Engaging + Clear typography
- **Key effects:** Unboxing reveal animations + Product carousel
- **Decision rules:** `{"must_have": "personalization-quiz", "must_have": "subscription-management"}`
- **Anti-patterns:** Confusing pricing + No unboxing preview

### 27. Podcast Platform — Severity: HIGH

- **Recommended pattern:** Storytelling + Feature-Rich
- **Style priority:** Dark Mode (OLED) + Minimalism
- **Color mood:** Dark + Audio waveform accents
- **Typography mood:** Modern + Clear typography
- **Key effects:** Waveform visualizations + Episode transitions
- **Decision rules:** `{"must_have": "audio-player-ux", "must_have": "episode-discovery"}`
- **Anti-patterns:** Poor audio player + Cluttered layout

### 28. Dating App — Severity: HIGH

- **Recommended pattern:** Social Proof + Feature-Rich
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Warm + Romantic (Pink/Red gradients)
- **Typography mood:** Modern + Friendly typography
- **Key effects:** Profile card swipe + Match animations
- **Decision rules:** `{"must_have": "profile-cards", "must_have": "safety-features"}`
- **Anti-patterns:** Generic profiles + No safety

### 29. Micro-Credentials/Badges Platform — Severity: MEDIUM

- **Recommended pattern:** Trust & Authority + Feature
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Trust Blue + Gold (#FFD700)
- **Typography mood:** Professional + Clear typography
- **Key effects:** Badge reveal animations + Progress tracking
- **Decision rules:** `{"must_have": "credential-verification", "must_have": "progress-display"}`
- **Anti-patterns:** No verification + Hidden progress

### 30. Knowledge Base/Documentation — Severity: HIGH

- **Recommended pattern:** FAQ + Minimal
- **Style priority:** Minimalism + Accessible & Ethical
- **Color mood:** Clean hierarchy + Minimal color
- **Typography mood:** Clear + Readable typography
- **Key effects:** Search highlight + Smooth scrolling
- **Decision rules:** `{"must_have": "search-first", "must_have": "version-switching"}`
- **Anti-patterns:** Poor navigation + No search

### 31. Hyperlocal Services — Severity: HIGH

- **Recommended pattern:** Conversion + Feature-Rich
- **Style priority:** Minimalism + Vibrant & Block-based
- **Color mood:** Location markers + Trust colors
- **Typography mood:** Clear + Functional typography
- **Key effects:** Map hover + Provider card reveals
- **Decision rules:** `{"must_have": "map-integration", "must_have": "booking-system"}`
- **Anti-patterns:** No map + Hidden reviews

### 32. Beauty/Spa/Wellness Service — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Social Proof
- **Style priority:** Soft UI Evolution + Neumorphism
- **Color mood:** Soft pastels (Pink Sage Cream) + Gold accents
- **Typography mood:** Elegant + Calming typography
- **Key effects:** Soft shadows + Smooth transitions (200-300ms) + Gentle hover
- **Decision rules:** `{"must_have": "booking-system", "must_have": "before-after-gallery", "if_luxury": "add-gold-accents"}`
- **Anti-patterns:** Bright neon colors + Harsh animations + Dark mode

### 33. Luxury/Premium Brand — Severity: HIGH

- **Recommended pattern:** Storytelling + Feature-Rich
- **Style priority:** Liquid Glass + Glassmorphism
- **Color mood:** Black + Gold (#FFD700) + White
- **Typography mood:** Elegant + Refined typography
- **Key effects:** Slow parallax + Premium reveals (400-600ms)
- **Decision rules:** `{"must_have": "high-quality-imagery", "must_have": "storytelling"}`
- **Anti-patterns:** Cheap visuals + Fast animations

### 34. Restaurant/Food Service — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Conversion
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Warm colors (Orange Red Brown)
- **Typography mood:** Appetizing + Clear typography
- **Key effects:** Food image reveal + Menu hover effects
- **Decision rules:** `{"must_have": "high_quality_images", "if_delivery": "emphasize-speed"}`
- **Anti-patterns:** Low-quality imagery + Outdated hours

### 35. Fitness/Gym App — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Data
- **Style priority:** Vibrant & Block-based + Dark Mode (OLED)
- **Color mood:** Energetic (Orange #FF6B35) + Dark bg
- **Typography mood:** Bold + Motivational typography
- **Key effects:** Progress ring animations + Achievement unlocks
- **Decision rules:** `{"must_have": "progress-tracking", "must_have": "workout-plans"}`
- **Anti-patterns:** Static design + No gamification

### 36. Real Estate/Property — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Glassmorphism + Minimalism
- **Color mood:** Trust Blue + Gold + White
- **Typography mood:** Professional + Confident
- **Key effects:** 3D property tour zoom + Map hover
- **Decision rules:** `{"if_luxury": "add-3d-models", "must_have": "map-integration"}`
- **Anti-patterns:** Poor photos + No virtual tours

### 37. Travel/Tourism Agency — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Hero
- **Style priority:** Aurora UI + Motion-Driven
- **Color mood:** Vibrant destination + Sky Blue
- **Typography mood:** Inspirational + Engaging
- **Key effects:** Destination parallax + Itinerary animations
- **Decision rules:** `{"if_experience_focused": "use-storytelling", "must_have": "mobile-booking"}`
- **Anti-patterns:** Generic photos + Complex booking

### 38. Hotel/Hospitality — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Social Proof
- **Style priority:** Liquid Glass + Minimalism
- **Color mood:** Warm neutrals + Gold (#D4AF37)
- **Typography mood:** Elegant + Welcoming typography
- **Key effects:** Room gallery + Amenity reveals
- **Decision rules:** `{"must_have": "room-booking", "must_have": "virtual-tour"}`
- **Anti-patterns:** Poor photos + Complex booking

### 39. Wedding/Event Planning — Severity: HIGH

- **Recommended pattern:** Storytelling + Social Proof
- **Style priority:** Soft UI Evolution + Aurora UI
- **Color mood:** Soft Pink (#FFD6E0) + Gold + Cream
- **Typography mood:** Elegant + Romantic typography
- **Key effects:** Gallery reveals + Timeline animations
- **Decision rules:** `{"must_have": "portfolio-gallery", "must_have": "planning-tools"}`
- **Anti-patterns:** Generic templates + No portfolio

### 40. Legal Services — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Minimal
- **Style priority:** Trust & Authority + Minimalism
- **Color mood:** Navy Blue (#1E3A5F) + Gold + White
- **Typography mood:** Professional + Authoritative typography
- **Key effects:** Practice area reveal + Attorney profile animations
- **Decision rules:** `{"must_have": "case-results", "must_have": "credential-display"}`
- **Anti-patterns:** Outdated design + Hidden credentials + AI purple/pink gradients

### 41. Insurance Platform — Severity: HIGH

- **Recommended pattern:** Conversion + Trust
- **Style priority:** Trust & Authority + Flat Design
- **Color mood:** Trust Blue (#0066CC) + Green + Neutral
- **Typography mood:** Clear + Professional typography
- **Key effects:** Quote calculator animations + Policy comparison
- **Decision rules:** `{"must_have": "quote-calculator", "must_have": "policy-comparison"}`
- **Anti-patterns:** Confusing pricing + No trust signals + AI purple/pink gradients

### 42. Banking/Traditional Finance — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Feature
- **Style priority:** Minimalism + Accessible & Ethical
- **Color mood:** Navy (#0A1628) + Trust Blue + Gold
- **Typography mood:** Professional + Trustworthy typography
- **Key effects:** Smooth number animations + Security indicators
- **Decision rules:** `{"must_have": "security-first", "must_have": "accessibility"}`
- **Anti-patterns:** Playful design + Poor security UX + AI purple/pink gradients

### 43. Online Course/E-learning — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Social Proof
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Vibrant learning colors + Progress green
- **Typography mood:** Friendly + Engaging typography
- **Key effects:** Progress bar animations + Certificate reveals
- **Decision rules:** `{"must_have": "progress-tracking", "must_have": "video-player"}`
- **Anti-patterns:** Boring design + No gamification

### 44. Non-profit/Charity — Severity: HIGH

- **Recommended pattern:** Storytelling + Trust
- **Style priority:** Accessible & Ethical + Organic Biophilic
- **Color mood:** Cause-related colors + Trust + Warm
- **Typography mood:** Heartfelt + Readable typography
- **Key effects:** Impact counter animations + Story reveals
- **Decision rules:** `{"must_have": "impact-stories", "must_have": "donation-transparency"}`
- **Anti-patterns:** No impact data + Hidden financials

### 45. Music Streaming — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Dark Mode (OLED) + Vibrant & Block-based
- **Color mood:** Dark (#121212) + Vibrant accents + Album art colors
- **Typography mood:** Modern + Bold typography
- **Key effects:** Waveform visualization + Playlist animations
- **Decision rules:** `{"must_have": "audio-player-ux", "if_discovery_focused": "add-playlist-recommendations"}`
- **Anti-patterns:** Cluttered layout + Poor audio player UX

### 46. Video Streaming/OTT — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Dark Mode (OLED) + Motion-Driven
- **Color mood:** Dark bg + Poster colors + Brand accent
- **Typography mood:** Bold + Engaging typography
- **Key effects:** Video player animations + Content carousel (parallax)
- **Decision rules:** `{"must_have": "continue-watching", "if_personalized": "add-recommendations"}`
- **Anti-patterns:** Static layout + Slow video player

### 47. Job Board/Recruitment — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized + Feature-Rich
- **Style priority:** Flat Design + Minimalism
- **Color mood:** Professional Blue + Success Green + Neutral
- **Typography mood:** Clear + Professional typography
- **Key effects:** Search/filter animations + Application flow
- **Decision rules:** `{"must_have": "advanced-search", "if_salary_focused": "highlight-compensation"}`
- **Anti-patterns:** Outdated forms + Hidden filters

### 48. Marketplace (P2P) — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Vibrant & Block-based + Flat Design
- **Color mood:** Trust colors + Category colors + Success green
- **Typography mood:** Modern + Engaging typography
- **Key effects:** Review star animations + Listing hover effects
- **Decision rules:** `{"must_have": "seller-profiles", "must_have": "secure-payment"}`
- **Anti-patterns:** Low trust signals + Confusing layout

### 49. Logistics/Delivery — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Real-Time
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Blue (#2563EB) + Orange (tracking) + Green
- **Typography mood:** Clear + Functional typography
- **Key effects:** Real-time tracking animation + Status pulse
- **Decision rules:** `{"must_have": "tracking-map", "must_have": "delivery-updates"}`
- **Anti-patterns:** Static tracking + No map integration + AI purple/pink gradients

### 50. Agriculture/Farm Tech — Severity: MEDIUM

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Organic Biophilic + Flat Design
- **Color mood:** Earth Green (#4A7C23) + Brown + Sky Blue
- **Typography mood:** Clear + Informative typography
- **Key effects:** Data visualization + Weather animations
- **Decision rules:** `{"must_have": "sensor-dashboard", "if_crop_focused": "add-health-indicators"}`
- **Anti-patterns:** Generic design + Ignored accessibility + AI purple/pink gradients

### 51. Construction/Architecture — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Minimalism + 3D & Hyperrealism
- **Color mood:** Grey (#4A4A4A) + Orange (safety) + Blueprint Blue
- **Typography mood:** Professional + Bold typography
- **Key effects:** 3D model viewer + Timeline animations
- **Decision rules:** `{"must_have": "project-portfolio", "if_team_collaboration": "add-real-time-updates"}`
- **Anti-patterns:** 2D-only layouts + Poor image quality + AI purple/pink gradients

### 52. Automotive/Car Dealership — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Motion-Driven + 3D & Hyperrealism
- **Color mood:** Brand colors + Metallic + Dark/Light
- **Typography mood:** Bold + Confident typography
- **Key effects:** 360 product view + Configurator animations
- **Decision rules:** `{"must_have": "vehicle-comparison", "must_have": "financing-calculator"}`
- **Anti-patterns:** Static product pages + Poor UX

### 53. Photography Studio — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Hero-Centric
- **Style priority:** Motion-Driven + Minimalism
- **Color mood:** Black + White + Minimal accent
- **Typography mood:** Elegant + Minimal typography
- **Key effects:** Full-bleed gallery + Before/after reveal
- **Decision rules:** `{"must_have": "portfolio-showcase", "if_booking": "add-calendar-system"}`
- **Anti-patterns:** Heavy text + Poor image showcase

### 54. Coworking Space — Severity: MEDIUM

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Vibrant & Block-based + Glassmorphism
- **Color mood:** Energetic colors + Wood tones + Brand
- **Typography mood:** Modern + Engaging typography
- **Key effects:** Space tour video + Amenity reveal animations
- **Decision rules:** `{"must_have": "virtual-tour", "must_have": "booking-system"}`
- **Anti-patterns:** Outdated photos + Confusing layout

### 55. Home Services (Plumber/Electrician) — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized + Trust
- **Style priority:** Flat Design + Trust & Authority
- **Color mood:** Trust Blue + Safety Orange + Grey
- **Typography mood:** Professional + Clear typography
- **Key effects:** Emergency contact highlight + Service menu animations
- **Decision rules:** `{"must_have": "emergency-contact", "must_have": "certifications-display"}`
- **Anti-patterns:** Hidden contact info + No certifications

### 56. Childcare/Daycare — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Trust
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Playful pastels + Safe colors + Warm
- **Typography mood:** Friendly + Playful typography
- **Key effects:** Parent portal animations + Activity gallery reveal
- **Decision rules:** `{"must_have": "parent-communication", "must_have": "safety-certifications"}`
- **Anti-patterns:** Generic design + Hidden safety info

### 57. Senior Care/Elderly — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Accessible
- **Style priority:** Accessible & Ethical + Soft UI Evolution
- **Color mood:** Calm Blue + Warm neutrals + Large text
- **Typography mood:** Large + Clear typography (18px+)
- **Key effects:** Large touch targets + Clear navigation
- **Decision rules:** `{"must_have": "wcag-aaa", "must_have": "family-portal"}`
- **Anti-patterns:** Small text + Complex navigation + AI purple/pink gradients

### 58. Medical Clinic — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Conversion
- **Style priority:** Accessible & Ethical + Minimalism
- **Color mood:** Medical Blue (#0077B6) + Trust White
- **Typography mood:** Professional + Readable typography
- **Key effects:** Online booking flow + Doctor profile reveals
- **Decision rules:** `{"must_have": "appointment-booking", "must_have": "insurance-info"}`
- **Anti-patterns:** Outdated interface + Confusing booking + AI purple/pink gradients

### 59. Pharmacy/Drug Store — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized + Trust
- **Style priority:** Flat Design + Accessible & Ethical
- **Color mood:** Pharmacy Green + Trust Blue + Clean White
- **Typography mood:** Clear + Functional typography
- **Key effects:** Prescription upload flow + Refill reminders
- **Decision rules:** `{"must_have": "prescription-management", "must_have": "drug-interaction-warnings"}`
- **Anti-patterns:** Confusing layout + Privacy concerns + AI purple/pink gradients

### 60. Dental Practice — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Conversion
- **Style priority:** Soft UI Evolution + Minimalism
- **Color mood:** Fresh Blue + White + Smile Yellow
- **Typography mood:** Friendly + Professional typography
- **Key effects:** Before/after gallery + Patient testimonial carousel
- **Decision rules:** `{"must_have": "before-after-gallery", "must_have": "appointment-system"}`
- **Anti-patterns:** Poor imagery + No testimonials

### 61. Veterinary Clinic — Severity: MEDIUM

- **Recommended pattern:** Social Proof-Focused + Trust
- **Style priority:** Claymorphism + Accessible & Ethical
- **Color mood:** Caring Blue + Pet colors + Warm
- **Typography mood:** Friendly + Welcoming typography
- **Key effects:** Pet profile management + Service animations
- **Decision rules:** `{"must_have": "pet-portal", "must_have": "emergency-contact"}`
- **Anti-patterns:** Generic design + Hidden services

### 62. Florist/Plant Shop — Severity: MEDIUM

- **Recommended pattern:** Hero-Centric + Conversion
- **Style priority:** Organic Biophilic + Vibrant & Block-based
- **Color mood:** Natural Green + Floral pinks/purples
- **Typography mood:** Elegant + Natural typography
- **Key effects:** Product reveal + Seasonal transitions
- **Decision rules:** `{"must_have": "delivery-scheduling", "must_have": "care-guides"}`
- **Anti-patterns:** Poor imagery + No seasonal content

### 63. Bakery/Cafe — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Conversion
- **Style priority:** Vibrant & Block-based + Soft UI Evolution
- **Color mood:** Warm Brown + Cream + Appetizing accents
- **Typography mood:** Warm + Inviting typography
- **Key effects:** Menu hover + Order animations
- **Decision rules:** `{"must_have": "menu-display", "must_have": "online-ordering"}`
- **Anti-patterns:** Poor food photos + Hidden hours

### 64. Brewery/Winery — Severity: HIGH

- **Recommended pattern:** Storytelling + Hero-Centric
- **Style priority:** Motion-Driven + Storytelling-Driven
- **Color mood:** Deep amber/burgundy + Gold + Craft
- **Typography mood:** Artisanal + Heritage typography
- **Key effects:** Tasting note reveals + Heritage timeline
- **Decision rules:** `{"must_have": "product-showcase", "must_have": "story-heritage"}`
- **Anti-patterns:** Generic product pages + No story

### 65. Airline — Severity: HIGH

- **Recommended pattern:** Conversion + Feature-Rich
- **Style priority:** Minimalism + Glassmorphism
- **Color mood:** Sky Blue + Brand colors + Trust
- **Typography mood:** Clear + Professional typography
- **Key effects:** Flight search animations + Boarding pass reveals
- **Decision rules:** `{"must_have": "flight-search", "must_have": "mobile-first"}`
- **Anti-patterns:** Complex booking + Poor mobile

### 66. News/Media Platform — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Brand colors + High contrast
- **Typography mood:** Clear + Readable typography
- **Key effects:** Breaking news badge + Article reveal animations
- **Decision rules:** `{"must_have": "mobile-first-reading", "must_have": "category-navigation"}`
- **Anti-patterns:** Cluttered layout + Slow loading

### 67. Magazine/Blog — Severity: HIGH

- **Recommended pattern:** Storytelling + Hero-Centric
- **Style priority:** Swiss Modernism 2.0 + Motion-Driven
- **Color mood:** Editorial colors + Brand + Clean white
- **Typography mood:** Editorial + Elegant typography
- **Key effects:** Article transitions + Category reveals
- **Decision rules:** `{"must_have": "article-showcase", "must_have": "newsletter-signup"}`
- **Anti-patterns:** Poor typography + Slow loading

### 68. Freelancer Platform — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Conversion
- **Style priority:** Flat Design + Minimalism
- **Color mood:** Professional Blue + Success Green
- **Typography mood:** Clear + Professional typography
- **Key effects:** Skill match animations + Review reveals
- **Decision rules:** `{"must_have": "portfolio-display", "must_have": "skill-matching"}`
- **Anti-patterns:** Poor profiles + No reviews

### 69. Marketing Agency — Severity: HIGH

- **Recommended pattern:** Storytelling + Feature-Rich
- **Style priority:** Brutalism + Motion-Driven
- **Color mood:** Bold brand colors + Creative freedom
- **Typography mood:** Bold + Expressive typography
- **Key effects:** Portfolio reveals + Results animations
- **Decision rules:** `{"must_have": "portfolio", "must_have": "results-metrics"}`
- **Anti-patterns:** Boring design + Hidden work

### 70. Event Management — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Event theme colors + Excitement accents
- **Typography mood:** Bold + Engaging typography
- **Key effects:** Countdown timer + Registration flow
- **Decision rules:** `{"must_have": "registration", "must_have": "agenda-display"}`
- **Anti-patterns:** Confusing registration + No countdown

### 71. Membership/Community — Severity: HIGH

- **Recommended pattern:** Social Proof + Conversion
- **Style priority:** Vibrant & Block-based + Soft UI Evolution
- **Color mood:** Community brand colors + Engagement
- **Typography mood:** Friendly + Engaging typography
- **Key effects:** Member counter + Benefit reveals
- **Decision rules:** `{"must_have": "member-benefits", "must_have": "pricing-tiers"}`
- **Anti-patterns:** Hidden benefits + No community proof

### 72. Newsletter Platform — Severity: MEDIUM

- **Recommended pattern:** Minimal + Conversion
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Brand primary + Clean white + CTA
- **Typography mood:** Clean + Readable typography
- **Key effects:** Subscribe form + Archive reveals
- **Decision rules:** `{"must_have": "subscribe-form", "must_have": "sample-content"}`
- **Anti-patterns:** Complex signup + No preview

### 73. Digital Products/Downloads — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Conversion
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Product colors + Brand + Success green
- **Typography mood:** Modern + Clear typography
- **Key effects:** Product preview + Instant delivery animations
- **Decision rules:** `{"must_have": "product-preview", "must_have": "instant-delivery"}`
- **Anti-patterns:** No preview + Slow delivery

### 74. Church/Religious Organization — Severity: MEDIUM

- **Recommended pattern:** Hero-Centric + Social Proof
- **Style priority:** Accessible & Ethical + Soft UI Evolution
- **Color mood:** Warm Gold + Deep Purple/Blue + White
- **Typography mood:** Welcoming + Clear typography
- **Key effects:** Service time highlights + Event calendar
- **Decision rules:** `{"must_have": "service-times", "must_have": "community-events"}`
- **Anti-patterns:** Outdated design + Hidden info

### 75. Sports Team/Club — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Feature-Rich
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Team colors + Energetic accents
- **Typography mood:** Bold + Impactful typography
- **Key effects:** Score animations + Schedule reveals
- **Decision rules:** `{"must_have": "schedule", "must_have": "roster"}`
- **Anti-patterns:** Static content + Poor fan engagement

### 76. Museum/Gallery — Severity: HIGH

- **Recommended pattern:** Storytelling + Feature-Rich
- **Style priority:** Minimalism + Motion-Driven
- **Color mood:** Art-appropriate neutrals + Exhibition accents
- **Typography mood:** Elegant + Minimal typography
- **Key effects:** Virtual tour + Collection reveals
- **Decision rules:** `{"must_have": "virtual-tour", "must_have": "exhibition-info"}`
- **Anti-patterns:** Cluttered layout + No online access

### 77. Theater/Cinema — Severity: HIGH

- **Recommended pattern:** Hero-Centric + Conversion
- **Style priority:** Dark Mode (OLED) + Motion-Driven
- **Color mood:** Dark + Spotlight accents + Gold
- **Typography mood:** Dramatic + Bold typography
- **Key effects:** Seat selection + Trailer reveals
- **Decision rules:** `{"must_have": "showtimes", "must_have": "seat-selection"}`
- **Anti-patterns:** Poor booking UX + No trailers

### 78. Language Learning App — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Social Proof
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Playful colors + Progress indicators
- **Typography mood:** Friendly + Clear typography
- **Key effects:** Progress animations + Achievement unlocks
- **Decision rules:** `{"must_have": "progress-tracking", "must_have": "gamification"}`
- **Anti-patterns:** Boring design + No motivation

### 79. Coding Bootcamp — Severity: HIGH

- **Recommended pattern:** Feature-Rich + Social Proof
- **Style priority:** Dark Mode (OLED) + Minimalism
- **Color mood:** Code editor colors + Brand + Success
- **Typography mood:** Technical + Clear typography
- **Key effects:** Terminal animations + Career outcome reveals
- **Decision rules:** `{"must_have": "curriculum", "must_have": "career-outcomes"}`
- **Anti-patterns:** Light mode only + Hidden results

### 80. Cybersecurity Platform — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Real-Time
- **Style priority:** Cyberpunk UI + Dark Mode (OLED)
- **Color mood:** Matrix Green (#00FF00) + Deep Black
- **Typography mood:** Technical + Clear typography
- **Key effects:** Threat visualization + Alert animations
- **Decision rules:** `{"must_have": "real-time-monitoring", "must_have": "threat-display"}`
- **Anti-patterns:** Light mode + Poor data viz

### 81. Developer Tool / IDE — Severity: HIGH

- **Recommended pattern:** Minimal + Documentation
- **Style priority:** Dark Mode (OLED) + Minimalism
- **Color mood:** Dark syntax theme + Blue focus
- **Typography mood:** Monospace + Functional typography
- **Key effects:** Syntax highlighting + Command palette
- **Decision rules:** `{"must_have": "keyboard-shortcuts", "must_have": "documentation"}`
- **Anti-patterns:** Light mode default + Slow performance

### 82. Biotech / Life Sciences — Severity: HIGH

- **Recommended pattern:** Storytelling + Data
- **Style priority:** Glassmorphism + Clean Science
- **Color mood:** Sterile White + DNA Blue + Life Green
- **Typography mood:** Scientific + Clear typography
- **Key effects:** Data visualization + Research reveals
- **Decision rules:** `{"must_have": "data-accuracy", "must_have": "clean-aesthetic"}`
- **Anti-patterns:** Cluttered data + Poor credibility

### 83. Space Tech / Aerospace — Severity: HIGH

- **Recommended pattern:** Immersive + Feature-Rich
- **Style priority:** Holographic/HUD + Dark Mode
- **Color mood:** Deep Space Black + Star White + Metallic
- **Typography mood:** Futuristic + Precise typography
- **Key effects:** Telemetry animations + 3D renders
- **Decision rules:** `{"must_have": "high-tech-feel", "must_have": "precision-data"}`
- **Anti-patterns:** Generic design + No immersion

### 84. Architecture / Interior — Severity: HIGH

- **Recommended pattern:** Portfolio + Hero-Centric
- **Style priority:** Exaggerated Minimalism + High Imagery
- **Color mood:** Monochrome + Gold Accent + High Imagery
- **Typography mood:** Architectural + Elegant typography
- **Key effects:** Project gallery + Blueprint reveals
- **Decision rules:** `{"must_have": "high-res-images", "must_have": "project-portfolio"}`
- **Anti-patterns:** Poor imagery + Cluttered layout

### 85. Quantum Computing Interface — Severity: HIGH

- **Recommended pattern:** Immersive + Interactive
- **Style priority:** Holographic/HUD + Dark Mode
- **Color mood:** Quantum Blue (#00FFFF) + Deep Black
- **Typography mood:** Futuristic + Scientific typography
- **Key effects:** Probability visualizations + Qubit state animations
- **Decision rules:** `{"must_have": "complexity-visualization", "must_have": "scientific-credibility"}`
- **Anti-patterns:** Generic tech design + No viz

### 86. Biohacking / Longevity App — Severity: HIGH

- **Recommended pattern:** Data-Dense + Storytelling
- **Style priority:** Biomimetic/Organic 2.0 + Minimalism
- **Color mood:** Cellular Pink/Red + DNA Blue + White
- **Typography mood:** Scientific + Clear typography
- **Key effects:** Biological data viz + Progress animations
- **Decision rules:** `{"must_have": "data-privacy", "must_have": "scientific-credibility"}`
- **Anti-patterns:** Generic health app + No privacy

### 87. Autonomous Drone Fleet Manager — Severity: HIGH

- **Recommended pattern:** Real-Time + Feature-Rich
- **Style priority:** HUD/Sci-Fi FUI + Real-Time
- **Color mood:** Tactical Green + Alert Red + Map Dark
- **Typography mood:** Technical + Functional typography
- **Key effects:** Telemetry animations + 3D spatial awareness
- **Decision rules:** `{"must_have": "real-time-telemetry", "must_have": "safety-alerts"}`
- **Anti-patterns:** Slow updates + Poor spatial viz

### 88. Generative Art Platform — Severity: HIGH

- **Recommended pattern:** Showcase + Feature-Rich
- **Style priority:** Minimalism + Gen Z Chaos
- **Color mood:** Neutral (#F5F5F5) + User Content
- **Typography mood:** Minimal + Content-focused typography
- **Key effects:** Gallery masonry + Minting animations
- **Decision rules:** `{"must_have": "fast-loading", "must_have": "creator-attribution"}`
- **Anti-patterns:** Heavy chrome + Slow loading

### 89. Spatial Computing OS / App — Severity: HIGH

- **Recommended pattern:** Immersive + Interactive
- **Style priority:** Spatial UI (VisionOS) + Glassmorphism
- **Color mood:** Frosted Glass + System Colors + Depth
- **Typography mood:** Spatial + Readable typography
- **Key effects:** Depth hierarchy + Gaze interactions
- **Decision rules:** `{"must_have": "depth-hierarchy", "must_have": "environment-awareness"}`
- **Anti-patterns:** 2D design + No spatial depth

### 90. Sustainable Energy / Climate Tech — Severity: HIGH

- **Recommended pattern:** Data + Trust
- **Style priority:** Organic Biophilic + E-Ink/Paper
- **Color mood:** Earth Green + Sky Blue + Solar Yellow
- **Typography mood:** Clear + Informative typography
- **Key effects:** Impact viz + Progress animations
- **Decision rules:** `{"must_have": "data-transparency", "must_have": "impact-visualization"}`
- **Anti-patterns:** Greenwashing + No real data

### 91. Personal Finance Tracker — Severity: HIGH

- **Recommended pattern:** Interactive Product Demo
- **Style priority:** Glassmorphism + Dark Mode (OLED)
- **Color mood:** Calm blue + success green + alert red + chart accents
- **Typography mood:** Modern + Clear hierarchy
- **Key effects:** Backdrop blur (10-20px) + Translucent overlays
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_low_performance": "fallback-to-flat"}`
- **Anti-patterns:** Pure white backgrounds

### 92. Chat & Messaging App — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Demo
- **Style priority:** Minimalism + Micro-interactions
- **Color mood:** Brand primary + bubble contrast (sender/receiver) + typing grey
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration

### 93. Notes & Writing App — Severity: HIGH

- **Recommended pattern:** Minimal & Direct
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Clean white/cream + minimal accent + editor syntax colors
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 94. Habit Tracker — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Demo
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Streak warm (amber/orange) + progress green + motivational accents
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Muted colors + Low energy

### 95. Food Delivery / On-Demand — Severity: HIGH

- **Recommended pattern:** Hero-Centric Design + Feature-Rich
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Appetizing warm (orange/red) + trust blue + map accent
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Scroll animations + Parallax + Page transitions
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Muted colors + Low energy

### 96. Ride Hailing / Transportation — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized + Demo
- **Style priority:** Minimalism + Glassmorphism
- **Color mood:** Brand primary + map neutral + status indicator colors
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Backdrop blur (10-20px) + Translucent overlays
- **Decision rules:** `{"if_low_performance": "fallback-to-flat", "if_conversion_focused": "add-urgency-colors"}`
- **Anti-patterns:** Excessive decoration

### 97. Recipe & Cooking App — Severity: HIGH

- **Recommended pattern:** Hero-Centric Design + Feature-Rich
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Warm food tones (terracotta/sage/cream) + appetizing imagery
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Muted colors + Low energy

### 98. Meditation & Mindfulness — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Social Proof
- **Style priority:** Neumorphism + Soft UI Evolution
- **Color mood:** Ultra-calm pastels (lavender/sage/sky) + breathing animation gradient
- **Typography mood:** Subtle + Soft + Monochromatic
- **Key effects:** Dual shadows (light+dark) + Soft press 150ms
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 99. Weather App — Severity: HIGH

- **Recommended pattern:** Hero-Centric Design
- **Style priority:** Glassmorphism + Aurora UI
- **Color mood:** Atmospheric gradients (sky blue → sunset → storm grey) + temp scale
- **Typography mood:** Modern + Clear hierarchy
- **Key effects:** Backdrop blur (10-20px) + Translucent overlays
- **Decision rules:** `{"if_low_performance": "fallback-to-flat"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 100. Diary & Journal App — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven
- **Style priority:** Soft UI Evolution + Minimalism
- **Color mood:** Warm paper tones (cream/linen) + muted ink + mood-coded accents
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration

### 101. CRM & Client Management — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Demo
- **Style priority:** Flat Design + Minimalism
- **Color mood:** Professional blue + pipeline stage colors + closed-won green
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 102. Inventory & Stock Management — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Flat Design + Minimalism
- **Color mood:** Functional neutral + status traffic-light (green/amber/red) + scanner accent
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 103. Flashcard & Study Tool — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Demo
- **Style priority:** Claymorphism + Micro-interactions
- **Color mood:** Playful primary + correct green + incorrect red + progress blue
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 104. Booking & Appointment App — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized
- **Style priority:** Soft UI Evolution + Flat Design
- **Color mood:** Trust blue + available green + booked grey + confirm accent
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_conversion_focused": "add-urgency-colors"}`
- **Anti-patterns:** Complex shadows + 3D effects

### 105. Invoice & Billing Tool — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized + Trust
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Professional navy + paid green + overdue red + neutral grey
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_conversion_focused": "add-urgency-colors"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 106. Grocery & Shopping List — Severity: HIGH

- **Recommended pattern:** Minimal & Direct + Demo
- **Style priority:** Flat Design + Vibrant & Block-based
- **Color mood:** Fresh green + food-category colors + checkmark accent
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Complex shadows + 3D effects + Muted colors + Low energy

### 107. Timer & Pomodoro — Severity: HIGH

- **Recommended pattern:** Minimal & Direct
- **Style priority:** Minimalism + Neumorphism
- **Color mood:** High-contrast on dark + focus red/amber + break green
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Dual shadows (light+dark) + Soft press 150ms
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration

### 108. Parenting & Baby Tracker — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Trust
- **Style priority:** Claymorphism + Soft UI Evolution
- **Color mood:** Soft pastels (baby pink/sky blue/mint/peach) + warm accents
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 109. Scanner & Document Manager — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Demo
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Clean white + camera viewfinder accent + file-type color coding
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 110. Calendar & Scheduling App — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Demo
- **Style priority:** Flat Design + Micro-interactions
- **Color mood:** Clean blue + event category accent colors + success green
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Complex shadows + 3D effects

### 111. Password Manager — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Feature-Rich
- **Style priority:** Minimalism + Accessible & Ethical
- **Color mood:** Trust blue + security green + dark neutral
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Color-only indicators

### 112. Expense Splitter / Bill Split — Severity: HIGH

- **Recommended pattern:** Minimal & Direct + Demo
- **Style priority:** Flat Design + Vibrant & Block-based
- **Color mood:** Success green + alert red + neutral grey + avatar accent colors
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Complex shadows + 3D effects + Muted colors + Low energy

### 113. Voice Recorder & Memo — Severity: HIGH

- **Recommended pattern:** Interactive Product Demo + Minimal
- **Style priority:** Minimalism + AI-Native UI
- **Color mood:** Clean white + recording red + waveform accent
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration

### 114. Bookmark & Read-Later — Severity: HIGH

- **Recommended pattern:** Minimal & Direct + Demo
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Paper warm white + ink neutral + minimal accent + tag colors
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 115. Translator App — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Interactive Demo
- **Style priority:** Flat Design + AI-Native UI
- **Color mood:** Global blue + neutral grey + language flag accent
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Complex shadows + 3D effects

### 116. Calculator & Unit Converter — Severity: HIGH

- **Recommended pattern:** Minimal & Direct
- **Style priority:** Neumorphism + Minimalism
- **Color mood:** Dark functional + orange operation keys + clear button hierarchy
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Dual shadows (light+dark) + Soft press 150ms
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration

### 117. Alarm & World Clock — Severity: HIGH

- **Recommended pattern:** Minimal & Direct
- **Style priority:** Dark Mode (OLED) + Minimalism
- **Color mood:** Deep dark + ambient glow accent + timezone gradient
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle"}`
- **Anti-patterns:** Excessive decoration + Pure white backgrounds

### 118. File Manager & Transfer — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Demo
- **Style priority:** Flat Design + Minimalism
- **Color mood:** Functional neutral + file type color coding (PDF orange, doc blue, image purple)
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 119. Email Client — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Demo
- **Style priority:** Flat Design + Minimalism
- **Color mood:** Clean white + brand primary + priority red + snooze amber
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 120. Casual Puzzle Game — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Cheerful pastels + progression gradient + reward gold + bright accent
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Muted colors + Low energy

### 121. Trivia & Quiz Game — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Vibrant & Block-based + Micro-interactions
- **Color mood:** Energetic blue + correct green + incorrect red + leaderboard gold
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Haptic feedback + Small 50-100ms animations
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Muted colors + Low energy

### 122. Card & Board Game — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** 3D & Hyperrealism + Flat Design
- **Color mood:** Game-theme felt green + dark wood + card back patterns
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Complex shadows + 3D effects

### 123. Idle & Clicker Game — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Coin gold + upgrade blue + prestige purple + progress green
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Scroll animations + Parallax + Page transitions
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Muted colors + Low energy

### 124. Word & Crossword Game — Severity: HIGH

- **Recommended pattern:** Minimal & Direct + Demo
- **Style priority:** Minimalism + Flat Design
- **Color mood:** Clean white + warm letter tiles + success green + shake red
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration + Complex shadows + 3D effects

### 125. Arcade & Retro Game — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Hero-Centric
- **Style priority:** Pixel Art + Retro-Futurism
- **Color mood:** Neon on black + pixel palette + score gold + danger red
- **Typography mood:** Nostalgic + Monospace + Neon
- **Key effects:** Subtle hover (200ms) + Smooth transitions
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 126. Photo Editor & Filters — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Interactive Demo
- **Style priority:** Minimalism + Dark Mode (OLED)
- **Color mood:** Dark editor background + vibrant filter preview strip + tool icon accent
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle"}`
- **Anti-patterns:** Excessive decoration + Pure white backgrounds

### 127. Short Video Editor — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Hero-Centric
- **Style priority:** Dark Mode (OLED) + Motion-Driven
- **Color mood:** Dark background + timeline track accent colors + effect preview vivid
- **Typography mood:** High contrast + Light on dark
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle"}`
- **Anti-patterns:** Pure white backgrounds

### 128. Drawing & Sketching Canvas — Severity: HIGH

- **Recommended pattern:** Interactive Product Demo + Storytelling
- **Style priority:** Minimalism + Dark Mode (OLED)
- **Color mood:** Neutral canvas + full-spectrum color picker + tool panel dark
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle"}`
- **Anti-patterns:** Excessive decoration + Pure white backgrounds

### 129. Music Creation & Beat Maker — Severity: HIGH

- **Recommended pattern:** Interactive Product Demo + Storytelling
- **Style priority:** Dark Mode (OLED) + Motion-Driven
- **Color mood:** Dark studio background + track colors rainbow + waveform accent + BPM pulse
- **Typography mood:** High contrast + Light on dark
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle"}`
- **Anti-patterns:** Pure white backgrounds

### 130. Meme & Sticker Maker — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Vibrant & Block-based + Flat Design
- **Color mood:** Bold primary + comedic yellow + viral red + high saturation accent
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Complex shadows + 3D effects + Muted colors + Low energy

### 131. AI Photo & Avatar Generator — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** AI-Native UI + Aurora UI
- **Color mood:** AI purple + aurora gradients + before/after neutral
- **Typography mood:** Elegant + Gradient-friendly
- **Key effects:** Flowing gradients 8-12s + Color morphing
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 132. Link-in-Bio Page Builder — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized + Social Proof
- **Style priority:** Vibrant & Block-based + Bento Box Grid
- **Color mood:** Brand-customizable + accent link color + clean white canvas
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Large section gaps 48px+ + Color shift hover + Scroll-snap
- **Decision rules:** `{"if_conversion_focused": "add-urgency-colors", "if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Muted colors + Low energy

### 133. Wardrobe & Outfit Planner — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Feature-Rich
- **Style priority:** Minimalism + Motion-Driven
- **Color mood:** Clean fashion neutral + full clothes color palette + accent
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration

### 134. Plant Care Tracker — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Social Proof
- **Style priority:** Organic Biophilic + Soft UI Evolution
- **Color mood:** Nature greens + earth brown + sunny yellow reminder + water blue
- **Typography mood:** Warm + Humanist + Natural
- **Key effects:** Rounded 16-24px + Natural shadows + Flowing SVG
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 135. Book & Reading Tracker — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Feature-Rich
- **Style priority:** Swiss Modernism 2.0 + Minimalism
- **Color mood:** Warm paper white + ink brown + reading progress green + book cover colors
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Excessive decoration

### 136. Couple & Relationship App — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Social Proof
- **Style priority:** Aurora UI + Soft UI Evolution
- **Color mood:** Warm romantic pink/rose + soft gradient + memory photo tones
- **Typography mood:** Elegant + Gradient-friendly
- **Key effects:** Flowing gradients 8-12s + Color morphing
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 137. Family Calendar & Chores — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Flat Design + Claymorphism
- **Color mood:** Warm playful + member color coding + chore completion green
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Complex shadows + 3D effects

### 138. Mood Tracker — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Social Proof
- **Style priority:** Soft UI Evolution + Minimalism
- **Color mood:** Emotion gradient (blue sad to yellow happy) + pastel per mood + insight accent
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Excessive decoration

### 139. Gift & Wishlist — Severity: HIGH

- **Recommended pattern:** Minimal & Direct + Conversion
- **Style priority:** Vibrant & Block-based + Soft UI Evolution
- **Color mood:** Celebration warm pink/gold/red + category colors + surprise accent
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Large section gaps 48px+ + Color shift hover + Scroll-snap
- **Decision rules:** `{"if_conversion_focused": "add-urgency-colors"}`
- **Anti-patterns:** Muted colors + Low energy

### 140. Running & Cycling GPS — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Dark Mode (OLED) + Vibrant & Block-based
- **Color mood:** Energetic orange + map accent + pace zones (green/yellow/red)
- **Typography mood:** High contrast + Light on dark
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Pure white backgrounds + Muted colors + Low energy

### 141. Yoga & Stretching Guide — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Social Proof
- **Style priority:** Organic Biophilic + Soft UI Evolution
- **Color mood:** Earth calming sage/terracotta/cream + breathing gradient + warm accent
- **Typography mood:** Warm + Humanist + Natural
- **Key effects:** Rounded 16-24px + Natural shadows + Flowing SVG
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 142. Sleep Tracker — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Dark Mode (OLED) + Neumorphism
- **Color mood:** Deep midnight blue + stars/moon accent + sleep quality gradient (poor red to great green)
- **Typography mood:** High contrast + Light on dark
- **Key effects:** Dual shadows (light+dark) + Soft press 150ms
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Pure white backgrounds

### 143. Calorie & Nutrition Counter — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Flat Design + Vibrant & Block-based
- **Color mood:** Healthy green + macro colors (protein blue, carb orange, fat yellow) + progress circle
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Complex shadows + 3D effects + Muted colors + Low energy

### 144. Period & Cycle Tracker — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Trust
- **Style priority:** Soft UI Evolution + Aurora UI
- **Color mood:** Rose/blush + lavender + fertility green + soft calendar tones
- **Typography mood:** Elegant + Gradient-friendly
- **Key effects:** Flowing gradients 8-12s + Color morphing
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 145. Medication & Pill Reminder — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Feature-Rich
- **Style priority:** Accessible & Ethical + Flat Design
- **Color mood:** Medical trust blue + missed alert red + taken green + clean white
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Complex shadows + 3D effects + Color-only indicators

### 146. Water & Hydration Reminder — Severity: HIGH

- **Recommended pattern:** Minimal & Direct + Demo
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Refreshing blue + water wave animation + goal progress accent
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Muted colors + Low energy

### 147. Fasting & Intermittent Timer — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Minimalism + Dark Mode (OLED)
- **Color mood:** Fasting deep blue/purple + eating window green + timeline neutral
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Excessive decoration + Pure white backgrounds

### 148. Anonymous Community / Confession — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Feature-Rich
- **Style priority:** Dark Mode (OLED) + Minimalism
- **Color mood:** Dark protective + subtle gradient + upvote green + empathy warm accent
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Excessive decoration + Pure white backgrounds

### 149. Local Events & Discovery — Severity: HIGH

- **Recommended pattern:** Hero-Centric Design + Feature-Rich
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** City vibrant + event category colors + map accent + date highlight
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Scroll animations + Parallax + Page transitions
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Muted colors + Low energy

### 150. Study Together / Virtual Coworking — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Feature-Rich
- **Style priority:** Minimalism + Soft UI Evolution
- **Color mood:** Calm focus blue + session progress indicator + ambient warm neutrals
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Excessive decoration

### 151. Coding Challenge & Practice — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Dark Mode (OLED) + Cyberpunk UI
- **Color mood:** Code editor dark + success green + difficulty gradient (easy green / medium amber / hard red)
- **Typography mood:** High contrast + Light on dark
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Pure white backgrounds

### 152. Kids Learning (ABC & Math) — Severity: HIGH

- **Recommended pattern:** Social Proof-Focused + Trust
- **Style priority:** Claymorphism + Vibrant & Block-based
- **Color mood:** Bright primary + child-safe pastels + reward gold + interactive accent
- **Typography mood:** Playful + Rounded + Friendly
- **Key effects:** Multi-layer shadows + Spring bounce + Soft press 200ms
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Muted colors + Low energy

### 153. Music Instrument Learning — Severity: HIGH

- **Recommended pattern:** Interactive Product Demo + Social Proof
- **Style priority:** Vibrant & Block-based + Motion-Driven
- **Color mood:** Musical warm deep red/brown + note color system + skill progress bar
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Scroll animations + Parallax + Page transitions
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Muted colors + Low energy

### 154. Parking Finder — Severity: HIGH

- **Recommended pattern:** Conversion-Optimized + Feature-Rich
- **Style priority:** Minimalism + Glassmorphism
- **Color mood:** Trust blue + available green + occupied red + map neutral
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Backdrop blur (10-20px) + Translucent overlays
- **Decision rules:** `{"if_low_performance": "fallback-to-flat", "if_conversion_focused": "add-urgency-colors"}`
- **Anti-patterns:** Excessive decoration

### 155. Public Transit Guide — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Interactive Demo
- **Style priority:** Flat Design + Accessible & Ethical
- **Color mood:** Transit brand line colors + real-time indicator green/red + map neutral
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Complex shadows + 3D effects + Color-only indicators

### 156. Road Trip Planner — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Hero-Centric
- **Style priority:** Aurora UI + Organic Biophilic
- **Color mood:** Adventure warm sunset orange + map teal + stop markers + road neutral
- **Typography mood:** Elegant + Gradient-friendly
- **Key effects:** Flowing gradients 8-12s + Color morphing
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Inconsistent styling + Poor contrast ratios

### 157. VPN & Privacy Tool — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Conversion-Optimized
- **Style priority:** Minimalism + Dark Mode (OLED)
- **Color mood:** Dark shield blue + connected green + disconnected red + trust accent
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_conversion_focused": "add-urgency-colors"}`
- **Anti-patterns:** Excessive decoration + Pure white backgrounds

### 158. Emergency SOS & Safety — Severity: HIGH

- **Recommended pattern:** Trust & Authority + Social Proof
- **Style priority:** Accessible & Ethical + Flat Design
- **Color mood:** Alert red + safety blue + location green + high contrast critical
- **Typography mood:** Bold + Clean + Sans-serif
- **Key effects:** Color shift hover + Fast 150ms transitions + No shadows
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Complex shadows + 3D effects + Color-only indicators

### 159. Wallpaper & Theme App — Severity: HIGH

- **Recommended pattern:** Feature-Rich Showcase + Social Proof
- **Style priority:** Vibrant & Block-based + Aurora UI
- **Color mood:** Content-driven + trending aesthetic palettes + download accent
- **Typography mood:** Energetic + Bold + Large
- **Key effects:** Large section gaps 48px+ + Color shift hover + Scroll-snap
- **Decision rules:** `{"if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Muted colors + Low energy

### 160. White Noise & Ambient Sound — Severity: HIGH

- **Recommended pattern:** Minimal & Direct + Social Proof
- **Style priority:** Minimalism + Dark Mode (OLED)
- **Color mood:** Calming dark + ambient texture visual + subtle sound wave + sleep blue
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle glow + Neon accents + High contrast
- **Decision rules:** `{"if_light_mode_needed": "provide-theme-toggle", "if_trust_needed": "add-testimonials"}`
- **Anti-patterns:** Excessive decoration + Pure white backgrounds

### 161. Home Decoration & Interior Design — Severity: HIGH

- **Recommended pattern:** Storytelling-Driven + Feature-Rich
- **Style priority:** Minimalism + 3D Product Preview
- **Color mood:** Neutral interior palette + material texture accent + AR blue
- **Typography mood:** Professional + Clean hierarchy
- **Key effects:** Subtle hover 200ms + Smooth transitions + Clean
- **Decision rules:** `{"if_ux_focused": "prioritize-clarity", "if_mobile": "optimize-touch-targets"}`
- **Anti-patterns:** Excessive decoration
