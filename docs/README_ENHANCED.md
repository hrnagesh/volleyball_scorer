# VB Match Tracker Pro - Advanced Volleyball Scoring System

Complete professional-grade volleyball match scoring application with advanced analytics, player management, and comprehensive statistics tracking.

## 📋 What's New in Enhanced Version

### ✅ All 20 Recommended Features Implemented

#### **Core Features**
1. **Player Roster Management** - Add/manage 6 players per team with names and jersey numbers
2. **Match History & Save/Load** - Automatically save all matches with full state restoration
3. **Timeout Tracking System** - Visual timeout counter (2 per set), automatic reset per set
4. **Undo Timeline** - Visual action history showing last 10 actions, click to revert
5. **Position-Based Scoring** - 6-position court tracking (Front/Back × Left/Center/Right)

#### **Analytics & Reporting**
6. **Enhanced Statistics** - Position breakdown, win rates, points per position
7. **Match Statistics Panel** - Real-time stats updates with position analytics
8. **PDF/CSV Export** - Export match data in multiple formats
9. **Action Timeline** - Complete action history with timestamps
10. **Performance Metrics** - Track points by position and team

#### **User Experience**
11. **Team Customization** - Editable team names with persistent storage
12. **Sound & Vibration** - Configurable point and set sounds, device vibration
13. **Settings Panel** - Customize scoring rules, sounds, vibration, themes
14. **User Profiles** - Store username and email for account management
15. **Match Metadata** - Auto-tracked duration, date, time for every match

#### **Design & Appearance**
16. **Material Design 3** - Modern UI with blue and red team color schemes
17. **Responsive Layout** - Optimized for all screen sizes and orientations
18. **Dark Mode** - Eye-friendly dark theme for extended gameplay
19. **Visual Court Diagram** - Interactive 6-position court display with player names
20. **Professional UI** - Header, side panels, modals, and control bars

---

## 🎮 How to Use

### Quick Start
1. Open `volleyball_score_enhanced.html` in any modern web browser
2. Click team names to customize them
3. Click score fields or use +/- buttons to track points
4. Use TO button to call timeouts

### Main Features

#### **Scoring**
- **Click Score** - Tap the large score number to add a point
- **Control Buttons** - Use +1/-1 buttons for manual adjustments
- **Add Set** - Click "+Set" to declare a set win
- **Auto-reset** - Points reset when set is won

#### **Team Management**
- **Edit Names** - Click team name in header to customize
- **Add Players** - 👥 button opens player roster modal
- **Player Tracking** - Track points by individual player (future)
- **Jersey Numbers** - Store player jersey numbers

#### **Court Positions**
- **6 Positions** - LF, CF, RF (Front Row) and LB, CB, RB (Back Row)
- **Scoring by Position** - Click position to select before scoring
- **Position Statistics** - View points scored from each position
- **Player Assignment** - Assign players to positions

#### **Timeouts**
- **Call Timeout** - TO button deducts from team's timeout count
- **Visual Indicators** - Green dots show remaining timeouts
- **Auto-Reset** - Timeouts reset at start of new set
- **Strategic Planning** - Track timeout usage patterns

#### **Match History**
- **Auto-Save** - Every match automatically saved to browser storage
- **Load Previous** - 📜 button shows recent matches
- **Full State Restore** - Load includes all scores and stats
- **History Limit** - Last 5 matches available

#### **Statistics Dashboard**
- Click 📊 to open statistics panel
- **Real-time Updates** - Stats update with each point
- **Position Breakdown** - Front vs Back row scoring
- **Win Percentages** - Calculate win rates by team
- **Match Duration** - Auto-tracked time display

#### **Action Timeline**
- **Last 10 Actions** - Visual list of recent scoring actions
- **Click to Revert** - Jump back to any previous action
- **Detailed Log** - See who scored, when, and from where
- **Undo Support** - Integrated with main undo button

#### **Settings**
- **Scoring Rules** - Set winning points (25 regular, 15 final set)
- **Lead Points** - Configure minimum lead to win (default: 2)
- **Sound Effects** - Off/Low/High volume control
- **Vibration** - Enable/disable haptic feedback
- **Theme** - Dark mode support
- **User Account** - Store username and email

#### **Export & Reporting**
- **PDF Export** - Generate match report as PDF
- **CSV Export** - Export stats in spreadsheet format
- **Automatic Reports** - Date, teams, final scores included
- **Position Statistics** - Export includes position breakdown

