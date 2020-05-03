# Hide Watched YouTube Videos Bookmark
Hide the videos you have watched from your YouTube subscription feed. Procrastinate more efficiently.

### To Use:

1) Create a bookmark with this script in it: 

```
javascript: {var thumbs = document.getElementsByTagName("ytd-grid-video-renderer");var hidden = 0;for (i = 0; i < thumbs.length; i++){var watchedStr = thumbs[i].querySelector('yt-formatted-string.ytd-thumbnail-overlay-playback-status-renderer');var progressBar = thumbs[i].querySelector('ytd-thumbnail-overlay-resume-playback-renderer #progress');if((progressBar != null && parseInt(progressBar.style.width) > 60) || (watchedStr != null && watchedStr.innerText === "WATCHED")){hidden++;thumbs[i].setAttribute("style", "display:none;");}}console.log("Hidden " + hidden + " videos.");}
```

2) Press the bookmark to run the script.

**Note:** If you keep scrolling you will have to press it again.
