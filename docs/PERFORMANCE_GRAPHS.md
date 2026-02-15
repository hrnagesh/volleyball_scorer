# Performance Graphs 📈 - Feature Documentation

Advanced visual analytics for volleyball match performance tracking and analysis.

## Overview

Performance Graphs provide real-time visual representations of match data, helping coaches and players analyze patterns, trends, and performance metrics throughout the game.

## Available Charts

### 1. **Point Progression Chart**
**Type**: Line Chart  
**Shows**: Point trends over time for both teams

**Features**:
- Real-time point tracking
- Visual comparison between teams
- Color-coded lines (Blue for Team A, Red for Team B)
- Point markers at each recorded point
- Entire match progression in one view

**What It Shows**:
- How teams scored over the course of the match
- Lead changes and momentum shifts
- Game progression from start to finish
- Performance consistency

**Use Cases**:
- Analyze scoring patterns
- Identify critical momentum points
- See which team dominated scoring
- Track comebacks and run scoring

---

### 2. **Set-by-Set Scores Chart**
**Type**: Bar Chart  
**Shows**: Final score of each set

**Features**:
- Visual comparison of set scores
- Up to 5 sets displayed
- Side-by-side team scores
- Color-coded by team

**What It Shows**:
- How close each set was
- Which set was most competitive
- Winning margins for each set
- Set progression difficulty

**Use Cases**:
- Quick overview of match difficulty
- Identify problem sets
- See if team improved/declined
- Plan strategy for future matches

---

### 3. **Position Breakdown Charts (Team A & Team B)**
**Type**: Bar Chart  
**Shows**: Points scored from each court position

**Positions Tracked**:
- **LF** - Left Forward
- **CF** - Center Forward  
- **RF** - Right Forward
- **LB** - Left Back
- **CB** - Center Back
- **RB** - Right Back

**Features**:
- Color-coded by position
- Value labels on each bar
- Both teams displayed separately
- Easy position identification

**What It Shows**:
- Which positions are most effective
- Position-specific performance
- Court coverage quality
- Rotation effectiveness

**Use Cases**:
- Identify your strongest positions
- Find weak spots in the court
- Optimize player placement
- Train specific position skills
- Analyze opponent strengths

---

### 4. **Front vs Back Row Performance Chart**
**Type**: Bar Chart  
**Shows**: Total points from front and back rows

**Data Displayed**:
- Team A Front Row total
- Team A Back Row total
- Team B Front Row total
- Team B Back Row total

**Features**:
- Clear front/back distinction
- Team comparison
- Performance balance visualization
- Strategy effectiveness indicator

**What It Shows**:
- Front row dominance vs back row
- Attacking power distribution
- Defensive contribution
- Balanced offensive strategy

**Use Cases**:
- Evaluate front row attack effectiveness
- Assess back row defense contribution
- Balance team positioning
- Identify tactical advantages
- Adjust serving strategy

---

## How to Access Performance Graphs

### In the App:
1. Click **📈 Graphs** button in the header
2. Performance Graphs modal opens
3. View all available charts
4. Scroll through for detailed analysis

### Charts You Can View:
- Point Progression (line chart)
- Set Scores (bar chart)
- Team A Position Breakdown (bar chart)
- Team B Position Breakdown (bar chart)
- Front vs Back Row Performance (bar chart)

---

## Reading the Charts

### Color Legend

**Team Colors**:
- 🔵 Blue variations = Team A
- 🔴 Red variations = Team B

**Position Colors (Team A)**:
- #1e88e5 = LF (Light Blue)
- #42a5f5 = CF (Medium Blue)
- #90caf9 = RF (Light Blue)
- #1565c0 = LB (Dark Blue)
- #0d47a1 = CB (Darker Blue)
- #1976d2 = RB (Navy)

**Position Colors (Team B)**:
- #ff6b6b = LF (Light Red)
- #ef5350 = CF (Medium Red)
- #e53935 = RF (Red)
- #c62828 = LB (Dark Red)
- #b71c1c = CB (Darker Red)
- #a71a1a = RB (Maroon)

---

## Chart Analysis Tips

### Point Progression Analysis

```
Features to Look For:
- Steep climbs = scoring runs
- Flat sections = defensive rallies
- Intersection points = score ties
- Parallel lines = tight competition
- Diverging lines = one team pulling ahead
```

**What Good Point Progression Looks Like**:
- Relatively balanced climbing
- Multiple lead changes (competitive)
- Steady improvement if winning

**Warning Signs**:
- One team's line much higher = dominated
- Flat lines = team stuck without scoring

---

### Set Scores Analysis

```
Competitive Set: Close bar heights
Dominant Set: Large difference in bar heights
Shutout: One team much taller
```

**What to Look For**:
- Are sets getting closer or further apart?
- Did the team improve between sets?
- Which sets were struggles?

---

### Position Breakdown Analysis

```
Balanced Position: Similar bar heights
Concentrated Scoring: Few tall bars
Weak Positions: Very short bars
```

**Good Indicators**:
- Multiple positions contributing points
- No single position dominates excessively
- Back row contributing significantly

**Problem Indicators**:
- One position much higher than others
- Some positions with zero points
- Imbalanced front/back distribution

---

## Using Graphs for Strategy

### Before the Match
- Review previous match graphs
- Identify opponent patterns
- Plan position strengths
- Set defensive focus areas

