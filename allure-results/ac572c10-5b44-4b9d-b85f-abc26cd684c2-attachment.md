# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: FrameHandling.spec.js >> SingleFrame
- Location: tests\FrameHandling.spec.js:7:5

# Error details

```
Test timeout of 30000ms exceeded.
```

```
Error: locator.fill: Test timeout of 30000ms exceeded.
Call log:
  - waiting for locator('//iframe[@id=\'singleframe\']').contentFrame().locator('//input[@type=\'text\']')

```

# Page snapshot

```yaml
- generic [active] [ref=f2e1]:
  - banner [ref=f2e2]:
    - generic [ref=f2e5]:
      - link [ref=f2e7] [cursor=pointer]:
        - /url: http://www.automationtesting.in
        - img "image not displaying" [ref=f2e8]
      - heading "Automation Demo Site" [level=1] [ref=f2e10]
    - navigation [ref=f2e11]:
      - list [ref=f2e14]:
        - listitem [ref=f2e15]:
          - link "Home" [ref=f2e16] [cursor=pointer]:
            - /url: Index.html
        - listitem [ref=f2e17]:
          - link "Register" [ref=f2e18] [cursor=pointer]:
            - /url: Register.html
        - listitem [ref=f2e19]:
          - link "WebTable" [ref=f2e20] [cursor=pointer]:
            - /url: WebTable.html
        - listitem [ref=f2e21]:
          - link "SwitchTo" [ref=f2e22] [cursor=pointer]:
            - /url: SwitchTo.html
          - generic [ref=f2e23]: 
        - listitem [ref=f2e24]:
          - link "Widgets" [ref=f2e25] [cursor=pointer]:
            - /url: Widgets.html
          - generic [ref=f2e26]: 
        - listitem [ref=f2e27]:
          - link "Interactions" [ref=f2e28] [cursor=pointer]:
            - /url: Interactions.html
          - generic [ref=f2e29]: 
        - listitem [ref=f2e30]:
          - link "Video" [ref=f2e31] [cursor=pointer]:
            - /url: SwitchTo.html
          - generic [ref=f2e32]: 
        - listitem [ref=f2e33]:
          - link "WYSIWYG" [ref=f2e34] [cursor=pointer]:
            - /url: WYSIWYG.html
          - generic [ref=f2e35]: 
        - listitem [ref=f2e36]:
          - link "More" [ref=f2e37] [cursor=pointer]:
            - /url: "#"
          - generic [ref=f2e38]: 
        - listitem [ref=f2e39]:
          - link "Practice Site" [ref=f2e40] [cursor=pointer]:
            - /url: http://practice.automationtesting.in/
  - generic [ref=f2e41]:
    - generic [ref=f2e45]:
      - list [ref=f2e48]:
        - listitem [ref=f2e49]:
          - link "Single Iframe" [ref=f2e50]:
            - /url: "#Single"
        - listitem [ref=f2e51]:
          - link "Iframe with in an Iframe" [ref=f2e52] [cursor=pointer]:
            - /url: "#Multiple"
      - iframe [ref=f2e54]: <p>Your browser does not support iframes.</p>
    - generic [ref=f2e56]:
      - insertion [ref=f2e59]
      - insertion [ref=f2e63]
      - insertion [ref=f2e67]
      - insertion [ref=f2e71]
      - generic [ref=f2e76]:
        - generic [ref=f2e77]:
          - text: "\"@ 2016\""
          - link "Automation Testing" [ref=f2e78] [cursor=pointer]:
            - /url: "#"
          - text: "\"All Rights Reserved.\""
        - generic [ref=f2e79]:
          - link "" [ref=f2e80] [cursor=pointer]:
            - /url: https://www.facebook.com/automationtesting2016/
          - link "" [ref=f2e82] [cursor=pointer]:
            - /url: https://twitter.com/krishnasakinala
          - link "" [ref=f2e84] [cursor=pointer]:
            - /url: https://www.linkedin.com/nhome/?trk=hb_signin
          - link "" [ref=f2e86] [cursor=pointer]:
            - /url: https://plus.google.com/105286300926085335367
          - link "" [ref=f2e88] [cursor=pointer]:
            - /url: https://www.youtube.com/channel/UCmQRa3pWM9zsB474URz8ESg
```

# Test source

```ts
  1  | import {test, expect} from "@playwright/test"
  2  | 
  3  | //Frame Handling ----> Frame handling is the process of interacting with elements that are present inside an iframe.
  4  | 
  5  | //Single Frame
  6  | 
  7  | test ('SingleFrame', async ({page}) => {
  8  | 
  9  | await page.goto ("https://demo.automationtesting.in");                               // ------> Home Page URL
  10 | 
  11 | await page.locator('//button[@id="btn2"]').click();                                 // ------> click Skip Signin
  12 | 
  13 | await expect(page).toHaveURL("https://demo.automationtesting.in/Register.html")    // ------> After skip, URL check
  14 | 
  15 | await page.locator("//a[text() = 'SwitchTo']").click()                            // -----> Click SwitchTo option in the UI page
  16 | 
  17 | await page.locator("//a[text() = 'Frames']").click();                             //  ------> Click Frame from Dropdown
  18 | 
  19 | // Handling Single iFrame
  20 | 
  21 | const SingleFrame = await page.frameLocator("//iframe[@id='singleframe']");
> 22 | await SingleFrame.locator("//input[@type='text']").fill("Hi Devaraj Welcome to FrameHandling");
     |                                                    ^ Error: locator.fill: Test timeout of 30000ms exceeded.
  23 | 
  24 | 
  25 | })
  26 | 
  27 | 
  28 | //Handle Multi Frames
  29 | 
  30 | test ('MultiFrame', async ({page}) => {
  31 | 
  32 | await page.goto ("https://demo.automationtesting.in");                                   // ------> Home Page URL
  33 | 
  34 | await page.locator('//button[@id="btn2"]').click();                                     // ------> click Skip Signin
  35 | 
  36 | await expect(page).toHaveURL("https://demo.automationtesting.in/Register.html")        // ------> After skip URL check
  37 | 
  38 | await page.locator("//a[text() = 'SwitchTo']").click()                                // -----> Click SwitchTo option in the page
  39 | 
  40 | await page.locator("//a[text() = 'Frames']").click(); 
  41 | 
  42 | //Multi iFrames
  43 | 
  44 | await page.locator('//a[@href="#Multiple"]').click();  // click iframe with an iframe tap in UI
  45 | 
  46 | //HAndle MultiFrames
  47 | await page.frameLocator("//iframe[@src='MultipleFrames.html']")  // ----> frameLocator 1st iframe
  48 | .frameLocator("//iframe[@src='SingleFrame.html']")               // ----> frameLocator 2nd iframe
  49 | .locator("//input[@type='text']")                              // ----> text box page locator
  50 | .fill("MultiFrame Handling");
  51 | 
  52 | })
```