## Installation

- Assume that your Unity project has Parse setup and installed.
- Compile the project into jar file.
- Copy badger.jar + compiled jar file in to Assets/Plugins/Android folder.
- Remove ParsePush.jar if it exists in the Assets/Plugins/Android folder.
- Add these lines to your AndroidManifest.xml.
  
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

- Badge number will automatically increased when it received notification.
- To reset badge number, use these codes in your Unity script.
```cs
#if UNITY_ANDROID && !UNITY_EDITOR        

        using (AndroidJavaClass pluginClass = new AndroidJavaClass("com.parse.ParsePushUnityHelper"))
        {
            if (pluginClass != null)
            {
                pluginClass.CallStatic("ResetBadgeNumber");    
            }
        }
        
#endif
```

## Credits

- ShortcutBadger: https://github.com/leolin310148/ShortcutBadger
- ParsePush Native Android: https://github.com/ParsePlatform/Parse-SDK-dotNET/tree/master/ParsePush/Native
