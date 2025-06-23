# PowerPoint to Slidev Conversion Prompt Template

Convert this PowerPoint slide content to Slidev format with complete verification:

**Requirements:**
1. **Content Fitting**: Ensure ALL content fits within slide boundaries without overflow
2. **Styling**: Match existing presentation theme (blue gradient titles, consistent spacing)
3. **Animations**: Use v-click for progressive bullet point disclosure
4. **Responsive Design**: Optimize for presentation viewing distances

**Mandatory Process:**
1. **Find working slide template**: Search slides.md for a confirmed working slide with similar structure
2. **Copy proven structure**: Use existing working slide as exact template rather than creating new patterns
3. **Replace content only**: Keep structural elements, CSS classes, and container hierarchy identical
4. **Optimize v-click usage**:
   - **CRITICAL**: Use v-click ONLY on major sections, not individual bullets
   - Target 2-3 total clicks maximum for full slide revelation
   - Avoid nested v-click elements (v-click on container + v-click on bullets)
5. Use these optimized spacing values for content-heavy slides:
   - `.content-container`: `max-width: 900px; padding: 0 2rem`
   - `.section-item`: `margin-bottom: 2.5rem; padding: 1.5rem`
   - Font sizes: title `2em`, section headers `1.4em`, text `1em`
   - Line height: `1.4` for readability
6. **MANDATORY Playwright verification**:
   - Navigate to the new slide immediately after creation
   - Test each v-click animation step-by-step
   - Take screenshots at each state to verify content visibility
   - **CRITICAL**: If slide appears blank, rebuild using different working template
   - Ensure no content is cut off or overflowing
   - Verify all text is readable and properly spaced
7. **If slide rendering fails**: Rebuild from scratch using proven working slide structure

**Success Criteria:**
- All content visible within slide boundaries
- Progressive animations work smoothly (2-3 clicks maximum)
- Consistent with presentation theme
- Professional presentation quality maintained
- No content truncation or overflow

**CRITICAL TROUBLESHOOTING:**

**If slide appears completely blank:**
1. **Symptom**: Playwright screenshots show only navigation, no slide content
2. **Root cause**: Structural rendering issue, not content overflow
3. **Solution**: DO NOT attempt to fix - rebuild completely using different working template

**Proven Working Slide Templates in this presentation:**
- "Prompting: Clear and Precise" (lines 916-1024) - Two-section layout with examples
- "Zero-Shot vs One-Shot Prompting" (lines 2088-2203) - Definition + example pairs layout
- "Think first! / Chain of Thought" (lines 1666-1738) - Simple bullet point layout  
- "Formatting Output" (lines 1350-1450) - Multi-column grid layout

**Template Selection Guide:**
- **For comparison content**: Use "Prompting: Clear and Precise" template
- **For definition + example pairs**: Use "Zero-Shot vs One-Shot Prompting" template
- **For simple bullet lists**: Use "Think first!" template  
- **For categorized content**: Use "Formatting Output" template

**Emergency Rebuild Process:**
1. Identify closest working template from above list
2. Copy entire slide structure (HTML + CSS) 
3. Replace ONLY the content text, keep all class names and structure
4. Test with Playwright immediately
5. If still blank, try different template

**Slide Content:**
I will present you the content in the following format:
<Title>

</Title>
<Content>

</Content>

Let's start