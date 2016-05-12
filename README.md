## Installation

- Compile the project into jar file.
- Copy badger.jar + compiled jar file in to Assets/Plugins/Android folder
- Remove ParsePush.jar if it exists in the Assets/Plugins/Android folder
- Add these line to your AndroidManifest.xml
- 
```xml
  <!-- for Samsung -->
    <uses-permission android:name="com.sec.android.provider.badge.permission.READ" />
    <uses-permission android:name="com.sec.android.provider.badge.permission.WRITE" />

    <!-- for htc -->
    <uses-permission android:name="com.htc.launcher.permission.READ_SETTINGS" />
    <uses-permission android:name="com.htc.launcher.permission.UPDATE_SHORTCUT" />

    <!-- for sony -->
    <uses-permission android:name="com.sonyericsson.home.permission.BROADCAST_BADGE" />

    <!-- for apex -->
    <uses-permission android:name="com.anddoes.launcher.permission.UPDATE_COUNT" />

    <!-- for solid -->
    <uses-permission android:name="com.majeur.launcher.permission.UPDATE_BADGE" />
  ```

## Usage

TODO: Write usage instructions

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

TODO: Write history

## Credits

- ShortcutBadger: https://github.com/leolin310148/ShortcutBadger

## License

TODO: Write license
