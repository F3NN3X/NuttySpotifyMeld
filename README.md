# Nutty Spotify Widget for Meld Studio

A sleek, customizable Spotify widget for Meld Studio, ported from [@nuttylmao](https://nuttylmao.notion.site/Spotify-Widget-18e19969b237807ca88cfc9c4159da15)'s original widget by F3NN3X. Display your currently playing Spotify track with album art, song info, and a progress bar—perfect for streamers and creators.

## Features
- **Real-Time Playback**: Shows current song, artist, album art, and playback progress from Spotify.
- **Customizable**: Adjust fonts, colors, sizes, and blur via Meld Studio properties.
- **Toggle Album Art**: Option to show/hide album art, with song info stretching full width when off.
- **Persistent Settings**: Properties save across resizes using `localStorage`.
- **Reset Options**: Built-in Meld Studio resets (right-click "Reset to Default" or "Reset All Properties").

## Requirements
- **Meld Studio**: Compatible with Meld Studio’s upcoming widget feature.
- **Spotify URL**: Requires a URL with `client_id`, `client_secret`, and `refresh_token` from [@nuttylmao’s setup](https://nuttylmao.notion.site/Spotify-Widget-18e19969b237807ca88cfc9c4159da15).

## Installation Locally
1. **Download**: Grab `spotify.htm` from this repo’s releases or main branch.
2. **Host Locally** (optional): Serve via `python -m http.server 8000` and use `http://localhost:8000/spotify.htm`.
3. **Host Online** (recommended): Upload to GitHub Pages or another static host for a public URL.
4. **Add to Meld Studio**:
   - In Meld Studio, add one of the currently available widgets.
   - In the widget properties panel, click on the menu roght of Widget Info and select "Show Hidden Controls".
   - Set the URL to your hosted `spotify.htm` (e.g., `https://<your-username>.github.io/spotify-widget/spotify.htm`).

## Usage
1. **Get Spotify URL**:
   - Follow [@nuttylmao’s instructions](https://nuttylmao.notion.site/Spotify-Widget-18e19969b237807ca88cfc9c4159da15) to obtain your Spotify URL with `client_id`, `client_secret`,.
2. **Configure in Meld Studio**:
   - In the properties panel, paste your Spotify URL into the “Spotify URL” field and press Enter.
   - Customize fonts, colors, sizes, and toggle “Show Album Art” as desired.
3. **Reset Settings** (if needed):
   - You can reset individual changes by using the reset circle for the property.
   - You can reset the widget state by clicking the menu next to Widget Info and selecting "Reset Widget".
4. **Play Music**: Open Spotify, play a track—watch it sync live!

## Properties
| Property               | Type   | Default Value                         | Description                              |
|-----------------------|--------|---------------------------------------|------------------------------------------|
| `spotifyUrl`          | String | `""`                                  | Full Spotify widget URL                  |
| `trackFontColor`      | Color  | `#ffffff`                             | Song title font color                    |
| `artistFontColor`     | Color  | `#ffffff`                             | Artist name font color                   |
| `durationFontColor`   | Color  | `#ffffff`                             | Duration text color                      |
| `trackFontFamily`     | String | `"Proxima Nova", sans-serif`          | Song title font family                   |
| `artistFontFamily`    | String | `"Proxima Nova", sans-serif`          | Artist name font family                  |
| `durationFontFamily`  | String | `"Proxima Nova", sans-serif`          | Duration text font family                |
| `trackFontSize`       | Int    | `24`                                  | Song title font size (px)                |
| `artistFontSize`      | Int    | `16`                                  | Artist name font size (px)               |
| `durationFontSize`    | Int    | `20`                                  | Duration text size (px)                  |
| `backgroundColor`     | Color  | `rgba(0,0,0,0.5)`                    | Song info background color               |
| `refreshInterval`     | Int    | `1`                                   | Playback refresh interval (seconds)      |
| `progressBgColor`     | Color  | `#404040`                             | Progress bar background color            |
| `progressFillColor`   | Color  | `#1db954`                             | Progress bar fill color                  |
| `imageSize`           | Int    | `140`                                 | Album art size (px)                      |
| `progressBarHeight`   | Int    | `8`                                   | Progress bar height (px)                 |
| `blurAmount`          | Int    | `20`                                  | Background art blur amount (px)          |
| `showAlbumArt`        | Bool   | `true`                                | Toggle album art visibility              |

## Troubleshooting
- **No Playback**: Ensure your Spotify URL is correct and you’re playing music.
- **Properties Reset**: Use Meld Studio’s reset options if settings get funky.
- **Blank Widget**: Check WebSocket connection (`ws://127.0.0.1:13376`)—Meld Studio must be running.

## Credits
- **Original Widget**: [@nuttylmao](https://github.com/nuttylmao)
- **Ported By**: F3NN3X
- **License**: Same as original [@nuttylmao widget](https://github.com/nuttylmao/spotify-widget#license)
