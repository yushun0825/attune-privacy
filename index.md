# Attune プライバシーポリシー

最終更新日: 2026年10月1日

Attune(以下「本アプリ」)は、あなたの体調と環境の関係を可視化する個人向けアプリです。
本アプリは**あなたの健康情報を開発者に送信しません**。この方針は機能上の制約ではなく、設計上の前提です。

---

## 1. 開発者が受け取る情報

**ありません。**

本アプリには開発者が運営するサーバーが存在しません。アカウント登録もありません。
利用状況の解析ツール(アナリティクス)、広告SDK、クラッシュレポート収集ツールのいずれも組み込んでいません。
したがって、あなたが記録した内容・ヘルスケアのデータ・位置情報を開発者が閲覧・取得することはできません。

## 2. 本アプリが扱う情報と、その保管場所

| 情報の種類 | 取得元 | 保管場所 |
|---|---|---|
| 気分・症状・水分/カフェイン/飲酒・食事・服薬・サプリ・仮眠・トイレの記録、1日のふりかえり | あなたの手入力 | この端末内、およびあなた自身のiCloud |
| 移動・滞在した場所(自動記録をオンにした場合のみ) | 位置情報 | 同上 |
| 睡眠(時間・ステージ・呼吸の乱れ)・心拍・心拍変動・安静時心拍・歩数・消費エネルギー・呼吸数・手首皮膚温・ワークアウト・血中酸素・血糖・体組成・栄養・服薬・月経周期・心電図・メンタルヘルスの質問票、および生年月日・生物学的性別・身長・体重 | ヘルスケア(HealthKit) | **この端末内のみ**(iCloudには保管しません) |
| 気圧・気温・湿度・天気・大気質(PM2.5)・紫外線 | Open-Meteo(気象API) | 同上 |
| 食事の写真から読み取った料理名・成分表の文字 | カメラ | **この端末内のみ**。写真は保存も送信もしません |
| 移動手段(徒歩・自転車・乗り物)の判定 | モーションとフィットネス | この端末内、およびあなた自身のiCloud |
| 1日のふりかえりに添えた写真 | あなたが選んだ写真 | この端末内(長辺1200pxに縮小)、およびあなた自身のiCloud |
| アプリの設定 | あなたの操作 | この端末内、およびあなた自身のiCloud |

## 3. iCloudでの同期について

本アプリは、あなたが記録した内容をAppleのiCloud(CloudKitのプライベートデータベース)に保管し、
同じApple Accountの端末間で同期します。これはあなた自身のiCloud領域であり、**開発者はその内容にアクセスできません**。
同期はiCloudにサインインしている場合に自動的に行われ、アプリ内でアカウントを作る必要はありません。

なお、**ヘルスケア由来のデータはiCloudに保管しません**。これはAppleの開発者規約に従った措置です。
基礎情報(生年月日・生物学的性別・身長・体重)をヘルスケアから読み取って初期値に使う場合も、
読み取った値はこの端末の中だけに保持します。あなたが自分で入力し直した値だけが、
アプリの設定としてiCloudに同期されます。

## 4. 位置情報の利用

- **現在地(おおよその位置)**: 気圧・天気を取得するために使用します。市区町村レベルの粗い精度で取得し、後述のとおり気象APIへ座標を送信します。
- **移動と場所の自動記録**: 設定でオンにした場合のみ、滞在した場所と移動を自動的に記録します。この記録はタイムラインに「自動」と表示され、いつでも削除できます。オフのままにしても、本アプリの他の機能はすべて利用できます。

位置情報の利用を許可しない場合、天気の表示は東京の値で代替され、その旨が画面に明示されます。

## 4-2. Siri と端末内検索(Spotlight)

症状の記録を、この端末の Spotlight の索引に入れています。ホーム画面の検索や Siri から
「先週いつ頭痛だったか」を辿れるようにするためです。

- 索引に入れるのは**症状の種類・強さ・日付**だけです。**あなたが書いたメモは入れません**
  (索引はロック画面の候補にも表示されるため)
- 索引はこの端末の中だけのもので、**外部にも開発者にも送信しません**。iCloud でも同期しません
- 設定 >「Siri と検索に出す」でいつでも切れます。切った時点で索引から削除します

## 4-3. 文章の生成(端末内、任意で Apple の Private Cloud Compute)

「今日の要約」「今日のアドバイス」「自分のデータに聞く」の文章は、**既定ではこの端末の中で**生成します。記録は外に出ません。