### During the Match
- Periodically refresh graphs
- Monitor momentum shifts
- Identify score patterns
- Adjust strategy as needed

### After the Match
- Analyze overall performance
- Identify improvement areas
- Track progress over matches
- Plan training focus

---

## Data Collection for Graphs

### Automatically Tracked:
- Every point scored (recorded in action history)
- Position of each point (when selected)
- Set completion scores
- Match duration
- Team names and scores

### For Accurate Graphs:
1. **Select Position** before each point (for position stats)
2. **Complete the match** (use Next Set button)
3. **View graphs** after significant scoring events
4. **Refresh graphs** for latest data (📈 → Refresh button)

### What Gets Displayed:
- If no points scored: empty chart
- If partial data: available data shown
- If complete match: full analytics

---

## Interpreting Key Metrics

### Point Progression
```
Formula: \(\text{Points} = \text{Running Total from Start}\)
Interpretation: Higher line = more points scored
```

### Set Win Rate
```
Formula: \(\text{Win \%} = \frac{\text{Sets Won}}{\text{Total Sets}} \times 100\)
Example: Win 2 of 3 sets = 66%
```

### Position Effectiveness
```
Formula: \(\text{Pts from Pos} = \sum \text{Points scored from that position}\)
Interpretation: Taller bar = more effective position
```

### Front/Back Distribution
```
Formula: 
Front = LF + CF + RF
Back = LB + CB + RB
```

---

## Refresh & Update

### Refreshing Graphs:
- Click **Refresh Graphs** button in modal
- Updated automatically when modal opens
- Charts reflect current match state
- Historical data included

### When Graphs Update:
- When you add a point
- When you call a timeout
- When a set ends
- When you undo an action

---

## Troubleshooting Graphs

| Issue | Cause | Solution |
|-------|-------|----------|
| Empty charts | No points recorded | Score some points and refresh |
| Missing data | Position not selected | Select position before scoring |
| Outdated data | Not refreshed | Click "Refresh Graphs" button |
| No set data | Set not completed | Use "Next Set" button |
| Misaligned data | Match in progress | Complete additional points |

---

## Performance Graph Features

### Canvas-Based Rendering
- Lightweight (no external libraries)
- Fast updates
- Works offline
- Responsive to data changes

### Automatic Scaling
- Adapts to match score ranges
- Responsive to data values
- Proper axis labeling
- Grid for reference

### Color Accessibility
- Team colors distinct
- High contrast for visibility
- Position color differentiation
- Legend clearly labeled

---

## Integration with Other Features

### Works With:
- ✅ Position Tracking System
- ✅ Match History
- ✅ Undo/Redo Timeline
- ✅ Player Rosters
- ✅ Real-time Statistics
- ✅ Match Metadata

### Data Persistence:
- Graphs save with match
- Reload previous match = reload graphs
- Export includes graph data
- Historical matches preserve graphs

---

## Advanced Analysis

### Momentum Analysis
Watch the Point Progression chart for:
- **Positive Momentum**: Line climbing steadily
- **Momentum Swing**: Line changes from flat to steeply climbing
- **Momentum Loss**: Line flattens unexpectedly

### Pattern Recognition
Look for repeats in:
- Scoring positions (do certain positions score regularly?)
- Scoring patterns (do certain teams score in runs?)
- Set patterns (do similar positions score similarly each set?)

### Tactical Insights
From Position Breakdown charts:
- **Strength**: Highest bars show your best attacking positions
- **Weakness**: Lowest bars show vulnerable positions
- **Balance**: Distributed heights indicate balanced play
- **Consistency**: Similar heights across positions

---

## Quick Reference

**To View Graphs**: Header → 📈 Graphs

**Available Charts**:
1. Point Progression (how each point was scored over time)
2. Set Scores (final scores for each set)
3. Position Breakdown T1 (Team A position distribution)
4. Position Breakdown T2 (Team B position distribution)
5. Front vs Back (row-based analysis)

**To Refresh**: Click "Refresh Graphs" button

**To Close**: Click "Close" button

---

## Best Practices

1. **Review after sets** - Understand what happened
2. **Track patterns** - Note recurring sequences
3. **Compare teams** - Use charts for head-to-head analysis
4. **Train accordingly** - Focus on weak positions
5. **Export with match** - Save graphs with match data
6. **Use for strategy** - Adjust positions based on data

---

## Frequently Asked Questions

**Q: Why are some charts empty?**
A: No data recorded yet. Score points and select positions.

**Q: Do I need to select position for graphs?**
A: For position breakdown charts, yes. Other charts work without it.

**Q: Can I export the graphs?**
A: The graph data is exported with PDF/CSV match exports.

**Q: How far back do graphs show?**
A: Current match only. Each match has its own graphs.

**Q: Can I compare two matches visually?**
A: Load each match separately and view graphs. Export for external comparison.

**Q: Why is position data missing?**
A: Position wasn't selected when points were scored. Select position before points in future matches.

---

## Version Information

**Feature**: Performance Graphs 📈  
**Status**: ✅ Implemented  
**Version**: 2.1  
**Added**: December 2025  
**Dependencies**: None (Canvas API)  
**Browser Support**: All modern browsers  

---

**Last Updated**: December 2025  
**Next Review**: As features evolve
