# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Repository Overview

This is a collection of frontend development challenges from DevChallenges.io, focusing on HTML and CSS skill building through responsive web component design. The repository contains multiple independent challenge projects, each implementing specific UI components from provided design mockups.

## Architecture & Structure

### Project Organization
- Each challenge is contained in its own directory (e.g., `testimonial-page-master/`, `business-blog-card-starter-master/`, `minimal-blog-card-starter/`)
- Projects are independent and self-contained with no shared dependencies
- Each project follows the same structure:
  - `index.html` - Main HTML file
  - `style.css` or `styles.css` - Stylesheet (if external CSS is used)
  - `design/` - Reference designs for desktop, tablet, and mobile views
  - `resources/` - Image assets, icons, and other media files
  - `README.md` - Challenge-specific instructions and guidelines
  - `README_template.md` - Template for custom project documentation

### Design Implementation Pattern
All challenges follow a consistent pattern:
1. **Design-first approach**: Each project includes JPG mockups for desktop (1350px), tablet (1024px), and mobile (412px) breakpoints
2. **Resource optimization**: Assets are provided in the `resources/` folder and may need optimization
3. **Responsive implementation**: Projects must work across all three breakpoints
4. **Visual accuracy**: Implementation should closely match provided designs using best judgment for spacing, fonts, and colors

### Common Technical Patterns
- CSS reset/normalize using `* { margin: 0; padding: 0; box-sizing: border-box; }`
- Flexbox-based layouts for card components and centering
- Google Fonts integration for typography (Poppins, Lato, Manrope, Sora)
- Semantic HTML structure with proper accessibility considerations
- Mobile-first responsive design approach

## Common Development Commands

### Working with Individual Projects
```bash
# Navigate to a specific challenge
cd testimonial-page-master/
cd business-blog-card-starter-master/
cd minimal-blog-card-starter/

# Open project in browser (requires local server)
python3 -m http.server 8000
# or
npx serve .
```

### Development Workflow
```bash
# Check current git status
git status

# Add and commit changes for a specific challenge
git add [challenge-directory]/
git commit -m "feat: [challenge-name] - [description]"

# View project history
git log --oneline

# Create a new challenge project
mkdir new-challenge-name/
cd new-challenge-name/
# Copy structure from existing project as template
```

### Testing Responsive Design
Since these are static HTML/CSS projects, testing is primarily visual:
- Use browser developer tools to test responsive breakpoints (412px, 1024px, 1350px)
- Test in multiple browsers for compatibility
- Validate HTML and CSS using browser tools or online validators

## Challenge Development Process

### Starting a New Challenge
1. Create project directory following naming convention (`challenge-name-master/` or `challenge-name-starter/`)
2. Set up basic project structure with `index.html`, stylesheet, `design/`, and `resources/` folders
3. Copy design mockups to `design/` folder
4. Add all required assets to `resources/` folder
5. Implement responsive HTML structure
6. Style components from top to bottom, ensuring mobile-first approach
7. Test across all three breakpoints
8. Optimize assets as needed

### Project Completion Checklist
- [ ] HTML structure matches design semantically
- [ ] Responsive behavior works at 412px, 1024px, and 1350px
- [ ] All assets are optimized and properly referenced
- [ ] Code follows consistent styling patterns used in other projects
- [ ] Visual implementation closely matches provided designs
- [ ] Accessibility considerations are addressed (alt text, semantic HTML)

## Design System Patterns

### Typography
- **Primary headings**: Poppins (600-800 weight)
- **Body text**: Lato (400 weight) or Poppins (300-400 weight)
- **Accent fonts**: Sora, Manrope for specific design requirements

### Color Patterns
- **Background**: Often light grays (#F2F5F9, #FFFFFF)
- **Text**: Dark grays and blues (#111729, #4A5567)
- **Cards**: White backgrounds with subtle shadows or borders

### Layout Patterns
- **Card components**: White background, rounded corners (10px), appropriate padding
- **Centering**: Flexbox with `justify-content: center` and `align-items: center`
- **Spacing**: Consistent gap values (16px, 24px, 38px commonly used)
- **Images**: Proper aspect ratios with overlay elements when needed

## File Management

### Asset Optimization
- Images should be optimized for web use
- Use appropriate formats (JPG for photos, PNG for graphics with transparency, SVG for icons)
- Consider providing @2x versions for high-DPI displays when assets are available

### CSS Organization
- Follow mobile-first responsive design principles
- Group related styles together (typography, layout, components)
- Use consistent naming conventions for classes
- Keep specificity low and avoid overly nested selectors

## DevChallenges.io Integration

This repository is designed to work with the DevChallenges.io platform:
- Projects can be deployed to GitHub Pages, Vercel, or Netlify for submission
- Each challenge includes specific requirements that should be met for platform submission
- README templates are provided for documenting completed solutions
- Community sharing and feedback processes are outlined in individual project READMEs