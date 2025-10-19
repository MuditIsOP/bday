# 🎨 Customization Guide

This guide shows you exactly how to customize every part of your website.

## 🔧 Quick Customization Checklist

### Essential (Must Do Before Sharing):
- [ ] Change password
- [ ] Update her name
- [ ] Set correct dates (birthday, friendship start)
- [ ] Add at least 10 personal messages
- [ ] Upload at least 5 real photos

### Recommended:
- [ ] Add 20+ compliments
- [ ] Customize inside jokes
- [ ] Update music playlist
- [ ] Add voice note descriptions
- [ ] Personalize all section content

## 📍 Where to Find What

All customizable content is in `index.html` in the `<script>` section near the bottom of the file.

### Line Reference:
- **Lines 1031-1043**: CONFIG (password, name, dates)
- **Lines 1047-1129**: COMPLIMENTS (80 compliments)
- **Lines 1134-1197**: MESSAGES (categorized messages)
- **Lines 1202-1228**: MEMORIES (photo gallery)
- **Lines 1233-1254**: VOICE_NOTES (audio items)
- **Lines 1259-1280**: VIDEOS (video items)
- **Lines 1285-1317**: MUSIC (playlist)
- **Lines 1324-1357**: JOKES (inside jokes)

## 🔒 Step 1: Change Password (REQUIRED)

**Line ~1031**

```javascript
const CONFIG = {
    password: "iloveyou", // ← Change this to your secret password
```

**Examples:**
- Simple: `"ourfriendship"`
- Date-based: `"march152024"`
- Personal: `"coffeeaddict"`
- Secure: `"MyF!rst$pecialFriend2024"`

⚠️ **Important**: 
- Use quotes around the password
- Case-sensitive
- No spaces (or use underscores)
- Remember to share it with her!

## 👤 Step 2: Update Personal Info

**Lines ~1033-1042**

```javascript
user: {
    name: "Beautiful Friend", // ← Her name or nickname
    favoriteColor: "#E6E6FA" // Keep lavender or change
},
dates: {
    birthday: "2025-12-31", // ← Her birthday (YYYY-MM-DD)
    friendshipStart: "2024-01-01", // ← When you became friends
    specialEvent: "2025-06-15" // ← Any special event
}
```

**Date Format**: Always use `YYYY-MM-DD` format
- ✅ Correct: `"2024-03-15"`
- ❌ Wrong: `"03/15/2024"` or `"15-03-2024"`

## 💬 Step 3: Add Your Messages

**Lines ~1134-1197**

Messages are organized by category. Here's how to add more:

```javascript
smile: [
    {
        title: "Your Title Here",
        content: "Your message content goes here. Make it personal and heartfelt!",
        emoji: "😊"
    },
    // Add more messages here
],
```

### Message Categories:
- **smile**: When You Need A Smile
- **down**: When You're Feeling Down  
- **motivation**: When You Need Motivation
- **appreciation**: Random Appreciation

### Tips for Great Messages:
1. **Be specific**: Reference shared memories
2. **Be genuine**: Write from the heart
3. **Vary length**: Mix short and long messages
4. **Use emojis**: They add emotion and fun
5. **Different tones**: Funny, serious, supportive, loving

### Example Message:
```javascript
{
    title: "Remember That Day?",
    content: "Remember when we stayed up all night talking about our dreams? You inspired me so much that night. Your passion and determination are contagious! Keep chasing those dreams! 🌟",
    emoji: "💭"
}
```

## 🎨 Step 4: Customize Compliments

**Lines ~1047-1129**

The site comes with 80 compliments. You can:

### Option A: Add Your Own (Recommended)
```javascript
const COMPLIMENTS = [
    "Your laugh is the best sound in the world! 😄",
    "You have the most creative mind I know! 🎨",
    "Your kindness makes everyone's day better! 💝",
    // Add 77+ more...
];
```

### Option B: Edit Existing Ones
Find compliments you want to change and make them more personal:

**Generic:**
```javascript
"You're incredibly talented! 🌟"
```

**Personal:**
```javascript
"Your guitar playing always gives me chills! 🎸✨"
```

### Tips:
- Reference specific qualities
- Mention things you've noticed
- Be sincere and specific
- Use emojis (1-2 per compliment)
- Mix categories: personality, talents, looks, character

## 📸 Step 5: Add Your Photos

**Lines ~1202-1228**

### Replace Placeholder Images:

```javascript
const MEMORIES = [
    {
        src: "path/to/your/image.jpg", // ← Your image path
        caption: "That day at the beach!", // ← Your caption
        date: "2024-06-15" // ← When it happened
    },
    // Add more photos...
];
```

### Image Sources (Choose One):

#### Option 1: Upload to Same Folder
1. Put photos in same directory as index.html
2. Use: `src: "photo1.jpg"`

#### Option 2: Create Images Folder
1. Create folder: `images/`
2. Use: `src: "images/photo1.jpg"`

#### Option 3: Use Online Hosting
1. Upload to Imgur/Cloudinary
2. Get direct link
3. Use: `src: "https://i.imgur.com/abc123.jpg"`

### Caption Tips:
- Short and sweet (1-2 sentences)
- What happened in the photo
- Why it's special
- Inside reference if applicable

## 🎵 Step 6: Update Music Playlist

