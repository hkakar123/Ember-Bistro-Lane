✨ Main Features
1. Top Bar & Logo

Sticky top bar with:

Logo: EmberLaneBistro.png (transparent PNG, fairly large)

Order mode toggle: Delivery / Pickup

Log in / Sign up buttons that open a modal

You can swap the logo by replacing EmberLaneBistro.png with your own file (same name or update the src).

2. Uber-Style Hero Section

Full-height hero with a food background image and warm gradient overlay

Clear title & subtitle:

“Food delivery from Ember Lane Bistro”

Address bar with:

Left 📍 icon

Input field (addressInput)

Black “Find food” button (findFoodBtn)

Behavior

Clicking Find food:

Shows a temporary address banner at the bottom (“Delivering or ready for pickup at …”)

Smooth-scrolls to the menu section

3. Delivery vs Pickup Toggle

The toggle in the header controls two shells:

#deliveryShell

#pickupShell

JavaScript:

Adds/removes .hidden on those sections

Updates the hero title, subtitle, and note depending on mode

Delivery mode = full detailed menu
Pickup mode = simplified “Pickup-friendly favorites” and pickup instructions

4. Menu & Category Filters

Intro section with rating, cuisine tags, and estimated time/price

Category chips (All dishes, Starters, Mains, Sides, Desserts, Drinks)

JS filters the dish cards inside #dishesGrid using data-category attributes.

To add a new dish:

Duplicate an <article class="dish-card"> block.

Adjust:

data-category="mains" (or starters, sides, etc.)

Title, description, tags, price, rating text

img src and alt text

5. Sidebar

Sticky sidebar on desktop with:

“Tonight at Ember Lane” gallery (4 food images)

Tag chips like “Wood-fired kitchen” / “Seasonal menu”

Hours & info card with open times and address

The sidebar becomes non-sticky and full-width on smaller screens.

6. Pickup Mode

Inside #pickupShell:

“Pickup at Ember Lane Bistro” introduction

Badges (Dedicated pickup shelf / Parking / Contactless hand-off)

A smaller grid of pickup-friendly favorites (bowls, burger, sandwich, salad)

“Pickup details” paragraph (explaining where to go in the restaurant)

7. Auth Modal (Fake)

Click Log in or Sign up:

Opens a modal overlay with:

Title & subtitle

Email & password fields

Primary button (“Log in” / “Sign up”)

Small text to switch modes

It doesn’t talk to a server – the form onsubmit is prevented in JS.

8. Promo Strip & Address Banner

Promo strip at the very bottom (fixed):

Message: “Free dessert on your first Ember Lane delivery or pickup order this week.”

“View menu” button scrolls to the menu

Close ✖ button hides the strip

Address banner:

Appears above the promo strip after clicking “Find food”

Auto-hides after a few seconds

9. Social Media Footer

At the bottom of the page (above the promo strip):

Icons for Instagram, Facebook, YouTube, TikTok, Twitter

Default: white background, gray icons

On hover: brand colors (pink, blue, red, black, etc.), with a subtle lift animation

Each icon links to the real homepage of the platform in a new tab

🚀 How to Run

No build tools needed.

Make sure index.html and EmberLaneBistro.png are in the same folder.

Open index.html in a browser:

Double-click it, or

Right-click → “Open with…” → your browser

That’s it.

For a more “real” dev feeling, you can use a simple local server (e.g. Live Server extension in VS Code), but it’s not required.

🛠 Customizing
Change Restaurant Name / Text

Search and replace “Ember Lane Bistro” with your restaurant name.

Key spots:

Top bar logo alt text

Hero heading

Intro title and description

Footer copyright

Pickup headings

Change Colors

Main accent colors live at the top in :root and in a few specific classes:

--bg-hero

--bg-body

--accent, --accent-soft

.bottom-strip background

Social hover colors per platform

Change them to match your brand.

Swap Images

All food pictures are from Unsplash:

Inside each <img src="https://images.unsplash.com/...">

You can replace these URLs with your own images or local files.

❗ Notes & Limitations

No real authentication – login/signup is just a mock interface.

No real ordering system – nothing is saved, no cart, no payments.

All data (menu, prices, ratings) is hard-coded in the HTML.

This is meant as a UI concept / portfolio piece, or a starting point before wiring it up to a backend.
