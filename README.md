# MioNext App Customer Experience Project

![demoImage](https://user-images.githubusercontent.com/10300848/212829134-8783176f-fe7f-41c9-a3c1-d2747321994e.png)

## 一、簡介

為了讓 MioNext App 可以更有效的與使用者進行互動並在未來建立可觀的 User Database，此項目透過整合了以下幾個工具來達成 MioNext 對使用者數據的主動與被動數據搜集與分析。

- 主動工具
  - [OneSignal](https://onesignal.com/)
    - 主流推播工具之一。
    - 對使用者推播問卷，主動對使用者進行數據搜集。
- 被動工具
  - [Google Analytics for Firebase](https://firebase.google.com/docs/analytics)
    - 原 Firebase Analytic 現改名 Google Analytics for Firebase，主流數據搜集工具。
    - 設置 Events 於 App 中，並在 App 背景中對使用者的操作進行被動數據搜集。
- 問卷工具
  - [SurveyCake](https://www.surveycake.com/)
    - 主流線上問卷工具之一。
    - 透過 OneSignal 服務推播問卷至 App 中達成主動對使用者數據搜集。

> 註：本項目僅展示主要的數據搜集規格與模式，並用做項目 POC 展示所使用，非 MioNext 正式 App

#### 整體架構：

- [OneSignal & SurveyCake Integration Sequence Diagram](https://www.figma.com/file/4jPXqQIToo5NScE4yCZ1fq/N712-B2C_UX-Research?node-id=679%3A4469&t=KDQ82RW8c1tboUj3-4)

#### 支持功能：

1. 在 App 中接收 OneSignal 於 Dashboard 中設置的 Push Notification
2. 在 App 中操作完某個 Function 後傳送 Data Tags 至 OneSignal Dashboard
3. 在 App 中接收 OneSignal 於 Dashboard 中設置的 IAM (In-App Message)
4. 將 SurveyCake embedded 至 OneSignal IAM 中並推送至 App 中
5. 將 App 已設置的 Events 傳送至 Google Analytic Dashboard 中

#### 編譯環境：

- iOS 14+
- Android 10+

## 二、效果展示

**OneSignal Push Notification Demo**
<img src="https://user-images.githubusercontent.com/10300848/212827696-00c7bafd-bd92-4d00-968f-4095ab3cb2a6.png">

**OneSignal In-App Message Demo**
<img src="https://user-images.githubusercontent.com/10300848/212827977-441c36e9-d237-468c-a440-3228b6fd5ce1.png">

**OneSignal In-App Message + SurveyCake Demo**
<img src="https://user-images.githubusercontent.com/10300848/212837296-6d95ea0c-e717-451a-a40e-c47667de855c.png">

## 三、OneSignal 機制說明

本項目僅使用了 OneSignal SDK Methods 中的 sendTag(s)、addTrigger(s)、setNotificationOpenedHandler 來達成上述的 [功能](#支持功能)。此章節僅初步解釋使用的方式，以及如何達成使用者數據搜集之目的。若需更多 SDK 或 API 資訊，請參考 [OneSignal 官方文件](<(https://documentation.onesignal.com/docs)>)。

**3.1 sendTag(s)**

## 四、安裝 (🚧 WIP)

- [原始碼下載](https://github.com/weichiangko/mionext-cx-app/releases)
- [安裝方式](https://github.com/weichiangko/mionext-cx-app)

> 可參考 Repo 內的 README 指示進行安裝。
