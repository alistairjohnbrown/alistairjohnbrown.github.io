# Personal Dashboards - Alistair Brown

A collection of responsive web dashboards featuring running club management and fantasy football analytics.

## 🌟 Dashboards

### 🏃‍♂️ **Løpegruppen** - Running Club Dashboard
- **Member Profiles**: Admin showcase with photos and names
- **Competition Leaderboards**: Podium-style displays for various running challenges
- **Strava Integration**: Live activity feeds from club Strava account
- **Event Calendar**: Dynamic events loaded from CSV data
- **Display Optimized**: Designed for ScreenCloud digital display screens

### ⚽ **Fantasy Football** - League Analytics Dashboard
- **Live FPL Integration**: Real-time data from Fantasy Premier League API (League ID: 1509278)
- **Official FPL Styling**: Authentic Fantasy Premier League color scheme and design elements
- **Two-Column Layout**: 
  - Left: Title and newspaper image ("Runde 2.png")
  - Right: Live league table with auto-scroll functionality
- **Sticky Headers**: Fixed column headers that remain visible during scrolling
- **Auto-Scroll Table**: Smooth scrolling animation showcasing all league participants
- **Smart Caching**: 24-hour localStorage caching with multiple CORS proxy fallbacks
- **Position Tracking**: Live position movement indicators with gold/silver/bronze highlighting
- **Compressed Layout**: Optimized table design showing maximum teams per screen
- **Equal Height Containers**: Perfectly aligned left and right sections
- **Centered Design**: Professional layout centered on screen for optimal viewing

## 📺 ScreenCloud Integration

The individual dashboard pages are specifically designed for **ScreenCloud digital signage**:

- **Direct URL Access**: Pages can be accessed directly without navigation
  - Running Dashboard: `https://alistairjohnbrown.github.io/pages/running.html`
  - Fantasy Football: `https://alistairjohnbrown.github.io/pages/fantasy-football.html`
- **Clean Interface**: No navigation elements that would clutter display screens
- **Auto-Refresh**: Built-in refresh functionality for live data updates
  - FPL: Every 5 minutes with smart caching
  - Auto-scroll: Continuous table animation with 3-second pauses
- **Full-Screen Optimized**: Content utilizes full screen real estate with equal-height containers
- **Responsive Design**: Adapts to different screen sizes and orientations
- **Cross-Browser Compatible**: Enhanced with vendor prefixes for older display browsers
- **Professional Styling**: Official FPL colors and newspaper integration for authentic appearance

## 📁 Project Structure

```
alistairjohnbrown.github.io/
├── index.html                  # Main landing page
├── pages/
│   ├── running.html           # Løpegruppen dashboard
│   └── fantasy-football.html  # Fantasy football dashboard
├── assets/
│   ├── images/               # Photos, logos, and graphics
│   │   ├── Løpegruppen.png
│   │   ├── Runde 2.png      # Newspaper for fantasy football
│   │   ├── Alistair.jpg
│   │   ├── Maren.jpg
│   │   └── Sven.jpg
│   └── data/                 # CSV data files
│       └── events.csv        # Running events
│   ├── css/                  # Future: External stylesheets
│   └── js/                   # Future: External JavaScript
├── README.md
├── CODE_REVIEW.md            # Technical analysis
└── .git/
```

## 🚀 Technologies Used

- **HTML5**: Semantic markup with accessibility features
- **CSS3**: 
  - CSS Grid and Flexbox for responsive layouts with ScreenCloud compatibility
  - Official Fantasy Premier League color schemes and gradients
  - Sticky positioning for fixed table headers
  - Custom scrollbars and backdrop filters
  - Equal-height containers and centered layouts
  - Mobile-first responsive design with vendor prefixes
- **JavaScript**: 
  - Fantasy Premier League API integration with live data fetching
  - Auto-scroll animation system for table display
  - CSV parsing for dynamic data loading
  - Smart caching with localStorage and 24-hour expiration
  - Multiple CORS proxy fallback system for API reliability
  - Auto-refresh functionality and error handling
- **External APIs**: 
  - Strava club activity widgets with anti-caching
  - Fantasy Premier League API integration
  - Multiple CORS proxy fallback system

## 🛠️ Local Development

1. **Clone the repository**:
   ```bash
   git clone https://github.com/alistairjohnbrown/alistairjohnbrown.github.io.git
   cd alistairjohnbrown.github.io
   ```

2. **Serve locally**:
   - **VS Code**: Install Live Server extension, right-click `index.html` → "Open with Live Server"
   - **Python**: `python -m http.server 8000`
   - **Node.js**: `npx serve .`

3. **View in browser**: Navigate to `http://localhost:8000`

4. **ScreenCloud Testing**: Add `?screencloud-debug` to any page URL for compatibility testing

## 🔧 ScreenCloud Browser Compatibility

