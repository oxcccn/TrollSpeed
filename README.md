# TrollSpeed
Shows upload &amp; download speed below the status bar. Based on opa334’s TrollStore.

## How it works?
[TrollStore](https://github.com/opa334/TrollStore) + [UIDaemon](https://github.com/limneos/UIDaemon) + [NetworkSpeed13](https://github.com/lwlsw/NetworkSpeed13) + (some magic)
\=

  - An TrollStore app to spawn HUD process with root privilege.
  - Don’t call `waitpid` to that process. Let it go.
  - A HUD app with entitlements from `assistivetouchd` to display and persist global windows.

## How to build?
  - Use [theos](https://github.com/theos/theos) to compile.  
  - Wrap and archive generated `.app` bundle into a `.tipa`.

## Caveats
  - Spawn with root privileges is **required**. Otherwise, the HUD process will be killed by SpringBoard when unlocking device.
  - You have to “Exit HUD” manually from the app before uninstall it.

## Screenshot
![screenshot](https://user-images.githubusercontent.com/5410705/213263734-1ef1b553-88d4-41cc-856e-891ea08d185c.jpeg)
