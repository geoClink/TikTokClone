# TikTokClone (SwiftUI)

A lightweight TikTok-like SwiftUI demo app built as an Xcode project for learning and prototyping. This repository demonstrates a simple social video feed with user profiles, search/explore, notifications, and a tab bar — organized around SwiftUI + MVVM folder structure.

---

## Table of Contents

- Project Overview
- Key Features
- Architecture & Project Structure
- Getting Started (Requirements & Run)
- File Map (important files & folders)
- Assets
- Tests
- Contributing
- License
- Troubleshooting & FAQ

---

## Project Overview

TikTokClone is a SwiftUI-based demo app that mimics core UI flows found in short-video social apps. It's designed for learning and experimentation with SwiftUI, MVVM, and modular app structure.

Primary entry points:

- `App/TikTokCloneApp.swift` — App entry point (SwiftUI App).
- `Core(MainFlow)/Root(where app opens up)/ContentView.swift` — Root content view that composes the main flow and tabs.

---

## Key Features

- Video feed (Feed) with custom player components.
- User profiles with a post grid and header components.
- Search/Explore UI.
- Notifications list.
- Tab bar navigation.

Mapped folders:

- `Core(MainFlow)/Feed/` — Feed views, view models, and service layers.
- `Core(MainFlow)/Profile/` — Profile views and components.
- `Core(MainFlow)/Search/` — Explore view and user search cell.
- `Core(MainFlow)/Notifications/` — Notification views.
- `Model/Post.swift` — Primary data model for posts.

---

## Architecture & Project Structure

This project uses SwiftUI and follows an MVVM-inspired structure. The high-level responsibilities:

- Views: SwiftUI views that present UI and bind to view models (`View` folders under each feature).
- ViewModels: Provide data and user interaction logic (e.g., `FeedViewModel.swift`).
- Services: Networking or data-loading code (folder: `Service`).
- Models: Plain data structs representing domain objects (`Model/Post.swift`).
- Components (reusableViews): Small, shareable UI components.

Notes:
- The codebase avoids external dependencies by default; if you add packages, document them in this README.

---

## Getting Started

Requirements

- macOS with Xcode 14 or later (Xcode 15 recommended for the latest Swift and SwiftUI features).
- iOS 16.0+ (assumed). If you need a lower deployment target, open the project in Xcode and adjust the "iOS Deployment Target" in project settings.

Run the app

1. Open the project in Xcode:

   - Prefer: `TikTokClone.xcworkspace` if present.
   - Otherwise: `TikTokClone.xcodeproj`.

2. Select a simulator (iPhone 14 or similar) or a physical device.
3. Build and Run (⌘R).

---

## File Map (important files)

- `App/TikTokCloneApp.swift` — Application entry point.
- `Core(MainFlow)/Root(where app opens up)/ContentView.swift` — Root composition and tab bar wiring.
- `Core(MainFlow)/Feed/View/FeedView.swift` — The feed screen.
- `Core(MainFlow)/Feed/ViewModel/FeedViewModel.swift` — Feed view model & sample data loading.
- `Core(MainFlow)/Feed/View/FeedCell.swift` — The feed cell UI.
- `Core(MainFlow)/Profile/Components/ProfileHeaderView.swift` — Profile header UI.
- `Model/Post.swift` — Post model used across the app.

---

## Assets

Images and app icons live in `TikTokClone/Assets.xcassets/`.
Notable assets:

- `profilePic.imageset` — sample user avatar(s).
- `secondProfilePic.imageset` — another sample avatar.

Add or replace assets using the Assets catalog in Xcode.

---

## Tests

This repository does not include automated unit/UI tests yet. Recommended additions:

- Unit tests for `FeedViewModel` and any services (e.g., data parsing, network response handling).
- Snapshot tests for important SwiftUI views using a library like `iOSSnapshotTestCase` or `SnapshotTesting`.

To add tests: File > New > Target > Unit Testing Bundle in Xcode, then write tests under the new test target.

---

## Contributing

Contributions are welcome. Suggested workflow:

1. Fork the repo.
2. Create a feature branch: `git checkout -b feat/my-feature`.
3. Commit changes: `git commit -m "feat: add ..."`.
4. Push and open a pull request.

Guidelines:
- Keep UI and logic modular.
- Add tests for new features where possible.

---

## License

This project is unlicensed by default. If you'd like, change this to an OSI-approved license such as MIT.

Suggested MIT header:

```
MIT License

Copyright (c) YEAR Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

... (standard MIT text)
```

---

## Troubleshooting & FAQ

Q: The app fails to build with deployment target errors.
A: Open the project in Xcode. Select the project file in the Project navigator, choose the target, and set "iOS Deployment Target" to an appropriate OS version.

Q: Where are the sample videos used in the feed?
A: This demo uses placeholder components. Add video files to the asset catalog or include local media files in a bundle and update any playback paths.

Q: How do I add a Swift Package?
A: File > Add Packages... in Xcode, then search by Git URL or package name.

---

If you'd like, I can:
- Set the README license to MIT and add the full text.
- Add a quick screenshot to `Assets` and embed it in the README.
- Create a basic Unit Test target and add one sample test for `FeedViewModel`.

If you want any of those, tell me which and I'll add them.
