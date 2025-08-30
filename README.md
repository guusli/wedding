# Wedding Invitation & Honeymoon Fund

A beautiful wedding invitation website with an integrated honeymoon fund page.

## Pages

### Main Invitation (`index.html`)
- Interactive wedding invitation card
- Personalized messages based on URL parameters
- Responsive design with elegant animations
- Uses custom fonts: Ahsing Regular and Coffekan Regular

### Honeymoon Fund (`honeymoon.html`)
- Grid of honeymoon activities guests can contribute to
- Modal dialogs with QR code placeholders for payments
- Fully responsive design
- Matching design aesthetic with the main invitation

## GitHub Pages Setup

This site is designed to work perfectly with GitHub Pages. Here's how to set it up:

### 1. Repository Setup
1. Create a new GitHub repository (e.g., `wedding-site`)
2. Upload all files to the repository:
   - `index.html` (main invitation)
   - `honeymoon.html` (honeymoon fund page)
   - `ahsing-regular.otf` (custom font)
   - `CoffekanRegular.ttf` (custom font)
   - `front.png` (invitation front image)
   - `back.png` (invitation back image)

### 2. Enable GitHub Pages
1. Go to your repository settings
2. Scroll down to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Click "Save"

### 3. Access Your Site
Your site will be available at:
- Main invitation: `https://yourusername.github.io/repository-name/`
- Honeymoon fund: `https://yourusername.github.io/repository-name/honeymoon.html`

## URL Parameters

The main invitation supports personalized messages using URL parameters:

- `?to=anna` - Shows "Anna, Dan, Frank & Axel"
- `?to=jenny` - Shows "Jenny, Dennis, Tove-Lovisa & Valter"
- `?to=brittmarie` - Shows "Britt-Marie"
- `?to=camilla` - Shows "Camilla & Mikael"
- `?to=martina` - Shows "Martina, Pehr, Nils & Signe"
- `?to=malena` - Shows "Malena, Rasmus & Freya"
- `?to=tuisku` - Shows "Tuisku"

Example: `https://yourusername.github.io/repository-name/?to=anna`

## Customization

### Adding New Guest Groups
Edit the `groups` object in `index.html`:

```javascript
const groups = {
    anna: "Anna, Dan, Frank & Axel",
    newgroup: "New Names Here",
    // Add more groups...
};
```

### Adding Payment QR Codes
Replace the placeholder in `honeymoon.html`:

```html
<div class="qr-code">QR-kod kommer här</div>
```

With your actual QR code image:

```html
<div class="qr-code">
    <img src="your-qr-code.png" alt="Payment QR Code" style="width: 100%; height: 100%; object-fit: contain;">
</div>
```

### Adding New Activities
Copy an existing activity card in `honeymoon.html` and modify:

```html
<div class="activity-card">
    <div class="activity-image">
        <div class="activity-image-icon">🎯</div>
        <div class="activity-image-text">Your Activity Name</div>
    </div>
    <div class="activity-content">
        <h3 class="activity-title">Activity Title</h3>
        <p class="activity-description">
            Your activity description here.
        </p>
        <button class="activity-button" onclick="openModal('Activity Title')">
            Bidra till denna
        </button>
    </div>
</div>
```

## Features

- ✨ Fully responsive design
- 🎨 Custom fonts and elegant styling
- 📱 Mobile-optimized
- 🔄 Smooth animations and transitions
- 🎯 Interactive elements
- 💍 Wedding-themed design
- 💰 Integrated honeymoon fund
- 🔗 Easy navigation between pages

## Browser Support

Works in all modern browsers including:
- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## File Structure

```
/
├── index.html              # Main wedding invitation
├── honeymoon.html          # Honeymoon fund page
├── ahsing-regular.otf      # Custom font for names
├── CoffekanRegular.ttf     # Custom font for ampersand
├── front.png               # Invitation front image
├── back.png                # Invitation back image
└── README.md               # This file
```

## Development

To test locally:

```bash
# Start a local server
python3 -m http.server 8080

# Visit http://localhost:8080
```

## License

This is a personal wedding website. Please create your own version rather than copying directly.