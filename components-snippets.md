# Alexandra Fit - Reusable Component Snippets

Copy-paste these HTML blocks into your pages. All components use the global design tokens and CSS from `design-system.html`.

---

## 1. BUTTON COMPONENTS

### Primary Button
```html
<button class="btn-primary">
    Button Text
</button>
```

### Secondary Button
```html
<button class="btn-secondary">
    Button Text
</button>
```

### Ghost Button
```html
<button class="btn-ghost">
    Button Text
</button>
```

### Button with Icon
```html
<button class="btn-primary">
    ✓ Button with Icon
</button>
```

---

## 2. SECTION HEADER WITH UNDERLINE ANIMATION

Add `data-animate="true"` to enable scroll-triggered animation.

```html
<h2 class="section-header-underline text-3xl mb-8" data-animate="true">
    Your Heading Here
</h2>
```

**Tailwind Size Classes:**
- `.text-3xl` - 1.875rem (equivalent to h2 size)
- `.text-2xl` - 1.5rem (equivalent to h3 size)
- `.text-xl` - 1.25rem (smaller heading)

---

## 3. CARD 3D COMPONENT

Basic card structure with 3D hover effect and shadow transformation.

```html
<div class="card-3d p-6">
    <!-- Icon or Image -->
    <div class="w-12 h-12 bg-gradient-to-br from-primary to-secondary rounded-lg mb-4"></div>
    
    <!-- Content -->
    <h3 class="text-xl font-bold mb-3">Card Title</h3>
    <p class="text-gray-600 dark:text-gray-400 mb-4">
        Card description goes here.
    </p>
    
    <!-- CTA Button -->
    <button class="btn-primary text-sm">Learn More</button>
</div>
```

### Card Grid Layout (3 Columns)
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
    <div class="card-3d p-6"><!-- Card 1 --></div>
    <div class="card-3d p-6"><!-- Card 2 --></div>
    <div class="card-3d p-6"><!-- Card 3 --></div>
</div>
```

---

## 4. WHATSAPP MODAL & TRIGGER BUTTON

### Trigger Button (Place in Fixed Position)
```html
<!-- WhatsApp Trigger Button -->
<button id="whatsapp-trigger" title="Chat with us on WhatsApp">
    💬
</button>
```

### Full Modal & Form
```html
<!-- WhatsApp Modal -->
<div id="whatsapp-modal">
    <div class="whatsapp-modal-content p-8">
        <!-- Close Button -->
        <div class="flex justify-between items-center mb-6">
            <h3 class="text-2xl font-bold">Let's Get You Started</h3>
            <button id="whatsapp-close" class="text-2xl leading-none">&times;</button>
        </div>
        
        <!-- Qualification Form -->
        <form id="whatsapp-form" class="space-y-6">
            
            <!-- Goal -->
            <div>
                <label class="block font-semibold mb-3">What's Your Fitness Goal?</label>
                <div class="space-y-2">
                    <label class="flex items-center">
                        <input type="radio" name="goal" value="Weight Loss" class="mr-3" required>
                        <span>Weight Loss</span>
                    </label>
                    <label class="flex items-center">
                        <input type="radio" name="goal" value="Muscle Gain" class="mr-3">
                        <span>Muscle Gain</span>
                    </label>
                    <label class="flex items-center">
                        <input type="radio" name="goal" value="General Fitness" class="mr-3">
                        <span>General Fitness</span>
                    </label>
                    <label class="flex items-center">
                        <input type="radio" name="goal" value="Athletic Performance" class="mr-3">
                        <span>Athletic Performance</span>
                    </label>
                </div>
            </div>
            
            <!-- Level -->
            <div>
                <label class="block font-semibold mb-3">What's Your Fitness Level?</label>
                <div class="space-y-2">
                    <label class="flex items-center">
                        <input type="radio" name="level" value="Beginner" class="mr-3" required>
                        <span>Beginner</span>
                    </label>
                    <label class="flex items-center">
                        <input type="radio" name="level" value="Intermediate" class="mr-3">
                        <span>Intermediate</span>
                    </label>
                    <label class="flex items-center">
                        <input type="radio" name="level" value="Advanced" class="mr-3">
                        <span>Advanced</span>
                    </label>
                </div>
            </div>
            
            <!-- Location -->
            <div>
                <label class="block font-semibold mb-3">Where Are You Located?</label>
                <select name="location" class="w-full p-3 border border-gray-300 dark:border-gray-600 rounded-lg dark:bg-gray-700 dark:text-white" required>
                    <option value="">Select location...</option>
                    <option value="London">London</option>
                    <option value="Manchester">Manchester</option>
                    <option value="Birmingham">Birmingham</option>
                    <option value="Online">Online</option>
                    <option value="Other">Other</option>
                </select>
            </div>
            
            <!-- Timeline -->
            <div>
                <label class="block font-semibold mb-3">When Can You Start?</label>
                <div class="space-y-2">
                    <label class="flex items-center">
                        <input type="radio" name="timeline" value="Immediately" class="mr-3" required>
                        <span>Immediately</span>
                    </label>
                    <label class="flex items-center">
                        <input type="radio" name="timeline" value="This Week" class="mr-3">
                        <span>This Week</span>
                    </label>
                    <label class="flex items-center">
                        <input type="radio" name="timeline" value="Next Month" class="mr-3">
                        <span>Next Month</span>
                    </label>
                </div>
            </div>
            
            <!-- Submit Button -->
            <button type="submit" class="btn-primary w-full justify-center">
                Send to WhatsApp
            </button>
        </form>
    </div>