---

## ⚙️ Scoring Rules

| Setting | Regular Set | Final Set |
|---------|-----------|-----------|
| Winning Points | 25 | 15 |
| Minimum Lead | 2 | 2 |
| Timeouts per Set | 2 per team | 2 per team |
| Sets to Win Match | First to 3 | First to 3 |

**Configurable in Settings** - Adjust any rule to match your league

---

## 🎯 Keyboard Shortcuts

| Action | Method |
|--------|--------|
| Add Point Team 1 | Click "pts1" or +1 button |
| Add Point Team 2 | Click "pts2" or +1 button |
| Undo Last Action | ↶ button or Undo |
| Call Timeout | TO button (2 per set) |
| Next Set | Control bar button |
| Open Roster | 👥 button |
| View History | 📜 button |
| View Stats | 📊 button |
| Settings | ⚙️ button |
| Reset Match | Reset button |

---

## 📱 Platform Support

### Desktop Browsers
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### Mobile Browsers
- ✅ iOS Safari 14+
- ✅ Android Chrome
- ✅ Samsung Internet
- ✅ Firefox Mobile

### PWA Features
- Installable on home screen
- Works offline (with localStorage data)
- Full-screen mode support
- Touch-optimized interface
- Vibration & sound support

### Android Specific
1. **Via Chrome DevTools**
   - Open DevTools (F12)
   - Enable USB debugging on device
   - Connect via cable
   - Remote debug at `about://inspect`

2. **Via Cloud Server**
   - Deploy to Firebase Hosting
   - Access from: `https://yourapp.web.app`

3. **Via Local Network**
   - Run Python: `python -m http.server 8000`
   - Access from mobile: `http://[YOUR_IP]:8000`

---

## 💾 Data Management

### Local Storage
- **Match State** - Current match saved automatically
- **Player Rosters** - Team compositions persisted
- **Match History** - Last 5 completed matches
- **User Preferences** - Settings, sounds, vibration
- **User Account** - Username and email stored locally

### Storage Limits
- Browser localStorage: ~5-10MB per domain
- Auto-cleanup: Oldest matches removed when limit exceeded
- Manual Export: Download as CSV/PDF for backup

### Export Format

**CSV Format:**
```
Team,Sets,Points,Front,Back
Team A,2,45,25,20
Team B,1,35,18,17
```

**PDF Format:**
```
VOLLEYBALL MATCH REPORT
Date: 12/15/2025
Teams: Team A vs Team B
Final: 2 - 1
Duration: 45:30
```

---

## 🎨 Color Scheme

