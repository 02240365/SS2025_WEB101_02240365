# Practical 1 : Tiktok

## Overview
In this practical work, I built a TikTok-like frontend using Next.js, Tailwind CSS, and React. The project includes a responsive layout, a video feed, user profiles, and pages for uploading videos, exploring content, and viewing live streams. The goal was to replicate the core features of TikTok's web interface while learning modern frontend development practices.

---

## Objectives
1. **Set Up a Next.js Project**: Initialize a new Next.js project with Tailwind CSS for styling.
2. **Create a Responsive Layout**: Build a sidebar and main content area similar to TikTok's web interface.
3. **Implement a Video Feed**: Create a scrollable video feed with interactive components like likes, comments, and shares.
4. **Develop Additional Pages**: Build pages for user profiles, video uploads, exploring content, and live streams.
5. **Test the Application**: Ensure the application works as expected across different pages and components.

---

## Steps Taken

### 1. Project Setup
I started by setting up a new Next.js project with the following steps:
- Initialized the project using `npx create-next-app@latest`.
- Configured the project to use Tailwind CSS for styling.
- Organized the project structure with folders for components, layouts, and pages.

### 2. Creating the Layout
I designed a responsive layout with a sidebar and main content area:
- Created a `MainLayout` component that includes a sidebar with navigation links and a header with a search bar.
- Used Tailwind CSS to style the layout and ensure it was responsive across different screen sizes.

### 3. Building the Video Feed
I implemented a video feed similar to TikTok's:
- Created a `VideoCard` component to display individual videos with interactive buttons for likes, comments, and shares.
- Used dummy data to simulate a video feed and displayed it on the home page.

### 4. Developing Additional Pages
I created several pages to replicate TikTok's functionality:
- **Profile Page**: Displays user information, followers, and following counts.
- **Upload Page**: Allows users to upload videos with a drag-and-drop interface.
- **Explore Page**: Shows trending hashtags and popular videos.
- **Live Page**: Displays live streams with viewer counts.

### 5. Testing the Application
I tested the application by navigating through all the pages and ensuring the layout and components worked as expected. I also verified that the interactive elements (like buttons, comments, etc.) functioned correctly.



