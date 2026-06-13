# Safe Phishing Awareness Project - Dadlı Süfrə

## Project Overview

This is an **educational phishing awareness project** designed as a restaurant scenario to teach users about the differences between legitimate websites and phishing attempts. The project uses "Dadlı Süfrə," a traditional Azerbaijani restaurant in Baku, as the case study.

**Purpose:** Demonstrate how phishing websites can look identical to real websites and highlight the importance of being cautious with login pages and QR codes.

---

## File Structure & Descriptions

### Real Website
#### **index.html** - The Legitimate Restaurant Website
- **Purpose:** Represents the authentic, real restaurant website with a genuine QR code
- **Features:**
  - Beautiful, professional design with traditional Azerbaijani aesthetic
  - Color scheme: warm tones (pomegranate #b3422b, saffron #d6a23f, teal #4d6b63, olive #8c7f50)
  - Typography: Fraunces serif fonts for headers, Work Sans for body
  - Contains restaurant information and QR-based menu system
  - This is what users should trust and use for the real experience

---

### Fake/Phishing Website
#### **index_fake.html** - The Phishing/Fake Website
- **Purpose:** Mimics the real website design to demonstrate how phishing attempts look identical
- **Features:**
  - Appears visually identical to `index.html`
  - Uses the same styling, fonts, and color scheme
  - Contains a fake QR code (instead of a real one)
  - **Warning:** This is the attack vector - users scanning this QR would be directed to the phishing login page
  - Shows why visual similarity alone cannot be trusted; users must verify URLs and legitimacy

---

### Login Pages

#### **login_normal.html** - Legitimate Login Page
- **Purpose:** The real login page for authorized users
- **Features:**
  - Clean, professional login form
  - Fields: User email/ID and password
  - Form action: Submits to `success.html` (legitimate path)
  - Matches the restaurant's branding and aesthetic
  - **Safe to use:** This is connected to the real backend/system

#### **login_simulation.html** - Phishing/Fake Login Page
- **Purpose:** Demonstrates a fake login page that could steal credentials
- **Features:**
  - Nearly identical styling to `login_normal.html`
  - Same form layout and branding
  - Form action: Submits to `warning.html` (phishing path)
  - **Danger:** Users entering credentials here would be compromised
  - The key difference is the form's action attribute pointing to a suspicious page
  - In a real scenario, this would send credentials to an attacker's server

---

### Outcome Pages

#### **success.html** - Legitimate Login Success
- **Purpose:** Confirmation page after successful login on the real system
- **Content:** Displays "Giriş uğurla tamamlandı" (Login completed successfully - in Azerbaijani)
- **When reached:** User successfully logged in through `login_normal.html`
- **Design:** Clean, white background with dark text - simple confirmation

#### **warning.html** - Phishing Detection Alert
- **Purpose:** Warning page to alert users they've been "hacked"
- **Content:** Displays "hackləndin!" (You got hacked! - in Azerbaijani)
- **When reached:** User attempted login through `login_simulation.html`
- **Design:** Dramatic red text with glow effect on black background - clearly indicates danger
- **Educational value:** Teaches users the consequences of using phishing links

---

## How the Project Works

### Scenario Flow

**Legitimate Path:**
```
User scans real QR code from restaurant
↓
Visits index.html (real website)
↓
Clicks to login via login_normal.html
↓
Enters credentials
↓
Redirected to success.html (✓ Safe)
```

**Phishing Path:**
```
User scans fake QR code from phishing index_fake.html
↓
Visits index_fake.html (looks identical to real site)
↓
Clicks to login via login_simulation.html
↓
Enters credentials (thinking it's real)
↓
Redirected to warning.html (⚠️ You got hacked!)
```

---

## Key Security Lessons

1. **Visual Similarity is Deceptive**
   - Phishing sites can look nearly identical to legitimate ones
   - Don't rely on appearance alone

2. **Verify URLs**
   - Check the actual domain/URL in the address bar
   - Phishing sites often use slightly different domains

3. **QR Code Caution**
   - QR codes can direct to malicious websites
   - Always verify you're on a legitimate site after scanning

4. **Login Page Red Flags**
   - Check for secure connections (HTTPS)
   - Verify the URL matches the official domain
   - Be suspicious of unexpected login prompts

5. **Credential Safety**
   - Never enter passwords on suspicious-looking pages
   - Legitimate restaurants won't ask for passwords via random QR codes

---

## Technical Details

### Styling & Design
- **Language:** HTML/CSS (Azerbaijani text for authenticity)
- **Fonts:** Google Fonts (Fraunces, Work Sans, IBM Plex Mono)
- **Icons:** Font Awesome 6.5.1
- **Color System:** CSS variables for consistent theming

### Form Structure
- **login_normal.html:** `<form action="success.html" method="get">`
- **login_simulation.html:** `<form action="warning.html" method="get">`

The forms demonstrate how the action attribute (the destination) determines whether credentials go to a safe or unsafe location.

---

## Use Cases

### Educational Settings
- Teach cybersecurity awareness in classrooms
- Demonstrate phishing attack mechanics
- Train employees on security best practices
- Create awareness campaigns

### Security Training
- Interactive phishing simulation exercise
- Show the consequences of clicking suspicious links
- Help users understand credential theft risks
- Practice identifying legitimate vs. fake websites

---

## Related Project: Bill Splitter

**bill-splitter.html** - A separate utility tool
- **Purpose:** Bill-splitting calculator for restaurant scenarios
- **Features:** Different design theme (dark with yellow/lime accents)
- **Use Case:** Educational tool to calculate split payments

---

## Important Notes

⚠️ **This is an educational project for awareness purposes only.** 
- Designed to teach users about phishing threats
- Should only be used in controlled, educational environments
- Never use this to actually deceive or harm users
- Always inform participants when conducting phishing awareness training

---

## How to Use This Project

1. **For Awareness Training:**
   - Direct trainees to visit `index.html` first
   - Explain this is the "real" restaurant website
   - Then show them `index_fake.html`
   - Ask them to spot differences (there are none!)
   - Demonstrate how the phishing path leads to the warning page

2. **For Interactive Learning:**
   - Have users try the legitimate login first
   - Then attempt the phishing login
   - Discuss the outcomes and what made them different

3. **For Security Testing:**
   - Use as a template for internal phishing simulations
   - Customize with your organization's branding
   - Track which users fall for the phishing attempt

---

## Summary Table

| File | Type | Purpose | Form Action |
|------|------|---------|------------|
| `index.html` | Real Website | Authentic restaurant site with real QR | N/A |
| `index_fake.html` | Fake Website | Phishing replica with fake QR | N/A |
| `login_normal.html` | Login Page | Real login (safe) | success.html |
| `login_simulation.html` | Login Page | Phishing login (unsafe) | warning.html |
| `success.html` | Outcome | Successful login confirmation | N/A |
| `warning.html` | Outcome | Phishing detection alert | N/A |

---

**Stay safe, stay aware! 🔒**
