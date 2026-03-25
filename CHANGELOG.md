# Changelog - 全球大事件日历

## v2.0 - Location Scope Filtering (2026-03-25)

### ✨ New Features

#### 🌍 Geographic Location Filtering
- Added dual-layer filtering system combining **Event Type** + **Geographic Scope**
- New location scope filter with 5 options:
  - 🌍 **全部** (All) - Show all events
  - 🏙️ **杭州** (Hangzhou) - City-level events
  - 🏯 **浙江** (Zhejiang) - Province-level events
  - 🇨🇳 **全国** (National) - China-wide events
  - 🌐 **全球** (Global) - Worldwide events

#### 📊 Event Data Enhancement
- Added `locationScope` field to all 42 events
- Scope distribution:
  - 20 Global events (FIFA World Cup, Wimbledon, Apple Events, etc.)
  - 20 National events (Chinese festivals, concerts, shopping festivals)
  - 1 Province event (Midi Music Festival in Zhejiang)
  - 1 City event (Jay Chou concert in Hangzhou)

#### 🎨 UI/UX Improvements
- Reorganized filter section with clear labels:
  - 📋 Event Type filter (top)
  - 📍 Location Scope filter (bottom)
- Added location scope badges on event cards with color coding:
  - 🏙️ Hangzhou: Green (#22c55e)
  - 🏯 Zhejiang: Purple (#a855f7)
  - 🇨🇳 National: Gold (#f5c518)
  - 🌐 Global: Blue (#3b82f6)
- Event cards now display both type and location scope tags

### 🔧 Technical Changes

#### JavaScript
- Added `currentScope` state variable for location filtering
- Updated `getEventsForDate()` to filter by both type AND scope
- Updated `getEventTypesForDate()` to respect scope filter
- Added location scope filter event listeners
- Enhanced event card rendering with scope badges

#### CSS
- New `.location-scope` class with scope-specific colors
- Updated `.filter-section` for better organization
- Added `.filter-label` for filter section headers
- Improved `.filter-tabs-location` styling for location filters
- Added `.event-tags` container for multiple tags per event

#### HTML
- Split filter section into two parts:
  - Event Type filters (6 options)
  - Location Scope filters (5 options)
- Added `data-scope` attributes to location filter tabs
- Updated event card structure to display both tags

### 📈 Event Scope Mapping

**Global Events (20):**
- Sports: FIFA World Cup, Wimbledon, World Athletics, Asian Games
- Global Holidays: New Year, Valentine's Day, White Day, April Fools, Earth Day, International Labor Day, World Environment Day, Bastille Day, Halloween, Thanksgiving, Christmas
- Tech: Apple Events, WWDC

**National Events (20):**
- Chinese Festivals: Spring Festival, Qingming, Labor Day, Dragon Boat, Mid-Autumn, National Day, Double Eleven, Double Twelve
- Concerts: Taylor Swift (Shanghai), Coldplay (Beijing), Zhang Xueyou (Shanghai), May Day (Beijing)
- Shopping: Double Eleven, Double Twelve

**Province Events (1):**
- Midi Music Festival (Zhejiang)

**City Events (1):**
- Jay Chou Concert (Hangzhou)

### 🚀 Deployment

- ✅ Code pushed to GitHub: https://github.com/boyzhoulei-del/event-calendar
- ✅ Latest commit: `6680ae2` - feat: add location scope filtering
- ⏳ GitHub Pages deployment: Enable in repo Settings → Pages

### 📝 File Changes

- `index.html`: +152 lines (26.4 KB total)
- `SPEC.md`: Updated with location scope specifications
- `CHANGELOG.md`: This file

### 🎯 Usage

1. **Select Event Type**: Click tabs to filter by Sports, Festivals, Concerts, Tech, etc.
2. **Select Location Scope**: Click tabs to filter by Hangzhou, Zhejiang, National, or Global
3. **Combine Filters**: Both filters work together - only events matching BOTH criteria are shown
4. **View Events**: Click any date to see filtered events for that day

### ✅ Testing Checklist

- [x] All 42 events have locationScope field
- [x] Filters work independently
- [x] Filters work in combination
- [x] Calendar dots update based on filters
- [x] Event cards display both type and scope badges
- [x] No duplicate events
- [x] CSS braces balanced
- [x] HTML structure valid
- [x] Git history clean
- [x] Code pushed to GitHub

---

**Version**: 2.0  
**Release Date**: 2026-03-25  
**Status**: Ready for GitHub Pages deployment
