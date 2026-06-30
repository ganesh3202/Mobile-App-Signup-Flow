 GameZone — Mobile Signup Flow

A self-contained HTML prototype of the GameZone mobile signup experience, styled to match the brand's dark purple/blue gaming aesthetic.

 Files

- `gamezone-signup-flow.html` — the full interactive prototype

 What's included

A single mobile phone-frame mockup with 4 connected screens, switchable via the tab bar above the phone or by clicking through the flow itself:

1. **Sign Up** — Username, email, password, confirm password, terms checkbox
2. **Log In** — Email/username + password, "Forgot password?", social login buttons (Google, Discord)
3. **Verify** — 6-digit OTP entry with auto-advance/backspace navigation and resend timer
4. **Welcome** — Success state with Compete / Improve / Connect highlights and a final CTA

 How to use it

1. Open `gamezone-signup-flow.html` in any browser (double-click, or drag into a browser window).
2. Use the pill tab bar at the top to jump directly to any screen.
3. Or click through naturally:
   - **Sign Up** → "Sign Up" button → goes to **Verify**
   - **Verify** → "Verify Account" button → goes to **Welcome**
   - **Log In** → "Log In" button → goes to **Welcome**
   - Links like "Already have an account? Log in" and "New here? Create an account" jump between Sign Up and Log In

No build step, server, or dependencies required — it's plain HTML/CSS/JS (fonts loaded from Google Fonts via CDN).

 Tech notes

- Single file, no frameworks — easy to hand to a developer or paste into a design tool
- Fonts: Rajdhani (display/headings) + Inter (body text)
- Layout is fixed at mobile width (~390px) inside a phone-frame mockup; the screens themselves use standard responsive HTML so the markup can be lifted into a real app shell
- Colors, spacing, and component styles are defined as CSS custom properties at the top of the `<style>` block for easy theming

 Customizing

To adjust the look, edit the CSS variables near the top of the file:

```css
--purple: #7b3ff2;
--blue: #2dd4ff;
--bg-0: #070512;
```

To add or change copy, search for the relevant screen's `<div class="screen" id="...">` block and edit the text directly.

 Next steps

This is a visual/interaction prototype only — there's no real authentication, validation, or backend wired up. To turn this into a working app, the form fields and buttons would need to be connected to actual signup/login/verification logic.
