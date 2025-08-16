# Instaparse

## Description  
This lab is Part 2 of the Instaparse project. Users are able to sign up, log in, and upload photos to their feed from their photo library. Also new features have been added, including:  
- The ability to take photos with the camera  
- Viewing recent posts from other users  
- Filtering posts based on when they were uploaded

## Demo

  ![2024-09-25 02 39 08](https://github.com/user-attachments/assets/8c7b4b4b-92c0-4419-a2fd-0dbd009ac355)

All user authentication and data continue to be handled via the Parse backend hosted on Back4App.

## Key Features
- **Take Photos**: Users can take a photo using their device's camera and upload it to the server.
- **Conditional Photo Visibility**: Users must upload their own photo before they can see other users' posts in the feed.
- **Recent Post Filtering**: The app only shows the 10 most recent posts, and only posts from the last 24 hours are visible.
- **Blurred Posts**: Posts that are older than 24 hours (relative to the user’s last post) will appear blurred in the feed.
- **Track Last Post Date**: Each user’s last post date is saved, and this is used to filter which posts are visible in the feed.


**GIF of taking photos using phone camera**

![2024-09-25 03 03 02](https://github.com/user-attachments/assets/135d394f-4bd9-4929-9601-adbdb15e4a1e)





## Code Overview

### `PostViewController.swift`
- **Take Photos**: Allows users to take photos using the camera and upload them to the Parse server.
- **Upload Posts**: After taking a photo, users can post it to their feed.
- **Track Last Post**: Saves the date of the user's last post to help filter future posts.

### `FeedViewController.swift`
- **Filter Posts**: Only shows posts uploaded in the last 24 hours and limits the number of posts to 10.
- **Blur Old Posts**: Blurs posts that are older than 24 hours compared to the user's last post.
- **Display Posts**: Shows a feed of the latest posts from other users.
