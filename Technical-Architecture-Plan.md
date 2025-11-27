# Technical Architecture Plan: R.A Tents Website

## 1. Framework & Technology Stack
*   **Core:** Single-File HTML5 (`index.html`).
*   **Logic:** React 18 (via CDN, compiled in-browser with Babel Standalone).
    *   *Rationale:* Satisfies the "Single-File Mandate" while adhering to the "React/Next.js" requirement for component-based architecture.
*   **Styling:** Tailwind CSS (via CDN).
    *   *Rationale:* Rapid UI development, responsive design, and "Premium" aesthetic customization.
*   **Icons:** Lucide React (via CDN) or FontAwesome.
*   **Fonts:** Google Fonts (Playfair Display for headers, Poppins for body).

## 2. Component Structure
The application will be built as a single React App mounted to a root div.

*   `App` (Main Container)
    *   `Navbar`: Sticky header with Logo and Navigation links.
    *   `Hero`: Full-screen background image (`High End Large Event Tent.jpg`), animated text, Gold CTA.
    *   `ServicesOverview`: 3-column layout (Manufacturing, Premium Solutions, Shade Structures).
    *   `TheRADifference`: Horizontal block with "Quality", "Experience", "Variety".
    *   `ProductShowcase`: Grid with hover effects for Marquee, Arched, Bedouin, Ramadan, Parking.
    *   `Footer`: Client logos/names, Contact Info, Copyright.

## 3. State Management
*   **Local State (`useState`):**
    *   `isScrolled`: To toggle navbar styling on scroll.
    *   `mobileMenuOpen`: For responsive navigation.
    *   `hoveredProduct`: To track which product card is active for overlay effects.

## 4. Design System & Theming
*   **Colors:**
    *   Primary Gold: `#D4AF37` (approximate gold)
    *   Dark Charcoal: `#1A1A1A`
    *   Warm Sand: `#F5F5DC` or `#F3E5AB`
    *   Teal/Navy: `#003366`
*   **Typography:**
    *   Headings: `Playfair Display` (Serif)
    *   Body: `Poppins` (Sans-serif)

## 5. Data Flow
*   Content is hardcoded based on the "Proposed Website Theme" prompt data.
*   Images are referenced via relative paths to the `Images/` directory.

## 6. Security & Performance
*   **Security:** No backend, purely static frontend. No user input handling (except mailto links).
*   **Performance:**
    *   Native lazy loading for images below the fold.
    *   CDN usage for libraries (cached by browser).
    *   Optimized DOM structure.
