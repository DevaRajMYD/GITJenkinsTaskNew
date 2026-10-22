# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: Alerts.spec.js >> ConfirmationAlert
- Location: tests\Alerts.spec.js:30:5

# Error details

```
Test timeout of 30000ms exceeded.
```

```
Error: page.goto: Test timeout of 30000ms exceeded.
Call log:
  - navigating to "https://demo.automationtesting.in/Alerts.html", waiting until "load"

```

# Page snapshot

```yaml
- generic [active] [ref=e1]:
  - banner [ref=e2]:
    - generic [ref=e5]:
      - link [ref=e7]:
        - /url: http://www.automationtesting.in
        - img "image not displaying" [ref=e8]
      - heading "Automation Demo Site" [level=1] [ref=e10]
    - navigation [ref=e11]:
      - list [ref=e14]:
        - listitem [ref=e15]:
          - link "Home" [ref=e16]:
            - /url: Index.html
        - listitem [ref=e17]:
          - link "Register" [ref=e18]:
            - /url: Register.html
        - listitem [ref=e19]:
          - link "WebTable" [ref=e20]:
            - /url: WebTable.html
        - listitem [ref=e21]:
          - link "SwitchTo" [ref=e22]:
            - /url: SwitchTo.html
          - generic [ref=e23]: 
        - listitem [ref=e24]:
          - link "Widgets" [ref=e25]:
            - /url: Widgets.html
          - generic [ref=e26]: 
        - listitem [ref=e27]:
          - link "Interactions" [ref=e28]:
            - /url: Interactions.html
          - generic [ref=e29]: 
        - listitem [ref=e30]:
          - link "Video" [ref=e31]:
            - /url: SwitchTo.html
          - generic [ref=e32]: 
        - listitem [ref=e33]:
          - link "WYSIWYG" [ref=e34]:
            - /url: WYSIWYG.html
          - generic [ref=e35]: 
        - listitem [ref=e36]:
          - link "More" [ref=e37]:
            - /url: "#"
          - generic [ref=e38]: 
        - listitem [ref=e39]:
          - link "Practice Site" [ref=e40]:
            - /url: http://practice.automationtesting.in/
  - generic [ref=e44]:
    - list [ref=e46]:
      - listitem [ref=e47]:
        - link "Alert with OK" [ref=e48]:
          - /url: "#OKTab"
      - listitem [ref=e49]:
        - link "Alert with OK & Cancel" [ref=e50]:
          - /url: "#CancelTab"
      - listitem [ref=e51]:
        - link "Alert with Textbox" [ref=e52]:
          - /url: "#Textbox"
    - button "click the button to display an alert box:" [ref=e54] [cursor=pointer]
  - generic [ref=e56]:
    - insertion [ref=e59]:
      - generic [ref=e62]:
        - heading "These are topics related to the article that might interest you" [level=2] [ref=e64]: Discover more
        - link "Find Tech Guides" [ref=e65] [cursor=pointer]
        - link "Test script development" [ref=e70] [cursor=pointer]
        - link "Performance testing tools" [ref=e75] [cursor=pointer]
        - link "Load testing services" [ref=e80] [cursor=pointer]
        - link "Compare Broadband" [ref=e85] [cursor=pointer]
        - link "API testing software" [ref=e90] [cursor=pointer]
        - link "Mobile app automation" [ref=e95] [cursor=pointer]
        - link "Continuous integration tools" [ref=e100] [cursor=pointer]
    - insertion [ref=e107]:
      - generic [ref=e110]:
        - heading "These are topics related to the article that might interest you" [level=2] [ref=e112]: Discover more
        - link "Selenium training" [ref=e113] [cursor=pointer]
        - link "Try Cloud Tools" [ref=e118] [cursor=pointer]
        - link "Try Dev Tools" [ref=e123] [cursor=pointer]
        - link "Automated alert handling" [ref=e128] [cursor=pointer]
        - link "Source Robotics" [ref=e133] [cursor=pointer]
        - link "Web element interaction" [ref=e138] [cursor=pointer]
        - link "Learn to Code" [ref=e143] [cursor=pointer]
        - link "Cross browser testing" [ref=e148] [cursor=pointer]
    - insertion [ref=e155]:
      - generic [ref=e158]:
        - heading "These are topics related to the article that might interest you" [level=2] [ref=e160]: Discover more
        - link "Test Keyboards" [ref=e161] [cursor=pointer]
        - link "DevOps automation services" [ref=e166] [cursor=pointer]
        - link "Book Play Tickets" [ref=e171] [cursor=pointer]
        - link "Read Showbiz News" [ref=e176] [cursor=pointer]
        - link "Automation testing tools" [ref=e181] [cursor=pointer]
        - link "Automation demo site" [ref=e186] [cursor=pointer]
        - link "Web automation services" [ref=e191] [cursor=pointer]
        - link "Software testing courses" [ref=e196] [cursor=pointer]
    - insertion [ref=e203]:
      - generic [ref=e206]:
        - heading "These are topics related to the article that might interest you" [level=2] [ref=e208]: Discover more
        - link "Automation testing tools" [ref=e209] [cursor=pointer]
        - link "Automation demo site" [ref=e214] [cursor=pointer]
        - link "Web automation services" [ref=e219] [cursor=pointer]
        - link "Software testing courses" [ref=e224] [cursor=pointer]
        - link "Quality assurance consulting" [ref=e229] [cursor=pointer]
        - link "UI testing solutions" [ref=e234] [cursor=pointer]
        - link "Automation framework templates" [ref=e239] [cursor=pointer]
        - link "Test case management" [ref=e244] [cursor=pointer]
    - contentinfo [ref=e250]:
      - generic [ref=e252]:
        - generic [ref=e253]:
          - text: "\"@ 2016\""
          - link "Automation Testing" [ref=e254]:
            - /url: "#"
          - text: "\"All Rights Reserved.\""
        - generic [ref=e255]:
          - link "" [ref=e256]:
            - /url: https://www.facebook.com/automationtesting2016/
          - link "" [ref=e258]:
            - /url: https://twitter.com/krishnasakinala
          - link "" [ref=e260]:
            - /url: https://www.linkedin.com/nhome/?trk=hb_signin
          - link "" [ref=e262]:
            - /url: https://plus.google.com/105286300926085335367
          - link "" [ref=e264]:
            - /url: https://www.youtube.com/channel/UCmQRa3pWM9zsB474URz8ESg
```