**Lines ~1285-1317**

```javascript
{
    title: "Our Song", // ← Song name
    artist: "Artist Name", // ← Artist
    description: "This song always reminds me of you", // ← Why you chose it
    emoji: "🎵", // ← Matching emoji
    category: "special" // ← Category
}
```

### Music Categories:
- `special`: Songs that mean something
- `upbeat`: Happy, energetic songs
- `chill`: Relaxing music
- `throwback`: Nostalgic songs
- `motivation`: Pump-up songs
- `night`: Late-night listening

### Add External Links:
To add actual music links, you'll need to edit the `openMusic` function and add:

```javascript
link: "https://open.spotify.com/track/..."
// or
link: "https://youtube.com/watch?v=..."
```

## 😂 Step 7: Add Inside Jokes

**Lines ~1324-1357**

```javascript
{
    title: "The Coffee Incident", // ← Short name
    description: "Remember when we accidentally ordered 10 coffees instead of 1? Still laughing about that chaos! ☕😂", // ← Full story
    emoji: "☕", // ← Representative emoji
    date: "2024-02-14" // ← When it happened
}
```

### Inside Joke Tips:
1. **Title**: Short, memorable name
2. **Description**: Full story with context
3. **Emoji**: Makes it visual
4. **Date**: When it originated
5. **Be detailed**: Enough info to relive the moment

## 🎤 Step 8: Customize Voice Notes

**Lines ~1233-1254**

```javascript
{
    title: "Morning Motivation", // ← Note title
    description: "A little boost to start your day right", // ← What it is
    emoji: "☀️", // ← Emoji
    category: "motivation" // ← Category
}
```

These are placeholders. To add real audio:
1. Record voice messages
2. Save as MP3
3. Upload somewhere (same folder or hosting)
4. Update the `openVoiceNote` function to include audio player

## 🎬 Step 9: Add Video Messages

**Lines ~1259-1280**

Same format as voice notes:

```javascript
{
    title: "A Special Message",
    description: "Something I wanted to tell you",
    emoji: "🎬",
    category: "message"
}
```

## 🎨 Step 10: Change Colors (Advanced)

**Lines ~23-34**

Want to change from lavender to another color?

```css
:root {
    --color-lavender-primary: #E6E6FA; /* ← Main color */
    --color-lavender-light: #F5F3FF; /* ← Lighter version */
    --color-lavender-medium: #DCD0FF; /* ← Medium */
    --color-lavender-accent: #B8A9D9; /* ← Accent */
    --color-lavender-dark: #8B7AB8; /* ← Dark */
    --color-text-primary: #6B5B95; /* ← Text color */
}
```

### Color Palette Ideas:

**Blue Theme:**
```css
--color-primary: #AED9E0; /* Sky blue */
--color-light: #E3F4F8;
--color-medium: #8BBFC9;
--color-accent: #5F9EA0;
--color-dark: #2F6B6D;
--color-text: #1A4D4F;
```

**Pink Theme:**
```css
--color-primary: #FFB6C1; /* Light pink */
--color-light: #FFE4E9;
--color-medium: #FF9FB3;
--color-accent: #FF7A9A;
--color-dark: #D66A7F;
--color-text: #8B4554;
```

**Green Theme:**
```css
--color-primary: #B8E6B8; /* Mint green */
--color-light: #E6F9E6;
--color-medium: #9FD99F;
--color-accent: #7ABC7A;
--color-dark: #4A8F4A;
--color-text: #2D5A2D;
```

## 📝 Content Writing Tips

### For Messages:
- ✍️ Write like you're talking to her
- 💭 Reference shared experiences
- 🎯 Be specific, not generic
- ❤️ Show, don't just tell
- 😊 Mix humor and sincerity

### For Compliments:
- 🎯 Focus on specific traits
- 📊 Cover different areas (personality, looks, talents)
- 💡 Mention things you've noticed
- 🌟 Make her feel unique
- 🎨 Be creative with wording

### For Captions:
- 📸 Set the scene
- 📅 When and where
- 💭 What you remember
- 😊 Why it matters
- 🎭 One sentence is enough

## ✅ Testing Your Changes

After customization:

1. **Open in Browser**: Test locally first
2. **Check Password**: Try wrong password, then right one
3. **Browse Sections**: Click through everything
4. **Test Messages**: Open envelopes, read content
5. **View Photos**: Make sure they load
6. **Check Dates**: Verify countdowns are correct
7. **Mobile Test**: Use phone or browser dev tools
8. **Read Everything**: Proofread all text

## 🐛 Common Mistakes

### Missing Quotes:
❌ `title: Your Title`
✅ `title: "Your Title"`

### Missing Commas:
❌ 
```javascript
{
    title: "Test"
    content: "Text"
}
```
✅ 
```javascript
{
    title: "Test",
    content: "Text"
}
```

### Wrong Date Format:
❌ `"03/15/2024"`
✅ `"2024-03-15"`

### Broken Quotes:
❌ `"She said "hi""`
✅ `"She said \"hi\""`
or `'She said "hi"'`

## 🚀 After Customization

1. Save `index.html`
2. Test locally (open in browser)
3. Fix any issues
4. Deploy to hosting
5. Test on live site
6. Share with her! 💜

---

**Questions?** Check README.md or DEPLOYMENT.md for more help!
