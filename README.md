# Spotify Clone

A front-end clone of the Spotify web player, built with pure HTML and CSS. It recreates Spotify's signature dark UI — sidebar navigation, library shortcuts, scrollable content cards, and a fixed bottom music player.

## 🚀 Features

- **Sidebar navigation** — Home, Search, and Your Library links with icon states
- **Library panel** — prompts to create a playlist or browse podcasts
- **Sticky content nav** — back/forward navigation, "Install App" and "Explore Premium" badges, responsive hide-on-scroll for smaller screens
- **Content rows** — "Recently Played," "Trending Now Near You," and "Featured Charts" sections with card-based layout
- **Fixed bottom music player** — album art, track info, playback controls, progress bar, and volume slider
- **Responsive touches** — certain nav items hide automatically below 1000px width

## 🛠️ Built With

- **HTML5**
- **CSS3** (Flexbox-based layout, custom scrollbars via `overflow`, CSS-only range slider styling)
- [Font Awesome 7.3.1](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.3.1/css/all.min.css) — icons
- [Google Fonts — Montserrat & Poppins](https://fonts.google.com/) — typography

## 📁 Project Structure

```
spotify-clone/
├── index.html
├── style.css
├── logo.png
├── library_icon.png
├── backward_icon.png
├── forward_icon.png
├── player_icon1.png ... player_icon5.png
├── card1img.jpeg ... card6img.jpeg
├── arvind-pillai-Yl4Y7COttGo-unsplash.jpg
└── README.md
```

> Note: all images referenced in `index.html` (logo, icons, card thumbnails, album art) need to be added to the project root for the layout to render correctly.

## ⚙️ Layout Overview

- `.main` is a flex container splitting the page into `.sidebar` and `.main_content`.
- `.sidebar` holds the top nav (Home/Search) and the library section with "create playlist" / "browse podcasts" prompts.
- `.main_content` is scrollable (`overflow: auto`) and contains a `.sticky-nav` that stays pinned to the top while browsing, followed by rows of `.cards-container` → `.card` elements for each music/podcast section.
- `.music-player` is fixed to the bottom of the viewport and split into three sections: `.album` (art + track info), `.player` (playback controls + progress bar), and `.controls` (queue, devices, volume).

## ▶️ Getting Started

1. Clone or download this project.
2. Add the required image assets (see Project Structure above) to the root folder.
3. Open `index.html` in any modern browser — no build tools or server needed.

```bash
git clone <your-repo-url>
cd spotify-clone
open index.html   # or just double-click the file
```

## 🔧 Customization

| What to change         | Where                                         |
|--------------------------|--------------------------------------------------|
| Sidebar width            | `.sidebar { width: 340px; }`                   |
| Card size                | `.card { width: 150px; }`                      |
| Track/album info         | `.album` block in `index.html`                 |
| Playback/volume defaults | `value` attributes on `.progress-bar` / `.volume-bar` inputs |
| Theme colors             | `background-color`/`color` values throughout `style.css` (currently black / `#121212` / `#232323`) |

## 🐞 Known Issues / To-Do

- Player and volume controls are visual only — no JavaScript wired up yet for play/pause, seeking, skipping tracks, or volume changes.
- Repeated card content ("Top 50 - Global" and the same description) across sections — data isn't dynamic yet.
- Minor typo in card descriptions: "most palyed" → "most played" (repeated in several cards).
- `body { overflow: hidden; }` combined with `.main_content { overflow: auto; }` means only the content column scrolls — double check this is the intended behavior on smaller screens.
- No mobile layout below the sidebar/player breakpoint — the fixed-width `.sidebar` (340px) isn't collapsed on small screens.

## 📄 License

This project is a clone built for learning/practice purposes and is not affiliated with or endorsed by Spotify.

## 🙌 Credits

Icons by [Font Awesome](https://fontawesome.com/). Fonts by [Google Fonts](https://fonts.google.com/). UI design inspired by [Spotify](https://open.spotify.com/).