# Test source

```ts
  1  | import {test} from '@playwright/test'
  2  | 
  3  | 
  4  | //Types ===> Simple Alert, Confirmation Alert, Prompt Alert
  5  | 
  6  | //Simple Alert ----> only OK button in the Alert
  7  | 
  8  | test ('SimpleAlert', async ({page}) => {
  9  | 
  10 | await page.goto ("https://demo.automationtesting.in/Alerts.html");
  11 | 
  12 | //Syntax code for Alert Handling ---> should be before the click action in the test code
  13 | 
  14 |  page.once('dialog', async dialog => {
  15 | dialog.accept() //------> Handle OK button 
  16 | console.log(dialog.message())
  17 | console.log(dialog.type())
  18 | 
  19 |  } )
  20 | 
  21 | await page.locator('//button[@onclick="alertbox()"]').click() 
  22 | 
  23 | })
  24 | 
  25 | 
  26 | 
  27 | 
  28 | // Confirmation Alert Handling --->  OK or Cancel ----> dialog.accept()  or dialog.dismiss()
  29 | 
  30 | test ('ConfirmationAlert', async ({page}) => {
  31 | 
> 32 | await page.goto ("https://demo.automationtesting.in/Alerts.html");
     |            ^ Error: page.goto: Test timeout of 30000ms exceeded.
  33 | 
  34 | //Syntax code for Alert Handling 
  35 |  page.once('dialog', async dialog => {
  36 | dialog.accept() //------> Handle OK button
  37 | // dialog.dismiss() //------> Handle Cancel button
  38 | console.log(dialog.message())
  39 | console.log(dialog.type())
  40 |  } )
  41 | await page.locator('//a[@href="#CancelTab"]').click()
  42 | await page.locator('//button[@onclick="confirmbox()"]').click()
  43 | 
  44 | })
  45 | 
  46 | 
  47 | 
  48 | //Prompt Based Alert Handling
  49 | 
  50 | test ('PromptAlert', async ({page}) => {
  51 | 
  52 | await page.goto ("https://demo.automationtesting.in/Alerts.html");
  53 | //Syntax code for Alert Handling
  54 |  page.once('dialog', async dialog => {
  55 | await dialog.accept("Hi Devaraj") //------> in Prompt Alert we can pass the Text in the Prompt box into the .accept("gggggg") or .dismiss("ggggg")
  56 | // dialog.dismiss()
  57 | console.log(dialog.message())
  58 | console.log(dialog.type())
  59 | console.log(dialog.defaultValue()) //-----> used to print default text in the Prompt command box
  60 |  } )
  61 | await page.locator('//a[@href="#Textbox"]').click()
  62 | await page.locator('//button[@onclick="promptbox()"]').click()
  63 | 
  64 | })
  65 | 
  66 | 
  67 | 
```