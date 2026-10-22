# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: Alerts.spec.js >> PromptAlert
- Location: tests\Alerts.spec.js:50:5

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
    - insertion [ref=e59]
    - insertion [ref=e63]
    - insertion [ref=e67]
    - insertion [ref=e71]
    - contentinfo [ref=e74]:
      - generic [ref=e76]:
        - generic [ref=e77]:
          - text: "\"@ 2016\""
          - link "Automation Testing" [ref=e78]:
            - /url: "#"
          - text: "\"All Rights Reserved.\""
        - generic [ref=e79]:
          - link "" [ref=e80]:
            - /url: https://www.facebook.com/automationtesting2016/
          - link "" [ref=e82]:
            - /url: https://twitter.com/krishnasakinala
          - link "" [ref=e84]:
            - /url: https://www.linkedin.com/nhome/?trk=hb_signin
          - link "" [ref=e86]:
            - /url: https://plus.google.com/105286300926085335367
          - link "" [ref=e88]:
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
  32 | await page.goto ("https://demo.automationtesting.in/Alerts.html");
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
> 52 | await page.goto ("https://demo.automationtesting.in/Alerts.html");
     |            ^ Error: page.goto: Test timeout of 30000ms exceeded.
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