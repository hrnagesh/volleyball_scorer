# VB Match Tracker 🏐

A mobile-first volleyball match scoring application with user authentication, real-time statistics, and persistent data storage.

## Features

✨ **Core Functionality**
- Real-time point tracking for 2 teams
- Automatic set winner detection
- Match completion with victory alerts
- Undo/Redo functionality for quick corrections
- Sound and vibration feedback on events

👤 **User System**
- GitHub OAuth login integration (requires backend)
- Manual username/email entry with validation
- User profile persistence
- Logout functionality

📊 **Statistics & Analytics**
- Live match statistics panel
- Points per set tracking
- Win rate calculations
- Current set point display
- Match history with set records
- **Position-based scoring** (Front/Back row breakdown)
- Player position performance tracking (6-position court)

🎮 **Interface**
- Responsive design for all devices
- Fullscreen support on mobile
- Landscape and portrait orientation support
- Dark theme optimized for indoor use
- Touch-friendly buttons and controls
- Keyboard shortcuts support

⌨️ **Keyboard Shortcuts**
- `1` - Add point to Team 1
- `2` - Add point to Team 2
- `Z` - Undo Team 1 action
- `X` - Undo Team 2 action
- `Space` - Start next set
- `R` - Reset entire match

## Project Structure

```
volleyball_scorer/
├── README.md                    # This file
├── volleyball_score.html        # Main application (all-in-one)
├── src/                         # Source code folder (for future modularization)
│   └── (future JS/CSS modules)
└── docs/                        # Documentation
    └── (future documentation files)
```

## Getting Started

### Quick Start
1. Open `volleyball_score.html` in a modern web browser
2. Click "Login" to create a user account
3. Edit team names by clicking on them
4. Tap each team's scoring area to add points
5. Use buttons at the bottom for additional controls

### Browser Requirements
- Modern browser with ES6 support
- LocalStorage enabled
- Audio context support (for sound effects)
- Vibration API support (optional, for haptic feedback)

### Android Mobile Setup

#### Option 1: Using a Local Server (Recommended)
1. **Share file via Local Network**:
   - On Windows: Right-click `volleyball_score.html` → Properties → Share
   - Or use a simple HTTP server: `python -m http.server 8000`
   - Or use: `npx http-server`

2. **Access on Android**:
   - Find your computer's IP address (e.g., 192.168.1.100)
   - On Android phone, open browser and go to: `http://192.168.1.100:8000/volleyball_score.html`
   - Or directly: `http://192.168.1.100/volleyball_scorer/volleyball_score.html`

#### Option 2: Using Chrome DevTools DevServer
1. Connect Android phone via USB
2. Enable Developer Options on Android (tap Build Number 7 times)
3. Open Chrome on PC → DevTools → Remote Devices
4. Forward port and access locally

#### Option 3: Using a Cloud Service
1. Upload `volleyball_score.html` to GitHub Pages, Firebase Hosting, or Vercel
2. Share the public URL with your Android phone
3. Open in browser on your phone

#### Android Browser Recommendations
- **Chrome** (Best): Best compatibility, all features work
- **Firefox**: Full feature support
- **Samsung Internet**: Good performance
- **Edge**: Full compatibility

#### Adding to Home Screen (Android)
1. Open the URL in your browser
2. Tap the **Menu** (⋮) button
3. Select **"Add to Home screen"** or **"Install app"**
4. App will appear as an icon on your home screen
5. Launch like a native app for full-screen experience

#### Tips for Mobile Use
- **Fullscreen Mode**: Auto-activates on mobile (tap anywhere to keep it)
- **Notch Support**: App respects safe areas for phones with notches
- **Landscape Mode**: Rotate phone for wider scoring area
- **Storage**: Data saves locally - works offline once loaded
- **Battery Saver**: Use dark theme (already enabled)

#### Android-Specific Features Working
✅ Touch feedback (haptic vibration)  
✅ Sound effects (volume controlled by device)  
✅ Fullscreen mode  
✅ localStorage (persistent data)  
✅ Home screen shortcut  
✅ Orientation changes  

#### Troubleshooting on Android
| Issue | Solution |
|-------|----------|
| Can't connect to local server | Ensure both devices on same WiFi network |
| Static page won't load | Use a local HTTP server instead |
| Vibration not working | Enable haptics in phone settings |
| Sound not playing | Check volume is on and not muted |
| Data not saving | Ensure localStorage is enabled in browser settings |
| Page cuts off by notch | Update browser to latest version |

