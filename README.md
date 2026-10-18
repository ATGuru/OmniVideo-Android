# OmniVideo Android

Phone client for the OmniVideo board. The board is a separate project: https://github.com/ATGuru/OmniVideo

This repository is only the Android app. The phone does not run the models.

Copyright (c) 2026 Guru Morgan, AllTechGuru. See LICENSE.
Do not use, copy, modify, or run this software without written permission.

The screen is six full-width tabs: Generate audio, Transcribe audio, Master, Stills, Clips, and Render Video. Portrait and landscape both use those tabs.

```bash
flutter pub get
flutter run
```

The app calls the desktop board at `http://100.67.76.16:8080`, direct, with no HTTP proxy. That address is compiled in, and the screen has no server field. If that port answers HTTP 408, the app retries `http://100.67.76.16:18080`. Cleartext HTTP is allowed.

Create or open a named project before generating. The board stores those folders in `~/OmniVideo/Projects` unless it is started with `OMNIVIDEO_PROJECTS` set to the folder the phone's file app already browses.
