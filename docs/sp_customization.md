---
id: sp_customization
title: Customize Your game
---


## Validate your License 

> This section is based on [**Purchase Validation**](/Documentation/docs/purchase_validation) Tutorial , you can get your game key 
if you purchase the source code only from our [Store](https://codecanyon.net/user/b4dnetwork) .

**1**. Get your Key By Following these [**Steps**](/Documentation/docs/purchase_validation)

**2**. Open your game project folder 

![Project sln](https://drive.google.com/uc?id=1nVtB_H7Vp3FlofGnn7d8f8oQpmeJVFX0)

**3**. Go to **Space Rider > scripts > Utils.cs**

![utils.cs](https://drive.google.com/uc?id=1wqXRyauSEdUx1Weavzfryqqc2mk3lbp4)

**4**. Change The Key With the one you get from [Validation Website](https://b4dnetwork.com/Validation/)

**5**. Change The Purchase code with the one you received from **Envato**


## Admob + Unity **ADS** 

**1**. Go to **Space Rider > scripts > Utils.cs**

![utils.cs](https://drive.google.com/uc?id=1oF_TVinZr6qtRrUR6iJDuQKer95E5wLP)

**2**. Replace The **Admob** Ids with your Admob Banner , Interstitial and RewardedVideo

**3**. For **Unity Ads** You need to have your **Unity** Game Id and the **Placement Name**

**4**. If you want to use **Admob** only as an example , you can set `UnityAds = false` .


## **Firebase** RealTime Database

> To be able to use the game **Leader Board** feature , you have to set-up a Firebase project .

**1**. Create a new **Firebase** Project .

![Firebase](https://drive.google.com/uc?id=11fl3FDlt28Z3tkBaCRPK0IjHERkyFAqM)

**2**. Type Your **Project Name** then **Continue** .

![Project Name](https://drive.google.com/uc?id=1aoL8zdhWm_AFenOJEVdRWVi16KLp_EFf)

**3**. Go to **Database** from your **Dashboard** menu .

![Database from menu](https://drive.google.com/uc?id=10VkczfPAKCxBDAPfYRfUvfjEo61U1Pkb)

**4**. **_Scroll DOWN_** And Select **RealTime Database** , Then **Create** Database.

![RealTime database](https://drive.google.com/uc?id=1s5RrXTdEtDnHtuIEckV7gFdMt7f32wp1)

**5**. Click On the **+** icon to create a child 

![Add Child](https://drive.google.com/uc?id=1FnDTkAiEuxc-GwSDQkUnQqDV_ZK6konL)

**6**. Add A child and give it the name **Scores** , and create another child of **Scores** > **Player1** 
and inside **Player1** Create 2 **Child** , **name = Player1** and **score = 10** for example .

> this procedure is just to initialize your database . After That Data will be **Generated Automatically** from your game .

**_Finally your database should look like this , then press Add_**.

![Result](https://drive.google.com/uc?id=1NKs-hxkinbj5RHmS1SHVSTn4nlPnC87l)

![Result](https://drive.google.com/uc?id=11RwlP4L4THo85tEcdhMCgpFdS0QcKa-m)

**7**. Select **Rules** from the menu above .

![Rules](https://drive.google.com/uc?id=1ifudd_ACwn56OQmb6V6gUc_S-ATFo-V-)


> Copy this bloc of code and , past it in your **Firebase Rules** 
```json
{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null",
    "scores" : {
      ".indexOn" : "score"
    }
  }
}
```

Finally press publish to update your **Database Rules**

![publish rules](https://drive.google.com/uc?id=1WA2pG97PyQo2y1Vey7IPG0ttsId3gNp5)


**8.** **Enable Anonymous Authentication** , From the menu select **_Authentication_** .

![Authentication](https://drive.google.com/uc?id=11zULgPFGg5IPNQ-MzXZ_9aqY66ahHOiv)
![Anonymous auth](https://drive.google.com/uc?id=15tyfeWOR9xQQsx_QS5YmZ7sYWZrS_AQX)


> **Congratulations !!**  Your database is ready to be **Linked With your Game**

> The final Step is To copy your Database URL and your Project **API Key**

**Firebase realTime Database URL**

![fb url copy](https://drive.google.com/uc?id=1Q_VjPN1fecEKdxjqQuMtLqyfl38qaUw8)

![fb url paste](https://drive.google.com/uc?id=1sGmZPoicx6D3SFf3Ibnaf3LoiFG2ys92)

<br/>
<br/>
<br/>

**Firebase API Key**

![fb api copy](https://drive.google.com/uc?id=1PNXjnUAdaQIEjlP3W3WCh0BQvxViON4G)

![fb api paste](https://drive.google.com/uc?id=1IGLwqsBo-n0cMXJu9rGLrFbQn81UibOi)

> That's it 😊 , Your Game Is Ready For A build .