## Usage

### Team Management
- **Edit Team Names**: Click on team name in header to rename
- **Switch Teams**: The current scoring team is highlighted

### Scoring
- **Add Point**: Tap the large scoring area or use `1/2` keys
- **Add Set**: Click "+Set" button (automatic on winning points)
- **Undo**: Click "Undo" button or press `Z/X` keys
- **Adjust Score**: Use "-1" button to correct mistakes

### User Login
1. Click "Login" button in header
2. Choose: GitHub login or manual entry
3. For manual entry:
   - Username: 3-50 characters (letters, numbers, dash, underscore)
   - Email: Valid email format required
4. Click "Save" to complete login

### Position Tracking (Player Position Performance) 🆕
Track scoring by player position on the court:

**Available Positions:**
- **Front Row**: Front Left (LF), Front Center (CF), Front Right (RF)
- **Back Row**: Back Left (LB), Back Center (CB), Back Right (RB)

**How to Use:**
1. Click the **"📍 Pos"** button in the controls
2. Select the position that scored the point
3. Click the position button before scoring (or right after)
4. Position points are tracked automatically with each score
5. View position statistics in the **Stats** panel

**Position Statistics:**
- Each team shows front/back row scoring breakdown
- Total points by position and row tracked in match analytics
- Use this data to analyze player and formation effectiveness

**Example Workflow:**
1. Match starts, click "📍 Pos" 
2. Select "Front Center (CF)" 
3. Now each point scored will be attributed to CF position
4. Change position anytime before/after a point
5. Stats show CF had 8 points, LF had 5 points, etc.

### Statistics
- Click "📊" to view match analytics
- Shows real-time updates
- Includes points per set and win percentages
- **NEW**: Position-based scoring breakdown (front/back row)

### Reset
- Click "Reset" to clear match (preserves user and team names)
- Full Reset removes all data

## Scoring Rules

### Regular Sets
- First to 25 points
- Must win with 2+ point lead
- (e.g., 25-23 wins, 25-20 wins, but 24-25 continues)

### Final Set (5th)
- First to 15 points
- Must win with 2+ point lead
- Played when sets are 2-2

### Match
- Best of 5 sets
- First team to win 3 sets wins match

## Data Storage

All data is stored locally in browser:
- **Match State**: Current scores, sets, team names
- **User Info**: Username and email
- **History**: Point-by-point action history for undo functionality
- **Set History**: Complete records of all sets played

Data persists between browser sessions until cleared.

## Configuration

### Audio Context
Sound effects can be disabled by modifying the `playSound()` function.

### GitHub OAuth (Future Implementation)
To enable GitHub login:
1. Register OAuth app on GitHub
2. Update `clientId` in `initiateGitHubLogin()` function
3. Set up backend endpoint to handle OAuth callback
4. Update `redirectUri` accordingly

### Scoring Parameters
```javascript
const REGULAR_SET_WIN = 25;  // Points needed to win regular set
const FINAL_SET_WIN = 15;    // Points needed to win final set
const MIN_LEAD = 2;           // Minimum point lead to win
```

## Responsive Design

The app automatically adapts to:
- **Mobile**: Portrait and landscape modes
- **Tablet**: Optimized layouts
- **Desktop**: Full-featured display
- **Small Screens** (height < 500px): Condensed layouts

## Known Limitations

- Single page application (no persistence to cloud)
- GitHub OAuth requires backend implementation
- No real-time multiplayer support
- No match replay/analysis features

## Future Enhancements

- [x] Position-based scoring (Front/Back row tracking)
- [ ] Individual player position heatmaps
- [ ] Backend database for cloud storage
- [ ] GitHub OAuth full implementation
- [ ] Match history replay
- [ ] Advanced player statistics tracking
- [ ] Tournament mode
- [ ] Export match data (CSV, PDF)
- [ ] Offline PWA support
- [ ] Multi-language support
- [ ] AI-powered analytics and recommendations

## Browser Support

- Chrome/Chromium: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support (iOS 14+)
- Edge: ✅ Full support
- IE 11: ❌ Not supported

## License

This project is open source and available for personal and community use.

## Support

For issues or feature requests, please contact the development team.

---

**Version**: 1.0.0  
**Last Updated**: February 2026  
**Built for**: Volleyball match tracking and scoring
