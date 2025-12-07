# Portfolio Website - Zavyer Weller

A personal portfolio website showcasing projects, skills, and professional information. This project includes both a static HTML/CSS version and a Vue.js application.

## Project Structure

```
portfolio-website-Zavyer-Weller/
├── index.html              # Main static HTML page
├── style.css               # Stylesheet for static HTML page
├── README.md               # This file
└── Weller_Zavyer_Vue_CLI/
    └── hello-world/        # Vue.js application
        ├── src/
        │   ├── components/ # Vue components
        │   ├── views/      # Vue views/pages
        │   ├── router/     # Vue Router configuration
        │   └── store/      # Vuex store
        └── package.json    # Node.js dependencies
```

## Features

### Static HTML Version (`index.html`)

- **Hero Section**: Professional introduction with profile image and CTA buttons
- **About Section**: 3-column card layout with personal information
- **Skills Section**: Interactive skill badges with hover effects
- **Projects Section**: Project showcase with cards, tech tags, and GitHub links
- **Contact Section**: Contact information cards and functional contact form
- **Responsive Navigation**: Bootstrap-based navigation bar with theme toggle
- **Smooth Scrolling**: Enhanced user experience with smooth anchor links
- **Scroll Animations**: Intersection Observer-based fade-in animations
- **Theme Toggle**: Dark/light theme switcher with local storage persistence
- **SEO Optimized**: Comprehensive meta tags for search engines and social media
- **Favicon**: Custom SVG favicon with brand identity

### Vue.js Application

- **Multi-page Application**: Home, About, and Portfolio views
- **GitHub Integration**: Portfolio component fetches and displays GitHub repositories
- **Consistent Styling**: Matches static HTML theme and design system
- **Responsive Design**: Mobile-friendly layouts
- **Vue Router**: Client-side routing with styled navigation
- **Vuex Store**: State management

## Recent Changes & Improvements

### 1. Fixed Image Path Issue

**File**: `index.html`

