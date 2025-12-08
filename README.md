# ♟️ Chess Playback Viewer

A beautiful, interactive chess game playback viewer with sharing capabilities. Load any chess game in JSON format, share it with others, and watch games with auto-play controls.

## 🚀 Features

### Core Functionality
- ✅ **Auto-Play Mode** with adjustable speed (0.33x to 4x)
- ✅ **Manual Navigation** (Previous/Next, Start/End)
- ✅ **Visual Move Highlighting** - Last moved squares highlighted in yellow
- ✅ **Interactive Move List** - Click any move to jump to that position
- ✅ **Progress Bar** with move counter

### Game Loading Options
1. **Upload JSON File** - Load games from `.json` files
2. **Paste JSON** - Directly paste JSON game data
3. **Sample Game** - Pre-loaded example game
4. **URL Loading** - Games can be loaded from shareable links

### Sharing Features
- 🔗 **Generate Shareable Links** - Share games with anyone
- 📋 **One-Click Copy** - Copy link to clipboard
- 🌐 **URL-based Loading** - Recipients can view the game instantly

## 📦 Installation & Deployment

### Option 1: Simple File Hosting
1. Download `chess-playback-standalone.html`
2. Upload to any web hosting service:
   - **GitHub Pages** (Free)
   - **Netlify** (Free)
   - **Vercel** (Free)
   - **Firebase Hosting** (Free)
   - Any web server

### Option 2: GitHub Pages (Recommended)
```bash
# 1. Create a new GitHub repository
# 2. Upload chess-playback-standalone.html (rename to index.html)
# 3. Go to Settings → Pages
# 4. Select main branch → Save
# Your app will be live at: https://yourusername.github.io/your-repo-name
```

### Option 3: Netlify Drag & Drop
1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag & drop the HTML file
3. Get instant live URL!

### Option 4: Run Locally
Simply open `chess-playback-standalone.html` in any modern browser.

## 📝 JSON Format

Your chess game must follow this JSON structure:

```json
{
  "game": [
    {
      "move": 1,
      "white": "e2-e4",
      "black": "e7-e5"
    },
    {
      "move": 2,
      "white": "Ng1-f3",
      "black": "Nb8-c6"
    }
  ]
}
```

### Move Notation Rules
- **Regular moves**: `from-to` (e.g., `e2-e4`, `Ng1-f3`)
- **Captures**: `fromxto` (e.g., `e5xd4`, `Qd1xd4`)
- **Castling**: `O-O` (kingside) or `O-O-O` (queenside)
- **Check/Checkmate**: Add `+` or `#` (e.g., `Nb4xd3+`, `Rh2-h1#`)

### Piece Notation
- **K** = King
- **Q** = Queen
- **R** = Rook
- **B** = Bishop
- **N** = Knight
- **Pawns** = just use squares (e.g., `e2-e4`)

## 🎮 How to Use

### Loading a Game
1. **Upload JSON File**: Click "Upload JSON" tab → Select file → Click "Load Game from File"
2. **Paste JSON**: Click "Paste JSON" tab → Paste your JSON → Click "Load Game from JSON"
3. **Load Sample**: Click "Load Sample" tab → Click button to see demo

### Playback Controls
- **▶️ Play**: Auto-play through moves
- **⏸️ Pause**: Stop auto-play
- **◀️ Previous**: Go back one move
- **▶️ Next**: Advance one move
- **⏮️ Start**: Jump to starting position
- **⏭️ End**: Jump to final position

### Speed Control
- **−** button: Decrease speed (slower playback)
- **+** button: Increase speed (faster playback)
- Speed range: 0.33x to 4x

### Sharing a Game
1. Load your game using any method
2. Scroll to "Share This Game" section
3. Click "Generate Share Link"
4. Click "📋 Copy Link" to copy to clipboard
5. Share the link with anyone!

## 🔗 Share Link Example

When you generate a share link, it looks like this:
```
https://yoursite.com/chess-playback.html?game=eyJnYW1lIjpbeyJtb3ZlIjoxLCJ3a...
```

The game data is encoded in the URL, so anyone with the link can view your game immediately!

## 🎨 Customization

### Change Colors
Edit the CSS in the `<style>` section:

```css
/* Board colors */
.square.light { background-color: #f0d9b5; }
.square.dark { background-color: #b58863; }
.square.highlight { background-color: #ffd93d; }

/* Gradient theme */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Adjust Board Size
Change the square dimensions:

```css
.square {
    width: 60px;   /* Change to desired size */
    height: 60px;  /* Keep equal to width */
    font-size: 40px; /* Adjust piece size */
}
```

## 🛠️ Converting Your Chess Games

### From PGN Format
If you have games in PGN format, you'll need to convert them to JSON. Here's a simple structure:

**PGN:**
```
1. e4 e5
2. Nf3 Nc6
```

**JSON:**
```json
{
  "game": [
    { "move": 1, "white": "e2-e4", "black": "e7-e5" },
    { "move": 2, "white": "Ng1-f3", "black": "Nb8-c6" }
  ]
}
```

### Using OCR for Physical Scoresheets
If you have physical chess scoresheets, you can:
1. Take a photo/scan
2. Use Tesseract.js or similar OCR tools
3. Convert the extracted text to JSON format

## 📱 Mobile Friendly

The viewer is fully responsive and works great on:
- 📱 Smartphones
- 📱 Tablets
- 💻 Desktop browsers

## 🌐 Browser Support

Works in all modern browsers:
- ✅ Chrome
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## 🎯 Use Cases

- **Study Games**: Analyze your own or master games
- **Teaching**: Share instructive games with students
- **Chess Clubs**: Archive and share club games
- **Tournaments**: Share tournament games with participants
- **YouTube Content**: Embed in websites for chess content
- **Personal Archive**: Keep a collection of memorable games

## 🚀 Advanced: Embedding in Your Site

```html
<iframe 
  src="https://yoursite.com/chess-playback.html?game=ENCODED_GAME_DATA" 
  width="100%" 
  height="900px" 
  frameborder="0">
</iframe>
```

## 📄 License

Free to use, modify, and distribute. Attribution appreciated but not required.

## 🤝 Contributing

Feel free to:
- Report bugs
- Suggest features
- Submit improvements
- Share your customizations

## 💡 Tips

1. **Save Your Games**: Keep a folder of JSON files for quick loading
2. **Bookmark Share Links**: Save interesting games as bookmarks
3. **Speed Presets**: Use 0.5x for studying, 2x for quick review
4. **Mobile View**: Works great for analyzing on the go

## 🎓 Example Games to Try

Create JSON files with famous games:
- **Immortal Game** (Anderssen vs Kieseritzky, 1851)
- **Opera Game** (Morphy vs Duke Karl, 1858)
- **Game of the Century** (Fischer vs Byrne, 1956)

## ❓ FAQ

**Q: Can I load games from URLs?**
A: Yes! The app checks the URL for a `game` parameter on load.

**Q: Is the game data stored anywhere?**
A: No, everything is client-side. Your games stay private.

**Q: Can I edit moves?**
A: Currently view-only, but you can edit the JSON and reload.

**Q: Does it support variations/branches?**
A: Not yet - only main line games are supported.

**Q: Can I add annotations/comments?**
A: Not in the current version, but you could extend the JSON format.

---

**Made with ♟️ for chess enthusiasts everywhere!**
