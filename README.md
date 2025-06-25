# Offline_Course_Tracker
Tracking your downloaded courses Offline like Udemy,Coursera.

![Screenshot 2025-06-25 225534](https://github.com/user-attachments/assets/e7d18780-86f1-466d-aa2b-fc7053f66b3a)

A self-contained, single-page web application designed to help you track your progress through any local video course. This tool remembers where you left off, tracks which videos you've completed, and provides a smooth, modern interface for your learning journey.

## ✨ Features

This project is packed with features to make tracking your course seamless:

* **Persistent Session Memory:**
    * **Resume Playback:** Automatically loads the last video you were watching when you reopen the page.
    * **Saves Video Position:** Remembers the exact timestamp you stopped at for every video.
    * **Saves Scroll Position:** Remembers how far you were scrolled in the video list.
* **Progress Tracking:**
    * **Dynamic Progress Bar:** A prominent bar at the top shows your percentage of course completion.
    * **"Watched" Checkboxes:** Manually mark videos as complete. This state is saved automatically.
    * **Autoplay Next:** When a video finishes, it is marked as complete and the next video in the sequence automatically begins.
* **Modern User Interface:**
    * **Sleek Design:** A modern, responsive layout that looks great on desktop and mobile.
    * **Dark & Light Modes:** A theme toggle to switch between a dark interface and a light one.
    * **Resume Indicator:** A clear "Resume" badge appears on the last video you played, so you never lose your place.
* **User Experience:**
    * **Live Search:** Instantly filter the video list by typing in the search bar.
    * **Replay From Start:** Completed videos can be replayed from the beginning at any time.
    * **Smooth & Performant:** Optimized to be fast and responsive.

---

## 🚀 Setup & Customization

Because this application uses browser features to save your progress, you must run it through a simple local web server. The easiest way is with the **Live Server** extension in Visual Studio Code.

### Step 1: Add Your Video Files

1.  Place the `index.html` file in a new folder.
2.  Place all of your course's `.mp4` video files into the **same folder**.

### Step 2: Edit the Playlist in `index.html`

1.  Open the `index.html` file in a code editor like VS Code.
2.  Scroll down to the `<script>` section at the bottom.
3.  Find the `filenames` list and replace the examples with the **exact filenames** of your videos. Make sure they are in the correct order.
   Note:- Here i have put an Array.

    ```javascript
    // ...const filenames = Array.from({ length: 40 }, (_, i) => `5_62555417454638560${70 + i}.mp4`);
    ```

### Step 3: Run the Project

1.  In VS Code, with your project folder open, install the **"Live Server"** extension from the Extensions marketplace.
2.  Open the `.html` file.
3.  Click the **"Go Live"** button in the bottom-right corner of the window.

Your browser will open with the correct address, and the tracker will now be perfectly configured for your course!

---

## 🛠️ Technologies Used

* **HTML5:** For the core structure of the page.
* **CSS3:** For all styling, including Flexbox for layout, CSS Variables for theming, and keyframe animations for effects.
* **Vanilla JavaScript (ES6+):** For all application logic, including DOM manipulation, event handling, and saving state to `localStorage`.