- **Problem**: Image path used Windows backslashes (`\`) which don't work in web browsers
- **Solution**: Changed path from `Weller_Zavyer_Vue_CLI\hello-world\src\assets\profilepic.jpg` to `Weller_Zavyer_Vue_CLI/hello-world/src/assets/profilepic.jpg`
- **Impact**: Profile image now displays correctly in all browsers

### 2. Cleaned Up CSS Styling

**File**: `style.css`

- **Removed Debug Styles**: Eliminated red text shadows and underlines that appeared to be debug/test styles
  - Removed `text-shadow: 0 4px 12px red` from `.hero-section`
  - Removed `text-decoration: underline red` from `.hero-section`
  - Removed `text-shadow: 0 2px 12px red` from `.main-title`
  - Removed `text-decoration: underline red` from `.main-title`
  - Removed duplicate `border-radius` and `border-color: red` from `.profile-image`
- **Impact**: Cleaner, more professional appearance consistent with the design system

### 3. Enhanced Navigation

**File**: `index.html`

- **Added Skills Link**: Added navigation link to Skills section
- **Improved Layout**: Used Bootstrap's `d-flex gap-3` for better spacing between nav links
- **Impact**: Better navigation experience and easier access to all sections

### 4. Improved Skills Section

**File**: `index.html`

- **Problem**: Skills section was empty with no content
- **Solution**:
  - Added proper HTML structure with container, row, and column layout
  - Added heading and description text
  - Created placeholder for skills list
- **File**: `style.css`
- **Added Styling**:
  - Created `.skills-section` class with consistent styling matching About section
  - Added `.skills-list` class with flexbox layout for future skill items
- **Impact**: Skills section now has structure and styling ready for content

### 5. CSS Consistency Improvements

**File**: `style.css`

- **Unified Section Styling**: Skills section now matches About section styling for visual consistency
- **Better Organization**: Added clear comments and organized related styles together
- **Impact**: More maintainable and consistent design system

## Design Overhaul - Modern Portfolio Design

### 6. Enhanced Navigation with Glassmorphism

**Files**: `style.css`

- **Glassmorphism Effect**: Added backdrop blur and semi-transparent background to navigation bar
- **Sticky Navigation**: Navigation bar now sticks to top on scroll with smooth transitions
- **Interactive Hover States**:
  - Nav links have animated underline effects on hover
  - Brand name changes color and lifts slightly on hover
  - Smooth color transitions for all interactive elements
- **Impact**: Modern, professional navigation with excellent UX

### 7. Hero Section Redesign

**Files**: `index.html`, `style.css`

- **Animated Background**: Added pulsing radial gradient background effect
- **Typography Enhancement**:
  - Upgraded to Inter font family for better readability
  - Added gradient text effect to name using CSS `background-clip`
  - Improved font weights and letter spacing
- **Fade-in Animations**: Hero content animates in with smooth fade-up effect
- **Call-to-Action Buttons**:
  - Added "Learn More" and "View Skills" buttons with modern styling
  - Gradient primary button with hover lift effect
  - Outlined secondary button with smooth transitions
- **Impact**: More engaging and professional hero section

### 8. Profile Image Enhancements

**File**: `style.css`

- **Floating Animation**: Profile image has subtle floating animation
- **Enhanced Hover Effects**:
  - Image scales and lifts on hover
  - Glowing border effect with accent color
  - Smooth shadow transitions
- **Larger Size**: Increased from 150px to 180px for better visibility
- **Impact**: More dynamic and interactive profile presentation

### 9. Modern Section Cards

**Files**: `style.css`

- **Glassmorphism Cards**: About and Skills sections use glassmorphic design
- **Gradient Top Border**: Each section has a colorful gradient accent bar at the top
- **Hover Lift Effect**: Sections lift slightly on hover with enhanced shadows
- **Animated Underlines**: Section titles have animated gradient underlines
- **Better Spacing**: Improved padding and margins for better visual hierarchy
- **Impact**: Modern, cohesive card-based design system

### 10. Skills Section with Interactive Badges

**Files**: `index.html`, `style.css`

- **Skill Badges**: Added interactive skill badges (HTML, CSS, JavaScript, Vue.js, Bootstrap, Git)
- **Badge Styling**:
  - Glassmorphic design with accent borders
  - Hover effects with scale and lift animations
  - Shimmer effect on hover
- **Responsive Grid**: Skills automatically wrap and center on all screen sizes
- **Impact**: Visual representation of skills with engaging interactions

### 11. Modern Button System

**File**: `style.css`

- **Primary Button**: Gradient background with accent colors, shadow effects
- **Secondary Button**: Outlined style with transparent background
- **Back to Top Button**: Glassmorphic design matching section cards
- **Hover Effects**: All buttons lift on hover with enhanced shadows
- **Smooth Transitions**: All interactions use consistent transition timing
- **Impact**: Cohesive button system with excellent user feedback

### 12. Enhanced Visual Effects

**File**: `style.css`

- **Background Pattern**: Subtle radial gradient overlay for depth
- **CSS Variables**: Extended color system with shadows and transitions
- **Smooth Animations**: Consistent animation timing throughout
- **Shadow System**: Multi-level shadow system (sm, md, lg, accent)
- **Responsive Design**: Enhanced mobile breakpoints and adjustments
- **Impact**: Polished, professional appearance with consistent design language

### 13. Typography Improvements

**Files**: `index.html`, `style.css`

- **Font Upgrade**: Added Inter font family as primary, Roboto as fallback
- **Better Hierarchy**: Improved font sizes and weights for better readability
- **Line Height**: Increased line-height for better text readability
- **Letter Spacing**: Adjusted letter spacing for headings
- **Impact**: More readable and modern typography system

## Technologies Used

### Static HTML Version

- HTML5
- CSS3 (with CSS Variables, Animations, Glassmorphism)
- Bootstrap 5.3.2
- Google Fonts (Inter, Roboto)

### Vue.js Application

- Vue 3.2.13
- Vue Router 4.0.3
- Vuex 4.0.0
- Vue CLI 5.0.0
- Babel
- ESLint

## Getting Started

### Static HTML Version

1. Open `index.html` in a web browser
2. No build process required

### Vue.js Application

1. Navigate to the Vue project directory:

   ```bash
   cd Weller_Zavyer_Vue_CLI/hello-world
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Run development server:

   ```bash
   npm run serve
   ```

4. Build for production:

   ```bash
   npm run build
   ```

5. Lint code:
   ```bash
   npm run lint
   ```

## Color Palette

The website uses a custom color palette defined in CSS variables:

- **Primary Background**: `#0a192f` (Dark navy blue)
- **Secondary Background**: `#112240` (Lighter navy for cards)
- **Main Text**: `#e6f1ff` (Light blue-white)
- **Secondary Text**: `#8892b0` (Muted blue-gray)
- **Accent Color**: `hsla(75, 83%, 84%, 1)` (Tea green)
- **Accent Hover**: `hsla(75, 83%, 74%, 1)` (Darker tea green)
- **Card Background**: `rgba(17, 34, 64, 0.5)` (Semi-transparent navy)
- **Additional Colors**: Coffee, Reseda Green, Mindaro (defined but not actively used)

### Design Features

- **Glassmorphism**: Modern frosted glass effect on navigation and cards
- **Gradient Accents**: Gradient borders and text effects using accent colors
- **Smooth Animations**: CSS animations for floating, pulsing, and fade-in effects
- **Interactive Elements**: Hover effects on all interactive components
- **Shadow System**: Multi-level shadow system for depth and hierarchy

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Responsive design for mobile, tablet, and desktop
- No IE11 support (as per Vue.js configuration)

## New Features Implemented

### 14. Scroll-Triggered Animations (Intersection Observer)

**Files**: `index.html`, `style.css`

- **Intersection Observer API**: Implemented scroll-triggered animations using the Intersection Observer API
- **Fade-in Animations**: Sections and cards fade in and slide up when they enter the viewport
- **Staggered Animations**: Cards animate in sequence with staggered delays for visual appeal
- **Performance Optimized**: Uses efficient intersection observer instead of scroll event listeners
- **Impact**: More engaging user experience with smooth, professional animations

### 15. Contact Information Section

**Files**: `index.html`, `style.css`

- **Contact Cards**: Added a new contact section with 4 interactive cards
- **Contact Methods**:
  - Email contact information
  - LinkedIn profile link
  - GitHub profile link
  - General collaboration message
- **Card Design**: Matches the about section card style with glassmorphic design
- **Hover Effects**: Interactive cards with hover animations
- **Impact**: Easy way for visitors to connect and view your work

### 16. Dark/Light Theme Toggle

**Files**: `index.html`, `style.css`

- **Theme Toggle Button**: Added a toggle button in the navigation bar
- **Local Storage**: Theme preference is saved and persists across page reloads
- **Light Theme**: Complete light theme with adjusted colors, shadows, and backgrounds
- **Smooth Transitions**: All theme changes are smoothly animated
- **Icon Updates**: Theme icon changes based on current theme (🌙/☀️)
- **CSS Variables**: Uses CSS custom properties for easy theme switching
- **Impact**: Better accessibility and user preference support

### 17. Enhanced Vue.js App Styling

**Files**: `Weller_Zavyer_Vue_CLI/hello-world/src/App.vue`, `HomeView.vue`, `AboutView.vue`

- **Matching Navigation**: Vue app navigation now matches static HTML design
- **Consistent Styling**: All Vue components use the same color scheme and design system
- **HomeView Redesign**: Hero section matches static HTML with profile image and CTA buttons
- **AboutView Redesign**: About section uses the same 3-column card layout
- **Theme Consistency**: Vue app uses the same CSS variables and styling patterns
- **Impact**: Unified design experience across both static and Vue.js versions

### 18. SEO Meta Tags

**File**: `index.html`

- **Meta Description**: Added comprehensive meta description for search engines
- **Meta Keywords**: Included relevant keywords for web development and portfolio
- **Author Tag**: Added author meta tag
- **Robots Tag**: Configured robots meta tag for search engine indexing
- **Impact**: Better SEO and improved search engine visibility

### 19. Favicon Implementation

**Files**: `index.html`, `favicon.svg`

- **SVG Favicon**: Created custom SVG favicon with initials "ZW"
- **Multiple Formats**: Added support for both SVG and fallback ICO formats
- **Brand Identity**: Favicon uses the site's color scheme (dark background, accent color text)
- **Impact**: Professional branding and better browser tab recognition

### 20. Project Showcase Section

**Files**: `index.html`, `style.css`

- **Project Cards**: Added a new projects section with 3-column grid layout
- **Project Display**: Each project card includes:
  - Project image placeholder with icon
  - Project title and description
  - Technology tags
  - GitHub link with icon
- **Hover Effects**: Interactive cards with lift and glow effects on hover
- **Responsive Design**: Cards stack on mobile, 2 columns on tablet, 3 on desktop
- **Scroll Animations**: Projects animate in when scrolled into view
- **Impact**: Showcases your work and makes it easy for visitors to view your projects

### 21. Contact Form

**Files**: `index.html`, `style.css`

- **Contact Form**: Added a functional contact form alongside contact information cards
- **Form Fields**:
  - Name input
  - Email input
  - Subject input
  - Message textarea
- **Form Validation**: HTML5 validation with required fields
- **Email Integration**: Form opens default email client with pre-filled message
- **Success Feedback**: Visual feedback when form is submitted
- **Responsive Layout**: Form and contact cards side-by-side on desktop, stacked on mobile
- **Styling**: Matches the site's design system with glassmorphic styling
- **Impact**: Easy way for visitors to send messages directly

### 22. Image Optimization

**File**: `index.html`

- **Lazy Loading**: Added `loading="lazy"` attribute to profile image
- **Width/Height Attributes**: Added explicit width and height to prevent layout shift
- **Alt Text**: Proper alt text for accessibility
- **Impact**: Better page load performance and improved Core Web Vitals scores

## Future Improvements

- [x] Add actual skills content to the Skills section
- [x] Add animations and transitions
- [x] Enhance Vue.js app styling to match static HTML theme
- [x] Add contact form or contact information
- [x] Implement dark/light theme toggle
- [x] Add scroll-triggered animations (Intersection Observer)
- [x] Optimize images for web
- [x] Add meta tags for SEO
- [x] Add favicon
- [x] Add project showcase section
- [x] Add contact form (currently just contact information)

## Author

**Zavyer Weller**

- Student learning coding every day
- Building projects to improve skills

## License

This project is private and personal.

---

_Last Updated: December 2025_
