# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: WindowHandling.spec.js >> Multi Window Handling
- Location: tests\WindowHandling.spec.js:43:5

# Error details

```
TypeError: Cannot read properties of undefined (reading 'locator')
```

# Page snapshot

```yaml
- generic [ref=e1]:
  - banner [ref=e2]:
    - generic [ref=e5]:
      - link [ref=e7] [cursor=pointer]:
        - /url: http://www.automationtesting.in
        - img "image not displaying" [ref=e8]
      - heading "Automation Demo Site" [level=1] [ref=e10]
    - navigation [ref=e11]:
      - list [ref=e14]:
        - listitem [ref=e15]:
          - link "Home" [ref=e16] [cursor=pointer]:
            - /url: Index.html
        - listitem [ref=e17]:
          - link "Register" [ref=e18] [cursor=pointer]:
            - /url: Register.html
        - listitem [ref=e19]:
          - link "WebTable" [ref=e20] [cursor=pointer]:
            - /url: WebTable.html
        - listitem [ref=e21]:
          - link "SwitchTo" [ref=e22] [cursor=pointer]:
            - /url: SwitchTo.html
          - generic [ref=e23]: 
        - listitem [ref=e24]:
          - link "Widgets" [ref=e25] [cursor=pointer]:
            - /url: Widgets.html
          - generic [ref=e26]: 
        - listitem [ref=e27]:
          - link "Interactions" [ref=e28] [cursor=pointer]:
            - /url: Interactions.html
          - generic [ref=e29]: 
        - listitem [ref=e30]:
          - link "Video" [ref=e31] [cursor=pointer]:
            - /url: SwitchTo.html
          - generic [ref=e32]: 
        - listitem [ref=e33]:
          - link "WYSIWYG" [ref=e34] [cursor=pointer]:
            - /url: WYSIWYG.html
          - generic [ref=e35]: 
        - listitem [ref=e36]:
          - link "More" [ref=e37] [cursor=pointer]:
            - /url: "#"
          - generic [ref=e38]: 
        - listitem [ref=e39]:
          - link "Practice Site" [ref=e40] [cursor=pointer]:
            - /url: http://practice.automationtesting.in/
  - generic [ref=e44]:
    - list [ref=e46]:
      - listitem [ref=e47]:
        - link "Open New Tabbed Windows" [ref=e48] [cursor=pointer]:
          - /url: "#Tabbed"
      - listitem [ref=e49]:
        - link "Open New Seperate Windows" [ref=e50] [cursor=pointer]:
          - /url: "#Seperate"
      - listitem [ref=e51]:
        - link "Open Seperate Multiple Windows" [expanded] [ref=e52]:
          - /url: "#Multiple"
    - generic [ref=e53]:
      - paragraph [ref=e54]: Click the button to open multiple windows
      - button "click" [active] [ref=e55] [cursor=pointer]
  - generic [ref=e57]:
    - insertion [ref=e60]:
      - generic [ref=e63]:
        - heading "These are topics related to the article that might interest you" [level=2] [ref=e65]: Discover more
        - link "Software Testing Tools" [ref=e66] [cursor=pointer]
        - link "Automation Testing Services" [ref=e71] [cursor=pointer]
        - link "Automation Training Courses" [ref=e76] [cursor=pointer]
        - link "Selenium WebDriver Tutorials" [ref=e81] [cursor=pointer]
        - link "Window Handle Solutions" [ref=e86] [cursor=pointer]
        - link "Browser Window Management" [ref=e91] [cursor=pointer]
        - link "Web Application Testing" [ref=e96] [cursor=pointer]
        - link "Test Automation Frameworks" [ref=e101] [cursor=pointer]
    - insertion [ref=e108]:
      - generic [ref=e111]:
        - heading "These are topics related to the article that might interest you" [level=2] [ref=e113]: Discover more
        - link "Robotic Process Automation" [ref=e114] [cursor=pointer]
        - link "Source Robotics" [ref=e119] [cursor=pointer]
        - link "Try Cloud Tools" [ref=e124] [cursor=pointer]
        - link "Try Dev Tools" [ref=e129] [cursor=pointer]
        - link "Selenium Grid Setup" [ref=e134] [cursor=pointer]
        - link "Multiple Window Handling" [ref=e139] [cursor=pointer]
        - link "Window Switching Techniques" [ref=e144] [cursor=pointer]
        - link "QA Consulting Services" [ref=e149] [cursor=pointer]
    - insertion [ref=e156]:
      - iframe [ref=e158]:
        - generic [ref=f4e2]:
          - iframe [ref=f4e5]:
            - generic [ref=f9e2] [cursor=pointer]:
              - img [ref=f9e4]:
                - generic "Try for free" [ref=f9e272]
              - button [ref=f9e380]
          - generic [ref=f4e6]:
            - generic:
              - generic [ref=f4e7] [cursor=pointer]
              - button [ref=f4e12] [cursor=pointer]
    - insertion [ref=e161]:
      - generic [ref=e164]:
        - heading "These are topics related to the article that might interest you" [level=2] [ref=e166]: Discover more
        - link "Automated Regression Testing" [ref=e167] [cursor=pointer]
        - link "AI in Automation" [ref=e172] [cursor=pointer]
        - link "Compare Browsers" [ref=e177] [cursor=pointer]
        - link "Compare Broadband" [ref=e182] [cursor=pointer]
        - link "Selenium IDE Training" [ref=e187] [cursor=pointer]
        - link "Build a Website" [ref=e192] [cursor=pointer]
        - link "Popup Window Automation" [ref=e197] [cursor=pointer]
        - link "Test Keyboards" [ref=e202] [cursor=pointer]
    - contentinfo [ref=e208]:
      - generic [ref=e210]:
        - generic [ref=e211]:
          - text: "\"@ 2016\""
          - link "Automation Testing" [ref=e212] [cursor=pointer]:
            - /url: "#"
          - text: "\"All Rights Reserved.\""
        - generic [ref=e213]:
          - link "" [ref=e214] [cursor=pointer]:
            - /url: https://www.facebook.com/automationtesting2016/
          - link "" [ref=e216] [cursor=pointer]:
            - /url: https://twitter.com/krishnasakinala
          - link "" [ref=e218] [cursor=pointer]:
            - /url: https://www.linkedin.com/nhome/?trk=hb_signin
          - link "" [ref=e220] [cursor=pointer]:
            - /url: https://plus.google.com/105286300926085335367
          - link "" [ref=e222] [cursor=pointer]:
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
  7  | test ('WindowHandling', async ({page}) => {
  8  | 
  9  | await page.goto ("https://demo.automationtesting.in");                               // ------> Home Page URL
  10 | 
  11 | await page.locator('//button[@id="btn2"]').click();                                 // ------> click Skip Signin
  12 | 
  13 | await expect(page).toHaveURL("https://demo.automationtesting.in/Register.html")    // ------> After skip, URL check
  14 | 
  15 | await page.locator("//a[text() = 'SwitchTo']").click()                            // -----> Click SwitchTo option in the UI page
  16 | 
  17 | await page.locator('//a[text()="Windows"]').click();                             // ---> select window from dropdown
  18 | 
  19 | 
  20 | // Provide listener to store event while window handling
  21 | // const newEvent = page.waitForEvent('popup');
  22 | 
  23 | // await page.locator("//button[text()='    click   ']").click()                    // ---> Click "click" button
  24 | 
  25 | // const newTap = await newEvent;                                                   // ---> here declare new variable for line 20 ("newEvent") 
  26 | 
  27 | // await newTap.locator('//a[@class="nav-link"]').first().click()   //----> click "download" in the new tap, so pass the xpath using "newTap"
  28 | 
  29 | //                       ---------------- OR ----------
  30 | 
  31 | // Provide listener to store event while window handling - another way to create Listener
  32 | 
  33 | const [newTap] = await Promise.all([page.waitForEvent('popup'), page.locator("//button[text()='    click   ']").click() ])
  34 | 
  35 | await newTap.locator('//a[@class="nav-link"]').first().click()
  36 | 
  37 | 
  38 | }) 
  39 | 
  40 | 
  41 | //Code for MultiWindow Handling ---> need to find multiWindow optional website to run this code
  42 | 
  43 | test('Multi Window Handling', async ({context}) => {
  44 |   const mainPage = await context.newPage();
  45 |   await mainPage.goto('https://demo.automationtesting.in/Windows.html');
  46 |   await mainPage.locator('//a[@href="#Multiple"]').click()
  47 | 
  48 |   const pages = [];
  49 |   context.on('page', newPage => {pages.push(newPage)})
  50 | 
  51 |   await mainPage.locator('//button[@onclick="multiwindow()"]').click()
  52 |   console.log(pages.length);
> 53 |   await pages[0].locator('//input[@id="email"]').fill('xyz');
     |                  ^ TypeError: Cannot read properties of undefined (reading 'locator')
  54 | });
  55 | 
  56 | 
  57 | 
```