設定 >「より詳しい文章を Apple のクラウドで作る」を**あなたがオンにしたときだけ**、
「自分のデータに聞く」の答えと「今日のアドバイス」を Apple の Private Cloud Compute で生成します。
そのとき送られるのは、**アプリが計算した事実の文**(例:「昨夜の睡眠時間: 5.4時間」)と、質問文、
助言の候補の文(アプリに入っている、出典つきの一般的な助言)だけで、記録そのものは送られません。Private Cloud Compute の扱いは Apple の規定に従い、開発者はその内容にアクセスできません。
既定はオフで、いつでも切れます。

## 5. 外部サービスへの送信

本アプリが開発者のサーバーに何かを送ることはありません。外部への通信は次の2つです。

**気象と大気の情報の取得**(常に)

- **送信先**: Open-Meteo(https://open-meteo.com)
- **送信する内容**: おおよその緯度・経度
- **送信しない内容**: 氏名、メールアドレス、端末ID、健康に関する記録、その他あなたを特定しうる情報

**場所の名前の検索**(「移動と場所の自動記録」をオンにした場合と、場所を手で記録・編集するとき)

- **送信先**: Apple の地図サービス(MapKit)
- **送信する内容**: その地点の緯度・経度
- **目的**: 滞在した場所の施設名・住所を調べ、タイムラインに名前を出すため
- **送信しない内容**: 氏名、メールアドレス、健康に関する記録。Apple での扱いは Apple のプライバシーポリシーに従います

このほか、iCloud での同期(3.)と、任意の Private Cloud Compute(4-3.)は Apple のサービスを使います。

## 6. Appleでサインイン(任意)

Appleでサインインすると、書き出したバックアップファイルに「持ち主の目印」が付き、復元時に自分の記録であることを確認できます。
サインインしなくても、本アプリのすべての機能を利用できます。
取得する情報は氏名(任意)とAppleが発行する識別子のみで、いずれも**この端末のキーチェーンにのみ保存**され、外部に送信されません。

## 7. あなたの権利と操作

- **書き出し**: 設定 → アカウントとデータ → バックアップを書き出す で、すべての記録を1つのファイルとして取り出せます。
- **削除**: 設定 → アカウントとデータ → すべての記録を削除 で、記録とサインイン情報を消去できます。iCloud同期をしている場合、他の端末からも削除されます。
- **アプリの削除**: 端末からアプリを削除すると、端末内の記録も削除されます。iCloud上のデータを完全に消すには、削除の前に上記の「すべての記録を削除」を実行してください。
- **ヘルスケアの許可の取り消し**: ヘルスケアApp → プロフィール → プライバシー → App → Attune から、いつでも変更できます。

## 8. 子どものプライバシー

本アプリは13歳未満の子どもを対象としておらず、子どもから意図的に情報を収集することはありません。

## 9. 医療に関する注意

本アプリは医療機器ではありません。表示される分析・スコア・ヒントは診断・治療・予防を目的としたものではなく、
一般的な健康情報と、あなた自身の記録から見出した統計的な関連を示すものです。
体調に不安があるときは医療機関にご相談ください。

## 10. 本ポリシーの変更

内容を変更する場合は、本ページの最終更新日を改めます。重要な変更がある場合はアプリの更新情報でお知らせします。

## 11. お問い合わせ

本ポリシーおよび本アプリのプライバシーに関するお問い合わせ先:

- メール: yushun0825.o@gmail.com

---

# Attune Privacy Policy

Last updated: October 1, 2026

Attune helps you see how your body responds to your environment. **It does not send your health information to the developer.** That is a design premise, not a limitation.

## 1. What the developer receives

**Nothing.**

There is no developer-operated server and no account to create. The app contains no analytics, no advertising SDKs, and no crash-reporting services. The developer cannot see or retrieve anything you log, any Health data, or your location.

## 2. What the app handles, and where it is stored

| Data | Source | Stored |
|---|---|---|
| Mood, symptoms, drinks (water/caffeine/alcohol), meals, medication, supplements, naps, bathroom visits, daily review | Your input | On this device and in your own iCloud |
| Trips and places visited (only if auto-recording is on) | Location | Same as above |
| Sleep (duration, stages, breathing disturbances), heart rate, HRV, resting heart rate, steps, active energy, respiratory rate, wrist temperature, workouts, blood oxygen, blood glucose, body composition, nutrition, medication, cycle tracking, ECG, mental-health questionnaires, and date of birth, biological sex, height and weight | Health (HealthKit) | **On this device only** — never in iCloud |
| Air pressure, temperature, humidity, weather, air quality (PM2.5), UV | Open-Meteo | Same as above |
| Dish names and label text read from a photo of a meal | Camera | **On this device only.** Photos are never saved or sent |
| Travel mode (walking, cycling, in a vehicle) | Motion & Fitness | On this device and in your own iCloud |
| A photo attached to a daily review | A photo you choose | On this device (downscaled to 1200px on its long edge) and in your own iCloud |
| App settings | Your choices | On this device and in your own iCloud |

## 3. iCloud sync

Your records are stored in Apple's iCloud (CloudKit private database) and synced across devices signed in to the same Apple Account. This is your own iCloud storage; **the developer cannot access its contents**. Sync happens automatically when you are signed in to iCloud — there is no account to create in the app.

**Health-derived data is never stored in iCloud**, in accordance with Apple's developer agreement.
When your date of birth, biological sex, height or weight is read from Health to prefill your profile,
that value is kept on this device only. Only a value you type in yourself is synced to iCloud as an app setting.

## 4. Location

- **Approximate current location**: used to fetch air pressure and weather. Collected at a coarse (city-level) accuracy and sent to the weather API as described below.
- **Auto-recording trips and places**: only when you turn it on in Settings. These entries are marked "Auto" in your timeline and can be deleted at any time. Leaving it off does not limit any other feature.

If you decline location access, weather falls back to Tokyo, and the app states this on screen.

## 4-2. Siri and on-device search (Spotlight)

Your symptom records are added to this device's Spotlight index, so that Siri and the Home Screen
search can answer questions such as "when did I last have a headache".

- Only the **symptom, its severity and the date** are indexed. **Your notes are never included**,
  because the index can surface in Lock Screen suggestions
- The index stays on this device. It is **never sent anywhere, including to the developer**, and is not synced through iCloud
- You can turn it off at any time in Settings › Show in Siri and Search. Turning it off deletes the index straight away

## 4-3. Text generation (on device; Apple's Private Cloud Compute is optional)

The text in "Today's summary", "Today's advice" and "Ask my data" is generated **on this device by default**. Your records do not leave it.

Only if **you** turn on Settings › "Write more detailed answers with Apple's cloud" are the answers in "Ask my data"
and "Today's advice" generated with Apple's Private Cloud Compute. What is sent then is the question, the **facts the app computed**
(for example "Last night's sleep: 5.4 hours") and the candidate tips (general, cited tips built into the app), never your records themselves. Private Cloud Compute is governed by
Apple's terms; the developer cannot access its contents. It is off by default and can be turned off at any time.

## 5. Data sent to outside services

The app never sends anything to the developer's servers. There are two kinds of outbound request.

**Weather and air-quality data** (always)

- **Recipient**: Open-Meteo (https://open-meteo.com)
- **Sent**: approximate latitude and longitude
- **Never sent**: name, email, device identifiers, health records, or anything else that could identify you

**Place-name lookup** (when "automatic places and trips" is on, and when you log or edit a place by hand)

- **Recipient**: Apple's map service (MapKit)
- **Sent**: the latitude and longitude of that spot
- **Purpose**: to find the venue name or address of the place you stayed, so the timeline can show a name
- **Never sent**: name, email, or health records. Apple handles the request under Apple's privacy policy

In addition, iCloud sync (section 3) and the optional Private Cloud Compute (section 4-3) use Apple's services.

## 6. Sign in with Apple (optional)

Signing in stamps exported backups with an owner marker so a restore can confirm the records are yours. Every feature works without signing in. The app requests only your name (optional) and Apple's identifier; both are stored **only in this device's Keychain** and are never transmitted.

## 7. Your controls

- **Export**: Settings → Account & Data → Export Backup writes all records to a single file.
- **Delete**: Settings → Account & Data → Delete All Records erases your records and sign-in. With iCloud sync on, they are removed from your other devices too.
- **Deleting the app** removes the on-device copy. To also clear iCloud, use "Delete All Records" before deleting the app.
- **Revoking Health access**: Health app → Profile → Privacy → Apps → Attune.

## 8. Children's privacy

Attune is not directed at children under 13 and does not knowingly collect information from them.

## 9. Medical notice

Attune is not a medical device. Its scores, insights, and tips are not intended to diagnose, treat, or prevent any condition; they present general health information and statistical associations found in your own records. If you are concerned about your health, please consult a medical professional.

## 10. Changes to this policy

Any change is reflected in the "Last updated" date above. Significant changes will be noted in the app's release notes.

## 11. Contact

- Email: yushun0825.o@gmail.com
