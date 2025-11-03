# [Screen Name] Screen



## Decision Framework Quick Reference

**Use `/build-simple-screen` when:**
- ✓ You know exactly what to build
- ✓ All tools/patterns are familiar
- ✓ Standard CRUD + basic UI
- ✓ No research needed

**Use Simple Screen Agent when:**
- ✓ Minor unknowns exist
- ✓ Need to research RN Reusables or basic Supabase patterns
- ✓ Familiar patterns with organizational complexity
- ✓ Multiple states or components but no external packages

**Use Complex Screen Agent when:**
- ✓ Need to research packages/integrations
- ✓ Multi-level data hierarchies with joins
- ✓ Canvas/visualization libraries required
- ✓ Complex state management (drag-drop, real-time updates)
- ✓ Significant architectural decisions needed




## Complexity Level
**[ ] Simple** - Standard CRUD, basic UI, Supabase + RN Reusables only
**[X] Complex** - Check this if: external APIs, payments, real-time features, custom packages likely needed, or non-trivial business logic

*Note: Agent will research and determine actual requirements. This flag just signals "go slow, research first."*


---

## Purpose (Context)
[1-2 sentences: What user goal does this accomplish? What business logic does it serve?]

---

## Routing (INVARIANT)
**Incoming:**
- From [ScreenA] via [trigger/event]
- From [ScreenB] via [trigger/event]

**Outgoing:**
- To [ScreenX] via [user action]
- To [ScreenY] via [condition/event]

**Parameters passed:** [if any]

---

## Data (PATTERN + Flexible)

### Must Exist
These entities/columns must exist for this screen to function:
- Table: `[table_name]` with columns: `[col1, col2, col3]`
- [Any other guaranteed data structures]

### Probably Needed (Research Required)
- [Uncertain data needs - describe what you're not sure about]
- [Relationships between entities that may need definition]
- [Any data you suspect exists but haven't confirmed]

**Note:** AI should extend schema as needed to support functionality, following Supabase best practices.

**IMPORTANT** include as much as you can abut what data is required, FK's, PK's, who should be able to acces what, defaults, and other functions and triggers. THE AGENT SHOULD NOT HAVE TO GUESS ON THESE SPECIFICS!

---

## Screen Layout (PATTERN)

### Global Components (Use These)
- [Component name from /components/global] at [general position]
- [Component name] with [specific behavior if different from default]

### Layout Structure
[Describe the sectional layout as a template - e.g., "Header sticky at top, scrollable content area, bottom action bar fixed"]

**Visual hierarchy:**
- [Section 1]: [what goes here]
- [Section 2]: [what goes here]

### Responsive Behavior (COMMAND → Implementation Flexible)
**Must respond to:** [screen size changes, keyboard appearance, etc.]
**How:** [AI decides - just ensure it works]

### Screen States
**Known states:**
- [loading, error, empty, populated, etc.]

**Unknown states:** Likely additional edge case states exist - implement as needed.

---

## Components (SPECIFIC)

### [Component Name 1]
**What component should accomplish**
- naritive of how the user uses the component

**Data:** 
- Displays: `[data.field]`
- Needs: [describe data requirements, not exact schema]

**Position:** [Where in layout - template description]

**Actions:**
- User [action] → [effect/state change]
- User [action] → [navigation/backend call]

**States:**
- Known: [visible, disabled, loading, etc.]
- Unknown: Handle edge cases as needed

**Backend needs:** [Mention if services/functions/webhooks likely needed - AI will implement]

---

### [Component Name 2]
[Same structure as above]

---

## User Flow (NARRATIVE)
1. User arrives from [screen/state]
2. User sees [high-level description of screen state]
3. User can [primary actions available]
4. User [completes goal] and navigates to [destination]

---

## Notes & Considerations
- [Any special rules, validation logic, or edge cases]
- [Security considerations]
- [Performance notes]
- [Anything weird or non-standard]

---

## UI/UX Bias (FOR FUTURE DESIGN AGENT ONLY)
**Instruction to coding agent:** Copy the text below into a comment at the bottom of the .tsx file. Do not use this information for styling the current implementation. ONLY THE OPTIONS WITH AN X APPLY!!
```
- [ ]: Product Detail (PDP) - generous padding, soft corners, tactile feel, smooth visual weight shifts  
- [ ]: Product Grid / Browse - airy rhythm, light elevation, consistent spacing, balanced neutral palette  
- [ ]: Search Results - tighter layout, quick visual response, accent highlights, minimal decoration  
- [ ]: Category / Home Feed - modular balance, gentle motion, clear contrast, inviting palette  
- [ ]: Cart / Mini-Cart - compact grouping, calm tone, rounded accents, steady transitions  
- [ ]: Checkout - stripped-back color, clear hierarchy, steady pacing, low-friction visual flow  
- [ ]: Visual Data (Charts) - crisp edges, restrained color, subtle motion, focus on contrast and legibility  
- [ ]: Landing / Hero / Campaign - bold typography, wide spacing, expressive imagery, cinematic transitions  
- [ ]: Simple Task - centered focus, bold primary, minimal distraction, quick visual feedback  
- [ ]: Multi-field Form - consistent rhythm, soft feedback, focused transitions  
- [ ]: Profile / Order History - structured spacing, neutral warmth, quiet animation, stable tone  
- [ ]: Modal / Confirmation - dim calm background, centered weight, short entrance, gentle exit  
- [ ]: Empty / Loading / Error States - soft tone, optimistic palette, light motion, clear visual relief  
```