### Testing ScreenCloud Layout:
- **Debug Mode**: Add `?screencloud-debug` to running page URL
- **Recommended Resolutions**: 1920x1080, 1366x768, 1280x720
- **Browser Setup**: Chrome/Edge with `--disable-web-security` flag for CORS testing
- **Layout Verification**: Ensure header shows logo+admins side-by-side, main content in three columns

### Compatibility Features:
- **Flexbox with Vendor Prefixes**: `-webkit-`, `-ms-` prefixes for older browsers
- **No CSS Grid Dependency**: Uses flexbox for maximum compatibility
- **Graceful Degradation**: Responsive fallbacks for unsupported features

## 📊 Data Management

### Running Events (events.csv)
Add events to `assets/data/events.csv`:
```csv
date,title,description
2025-09-15,Fløyen Løp,Samling ved Fløibanen kl. 10:00
```

### Fantasy Football League
The Fantasy Football page connects directly to the Fantasy Premier League API:
- **League ID**: 1509278 (configurable in JavaScript)
- **Data Source**: Official FPL API with CORS proxy handling
- **Caching**: 24-hour localStorage cache for reliability
- **Refresh Rate**: Every 5 minutes when page is active
- **Fallback**: Displays clean message when API unavailable

### Member Photos
Place photos in `assets/images/` with naming: `FirstName.jpg`

## 🎨 Navigation

- **Landing Page** (`/`): Interactive dashboard selection with modern card interface
- **Running Dashboard** (`/pages/running.html`): Full Løpegruppen management (ScreenCloud ready)
- **Fantasy Football** (`/pages/fantasy-football.html`): League analytics and predictions (ScreenCloud ready)

### Usage Patterns:
- **Interactive Browsing**: Use landing page to navigate between dashboards
- **ScreenCloud Display**: Access individual pages directly via URL for digital signage
- **Development**: Landing page provides easy access during development and testing

## 🔧 Features in Detail

### Multi-Page Architecture:
- Clean URL structure with logical page separation
- Consistent navigation between dashboards
- Shared asset management across pages

### Responsive Design:
- Mobile-first CSS approach
- Flexible grid systems that adapt to screen size
- Optimized layouts for each dashboard type

### Data Integration:
- CSV-based data management (running events)
- Live API integration (Fantasy Premier League)
- Auto-refresh functionality for live updates
- Smart caching with localStorage fallback
- CORS proxy handling for external APIs
- ScreenCloud compatible refresh intervals

### ScreenCloud Optimization:
- Navigation-free individual pages for clean display
- Direct URL access for digital signage setup
- Full-screen content utilization without wasted space
- Automatic data refresh cycles (5 minutes for FPL, 10 minutes for Strava)
- Professional display appearance optimized for viewing from distance
- Cross-browser compatibility with vendor prefixes for older display hardware

## 🌐 Live Site

Visit: [https://alistairjohnbrown.github.io](https://alistairjohnbrown.github.io)

## 🎯 Recent Updates

### Fantasy Football Enhancements:
- **Live API Integration**: Now pulls real data from Fantasy Premier League API
- **Smart Caching**: 24-hour localStorage cache prevents loading issues
- **Position Indicators**: Shows ↑↓ movement from previous gameweek
- **Compact Layout**: Optimized table design fits more teams on screen
- **Gameweek Display**: Shows current gameweek and deadline information

### ScreenCloud Optimizations:
- **Browser Compatibility**: Enhanced with vendor prefixes for older display browsers
- **Debug Mode**: Added `?screencloud-debug` parameter for layout testing
- **Flexbox Migration**: Moved from CSS Grid to Flexbox for better compatibility
- **Layout Fixes**: Resolved stacking issues with logo/admin and three-column layouts

## 🔧 Features in Detail

### Anti-Caching for Live Data
- **Strava Widgets**: Automatic iframe refresh every 10 minutes with cache-busting
- **FPL Data**: Smart caching with 24-hour localStorage and 5-minute refresh cycles
- **Meta Tags**: Prevent browser caching for always-fresh content

### Responsive Design
- Mobile-first CSS approach
- Flexbox-based layouts with vendor prefixes for maximum compatibility
- Optimized emoji and text sizing
- ScreenCloud browser compatibility testing tools

### API Integration & Reliability
- **Fantasy Premier League**: Live data with multiple CORS proxy fallbacks
- **Smart Caching**: localStorage with 24-hour TTL and graceful degradation
- **Error Handling**: Clean fallback messages when APIs unavailable
- **Position Tracking**: Shows team movement with ↑↓ indicators

### Accessibility
- Semantic HTML structure
- Alt text for all images
- High contrast color schemes
- Keyboard navigation support

## 📝 License

Built for Løpegruppen with ❤️ and lots of ☕

---

*Based in Sotra, Norway 🇳�*