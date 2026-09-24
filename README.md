# Media-Streamer-And-Downloader---Youtube
1. Introduction & Product Philosophy
Vitorius: YouBeTu is a cyber-themed Android application designed for high-performance video streaming and offline media collection. Created with a futuristic cyberpunk aesthetic, the app addresses a growing frustration among mobile video viewers: excessive advertising, cluttered web interfaces, algorithmic distractions, and restrictive offline playback options.
The core philosophy of Vitorius: YouBeTu is simple: To deliver a pure, distraction-free video viewing experience.
Whether you are streaming videos online or playing video files saved directly on your mobile device, the app strips away platform clutter. It blocks video ads, removes pop-up banners, hides comment sections, eliminates like buttons, and removes algorithmic recommendation feeds. What remains is a clean, dark-mode media canvas focused entirely on high-definition video playback and essential media controls.
2. The 3-Window Navigation Matrix
Vitorius: YouBeTu organizes all user activities into three distinct primary windows accessible via a high-contrast bottom navigation bar.
+-----------------------------------------------------------------------------------+
|                               VITORIUS: YOUBETU                                   |
+-----------------------------------------------------------------------------------+
|                                                                                   |
|   +-----------------------+   +-----------------------+   +-------------------+   |
|   |    [1] STREAM         |   |   [2] SAVED STREAMS   |   | [3] LOCAL VIDEOS  |   |
|   +-----------------------+   +-----------------------+   +-------------------+   |
|   | • Global Search       |   | • Bookmarked Matrix   |   | • Storage Vault   |   |
|   | • Stream Player       |   | • 1-Tap Quick Launch  |   | • Custom Folders  |   |
|   | • Inline Search       |   | • SQLite Storage      |   | • Media3 ExoPlayer|   |
|   | • Watch History       |   | • Stream Removal      |   | • Progress Bars   |   |
|   +-----------------------+   +-----------------------+   +-------------------+   |
|                                                                                   |
+-----------------------------------------------------------------------------------+
Window 1: Stream (Search & Video Player)
The Stream Window is the main hub for finding and watching online video streams:
•
Global Search: Users can type any query into the search bar to find online videos with high-resolution thumbnails and titles.
•
Previously Viewed Streams: When no search query is typed, the screen displays a timestamped history of recently watched streams, allowing users to jump back into content they previously enjoyed.
•
The Stream Player: Tapping any search result launches the main video player. It provides essential video controls, video title information, and action buttons.
•
Inline Quick Search: While watching an active stream, users can type into a quick search field directly below the video. A pop-up results overlay appears, allowing the user to select and switch to a new video stream without leaving the player screen.
Window 2: Saved Streams (Bookmark Matrix)
The Saved Streams Window acts as a personal online video library:
•
One-Tap Bookmarking: While watching any online stream, pressing the Save Data button bookmarks the video.
•
Permanent Bookmark List: Bookmarked streams are stored in a local database and presented in a clean list format.
•
Quick Playback & Management: Users can tap Play Stream on any bookmarked video to start watching it immediately, or tap Remove to delete it from their saved streams list.
Window 3: Local Videos (Storage Vault & Settings)
The Local Videos Window manages video files saved directly to the device's physical memory:
•
Physical Device Storage: Downloads video files directly to the phone's public memory under a dedicated folder called Movies/Vitorius Media/.
•
Real-Time Progress Tracking: When a download is initiated, the app displays a progress card with a percentage bar showing live download progress.
•
Offline File Scanner: Scans the phone's media directories for saved video files and displays them in a structured list with file sizes and Play Offline File buttons.
•
Storage & Playback Settings: Includes a settings menu where users can change the target storage folder name or switch playlist playback modes between Playlist Until End, Shuffle Playlist, and Stop at End.
3. Dual-Engine Video Playback System
To provide smooth video playback under all conditions, Vitorius: YouBeTu utilizes two separate video playback engines depending on whether content is online or offline.
                             [ SELECT MEDIA ]
                                    |
                                    v
                   /----------------------------------\
                  / Is the file on local phone storage?\
                 +--------------------------------------+
                               /          \
                       (Yes)  /            \  (No)
                             /              \
                            v                v
            +-------------------+        +-------------------+
            |  EXOPLAYER ENGINE  |        |  WEB STREAM ENGINE|
            | (Offline MP4 File) |        |  (Online Video)   |
            +-------------------+        +-------------------+
            | • Hardware MP4    |        | • Blocks Ads      |
            | • Seeker & Loop   |        | • Hides Clutter   |
            | • Zero Lag        |        | • Pure Video View |
            +-------------------+        +-------------------+
Engine 1: The Online Web Streaming Engine
When watching online streams, the app loads the video through a modified web engine that automatically strips out website clutter. It removes video ads, header bars, comments, channel descriptions, like buttons, and subscriber counters. The result is a clean video view that retains essential player controls like play, pause, progress scrubbing, and play time.
Engine 2: The Offline Native Media3 ExoPlayer Engine
When playing local video files saved on the phone's storage, the app switches to a native AndroidX Media3 ExoPlayer engine. This engine uses the device's hardware decoders to play local video files smoothly with zero lag, built-in seeker bars, time controls, automatic looping, and offline error protection.
4. Viewing Experience & Cyberpunk Design System
Immersive Horizontal Theater Mode
For full-screen viewing, users can tap the Horizontal button on any video screen:
•
Landscape Orientation: Automatically rotates the phone to horizontal landscape view and hides top status and bottom navigation bars.
•
Full Screen Edge-to-Edge: Expands the video to occupy 100% of the display.
•
Permanent Exit Overlay: A neon Exit Horizontal View button stays pinned in the top-right corner, allowing users to return to portrait view at any time with a single tap.
Cyberpunk Visual Theme
Vitorius: YouBeTu features an OLED-friendly dark cyberpunk theme:
•
Color Palette: Deep space black background accented with Neon Cyan (headers and active borders), Cyber Purple (labels and containers), Hacker Green (download completion and offline indicators), and Neon Magenta (alerts and action highlights).
•
Cut-Corner Geometry: Buttons, video cards, text fields, and pop-up dialogs feature sharp, futuristic angled corners.
•
Monospace Typography: All text labels and statuses use monospace typography for a technical, terminal-like appearance.
5. Privacy, Reliability & Performance
•
Privacy & Security: The app operates locally on your device without requiring user registration, personal account logins, or tracking permissions.
•
Persistent Database Storage: All saved stream bookmarks, download records, and watch histories are stored in a local SQLite database that persists across app restarts and device reboots.
•
Optimized Performance: Built with code shrinking and resource optimization to ensure a small app size, fast startup times, and minimal battery usage.
6. Summary
Vitorius: YouBeTu combines the breadth of online video streaming with the reliability of a local offline media library. By eliminating online clutter and offering structured storage, quick inline searching, and a dual-engine video player, it provides a fast, privacy-focused, and visually striking video experience for Android users.
