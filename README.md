# fw-client-setup-scripts

These scripts aim to automatically setup the working environment on the ElevationFW/ClientApp.

They ask you want to do:
* Run `npm install`?
    * Run `npm install` in forced mode?
* Run linting?
* Run build?

They always redial your `vpn_primavera` at the start to make sure you have it running properly.

**They ALWAYS delete the `dist` folder at startup**. If you need it, select the option to `Run build`.


## ElevationFW

Place the script `setup_fw.bat` inside the ElevationJS folder and run it.

If you select the option to run `npm install` it will automatically delete all `node_modules` on every module and run `npm install` for each one.

Every option choosen will run for **every** module in the following order:

```
1. services
2. localization
3. components
4. search
5. ngcore
6. pushnotifications
7. attachments
8. dashboard
9. extensibility
10. notifications
11. printing
12. qbuilder
13. shell
14. client-app-core
```

The `node_modules` deletion will be faster than deleting from the Windows Explorer.


## ClientApp

Place the script `setup_fw.bat` inside the ClientApp folder and run it.

If you select the option to run `npm install` it will automatically delete the `node_modules` before running `npm install`.

The `node_modules` deletion will be faster than deleting from the Windows Explorer.
