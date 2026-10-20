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
Error: locator.click: Test timeout of 30000ms exceeded.
Call log:
  - waiting for locator('//button[@onclick="promptbox()"]')
    - locator resolved to <button class="btn btn-info" onclick="promptbox()">click the button to demonstrate the prompt box </button>
  - attempting click action
    2 × waiting for element to be visible, enabled and stable
      - element is not visible
    - retrying click action
    - waiting 20ms
    2 × waiting for element to be visible, enabled and stable
      - element is not visible
    - retrying click action
      - waiting 100ms
    29 × waiting for element to be visible, enabled and stable
       - element is not visible
     - retrying click action
       - waiting 500ms
    - waiting for element to be visible, enabled and stable

```

# Page snapshot

```yaml
- generic [active] [aria-hidden] [ref=e1]:
  - banner [ref=e2]:
    - generic [ref=e5]:
      - link [ref=e7]:
        - /url: http://www.automationtesting.in
      - heading [level=1] [ref=e10]: Automation Demo Site
    - navigation [ref=e11]:
      - list [ref=e14]:
        - listitem [ref=e15]:
          - link [ref=e16]:
            - /url: Index.html
            - text: Home
        - listitem [ref=e17]:
          - link [ref=e18]:
            - /url: Register.html
            - text: Register
        - listitem [ref=e19]:
          - link [ref=e20]:
            - /url: WebTable.html
            - text: WebTable
        - listitem [ref=e21]:
          - link [ref=e22]:
            - /url: SwitchTo.html
            - text: SwitchTo
          - generic [ref=e23]: 
        - listitem [ref=e24]:
          - link [ref=e25]:
            - /url: Widgets.html
            - text: Widgets
          - generic [ref=e26]: 
        - listitem [ref=e27]:
          - link [ref=e28]:
            - /url: Interactions.html
            - text: Interactions
          - generic [ref=e29]: 
        - listitem [ref=e30]:
          - link [ref=e31]:
            - /url: SwitchTo.html
            - text: Video
          - generic [ref=e32]: 
        - listitem [ref=e33]:
          - link [ref=e34]:
            - /url: WYSIWYG.html
            - text: WYSIWYG
          - generic [ref=e35]: 
        - listitem [ref=e36]:
          - link [ref=e37]:
            - /url: "#"
            - text: More
          - generic [ref=e38]: 
        - listitem [ref=e39]:
          - link [ref=e40]:
            - /url: http://practice.automationtesting.in/
            - text: Practice Site
  - generic [ref=e44]:
    - list [ref=e46]:
      - listitem [ref=e47]:
        - link [ref=e48]:
          - /url: "#OKTab"
          - text: Alert with OK
      - listitem [ref=e49]:
        - link [ref=e50]:
          - /url: "#CancelTab"
          - text: Alert with OK & Cancel
      - listitem [ref=e51]:
        - link [ref=e52]:
          - /url: "#Textbox"
          - text: Alert with Textbox
    - button [ref=e54] [cursor=pointer]: "click the button to display an alert box:"
  - generic [ref=e56]:
    - insertion [ref=e59]:
      - iframe [ref=e61]:
        - generic [ref=f2e2]:
          - iframe [ref=f2e5]:
            - generic [ref=f14e2] [cursor=pointer]:
              - img [ref=f14e4]:
                - generic "Try for free" [ref=f14e272]
              - button [ref=f14e380]
          - generic [ref=f2e6]:
            - generic:
              - generic [ref=f2e7] [cursor=pointer]
              - button [ref=f2e12] [cursor=pointer]
    - insertion [ref=e64]:
      - iframe [ref=e66]:
        - generic [ref=f3e2]:
          - iframe [ref=f3e5]:
            - generic [ref=f12e2] [cursor=pointer]:
              - img [ref=f12e4]:
                - generic "Try for free" [ref=f12e272]
              - button [ref=f12e380]
          - generic [ref=f3e6]:
            - generic:
              - generic [ref=f3e7] [cursor=pointer]
              - button [ref=f3e12] [cursor=pointer]
    - insertion [ref=e69]:
      - iframe [ref=e71]:
        - generic [ref=f4e2]:
          - iframe [ref=f4e5]:
            - generic [ref=f18e2] [cursor=pointer]:
              - img [ref=f18e4]:
                - generic "Try for free" [ref=f18e272]
              - button [ref=f18e380]
          - generic [ref=f4e6]:
            - generic:
              - generic [ref=f4e7] [cursor=pointer]
              - button [ref=f4e12] [cursor=pointer]
    - insertion [ref=e74]:
      - iframe [ref=e76]:
        - generic [ref=f5e2]:
          - iframe [ref=f5e5]:
            - generic [ref=f16e2] [cursor=pointer]:
              - img [ref=f16e4]:
                - generic "Try for free" [ref=f16e272]
              - button [ref=f16e380]
          - generic [ref=f5e6]:
            - generic:
              - generic [ref=f5e7] [cursor=pointer]
              - button [ref=f5e12] [cursor=pointer]
    - contentinfo [ref=e78]:
      - generic [ref=e80]:
        - generic [ref=e81]:
          - text: "\"@ 2016\""
          - link [ref=e82]:
            - /url: "#"
            - text: Automation Testing
          - text: "\"All Rights Reserved.\""
        - generic [ref=e83]:
          - link [ref=e84]:
            - /url: https://www.facebook.com/automationtesting2016/
            - generic [ref=e85]: 
          - link [ref=e86]:
            - /url: https://twitter.com/krishnasakinala
            - generic [ref=e87]: 
          - link [ref=e88]:
            - /url: https://www.linkedin.com/nhome/?trk=hb_signin
            - generic [ref=e89]: 
          - link [ref=e90]:
            - /url: https://plus.google.com/105286300926085335367
            - generic [ref=e91]: 
          - link [ref=e92]:
            - /url: https://www.youtube.com/channel/UCmQRa3pWM9zsB474URz8ESg
            - generic [ref=e93]: 
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
> 62 | await page.locator('//button[@onclick="promptbox()"]').click()
     |                                                        ^ Error: locator.click: Test timeout of 30000ms exceeded.
  63 | 
  64 | })
  65 | 
  66 | 
  67 | 
```