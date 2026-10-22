# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: WindowHandling.spec.js >> WindowHandling
- Location: tests\WindowHandling.spec.js:7:5

# Error details

```
Test timeout of 30000ms exceeded.
```

```
Error: locator.click: Test timeout of 30000ms exceeded.
Call log:
  - waiting for locator('//a[text() = \'SwitchTo\']')

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
> 15 | await page.locator("//a[text() = 'SwitchTo']").click()                            // -----> Click SwitchTo option in the UI page
     |                                                ^ Error: locator.click: Test timeout of 30000ms exceeded.
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
  53 |   await pages[0].locator('//input[@id="email"]').fill('xyz');
  54 | });
  55 | 
  56 | 
  57 | 
```