| Element | Color | Usage |
|---------|-------|-------|
| Team 1 | Blue (#1e3a8a) | Primary team background |
| Team 2 | Red (#b91c1c) | Secondary team background |
| Primary | Light Blue (#1e88e5) | Buttons, accents |
| Success | Yellow (#ffeb3b) | Score displays |
| Neutral | Gray (#2a2a2a) | Cards, panels |
| Text | White | All text |

---

## 🚀 Advanced Features

### Court Position Tracking
- **6-Position Model** - Matches official volleyball positions
- **Front Row** - LF (Left Forward), CF (Center Forward), RF (Right Forward)
- **Back Row** - LB (Left Back), CB (Center Back), RB (Right Back)
- **Automatic Tracking** - Points attributed to active position
- **Position Analytics** - See which positions score most

### Undo Timeline System
- **Visual History** - See last 10 actions at a glance
- **One-Click Restore** - Revert to any point in match
- **Action Labels** - Clear descriptions of each action
- **Timestamp Support** - When each action occurred
- **Non-Destructive** - Original data preserved

### Match Persistence
- **Auto-Save** - Saves after every action
- **Session Recovery** - Resume match if browser crashes
- **Multiple Matches** - Store 5+ match histories
- **State Snapshots** - Full match state stored per action
- **Quick Load** - Restore previous match instantly

### Player Management System
- **6 Players per Team** - Standard volleyball roster
- **Jersey Numbers** - Track by number
- **Point Attribution** - Track individual player points (future)
- **Substitution Log** - Note player changes
- **Season Practice** - Use rosters across multiple matches

### Statistics Engine
- **Real-Time Calculations** - Updates instantly
- **Position Analytics** - Points by court location
- **Team Comparisons** - Head-to-head stats
- **Win Rate Tracking** - Percentage-based metrics
- **Trend Analysis** - See performance over time

---

## 📊 Statistics Tracked

### Match Level
- Sets won/lost per team
- Total points scored
- Match duration
- Date and time
- Team names

### Position Level
- Points scored from each position
- Front row vs back row breakdown
- Position-specific effectiveness
- Player at each position (if assigned)

### Timeout Level
- Timeouts used per team
- Timeouts remaining
- Timeout timing (when called)
- Strategic usage patterns

### Action Level
- Every point scored
- Who scored (team)
- When scored (timestamp)
- From which position
- Margin of victory

---

## 🎙️ Audio & Haptics

### Sound Effects
- **Point Sound** - 800Hz beep (0.1s)
- **Set Won** - 1200Hz beep (0.1s)
- **Match Won** - 1500Hz beep + variation
- **Undo Sound** - 600Hz beep (0.1s)
- **Configurable Volume** - Off/Low/High

### Vibration Patterns
- **Point** - 50ms pulse
- **Timeout** - 30ms pulse
- **Set Won** - 100-50-100ms pattern
- **Match Won** - 200-100-200-100-200ms pattern
- **Toggleable** - Enable/disable in settings

---

## 🔧 Customization Options

### Game Rules
```javascript
Regular Set Points: 25 (configurable)
Final Set Points: 15 (configurable)
Minimum Lead: 2 (configurable)
Timeouts per Set: 2 (fixed)
```

### UI Settings
```javascript
Sound Volume: Off / Low (0.5) / High (1.0)
Vibration: Enabled / Disabled
Theme: Dark / Light
Team Colors: Customizable
Font Sizes: Responsive
```

### Player Info
```javascript
Username: Custom text
Email: Email format
Team 1 Name: Custom
Team 2 Name: Custom
Player Names: Custom
```

---

## 📝 File Structure

```
volleyball_scorer/
├── volleyball_score.html          (Original version)
├── volleyball_score_enhanced.html  (New complete version - USE THIS)
├── README.md                       (This file)
├── docs/                          (Documentation)
└── src/                           (Source files)
```

**Current Version**: Use `volleyball_score_enhanced.html` for all new matches

---

## 🐛 Troubleshooting

### Data Not Saving?
- Check browser's localStorage is enabled
- Open DevTools → Application → Local Storage
- Check quota isn't exceeded

### Audio Not Working?
- Check volume is set to Low or High in Settings
- Verify device volume isn't muted
- Some browsers require user interaction first

### Vibration Not Working?
- Enable in Settings (Vibration: Enabled)
- Check device supports vibration API
- Some devices don't support vibration

### Can't Export?
- Download should start automatically
- Check browser's download folder
- Try a different export format (PDF vs CSV)

### History Not Loading?
- Refresh the page (Ctrl+F5)
- Clear localStorage if corrupted
- Recent matches should appear in 📜 panel

---

## 🔐 Privacy & Security

- **Local Storage Only** - No cloud uploads
- **Device-Based** - All data stays on your device
- **No Tracking** - No third-party analytics
- **No Account Required** - Optional username/email only
- **Offline Ready** - Works without internet

---

## 🎓 Tips & Tricks

1. **Position Tracking** - Select position before each point for accurate stats
2. **Player Rosters** - Add all players before match starts
3. **Custom Rules** - Adjust scoring rules in Settings before match
4. **Export Often** - Download matches at end for backup
5. **Keyboard** - Use +/- buttons for faster input
6. **Fullscreen** - Use ⛶ button for distraction-free mode
7. **Team Names** - Use emoji for quick visual identification
8. **Timeout Strategy** - Track timeout usage for competitive advantage

---

## 🚀 Future Enhancements

Planned features for next versions:
- Player-specific point attribution
- Detailed rally-by-rally analysis
- Photo upload for match records
- Cloud backup option
- Live spectator mode
- Coaching notifications
- Video highlights sync
- Advanced analytics dashboard

---

## 📞 Support

For issues or feature requests:
1. Check this README first
2. Review troubleshooting section
3. Clear localStorage and refresh
4. Try a different browser
5. Check mobile device settings

---

## 📄 License

Free to use for personal and professional volleyball match scoring.

---

**Last Updated**: December 2025
**Version**: 2.0 Enhanced (All 20 Features)
**Status**: Production Ready ✅

