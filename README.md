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

### Statistics
- Click "Stats" to view match analytics
- Shows real-time updates
- Includes points per set and win percentages

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

- [ ] Backend database for cloud storage
- [ ] GitHub OAuth full implementation
- [ ] Match history replay
- [ ] Player statistics tracking
- [ ] Tournament mode
- [ ] Export match data (CSV, PDF)
- [ ] Offline PWA support
- [ ] Multi-language support

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
