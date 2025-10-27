# Physio Counter PWA

A Progressive Web App for tracking physiotherapy exercises with customizable sets, reps, and intervals. Works completely offline once installed!

## Features

- ✅ **Offline Support**: Works without internet connection
- ✅ **Installable**: Add to home screen on mobile and desktop
- ✅ **Customizable Exercises**: Configure sets, reps, intervals, and warm-up times
- ✅ **Audio Feedback**: TTS, beep, or both for counting
- ✅ **Set Completion Feedback**: Choose TTS, beep, or none
- ✅ **Pause/Resume**: Pause mid-set and resume exactly where you left off
- ✅ **History Tracking**: View exercise history by date
- ✅ **Data Export/Import**: Backup and restore your data as JSON
- ✅ **Voice Settings**: Customize TTS voice and speech rate

## Installation

### As a PWA (Recommended)

1. Visit the app in your browser
2. Look for the "Install" or "Add to Home Screen" prompt
3. Click Install/Add
4. The app will be available as a standalone app on your device

**On iOS Safari:**
- Tap the Share button
- Select "Add to Home Screen"
- Tap "Add"

**On Android Chrome:**
- Tap the menu (three dots)
- Select "Install app" or "Add to Home Screen"

**On Desktop Chrome/Edge:**
- Click the install icon in the address bar
- Or go to menu → "Install Physio Counter"

### Local Development

Simply open `index.html` in a web browser. For full PWA features, you'll need to serve it over HTTPS or localhost.

## Usage

1. **Create an Exercise**: Click "+ Add" to create a new exercise
2. **Configure**: Set the number of sets, reps, interval between reps, and warm-up time
3. **Start**: Click "Start" on any exercise
4. **Count**: The app will count your reps with audio feedback
5. **Next Set**: After completing a set, click "Next Set" to continue
6. **History**: View your exercise history in the History tab

## Settings

- **Voice Settings**: Choose TTS voice and speech rate
- **Test Voice**: Test the selected voice before saving
- **Test Beep**: Test all beep sounds (important for iOS - see below)
- **Warmup Countdown Feedback**:
  - TTS: Voice countdown ("Get ready", "5", "4", "3", "2", "1", "Go")
  - Beep: Beep countdown with lower tone (700Hz) and distinct "Go" beep (1400Hz)
- **Set Completion Feedback**: 
  - TTS: Says "set complete"
  - Beep: Plays a distinct beep sound (1200Hz)
  - None: No audio feedback
- **Export/Import**: Backup and restore your data

### Beep Tone Reference

The app uses different beep tones for different events:
- **Warmup countdown**: 700Hz (lower, mellower tone)
- **Warmup "Go"**: 1400Hz (high, energetic tone)
- **Exercise countdown**: 900Hz (standard tone)
- **Set complete**: 1200Hz (higher, completion tone)

### iOS Beep Support

On iOS devices, beep sounds require user interaction to initialize. To enable beeps on iOS:

1. Go to Settings tab
2. Click "Test Beep" button (this unlocks audio for iOS)
3. Now beeps will work during your exercises

Alternatively, beeps will automatically initialize when you start your first exercise.

## GitHub Pages Deployment

This app is ready to deploy to GitHub Pages!

### Steps to Deploy:

1. **Initialize Git Repository** (if not already done):
   ```bash
   cd /Users/kanantharamu/Desktop/counter
   git init
   git add .
   git commit -m "Initial commit: Physio Counter PWA"
   ```

2. **Create GitHub Repository**:
   - Go to [GitHub](https://github.com) and create a new repository
   - Name it something like `physio-counter` or `counter-app`
   - Don't initialize with README (we already have one)

3. **Push to GitHub**:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git branch -M main
   git push -u origin main
   ```

4. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click "Settings" tab
   - Scroll to "Pages" section (left sidebar)
   - Under "Source", select "main" branch
   - Click "Save"
   - Your app will be live at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

5. **Wait a few minutes** for GitHub to build and deploy your site

### Custom Domain (Optional)

You can also use a custom domain:
- Add a `CNAME` file with your domain
- Configure DNS settings with your domain provider
- Update GitHub Pages settings to use your custom domain

## File Structure

```
counter/
├── index.html          # Main app file
├── counter.html        # Backup of main file
├── manifest.json       # PWA manifest
├── sw.js              # Service worker for offline support
├── icons/             # App icons
│   ├── icon-192.png
│   ├── icon-512.png
│   └── icon.svg
├── backup/            # Backup folder
└── README.md          # This file
```

## Technical Details

- **Version**: 4.6.1
- **Storage**: LocalStorage (data persists in browser)
- **Offline**: Service Worker caches all assets
- **Audio**: Web Speech API for TTS, Web Audio API for beeps
- **Vibration**: Vibration API for haptic feedback (mobile)

## Browser Support

- Chrome/Edge (Desktop & Mobile) ✅
- Safari (Desktop & iOS) ✅
- Firefox (Desktop & Mobile) ✅
- Opera ✅

## Privacy

All data is stored locally in your browser. No data is sent to any server. Your exercise data never leaves your device.

## License

Free to use and modify for personal use.

## Contributing

Feel free to fork and improve! This is a single-file app for easy maintenance.

---

**Made with ❤️ for physiotherapy enthusiasts**

