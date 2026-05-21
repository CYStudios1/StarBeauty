# Star Beauty Supply -- Shared Content Bible

All three concepts pull from this single source of truth. Copy is final unless noted.

---

## Brand Identity

**Founded:** 1995
**Locations:** 7 active stores across Chicago's South and West sides
**Primary audience:** Black women in Chicago -- the customer who knows exactly what she needs AND the customer discovering her next look
**Brand position:** The neighborhood beauty authority that's been here longer than most chains. Premium without pretension. Chicago-rooted, culture-first.

---

## Store Locations

| Store | Address | Phone |
|-------|---------|-------|
| Star Beauty 1 | 1250 S Ashland Ave, Chicago, IL 60608 | (312) 285-2141 |
| Star Beauty 2 | 3258 W 87th St, Chicago, IL 60652 | (773) 434-5745 |
| Star Beauty 3 | 1637 E 95th St, Chicago, IL 60617 | (773) 902-7277 |
| Star Beauty 4 | 5400 W Chicago Ave, Chicago, IL 60651 | (773) 921-0995 |
| Star Beauty 5 | 800 N Kedzie Ave, Chicago, IL 60651 | (773) 638-4411 |
| Star Beauty 8 | 4937 W North Ave, Chicago, IL 60639 | (773) 394-6040 |
| Star Beauty 9 | 7546 S Stony Island Ave, Chicago, IL 60649 | (773) 966-4704 |

**Hours:** Mon--Sat 9 AM -- 8 PM | Sun 10 AM -- 6 PM

---

## May/June 2026 Mom Sale

### Bundles & Hair
- Pink Lemon 15A 3pc unprocessed human hair -- from **$74.99**
- Gold Luster 3pc human hair -- from **$69.99**
- Dream Weaver 3pc human hair -- from **$64.99**

### Braiding
- Outre X-Pression 3X Pre-Stretched Braid -- from **$2.99/ea**
- Sensationnel Empire Deep Bulk for Boho Braids -- **$29.99** (14")

### Tools & Styling
- Hot & Hotter Turbo Pro 4000 Stand Dryer -- **$79.99**
- BTL Braiding Gel 16oz -- **$8.99**

### Color & Care
- Adore Semi-Permanent Hair Color -- **$3.99**
- Bigen #59 Powder Hair Color -- **$3.99**
- Murray's Edgewax 4oz -- **$3.99**
- ORS Olive Oil Sheen Spray 10oz -- **$4.99**

### Star Exclusives & Oils
- Star Care Batana Oil/Butter -- **$6.99**
- Jamaican Mango & Lime Island Oil 8oz -- **$3.99**

---

## Brand Voice Guidelines

**Tone:** Confident, warm, Chicago-rooted. Celebrates Black hair as the centerpiece -- not a niche, not a segment, the main event.

**Register:** Premium without being sterile. Like a trusted neighborhood spot that elevated its game. The woman behind the counter who remembers your name and your texture.

**Sentence structure:** Short. Declarative. Specific word choice over flowery language.

**Avoid:** Corporate-speak. Preachy language. "Empower" / "celebrate diversity" / "inclusive beauty" -- show it, don't say it.

**Examples of good copy:**
- "Seven stores. One standard."
- "Your texture. Our obsession."
- "Since '95, we've stocked what Chicago actually uses."
- "The sale your group chat's been waiting for."
- "Real hair. Real prices. No games."
- "We don't do basic."

**Examples of bad copy:**
- "Discover your beauty journey today!"
- "Empowering women through inclusive beauty solutions"
- "Shop our curated collection of premium hair care products"

---

## Shared Components Spec

### A) Welcome Discount Modal

**Trigger:** 2 seconds after first page load. Use `sessionStorage.setItem('star_modal_shown', 'true')` to prevent re-trigger.

**Layout:**
- Mobile: full-screen sheet, slides up from bottom
- Desktop: centered modal, `max-width: 480px`, backdrop blur overlay

**Content:**
- Headline: "5% off, on the house."
- Subline: "Join the list. New drops, real sales, no spam -- texted straight to you when it matters."
- Email input (placeholder: "you@email.com")
- Phone input (placeholder: "(312) 555-0199") + checkbox: "Text me deals (2--4/month, reply STOP anytime)"
- CTA button: "Send me my code"
- Dismiss: small text link "Maybe later" -- not a button, not prominent

**Success State:**
- Animated reveal of code **MOM5OFF**
- Copy-to-clipboard button (with micro-animation on copy)
- Below code: "Show at any Star Beauty location"
- The success state replaces the form, same container

**Validation:**
- Email: standard regex, red inline error
- Phone: US format (10 digits), format as typed

---

### B) AI Stylist Chat

**Button:** 56px circle, bottom-right corner, 24px from edges. Concept-styled. Subtle pulse animation (2s interval, scale 1.0 to 1.05).

**Panel:**
- Desktop: 380px wide, slides in from right, height 520px
- Mobile: full-screen overlay with top safe-area padding

**Header:**
- Avatar (concept-styled) + Name + close (X) button
- Names per concept:
  - Editorial Premium: "Star Stylist"
  - Vibrant Modern: "Ask Star"
  - Neighborhood Trusted: "Ask Maya"

**Welcome state:** Bot message appears first, then 3 quick-reply chips:
1. "What's on sale?"
2. "Help me pick a wig"
3. "Closest store?"

**Scripted conversation:**

> **User:** "I have a wedding in 3 weeks. Need a wig that's elegant but not too formal."
>
> *[600ms typing indicator -- 3 animated dots]*
>
> **Bot:** "Congrats! For elegant-but-relaxed, our Gold Luster body wave bundles ($69.99 starting) photograph beautifully. If you want ready-to-wear, the Mane Concept 15A is a clean $34.99 pick. Want me to check stock near you?"
>
> **User:** "Yes, near 87th."
>
> *[600ms typing indicator]*
>
> **Bot:** "Star Beauty 2 on 87th & Kedzie has both. Open till 8 PM tonight. Want me to hold one?"
>
> *[Reserve button -- inline, concept-styled]*
>
> **User clicks Reserve**
>
> **Bot:** "Got it. We'll text when it's ready -- usually within the hour. Anything else?"

**Input:** Text field with send button (arrow or paper-plane icon, concept-styled). Disabled after scripted conversation ends.

**Footer:** "Powered by Star Beauty" in small caps, muted text.

---

### C) Footer Signup

Present on every page.

- Headline matches concept voice
- Desktop: two-field horizontal form (email + phone), single submit
- Mobile: stacked fields
- Same 5% code reveal on success (inline, no page reload)
- Success message: "Check your inbox. Code: MOM5OFF"

---

### D) /join.html -- Dedicated Landing Page

**Hero:** The 5% offer IS the headline. Not buried below a hero image.

**Three reasons to join (concept-styled cards or list):**
1. "Members get the new drops first."
2. "Texted-only sales -- not on the site, not on socials."
3. "$5 birthday treat, every single year."

**Form:** Same fields as modal, but larger and more prominent.

**Trust copy:** "We text 2--4 times a month. We never sell your info. Reply STOP anytime."

---

## Data Points to Use as Design Elements

These numbers should appear visually prominent somewhere in each concept -- treated as typography moments, not buried in body copy:

- **1995** -- the year Star Beauty opened its doors
- **7** -- stores across Chicago
- **29** -- years serving the South and West sides
- **$2.99** -- braids starting price (shows value)
- **9 AM -- 8 PM** -- we're open when you need us
