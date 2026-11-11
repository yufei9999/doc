# Privacy Policy for Floatage

Effective date: November 6, 2026
Last updated: November 6, 2026

Floatage ("the App") is a local note-taking app. You write down an item as it occurs to you, then add follow-up notes later, so that each item builds into a timeline of its own. This policy describes what the App actually does with information, and how that information is kept. Please read it before you start using the App.

## 1. What the App stores

Anything you type or dictate into the App is saved on your device, including:

- the title and body of each record (the body is also used to generate the list summary);
- follow-up notes you add to a record, together with their timestamps;
- each record's status flag and whether it is pinned;
- the creation and modification times of records and follow-up notes.

The App also keeps one local backup copy of the previous data, used to recover if the main data file is corrupted (see section 2).

The App does not collect your device model, OS version, device identifiers (IDFV or IDFA), location, contacts, photos, camera, health data or payment information, and it does not log your usage behaviour or navigation paths. Voice input produces no audio file and keeps no recording: only the recognised text is saved, as part of the record.

## 2. Where your information is stored

Records are kept as a JSON file inside the App's own sandbox (Application Support/Floatage), alongside a `.bak` backup copy. When saving, the App writes a temporary file and then replaces the main file atomically, to reduce the risk of corruption if a write is interrupted; if the main file cannot be read, the App tries to restore from the backup.

The App has no server. It does not upload, transmit or sync this content to any cloud service or third party. We cannot view, read or restore your records.

## 3. Network access, export and sharing

The App makes no network requests and uses no server. It contains no networking code, and the built app does not link against Apple's networking frameworks, so your records are never uploaded, transmitted or synced anywhere.

All features work without a network connection, including voice input: speech is recognised on your device, and the recognised text is written only to the local data file. Voice input depends on the system having dictation resources for your language and on system dictation being enabled; if either is missing, voice input is turned off and the App shows a notice that on-device speech recognition is currently unavailable and suggests checking the system dictation settings or using the keyboard. You can then keep typing, and the App never switches to a recognition method that needs a network connection.

The current version has no export or share feature and does not pass content to other apps through the iOS share sheet. If a future version adds one, we will explain it before use and update this policy.

Whether an iOS device backup (iCloud or computer backup) includes the record files in the App's sandbox depends on your system backup settings. That backup is carried out by an Apple system feature and is unrelated to the App.

## 4. System permissions and device access

Voice input is the only feature that needs permission. The first time you tap the voice input button, iOS asks whether the App may use the microphone; depending on the system API the App uses, iOS may also show a speech recognition authorisation request at that point. The App does not request notifications, photo library, camera, location, contacts or health data, and does not access them.

### Microphone and voice input

- What it is for: the App turns what you say into the text of a record, which you can edit before saving. The recognised text is written only to the App's local data file (cards.json); nothing else is created.
- When it is requested: only the first time you use voice input. The App does not open the microphone at launch or in the background, and recording stops as soon as you finish dictating, leave the editor or close the App.
- Audio is neither stored nor sent: the App creates no audio file and keeps no recording. Voice input uses the system's on-device speech recognition, so the audio is processed on your device only — it is not uploaded to Apple's servers or to us, and the recognised text stays in the local data file on your device. This requires dictation resources for your language to be present and system dictation to be enabled; if they are not, voice input is turned off and the App shows a notice that on-device speech recognition is currently unavailable and suggests checking the system dictation settings or using the keyboard. It never falls back to a recognition method that needs a network connection.
- If you decline: every other feature remains available, and you can keep adding and editing records by typing. You can allow the permission later in iOS Settings, or revoke it at any time; voice input will then stop working.

If a future version introduces a feature that needs another authorisation, we will show the standard iOS request before that feature is first used, explain its purpose, and update this policy on this page. You can revoke any permission at any time in iOS Settings; the related feature may then be unavailable.

## 5. Retention and deletion

- Records remain on your device until you delete them.
- You can delete a whole record in the App, or delete an individual follow-up note within a record.
- Deleting the App from your iPhone also deletes the main data file and the backup file in the App's sandbox.
- Deletion cannot be undone. Because the data exists only on your device and the App has no export feature, we cannot restore it for you; please delete with care.

## 6. Third-party SDKs, analytics and advertising

The App includes no third-party SDKs of any kind — no analytics, advertising, attribution or crash-reporting SDKs. It contains no ads, does not track you across apps or websites, does not use IDFA, and does not request App Tracking Transparency authorisation. Whether system-level diagnostics and crash logs are sent to Apple is controlled by your choice under iOS Settings > Privacy & Security > Analytics & Improvements; that is unrelated to the App.

## 7. Children's privacy

The App is not designed for children and does not collect personal information from anyone. Because all records stay in local storage on the device, we never obtain, store or share anything a child writes. If you are a parent or guardian and believe there is an issue, please contact us using the details below.

## 8. Changes to this policy

When this policy changes, we will update the "Last updated" date at the top of this page. If a change affects how your information is handled, we will flag it in the App or in the release notes on the App Store. Continuing to use the App after a change takes effect means you accept the updated policy.

## 9. Contact us

If you have questions about this policy, or wish to exercise any rights relating to your data, please contact us:

- Contact email: yufei.cjn@outlook.com
