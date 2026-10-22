# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: WindowHandling.spec.js >> Multi Window Handling
- Location: tests\WindowHandling.spec.js:43:5

# Error details

```
Test timeout of 30000ms exceeded.
```

```
Error: page.goto: Test timeout of 30000ms exceeded.
Call log:
  - navigating to "https://demo.automationtesting.in/Windows.html", waiting until "load"

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
        - link "Open New Tabbed Windows" [ref=e48]:
          - /url: "#Tabbed"
      - listitem [ref=e49]:
        - link "Open New Seperate Windows" [ref=e50]:
          - /url: "#Seperate"
      - listitem [ref=e51]:
        - link "Open Seperate Multiple Windows" [ref=e52]:
          - /url: "#Multiple"
    - generic [ref=e53]:
      - paragraph [ref=e54]:
        - text: If you set the target attribute to "_blank" , the link will open in a new browser window or a new tab
        - link "Compare Browsers" [ref=e55] [cursor=pointer]
      - link [ref=e59]:
        - /url: http://www.selenium.dev
        - button "click" [ref=e60] [cursor=pointer]
  - generic [ref=e62]:
    - insertion [ref=e65]:
      - iframe [ref=e67]:
        - iframe [ref=f2e1]:
          - generic [ref=f11e1]:
            - generic [ref=f11e2]:
              - generic:
                - generic [ref=f11e3] [cursor=pointer]
                - button [ref=f11e8] [cursor=pointer]
            - insertion [ref=f11e16]:
              - generic [ref=f11e17]:
                - link [ref=f11e18]:
                  - /url: https://googleads.g.doubleclick.net/dbm/clk?sa=L&ai=CRptQAr7Yao_9Ouvk2roPnNfg6QWI0YTjiAH0qoqg4xWeo5ia6UQQASCPvrcvYOWS6IPYDqABi-KKoAHIAQmoAwHIA5sEqgSCAk_Q69TaWQCJg8JMubXPdifA8NZ0e-q1uKIx0YEixGPxlkNPmrhugrAfQ1V4xBARVMOwxltgyvVsDV5ikSkvikoUcK0HVvoKYDstABbVjvPsAt_nudlgoasi5OQTx-60DYpvDK0LrCVzDz85G4mYs9nY16glncKC2o_gzBNAa_lDUrGXItrnfuzjwHI83BMjmzxJgDDbkHOk7WCvw5VU9Rv4w0q9Ci4XNPfrXkNHZPWXcCjwFu2AvXTQwf1LhogcYSmvMInC0aT_YS6aNLfPAsaXvANb9zc0KURVxJGKF4vEbRqS7LlPrqMOJ0dSsskNUmQS8khG8yidDh6K1EmLnZ50E8AEwsSCzu0E4AQDiAXojfL0UZAGAaAGTYAH3Z313wKoB6fMsQKoB6a-G6gHzM6xAqgH89EbqAeW2BuoB6qbsQKoB_7osQKoB47OG6gHk9gbqAfw4BuoB-6WsQKoB_6esQKoB6--sQKoB5_hsQKoB6brsQKoB9XJG6gH2baxAqgHmgaoB_-esQKoB9-fsQKoB_jCsQKoB_vCsQKoB-fXsQLYBwDSCDMIgGEQARifAzIIioKAgICAgAg6D4BAgMCAgICAqIACqIOAGEi9_cE6WMiz4cqby5cDYAGACgGYCwHICwGADAGqDQJJTuoNEwj7jePKm8uXAxVrslYBHZwrOF3wDQGIDgmwE7aR4SXIE_vm_eUD0BMA2BMKiBQB2BQB0BUByhYCCgD4FgGAFwGyFxAYAioKNjYzODYzMzU0N1AG6BcFqhgXCQAAAAB4vwdBEgo2NjM4NjMzNTQ3GAGyGAkSAp1jGE0iAQDQGQHYGQE&ae=1&num=1&cid=CAQShwIAQM4h3H7S54R4iYpMMUwPX_IkjLUCAhWejOib86tWn-wVL27iHv26NHsmrqik430pAmb7nzOJUPVTKXlI8oO6bK4L0rRGjMqv808oQPYfu2YP0TC-Aaqi4T4tFytWdEHz2wb3bz4JgJln6Lqmecf_i4JSVetSjBApDm9vd6tF4a7Xk9_mH6uF8ADnYZv6JD0C_kdqdpOweNhEl8RGqqMjPAdfo0vzPG1grShZPe0bYWb1y-YqFJh8K86YlyNmFCEHTjsKP4Pi3QMTy_fmMTrsbjKetyL9zF1aJagpKRpGVqlvWsIilLe_ny5L81QZxMRusPCblde_zP3jcixSCZf14GwVhKBzzBgB&sig=AOD64_2yHsi9wZkhkFxRCW24L_GOrdJ7pA&client=ca-pub-9173866185064071&dbm_c=AKAmf-BD7ojZnYVvj38hNkuHJ9NGXPPhUn68STBj2t0vIWNuQjVrgsABq0lT_sgzzhONJVmOjH4EVCPuVBsgEVAIo0T4dR3saoLm-FHtc6ExAyYTSM3bAx9NvHUSOIoc9XQbJXpMwEk-bYFiBDMnoHAYro5cXuOeeCykTjdX9YM9ijz7BwKRa-EyCaQp_ldYaGaPYK9GEjQ91SJzzTZkuNErpULNr0XUx5TwV3d4oyvSEeWmwfepp2swX7rz262_WGiVwINKJ2Fs8QwEBsmj0zb11fs1-qtITKevvCWTf4wExfDIe7HJCr6GJP3emjn6mzN0kIIoX2kg&cry=1&dbm_d=AKAmf-C3EKejdnoU6YOcdezMBOfvxTF_uVG0A746UiZrxxMvpjRN-38cLa6hQ1jODcdnSUUnDwrWDlSewZHIgS9I0uNYujPIjo1YWsu0yfBFsK53zcLA1-z06scVcyDrXKWuJ787br10RI-xyq20fVY0quUw2ANw5Po-B6pCMrrnmwyDAJmHRPsEnxEvnfERUevSiWhlF0VsvasaLH3cQ1XZJJ8bqkAOjuLrcULDqBT6EXRtHmLhqaTMJxRxVjV11UheyWuOf23o2ubZuAkz79cEbc8d7PKauVUCJYNi7Hg6ko58WEFpB10crE92b3qhPTWM74vE3hXO-zKuPViG4DKg0WI5pPV6GjTmggJCbOG7k_1DBCoKhxgTpVP5_XwdkFF0JSvo052VvWBWNpk0WfOoh-P4sCwGKCmvqLtzdkOm4Sp7sH0X8BLlx8jnFap0BWXq58ZyWAglELqUvzhH74eLFJRWL9yvFuxbTy_-mcZQ3VWI78qX7afIFvKRQMJz3BWFllYjpM9pitTZDT1VdOqvxDvRF1tQB6yQ0pX6fzUqpX7MU_9P9bNs5l6vIzVxh8Jm0p3hWLLEMsNnDhlgjzajWsR4oDeTRXSYxMhMsENm1Y1IM75LMz_JZJ_HfgVc6ynWK9idaH-58WxVloiJzx84-BQRzVPDZofChCUryhhC-FZBhXmUD5m0I4vTu1hd4XfqZPOCjO2g9uvZ3u8Iao-7uxI2483CmwC43n0sQwjtKeW4DSbc7_c&adurl=https://servedby.flashtalking.com/click/7/296969;10262637;4919258;210;0/?us_privacy=!!US_PRIVACY!&ft_partnerimpid=ABAjH0iFqCMxy6JtrH1puxjpjN_4&ft_impID=1C798955-420C-A996-E38C-CDBA2EFD08E1&ft_section=21988411112&g=68685A529B6C62&random=678263.424804179&ft_width=160&ft_height=600&url=https://www.adobe.com/in/creativecloud.html?sdid=PC1PQ9XF&mv=display&mv2=display
                  - img "Click Here" [ref=f11e19]
                - link [ref=f11e21]:
                  - /url: https://www.flashtalking.com/consumer-privacy
                  - img "AdChoices arrow" [ref=f11e22]
                - link "Privacy Notification" [ref=f11e24]:
                  - /url: https://www.flashtalking.com/consumer-privacy
    - insertion [ref=e70]:
      - iframe [ref=e72]:
        - iframe [ref=f3e1]:
          - generic [ref=f9e1]:
            - generic [ref=f9e2]:
              - generic:
                - generic [ref=f9e3] [cursor=pointer]
                - button [ref=f9e8] [cursor=pointer]
            - insertion [ref=f9e16]:
              - generic [ref=f9e17]:
                - link [ref=f9e18]:
                  - /url: https://googleads.g.doubleclick.net/dbm/clk?sa=L&ai=Cz667Ar7Yape_O57u2roP58jtwQOI0YTjiAH0qoqg4xWeo5ia6UQQASCPvrcvYOWS6IPYDqABi-KKoAHIAQmoAwHIA5sEqgSFAk_Qk0Z4ir1CJVvgTWxUoCE3uDNudP5sVuaYX-ziVA1w5ng1vkGeNeAaiHKGPCxk97CQ_uBHjWH12xZHY_70FG9TqyjOuJ5V5FeLJRcwhKws_I2gp6mSce2One2wDEAGSzDHU6C1F1iabsAhXaT1stYIe-JU-cp0VKCLCwjLmte6p9RhsyCDB9b5Guv-hnQ8_Ky7S5q7Dk_UeQs5ixKkQHHN3djnAXetQtBKnlU-djNhozElLYYye0digoNqMfGxAnzhvZU85-HP5APdBsbrwTU0PHuga0WU31JU6wp6dVBl0j9ud7Gjz7fU1hMBsPqVhc1GQprpnOnxSFzrMgf3W-rGLc3DzcAEwsSCzu0E4AQDiAXojfL0UZAGAaAGTYAH3Z313wKoB6fMsQKoB6a-G6gHzM6xAqgH89EbqAeW2BuoB6qbsQKoB_7osQKoB47OG6gHk9gbqAfw4BuoB-6WsQKoB_6esQKoB6--sQKoB5_hsQKoB6brsQKoB9XJG6gH2baxAqgHmgaoB_-esQKoB9-fsQKoB_jCsQKoB_vCsQKoB-fXsQLYBwDSCDMIgGEQARifAzIIioKAgICAgAg6D4BAgMCAgICAqIACqIOAGEi9_cE6WK774cqby5cDYAGACgGYCwHICwGADAGiDAwqCgoIjt-xApXisQKqDQJJTuoNEwjTzOPKm8uXAxUet1YBHWdkOzjwDQGIDgmwE7aR4SXIE_vm_eUD0BMA2BMKiBQB2BQB0BUByhYCCgD4FgGAFwGyFxAYAioKNjYzODYzMzU0N1AG6BcFqhgXCQAAAABg6wtBEgo2NjM4NjMzNTQ3GAGyGAkSAp1jGE0iAQDQGQHYGQE&ae=1&num=1&cid=CAQSiAIAQM4h3JGU3m1iFgXiszcKx0DrPXPMna-3EnWts9nLvalNPgLura6K7kiqoo7vxDM1llZ-BsMEqE0reDE_Z30awuNGxdjhKrhQlBRy4H0XrzHCFZX4gTxToNUfERRh_oCBLsSMWIMQP0h8pvvHgO7RYbGF7v15n7swK4UNwY_0vHpSWMGdbvJgGJhKj_fMKWH_uycRN3CZXjxGZtOHW0p87F5H8yf_whqJnvQoA69Oe8uuYt-QzD4cEEipoc6iDUtHM9iR4vMYvoQHMinmYgauGvHWfxoqpss6QMAaMWhfrqy5T0JogoBb5ezkawvNC2BYq-8bXmZl-4cajggmyJHUY17uJXQHicQYAQ&sig=AOD64_0XerlD_Pg_Sy-4SXVyafwioMsw5g&dbm_c=AKAmf-AoOSxFpwmJicVJJrhvkrKlrQmGdSHnAa7jaIDoUbJL-8m7MsS2BMFMZsqtOSmbjlomtQjf67rZUPN6mto3A2MHUz0gNTcirl6hjWJxjOviezkn-RS9guXHsecllVUkGeUJpgSBn58SIakDIStScP7DtMvxreR0aSreVYH-NioPRcqCkagK7dA9KOlKGtBAYqMN70QJJuzdKcNj_BuZD_wnqX6Brrw3rCJ5O21rWv6ZX7hxO4L8-rTFp305yWWL6mOGFqGkmqge6CYyWJmVdVnW2QwpwkRWFKVlRi3P-MaxELmDQaPUj8AF6t9_7xsHTiGa4-dJ&cry=1&dbm_d=AKAmf-CbYHz5bmcf166e25aSXT3tq_UNfJaySFGDzDpnN55InOgev2sMGz_JnyEp2vNJettdDAq9WtaAmxeKhwJpyL_U4gy4C8X31moZyESnhGxLv78AXHUnXPHTRUCgQmZxfL_PALQyiL5zd0LEsVC0M2B1ebb-jfGyCEzipcl68TNd32ZtTHSyrWDLSq8oqcofWscMEJR9yxxKPW3sIfczNOSExXdwYf36tSFN_L1T5Jsbkb0A50NpwiH9opX6wqqPhRPO77zU7mDunmmUHzRRDxX76djJdvZd9w8bcRI8O1-BusDXi4sJTVaHmHJisTr0O8oAoE-mSypaOVPsccALB60SNJYAbw-VufbryoxrAlqRcFBUmvBmN44VgNBDS2phYLudRpdWJOcFKdkklJrNUpNrHY7s3k71rrpNc7THRrkNqm5sj2Ahij_68Uo7URwZkvCCkslnpD2HHnxQQ34gKr7Uw2PVxZ8SBmD5rAiEP9TAvFKa2ChFMRtw5gTUxjKvJ6UMgD5XysFigtktd_FH1feIWjYefE8brr8xSm-2qPrkdzJ3W-kbLGzRs4iBlbcZD7f7W6st9gOViObHSNplyF0V_Fi-UlAQpD0WBWbrEpxeTAq82Mo3yBjbNTA7cqiSDOkFEHp1omVJWodgBENTR_4G7ezmVgZt3ei1--qsW1E0kF-3Fdl75iFe-5VxoB-SlDrRCR_HGOMA1b-ox69xRroP7xxwW26DIrNOGouIwh08iUy_KW7SrQPWp3YivCtVExYCG5I7&adurl=https://servedby.flashtalking.com/click/7/296969;10262637;4919222;210;0/?us_privacy=!!US_PRIVACY!&ft_partnerimpid=ABAjH0ggZYTOE2WnzIwXCouSV48A&ft_impID=2EDFBA94-6392-719E-1054-731C6A9404A2&ft_section=21988411112&g=686839FD31D56A&random=965780.4790484989&ft_width=160&ft_height=600&url=https://www.adobe.com/in/creativecloud.html?sdid=PC1PQ9XF&mv=display&mv2=display
                  - img "Click Here" [ref=f9e19]
                - link [ref=f9e21]:
                  - /url: https://www.flashtalking.com/consumer-privacy
                  - img "AdChoices arrow" [ref=f9e22]
                - link "Privacy Notification" [ref=f9e24]:
                  - /url: https://www.flashtalking.com/consumer-privacy
    - insertion [ref=e75]:
      - iframe [ref=e77]:
        - iframe [ref=f4e1]:
          - generic [ref=f7e1]:
            - generic [ref=f7e2]:
              - generic:
                - generic [ref=f7e3] [cursor=pointer]
                - button [ref=f7e8] [cursor=pointer]
            - insertion [ref=f7e16]:
              - generic [ref=f7e17]:
                - link [ref=f7e18]:
                  - /url: https://googleads.g.doubleclick.net/dbm/clk?sa=L&ai=C1c55Ar7YavPhPLmy2roPzae9iQiI0YTjiAH0qoqg4xWeo5ia6UQQASCPvrcvYOWS6IPYDqABi-KKoAHIAQmoAwHIA5sEqgSLAk_QihfNFz3z8gq2AWKlz6bFKVCmbER75Dmy0fu7mI9UG1pWhU7cHorL5DFz14L2Mhpz0TEDSgXjMo1StbL42M7csqUgQiJ5X_p4TJfIkFZzmOkjdnjdT-vOQ-IJBer2b9Upi4a8-lOoYejAmiOAy82VWm1wCbnobJRjzIFTxD-_gsDASRKKDdTtJFU57tvwEmdMNl6nO0r5ZGYq3pDeo3jUPNBl1fZE3foxX8EmQM_H9VUTfbiR6iymnFLMy1Odb_3IzqzwdlRpj25IDYvxNQ8XYJUW9_v2jIaRVsu2KeyHlEzGpzjSowV0Irg1eFf8pDojXjfRxVl_VdMfE8bPNSIl45QR2ZJFzTcdWcAEwsSCzu0E4AQDiAXojfL0UZAGAaAGTYAH3Z313wKoB6fMsQKoB6a-G6gHzM6xAqgH89EbqAeW2BuoB6qbsQKoB_7osQKoB47OG6gHk9gbqAfw4BuoB-6WsQKoB_6esQKoB6--sQKoB5_hsQKoB6brsQKoB9XJG6gH2baxAqgHmgaoB_-esQKoB9-fsQKoB_jCsQKoB_vCsQKoB-fXsQLYBwDSCDMIgGEQARifAzIIioKAgICAgAg6D4BAgMCAgICAqIACqIOAGEi9_cE6WPil48qby5cDYAGACgGYCwHICwGADAGqDQJJTuoNEwiJ8OTKm8uXAxU5mVYBHc1TL4HwDQGIDgmwE7aR4SXIE_vm_eUD0BMA2BMKiBQB2BQB0BUByhYCCgD4FgGAFwGyFxAYAioKNjYzODYzMzU0N1AG6BcFqhgXCQAAAAAgbAtBEgo2NjM4NjMzNTQ3GAGyGAkSAp1jGE0iAQDQGQHYGQE&ae=1&num=1&cid=CAQShwIAQM4h3M_nhBK8wCpFzf5LPJK5xhOdIixiEcHBZ_ueNUddKPAsV-MM5zR2Z_0tZDDazykfOXwFydbkeZObi7PUwuQ0D7qryHfdYDz-PKnfQtelgEmuJj1B4TCKH3RdgJGXNRuy7Lqsejv03oac-MZbYuEmzh2kiRYBr-8YK8nnnaOIWhHonFjnQQd0kT_-zH0ddjiDlfaAef942WMi_5rmeKoTyZj6d0kkFMm9mVO8KNCD4w2NRKRZ0JQYQGtf_Mk4DQIdb7oaw6NgmECC_4_tghDKIKIV6yjc2pQMg4YVnSrDYaBsupej5N07ovbdu5wp0TeCXPPLGh51GAiqaFdWn-eA8lvAahgB&sig=AOD64_287EJGxUCludQEq0b-RdTZDy1OAA&dbm_c=AKAmf-A0qMoY-FjapKK-sf9Vkm4zGSrraSa4yLrYE2p4JJN3cJ_ZgFBQw_8YMuM-fjn82_XKbvSW-0EndQm5VltsGyWs5B0uiyORYkNl2F6mK8AfS7Hk7jj96sgMMMsHgfCLl3Qw0zrpuuMacVMz4bFYKlF12xdyWBGXZCUGQWvqt8f4im8VBw_Z_SIyp7WfHlDq61O8h1MYtM7qfMmRozldOpFyXjxqc6eIzoJVnIHtmUE3OY48hQ67yrhaL5zZMbviTQ8FQ0Lvfu-DlfQ4p_sOX2rGP6XP6Q-h-nUlHsau6cDhXE5JVZXNvYeMZBETBoJqytg8vVk0&cry=1&dbm_d=AKAmf-AQodKeOtTCHlY_nxIhO0rtUl52KRNIYQvH7yrAS1JM1hDU215ZGw04HDCBj0EZGP_rkYsWvgvgx1BSoIXOCLCBZeoVfUaZ2sfjmreydNy48Pq0UpXtg9V-bJ4gGUQRHD6o8XXmFhOtT3Rh6SWcwnS4wjAUIfSjQjkN-gKYA5YKSQKzOewsvEjpBFXz9fCLWMPT1E8tivR8_sPBO68rA5F2BS1usYmgUTYtjfvXwVSV0CJc_1Ww7qlDVPFqGVeMh1JQVKlxbpcU6pD34RxupaCEhDJZbBbpD0OjezHG5RZe2vcrWWdfl-CCjX4ow9t0w_WFzSIfqFD0uo7UT6B0oG_hESElrrhtErgLpf1alBm6kyNJs7x1TMXqqrQ1l6u_aT3JENCIl8wqEghNnrpwhXaHaiwktmrOEO4FCXF-o3I1wQO7r60u1x3BxfKbxQtG3p7ieXqvM8zEjvoPovyvuik7shYhP-cLp7AooJpWzjtdhgScmK95Ug9lIj92HmcSoFzmA38VHJ04lRL3dKmtoMtEEp46bmqe1Ey5GzWQ_UEn6z3wcxQHzdKMvxalkr-gTWOtyGxhmEPjXJ4DsHOUPELthBPhClngA6xD14eor23i4MlDWXJD6mr5-YOZwJR-6trz2l0J-hSZ3l9wzcD_qyUrEG6z6scXd8S3iXlwxiCPfzEc_qNelzJTSYGQajDZCUBnYlJMUXTgllW0UJQGjwHCQhZtT_TeRXFXkIi9hzoEfe6igtg&adurl=https://servedby.flashtalking.com/click/7/296969;10262637;4919222;210;0/?us_privacy=!!US_PRIVACY!&ft_partnerimpid=ABAjH0h2LlHN7PSijoDflR90I3yA&ft_impID=FAB0CDB3-4942-F8F6-9323-CCF5CC9C29AE&ft_section=21988411112&g=6868F6BBDA9689&random=965780.4790484989&ft_width=160&ft_height=600&url=https://www.adobe.com/in/creativecloud.html?sdid=PC1PQ9XF&mv=display&mv2=display
                  - img "Click Here" [ref=f7e19]
                - link [ref=f7e21]:
                  - /url: https://www.flashtalking.com/consumer-privacy
                  - img "AdChoices arrow" [ref=f7e22]
                - link "Privacy Notification" [ref=f7e24]:
                  - /url: https://www.flashtalking.com/consumer-privacy
    - insertion [ref=e80]:
      - iframe [ref=e82]:
        - iframe [ref=f5e1]:
          - generic [ref=f13e1]:
            - generic [ref=f13e2]:
              - generic:
                - generic [ref=f13e3] [cursor=pointer]
                - button [ref=f13e8] [cursor=pointer]
            - insertion [ref=f13e16]:
              - generic [ref=f13e17]:
                - link [ref=f13e18]:
                  - /url: https://googleads.g.doubleclick.net/dbm/clk?sa=L&ai=CqSnTAr7YaoGCPZOs0-kPkO7fuA6I0YTjiAH0qoqg4xWeo5ia6UQQASCPvrcvYOWS6IPYDqABi-KKoAHIAQmoAwHIA5sEqgSLAk_QuQ9Vq8YgRR-mdVxFLWM4r12aoHLpLnAXVVJOJiLzDvXBnGZi7_yRS4Cm2DHJULydXBGuwTtMM4oy6vUguPPwYtR0bq2UEgJmv4xqxcdGb7QbmUWEdxsbkTqgH7v34qlP60OkwjOD7CRM9qwmovtIMb0p8yHSeG28Kfq1FqzM1Id7x4Ayyc9FZKXokb5_wHetfK8GNLmSuk3caEaTOyBlsD0_yJGU2jyO-Lw56w4YFeQGLQshu06ghOMRc5nS-AMWrBljL4A75iOWznIZyikwpsFX0CTbCxB_yz6QU4TxQ_7hfthimQEznYQASc52Zl5ujb7WgYlmHGtngwOQPXRoevcXAIqhdCtYB8AEwsSCzu0E4AQDiAXojfL0UZAGAaAGTYAH3Z313wKoB6fMsQKoB6a-G6gHzM6xAqgH89EbqAeW2BuoB6qbsQKoB_7osQKoB47OG6gHk9gbqAfw4BuoB-6WsQKoB_6esQKoB6--sQKoB5_hsQKoB6brsQKoB9XJG6gH2baxAqgHmgaoB_-esQKoB9-fsQKoB_jCsQKoB_vCsQKoB-fXsQLYBwDSCDMIgGEQARifAzIIioKAgICAgAg6D4BAgMCAgICAqIACqIOAGEi9_cE6WJWn48qby5cDYAGACgGYCwHICwGADAGiDBAqDgoMjt-xApXisQL28rECqg0CSU7qDRMI4pPlypvLlwMVE9Y0Bx0Q9xfn8A0BiA4JsBO2keElyBP75v3lA9ATANgTCogUAdgUAdAVAcoWAgoA-BYBgBcBshcQGAIqCjY2Mzg2MzM1NDdQBugXBaoYFwkAAAAAUE4HQRIKNjYzODYzMzU0NxgBshgJEgKdYxhNIgEA0BkB2BkB&ae=1&num=1&cid=CAQShwIAQM4h3AxiSjm7ysTb6T47Y2epU9C_SUF-AmlltH0-s-VHqLtimR6sZ_wP8ZmOBpmT6Q8ux3p6ngm5KXgK73fABxMeMpp1Jnw6yJVsgXwkhSppkguTTdQcGu7aX_qw1Gx7KYBc3GQA-MOSfvdnC5TrIe4uIGHg6qWM6GPFA7oQiWkUrWD_8wNUV4aZxCcnCRYwSKeykARp5iCD1Xl-gboiajIOxEnjQvxykve-_CQvUpQhVqZJyjRjQhx7J947efKAYKtk-rMa_zITm96_Fy7c_UIO33H9ve9z1gVIlMo-TWtxBO3knbgzBDumQYom-LDfBZsXtzGeX6NpioyMSody-1HhnhGrERgB&sig=AOD64_2nqfD8lEROtKe18IHY_ZG5yLK6ZA&dbm_c=AKAmf-AfbCp53w-dsBlG4eQtaRqQWRD2sTT8z6IVxIiPs1TZOIEp1Y3_9W7Wu1z0poAhGrGPGuY1_KGwonAn82zj67ODKk_JFP1qRh6fitkEcikhiRM4XjDZaHsGxtCe4OgRvbeU1ENZd4-I3A0sv5-AjFXgp576zSBIMIyVyk-M9K3kfXInjRHxEQW7k79oRpGWqCaML0a4zdAa4kBHdJy4CIGW-_kV4UIk0ZkInT0Qw8Lg2jMlSs069KyYi9lxSe8O_mCUCU7Rqk3Kbp4cyirENSykWqC8Wj7VJ_lF88SGA4O4yEh9E5LSsPrUMhAyQHFWyWHIy2zM&cry=1&dbm_d=AKAmf-Bdohnsun5rqkdbVhSKb1RCEpm9VPkYW3uuHncfG7ml-7LyIePOHOTAb5nkxJcJLf_CL0JpttxhDUDxP8ma9AGoB9Nnanq-VFBMoyKTtbHVSHSU83evxj-S9bgyASkX3o9lkFpkyqH6l5tEstdVpxldtBhextCbumyM8EjIj0L8IGnhb8ZxlFVxPvNjTJq4KjIsVxFQ9fvwOJL-WhzLq0BO6M5ASLZ4D1HnEKZI73thzsfbezrW3xWYXc-9VTs5czCS9npQM57f9HcUJ1F9vaPPyaHVvCcGgdrytj4KtzQIJ2BjbOeyhPHmJPjxkHPaEaTxBUZmtsTaT16BT6TxjUUloOkE7AZstLdsvMBgUJwMx57SwlW4MzboHsEaBB04q6YtVOtw4kJVQJAsKBk0c3Fk_u44yupGIUQKN2K72OhMnaLg-MwvEJ5DljjkL4jzCvt4cTEqh0Vrc4TMCVe1haYK6pAenw1YrDXpC_yiawRC4oVRPGLvX4rvtFAlgEjUjlVdJfZEEX5OSz3xnRXXoECyor45jOzFbnzVyjyY7p76CeBk2R8IClrE1I-m3eNthJg6uYLOyi_okIqI2oDU4XAr67wdU_Uas1k4OTFju1uLoq8BrTcN84T55Dtfvv-VFWBD9oyZ97-RQdjHBFhR8heA99tHc99VqoC3N2hXK89xab0izoJTXs2Y8tGi6d6rGRKkQfEikdGlL-VDjDJMdEnY6AaZgh-FIhCf1EIaB7Nunad25HPyAW3wra0ywPjBUzrww8HM&adurl=https://servedby.flashtalking.com/click/7/296969;10262637;4919222;210;0/?us_privacy=!!US_PRIVACY!&ft_partnerimpid=ABAjH0i74MI_i9ZJ_MKuyf4Eni5K&ft_impID=4DB6DF2A-BF49-9B55-B078-52C9FCEBA3A6&ft_section=21988411112&g=686889E49E9313&random=965780.4790484989&ft_width=160&ft_height=600&url=https://www.adobe.com/in/creativecloud.html?sdid=PC1PQ9XF&mv=display&mv2=display
                  - img "Click Here" [ref=f13e19]
                - link [ref=f13e21]:
                  - /url: https://www.flashtalking.com/consumer-privacy
                  - img "AdChoices arrow" [ref=f13e22]
                - link "Privacy Notification" [ref=f13e24]:
                  - /url: https://www.flashtalking.com/consumer-privacy
    - contentinfo [ref=e84]:
      - generic [ref=e86]:
        - generic [ref=e87]:
          - text: "\"@ 2016\""
          - link "Automation Testing" [ref=e88]:
            - /url: "#"
          - text: "\"All Rights Reserved.\""
        - generic [ref=e89]:
          - link "" [ref=e90]:
            - /url: https://www.facebook.com/automationtesting2016/
          - link "" [ref=e92]:
            - /url: https://twitter.com/krishnasakinala
          - link "" [ref=e94]:
            - /url: https://www.linkedin.com/nhome/?trk=hb_signin
          - link "" [ref=e96]:
            - /url: https://plus.google.com/105286300926085335367
          - link "" [ref=e98]:
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
> 45 |   await mainPage.goto('https://demo.automationtesting.in/Windows.html');
     |                  ^ Error: page.goto: Test timeout of 30000ms exceeded.
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