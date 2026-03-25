# 🌍 全球大事件日历 - Global Events Calendar

A mobile-friendly web app showcasing major global events for 2026, including sports, festivals, concerts, and tech events.

## ✨ Features

- **📱 Mobile-First Design**: Optimized for 375px baseline, responsive on all devices
- **🎨 Dark Theme**: Modern dark UI with gold accents (#0a0a0f background)
- **📅 Interactive Calendar**: Month navigation, click dates to view events
- **🏷️ Event Filtering**: Filter by Sports, Chinese Festivals, Global Holidays, Concerts, Tech
- **🎯 42 Events**: Comprehensive 2026 event database
- **⚡ Zero Dependencies**: Pure HTML/CSS/JavaScript, no build step needed
- **🌐 Chinese Support**: Full Chinese language interface with Noto Sans SC font

## 📊 Event Categories

| Category | Count | Examples |
|----------|-------|----------|
| 🏆 Sports | 5 | FIFA World Cup, Wimbledon, Asian Games |
| 🎌 Chinese Festivals | 13 | Spring Festival, Qingming, Mid-Autumn |
| 🌍 Global Holidays | 13 | New Year, Christmas, Thanksgiving |
| 🎵 Concerts | 6 | Taylor Swift, Coldplay, Jay Chou |
| 💻 Tech Events | 5 | Apple Events, WWDC |

## 🚀 Quick Start

### Local Testing
```bash
# Simply open in browser
open index.html
```

### Deploy to GitHub Pages

1. Push to GitHub:
```bash
cd event-calendar
git push -u origin main
```

2. Enable GitHub Pages:
   - Go to repo Settings → Pages
   - Select "Deploy from a branch"
   - Choose "main" branch, root folder
   - Save

3. Access at: `https://boyzhoulei-del.github.io/event-calendar/`

## 📁 Files

- **index.html** - Complete single-file web app (22KB)
- **SPEC.md** - Full specification and design document
- **DEPLOYMENT.md** - Deployment instructions
- **README.md** - This file

## 🎨 Design System

### Colors
- Background: `#0a0a0f`
- Card: `#14141f`
- Accent: `#f5c518` (Gold)
- Sports: `#3b82f6` (Blue)
- Festival: `#ef4444` (Red)
- Concert: `#a855f7` (Purple)
- Tech: `#22c55e` (Green)

### Typography
- Font: Noto Sans SC (Chinese), system-ui fallback
- Responsive sizing for mobile and desktop

## 🔧 Technical Stack

- **HTML5** - Semantic markup
- **CSS3** - Grid layout, animations, responsive design
- **Vanilla JavaScript** - No frameworks, no dependencies
- **Google Fonts** - Noto Sans SC for Chinese characters

## 📱 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🎯 Usage

1. **Navigate Months**: Use ‹ › buttons to move between months
2. **View Events**: Click any date to see events for that day
3. **Filter Events**: Click filter tabs to show specific event types
4. **Event Details**: Each event shows type, title, date, location, and description

## 📝 Event Data Structure

```javascript
{
  id: 1,
  date: "2026-04-04",
  endDate: "2026-04-06",
  title: "清明节",
  type: "festival-china",
  location: "中国",
  description: "中华民族传统节日，祭祖踏青"
}
```

## 🌟 Highlights

- **Today Indicator**: Current date highlighted with gold border
- **Event Dots**: Color-coded dots show event types at a glance
- **Smooth Animations**: Cards slide in, hover effects on interaction
- **Responsive Layout**: Adapts from 375px mobile to desktop
- **No Build Required**: Works immediately, no npm/webpack needed

## 📄 License

Open source - feel free to use and modify!

---

**Created**: March 25, 2026
**Status**: Ready for deployment
