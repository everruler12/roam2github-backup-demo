- Twitter link
    - ```css
a[href*="twitter.com"] {
/*
content: url('data:image/svg+xml;charset=UTF-8, <svg id="Logo_FIXED" data-name="Logo — FIXED" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 300 300"><defs><style>.cls-1{fill:none;}.cls-2{fill:#1da1f2;}</style></defs><title>Twitter_Logo_Blue</title><rect class="cls-1" width="400" height="400"/><path class="cls-2" d="M153.62,301.59c94.34,0,145.94-78.16,145.94-145.94,0-2.22,0-4.43-.15-6.63A104.36,104.36,0,0,0,325,122.47a102.38,102.38,0,0,1-29.46,8.07,51.47,51.47,0,0,0,22.55-28.37,102.79,102.79,0,0,1-32.57,12.45,51.34,51.34,0,0,0-87.41,46.78A145.62,145.62,0,0,1,92.4,107.81a51.33,51.33,0,0,0,15.88,68.47A50.91,50.91,0,0,1,85,169.86c0,.21,0,.43,0,.65a51.31,51.31,0,0,0,41.15,50.28,51.21,51.21,0,0,1-23.16.88,51.35,51.35,0,0,0,47.92,35.62,102.92,102.92,0,0,1-63.7,22A104.41,104.41,0,0,1,75,278.55a145.21,145.21,0,0,0,78.62,23"/></svg>');
height: 15px;
width: 15px;
*/
content: url('https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Feriknewhard%2F8PGA5cXehh.svg?alt=media&token=d70ff642-9f4d-4115-bfc2-f1fc2b74e5e0');
height: 1em;
position: relative;
top: 2px;
}```
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Feriknewhard%2F8PGA5cXehh.svg?alt=media&token=d70ff642-9f4d-4115-bfc2-f1fc2b74e5e0)
- Variables
    - No CSS
        ```css
:root {
  --tag-actual-height: 17px;
  --tag-actual-padding-horizontal: 3px;
  --hashtag-width: 9px;
  --tag-icon-padding: 1px;
  
  --reference-bg-color: #F5F8FA;
  --embed-bg-color: #EBF1F5;
}```
    - CALCULATIONS
        ```css
:root {
  --spacing-after-icon: var(--tag-actual-padding-horizontal);
  
  /* icon size */
  --tag-icon-height: calc(var(--tag-actual-height) - (2 * var(--tag-icon-padding)));
  --tag-icon-width: var(--tag-icon-height);
  
  /* hashtag blocking */
  --hash-blocking-bg-width: calc(var(--tag-icon-width) + var(--spacing-after-icon));
  --tag-extra-padding-left: calc(var(--tag-actual-padding-horizontal) + var(--hash-blocking-bg-width) - var(--hashtag-width));
}```
- 
- #Tweeted, #Retweeted, #[[Tweet reply]], #[[Tweet draft]]
    ```css
span.rm-page-ref[data-tag="Tweeted"],
span.rm-page-ref[data-tag="Retweeted"],
span.rm-page-ref[data-tag="Tweet reply"],
span.rm-page-ref[data-tag="Tweet draft"] {
  color: rgb(29, 161, 242) !important;
  font-weight: 700;
  background-color: white !important;

  position: relative;
  padding-left: var(--tag-extra-padding-left);
  padding-right: var(--tag-actual-padding-horizontal);
}

span.rm-page-ref[data-tag="Tweeted"]:before,
span.rm-page-ref[data-tag="Retweeted"]:before,
span.rm-page-ref[data-tag="Tweet reply"]:before,
span.rm-page-ref[data-tag="Tweet draft"]:before {
  background: white;

  content: '';
  width: var(--hash-blocking-bg-width);
  height: var(--tag-icon-height);
  position: absolute;
  left: var(--tag-actual-padding-horizontal);
  top: var(--tag-icon-padding);
}

span.rm-page-ref[data-tag="Tweeted"]:after,
span.rm-page-ref[data-tag="Retweeted"]:after,
span.rm-page-ref[data-tag="Tweet reply"]:after,
span.rm-page-ref[data-tag="Tweet draft"]:after {
  background: url('https://twitter.com/favicon.ico') no-repeat;
  
  content: '';
  width: var(--tag-icon-width);
  height: var(--tag-icon-height);
  position: absolute;
  left: var(--tag-actual-padding-horizontal);
  top: 0;
  margin-top: var(--tag-icon-padding);
  background-size: var(--tag-icon-width) var(--tag-icon-height);
}

.rm-reference-item span.rm-page-ref[data-tag="Tweeted"],
.rm-reference-item span.rm-page-ref[data-tag="Retweeted"],
.rm-reference-item span.rm-page-ref[data-tag="Tweet reply"],
.rm-reference-item span.rm-page-ref[data-tag="Tweet draft"] {
  background-color: var(--reference-bg-color) !important;
}

.rm-reference-item span.rm-page-ref[data-tag="Tweeted"]::before,
.rm-reference-item span.rm-page-ref[data-tag="Retweeted"]::before,
.rm-reference-item span.rm-page-ref[data-tag="Tweet draft"]::before {
  background-color: var(--reference-bg-color) !important;
}

.rm-embed-container span.rm-page-ref[data-tag="Tweeted"],
.rm-embed-container span.rm-page-ref[data-tag="Retweeted"],
.rm-embed-container span.rm-page-ref[data-tag="Tweet draft"], {
  background-color: var(--embed-bg-color) !important;
}

.rm-embed-container span.rm-page-ref[data-tag="Tweeted"]::before,
.rm-embed-container span.rm-page-ref[data-tag="Retweeted"]::before,
.rm-embed-container span.rm-page-ref[data-tag="Tweet draft"]::before {
  background-color: var(--embed-bg-color) !important;
}```
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Feriknewhard%2F-jFVqR50MY.png?alt=media&token=07d32ead-3660-4df1-be5e-b3810fd259da)
- 
