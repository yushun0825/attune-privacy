# Attune プライバシーポリシー

最終更新日: 2026年7月31日

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
| 睡眠・心拍・心拍変動・歩数・消費エネルギー・呼吸数・手首皮膚温・ワークアウト・水分・カフェイン | ヘルスケア(HealthKit) | **この端末内のみ**(iCloudには保管しません) |
| 気圧・気温・湿度・天気 | Open-Meteo(気象API) | 同上 |
| アプリの設定 | あなたの操作 | この端末内、およびあなた自身のiCloud |

## 3. iCloudでの同期について

本アプリは、あなたが記録した内容をAppleのiCloud(CloudKitのプライベートデータベース)に保管し、
同じApple Accountの端末間で同期します。これはあなた自身のiCloud領域であり、**開発者はその内容にアクセスできません**。
同期はiCloudにサインインしている場合に自動的に行われ、アプリ内でアカウントを作る必要はありません。

なお、**ヘルスケア由来のデータはiCloudに保管しません**。これはAppleの開発者規約に従った措置です。

## 4. 位置情報の利用

- **現在地(おおよその位置)**: 気圧・天気を取得するために使用します。市区町村レベルの粗い精度で取得し、後述のとおり気象APIへ座標を送信します。
- **移動と場所の自動記録**: 設定でオンにした場合のみ、滞在した場所と移動を自動的に記録します。この記録はタイムラインに「自動」と表示され、いつでも削除できます。オフのままにしても、本アプリの他の機能はすべて利用できます。

位置情報の利用を許可しない場合、天気の表示は東京の値で代替され、その旨が画面に明示されます。

## 5. 外部サービスへの送信

本アプリが外部に通信するのは、気象データの取得のみです。

- **送信先**: Open-Meteo(https://open-meteo.com)
- **送信する内容**: おおよその緯度・経度
- **送信しない内容**: 氏名、メールアドレス、端末ID、健康に関する記録、その他あなたを特定しうる情報

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

- メール: (公開前に連絡先を記載してください)

---

# Attune Privacy Policy

Last updated: July 31, 2026

Attune helps you see how your body responds to your environment. **It does not send your health information to the developer.** That is a design premise, not a limitation.

## 1. What the developer receives

**Nothing.**

There is no developer-operated server and no account to create. The app contains no analytics, no advertising SDKs, and no crash-reporting services. The developer cannot see or retrieve anything you log, any Health data, or your location.

## 2. What the app handles, and where it is stored

| Data | Source | Stored |
|---|---|---|
| Mood, symptoms, drinks (water/caffeine/alcohol), meals, medication, supplements, naps, bathroom visits, daily review | Your input | On this device and in your own iCloud |
| Trips and places visited (only if auto-recording is on) | Location | Same as above |
| Sleep, heart rate, HRV, steps, active energy, respiratory rate, wrist temperature, workouts, water, caffeine | Health (HealthKit) | **On this device only** — never in iCloud |
| Air pressure, temperature, humidity, weather | Open-Meteo | Same as above |
| App settings | Your choices | On this device and in your own iCloud |

## 3. iCloud sync

Your records are stored in Apple's iCloud (CloudKit private database) and synced across devices signed in to the same Apple Account. This is your own iCloud storage; **the developer cannot access its contents**. Sync happens automatically when you are signed in to iCloud — there is no account to create in the app.

**Health-derived data is never stored in iCloud**, in accordance with Apple's developer agreement.

## 4. Location

- **Approximate current location**: used to fetch air pressure and weather. Collected at a coarse (city-level) accuracy and sent to the weather API as described below.
- **Auto-recording trips and places**: only when you turn it on in Settings. These entries are marked "Auto" in your timeline and can be deleted at any time. Leaving it off does not limit any other feature.

If you decline location access, weather falls back to Tokyo, and the app states this on screen.

## 5. Data sent to outside services

The only outbound network request is for weather data.

- **Recipient**: Open-Meteo (https://open-meteo.com)
- **Sent**: approximate latitude and longitude
- **Never sent**: name, email, device identifiers, health records, or anything else that could identify you

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

- Email: (add a contact address before publishing)
