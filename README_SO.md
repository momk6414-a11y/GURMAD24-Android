# GURMAD 24 — Android wrapper (Demo)

Mashruucan waa Android Studio project loogu diyaariyey in website-ka GURMAD 24 lagu furo app Android ah.

- App ID: `com.gurmad24.app`
- URL: `https://gurmad24.onrender.com`
- Nooc: Demo wrapper; wuxuu u baahan yahay internet.
- Ma laha offline database ama adeegyo dispatch dhab ah.
- Ma jiro APK hore loo dhisay oo ku jira ZIP-kan.

## Sida APK loo dhiso
1. Ku rakib Android Studio kombiyuutar leh Android SDK.
2. Ka fur folder-kan Android Studio: `GURMAD24_Android_Wrapper`.
3. Sug Gradle Sync inuu dhammaado.
4. Dooro **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. APK-ga debug wuxuu ka muuqanayaa `app/build/outputs/apk/debug/app-debug.apk`.

## Tijaabo
- Ku tijaabi Android emulator ama taleefan tijaabo ah.
- Hubi in website-ku furmayo iyo in navigation-ku shaqaynayo.
- Ka hor daabacaad, samee signing release, privacy review, iyo tijaabo amni.

APK-kan marka la dhiso wuxuu soo bandhigayaa website-ka hadda yaalla Render. Isbeddelada website-ka ayaa ka muuqan kara app-ka marka internet jiro.

## Dhisid otomaatig ah (GitHub Actions)
Mashruucu wuxuu wataa workflow ku jira `.github/workflows/android-apk.yml`.
Marka folder-kan lagu daro repository-ga GitHub ee GURMAD24, kadibna `main` loo push-gareeyo, GitHub Actions ayaa dhisaya APK debug ah. Waxa kale oo gacanta looga bilaabi karaa tab-ka **Actions** adigoo dooranaya **Build GURMAD 24 Android APK** kadib **Run workflow**.

Marka workflow-gu guuleysto: fur run-ka → **Artifacts** → `GURMAD24-debug-apk` si aad u hesho `app-debug.apk`.

**Xaaladda hadda:** APK binary lama dhisin gudaha deegaanka shaqadan, sababtoo ah Android SDK iyo Gradle ma rakibna. Workflow-ga kore ayaa dhismaha ku fulinaya GitHub-hosted runner leh Android SDK.

## Isku-darka nooca HTML ee la bixiyey
Noocan wuxuu ku daraa `GURMAD24_Digital_Platform.html` gudaha Android app-ka
(`app/src/main/assets/index.html`). App-ku wuxuu furi karaa interface-ka demo-ga
xitaa marka internetku go'an yahay. Xogta demo-ga browser-ka (localStorage) waxay
ku kaydsan tahay qalabka, mana la mid aha database-ka server-ka.
APK-ga weli waa in lagu dhisaa Android SDK/Gradle; ZIP-kan waa source package.
