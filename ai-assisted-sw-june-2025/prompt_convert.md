# PowerPoint to Slidev Conversion Prompt Template

Convert this PowerPoint slide to Slidev format with complete verification:

**Requirements:**
1. **Content Fitting**: Ensure ALL content fits within slide boundaries without overflow
2. **Styling**: Match existing presentation theme (blue gradient titles, consistent spacing)
3. **Animations**: Use v-click for progressive bullet point disclosure
4. **Responsive Design**: Optimize for presentation viewing distances

**Mandatory Process:**
1. Read slides.md to understand current structure and styling patterns
2. Add new slide with appropriate spacing calculations for content density
3. Use these optimized spacing values for bullet-heavy slides:
   - `.content-container`: `padding: 1rem 2rem`
   - `.content-item`: `margin: 1.5rem 0; padding: 1.5rem`
   - Font sizes: title `2.2em`, bullets `1.5em`, text `1.1em`
   - Line height: `1.4` for readability
4. **MANDATORY Playwright verification**:
   - Navigate to the new slide
   - Test each v-click animation step-by-step
   - Take screenshots at each state to verify content visibility
   - Ensure no content is cut off or overflowing
   - Verify all text is readable and properly spaced
5. Fix any overflow issues before considering complete

**Success Criteria:**
- All content visible within slide boundaries
- Progressive animations work smoothly
- Consistent with presentation theme
- Professional presentation quality maintained
- No content truncation or overflow

**Slide Content:**
I will present you the content in the following format:
<Title>

</Title>
<Content>

</Content>

Let's start