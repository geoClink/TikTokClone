# TikTokClone

A SwiftUI practice project that recreates the core layout of a TikTok-style app. This app was built by following a tutorial and currently focuses on UI composition, tab navigation, and vertically paged video playback.

Tutorial source: https://www.youtube.com/watch?v=CnZKM9tFg7I

## Overview

The app launches into a tab-based interface with these sections:

- Home feed with full-screen vertical video scrolling
- Explore screen with a simple user list
- Placeholder upload tab
- Notifications screen
- Profile screen with stats and a post grid

The feed uses `AVPlayer` and a custom `UIViewControllerRepresentable` wrapper around `AVPlayerViewController` to play remote sample videos.

## Features Implemented

- `TabView`-based main navigation
- Full-screen vertically paged feed
- Auto-playing video as the visible post changes
- Custom video player wrapper for SwiftUI
- Explore, notifications, and profile UI screens
- Reusable profile stat and grid components

## Project Structure

```text
TikTokClone/
├── TikTokClone/App
├── TikTokClone/Core(MainFlow)
│   ├── Comments
│   ├── Feed
│   ├── Notifications
│   ├── Profile
│   ├── Root(where app opens up)
│   ├── Search
│   └── TabBar
├── TikTokClone/Model
└── TikTokClone/Assets.xcassets
```

## Notes

- This is a tutorial-based project, so several screens currently use static placeholder data.
- The upload tab is not implemented yet.
- Feed post metadata and social actions are present in the UI, but are not backed by a real backend.
- Video content is loaded from public sample MP4 URLs.

## Main Files

- `TikTokClone/TikTokClone/App/TikTokCloneApp.swift`: app entry point
- `TikTokClone/TikTokClone/Core(MainFlow)/TabBar/MainTabView.swift`: root tab navigation
- `TikTokClone/TikTokClone/Core(MainFlow)/Feed/View/FeedView.swift`: vertically paged feed
- `TikTokClone/TikTokClone/Core(MainFlow)/Feed/View/FeedCell.swift`: full-screen video cell UI
- `TikTokClone/TikTokClone/Core(MainFlow)/Comments/CustomVideoPlayer.swift`: SwiftUI wrapper for `AVPlayerViewController`
- `TikTokClone/TikTokClone/Core(MainFlow)/Profile/CurrentUserProfileView.swift`: profile screen

## Running the Project

1. Open the project in Xcode.
2. Select an iOS Simulator or device.
3. Build and run the `TikTokClone` scheme.

## Purpose

This project is mainly useful as a SwiftUI learning exercise for:

- tab-based app structure
- view composition
- basic AVKit integration
- scroll-driven media playback
- building reusable UI components
