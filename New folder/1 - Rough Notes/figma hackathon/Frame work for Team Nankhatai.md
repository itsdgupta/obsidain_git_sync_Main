# PIXELRUSH HACKATHON: AI-TO-FIGMA WORKFLOW FRAMEWORK

====================================================================

## THE "ASSET LOCK" SYSTEM PROMPT (Mandatory for every LLM chat)
Before starting any phase, paste this exact system prompt into your AI (ChatGPT/Claude/etc.) to enforce your source file rule:

> "Act as an Expert UI/UX Designer and Frontend Developer. I am participating in a hackathon. RULE 1: You must ONLY use the html and css tags  I explicitly provide in this chat (referred to as the 'Source File or something '). RULE 2: If you believe a design requires an external html and css code that is not in the Source File, YOU MUST ASK ME FOR PERMISSION FIRST. Do not output code with external placeholders until I say 'yes'. If I say 'no', you must use CSS styling or provided assets to solve the problem."

---

## PHASE 0: THE 4-MEMBER DIVERGENT THINKING (Initial Brainstorm)
Once the problem statement is revealed . 
All 4 members will prompt the AI independently using 4 different "Design Lenses" to generate distinct concepts.

*   **Member 1 (The Minimalist):** Prompts AI for a clean, whitespace-heavy, Apple-esque solution.
*   **Member 2 (The Bold/Gen-Z):** Prompts AI for high-contrast, brutalist, or highly vibrant/interactive solutions.
*   **Member 3 (The Data-Driven/Corporate):** Prompts AI for a highly structured, dashboard-like, dense information layout.
*   **Member 4 (The Empath/Accessibility):** Prompts AI for a solution focused heavily on accessibility, large fonts, clear navigation, and user hand-holding.

*After 30 minutes, reconvene, present the 4 AI-generated approaches, and merge the best ideas into ONE unified concept for Phase 1.*

---

## PHASE 1: DISCOVERY & USER RESEARCH
**Goal:** Define the 'who' and 'why'.
**Team Action:** Discuss the merged concept and feed it to the AI to solidify the foundation.

**AI Prompt for the Team Lead:**
> "Here is our hackathon problem statement: [Insert Problem]. We have decided on this general approach: [Insert merged idea]. 
> 1. Define the primary business goal of this platform.
> 2. Analyze 3 hypothetical competitors. Tell me what their UIs probably do well, and where they fail.
> 3. Create 2 distinct User Personas (Target Audience) for this specific problem."

**Output:** Use this text for your Round 1 Mentor Presentation (Team Planning).

---

## PHASE 2: INFORMATION ARCHITECTURE (IA) & USER FLOWS
**Goal:** The structural skeleton. Map out navigation.
**Team Action:** Define the pages required before writing any layout code.

**AI Prompt:**
> "Based on our personas and goal, act as an Information Architect.
> 1. Generate a hierarchical Sitemap for this solution.
> 2. Map out the exact User Flow for the core primary task (from Landing Page to Final Confirmation). Use a text-based flowchart format (e.g., Home -> Click 'X' -> Dashboard).
> Keep it scoped to what a 4-person team can design in a few hours."

**Output:** A clear map of how many screens you actually need to build.

---

## PHASE 3: WIREFRAMING (The AI-to-Figma Hack)
**Goal:** Low-fidelity layouts using your HTML-to-Figma workflow.
**Team Action:** Split the screens defined in Phase 2 among the 4 members. Each member uses the AI to generate structural HTML/CSS.

**AI Prompt for Wireframe Generation:**
> "I need a low-fidelity wireframe for the [Insert Page Name, e.g., Dashboard] based on our user flow.
> Generate a single HTML file containing both HTML and embedded responsive CSS.
> DESIGN RULES:
> - This is a wireframe. Use ONLY grayscale colors (whites, grays, black).
> - Use standard geometric shapes (divs) to represent image placeholders.
> - Use standard system fonts.
> - Ensure the CSS uses modern Flexbox/Grid for a highly responsive, clean layout.
> - Remember the Asset Lock: Do NOT include any external images or icon fonts. Ask first if you need them.
> Output ONLY the HTML block so I can copy it."

**Figma Action:** 
1. Save the AI output as `.html` files.
2. Open in Figma, use your "HTML to Figma" extension.
3. You now have editable, auto-layout structured gray-box wireframes in Figma!

---

## PHASE 4: HIGH-FIDELITY UI DESIGN
**Goal:** Visuals, branding, and applying the source files.
**Team Action:** Create the Design System, then upgrade the wireframes.

**Step 4A: Design System Generation**
**AI Prompt:**
> "Based on our solution for [Problem Statement], generate a UI Design System.
> 1. Suggest a primary, secondary, background, and text color palette (Provide Hex codes).
> 2. Suggest a Google Font pairing (One for headings, one for body) - *I am granting permission to use Google Fonts for this.*
> 3. Provide a CSS spacing scale (e.g., 4px, 8px, 16px)."
*Setup these colors and fonts in Figma as Local Styles.*

**Step 4B: Hi-Fi HTML Generation (If bypassing manual Figma design)**
**AI Prompt:**
> "Here is the wireframe HTML for [Page Name]: [Paste Wireframe Code].
> Also, here is the text/data from my Source File: [Paste Source Data].
> Upgrade this HTML/CSS to High-Fidelity UI.
> - Apply this color palette: [Insert Hex Codes].
> - Inject the Source File text into the correct layout sections.
> - Make it look premium, modern, and pixel-perfect.
> - ONLY use the source file data provided. If you need a placeholder image, ask me first."

**Figma Action:** Import the new Hi-Fi HTML into Figma using the extension. Manually tweak the UI, apply components, and clean up the layers for the **Round 2 Mentor Review**.

---

## PHASE 5: INTERACTIVE PROTOTYPING
**Goal:** Add functionality and micro-interactions in Figma.
**Team Action:** Do this manually in Figma, but use AI for strategic advice.

Extract your design as html pages or .png Images for each pages and do this in stich.

**AI Prompt:**
> "Our Figma UI is complete. We need to prototype it for the judges. 
> Based on our user flow: [Insert Flow], suggest specific, high-impact Figma prototype transitions and micro-interactions. 
> Where should we use 'Smart Animate'? Which elements should have hover states? Keep user psychology in mind to make the app feel alive."

**Figma Action:** Connect the screens based on AI suggestions. Ensure buttons, nav bars, and form inputs have interactive states.

---

## PHASE 6: USABILITY TESTING (Pre-Judging Prep)
**Goal:** Validate the design before Final Evaluation (Round 3).
**Team Action:** Test the prototype on each other or other non-competing friends.

**AI Prompt:**
> "We are about to present our Figma prototype to the hackathon judges. 
> Create a Usability Testing Script. 
> Give me 3 specific, scenario-based tasks to ask a tester to complete using our prototype. 
> Tell us what specific friction points (e.g., hesitated on button, couldn't find menu) we should watch out for silently."

**Final Action:** Run the test. Fix any confusing UI elements in Figma. 
Once Round 2 is officially cleared by mentors, you already have the highly-responsive HTML/CSS generated from Phase 4 to use as the base for your final coding phase!

Links:-
Html to Figma : https://www.figma.com/community/plugin/1665283117555101088