</div>
```

---

## GLOBAL SETUP (Include Once in Every Page)

Add this to the `<head>` of every page:

```html
<!-- Tailwind CSS CDN -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- Google Fonts: Poppins (700, 800) & Inter (400, 500) -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500&family=Poppins:wght@700;800&display=swap" rel="stylesheet">

<!-- Global CSS (from design-system.html) -->
<style>
    /* Copy the entire <style> block from design-system.html here */
</style>
```

Add this to the `<body>` of every page (before closing `</body>`):

```html
<!-- Dark Mode Toggle (in navigation) -->
<button id="dark-mode-toggle" class="btn-ghost">
    <span class="light-icon">🌙</span>
    <span class="dark-icon" style="display: none;">☀️</span>
</button>

<!-- WhatsApp Trigger Button -->
<button id="whatsapp-trigger" title="Chat with us on WhatsApp">
    💬
</button>

<!-- JavaScript (from design-system.html) -->
<script>
    /* Copy the entire <script> block from design-system.html here */
</script>
```

---

## DESIGN TOKEN REFERENCE

### Colors
- **Primary (Coral):** `#FF6B6B` - Use for buttons, CTAs, primary elements
- **Secondary (Turquoise):** `#4ECDC4` - Use for accents, hover states, underlines
- **Accent (Gold):** `#FFE66D` - Use for highlights, badges, special emphasis
- **Light BG:** `#F7FAFC` - Light mode background
- **Dark BG:** `#1A202C` - Dark mode background
- **Light Text:** `#1A202C` - Light mode text
- **Dark Text:** `#F7FAFC` - Dark mode text

### Shadow
- **Subtle:** `0 4px 6px rgba(0, 0, 0, 0.07)`
- **Card (Hover):** `0 10px 15px rgba(0, 0, 0, 0.08)`

### Border Radius
- **Cards:** `12px`
- **Buttons:** `8px`

### Typography
- **Headings:** Poppins, 700-800 weight
- **Body:** Inter, 400-500 weight

---

## DARK MODE USAGE

Use Tailwind's `dark:` prefix for dark mode styles:

```html
<div class="bg-white dark:bg-gray-800 text-gray-900 dark:text-gray-100">
    This div adapts to dark mode automatically.
</div>
```

The dark mode toggle automatically applies/removes the `dark` class to the `<html>` element and saves preference to `localStorage`.
