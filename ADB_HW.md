 ## Android Debug Bridge (ADB)

 #### 1. Display the device connected in the console
```
.\adb devices
```
<div style="display:flex;">
<img src="Screens/Adb_devices.jpg">
</div>
 
 #### 2. List address of todolist app in the Android system
 ```
.\adb shell 'pm list packages -f' | findstr list
```
<div style="display:flex;">
<img src="Screens/Adb_findstr.jpg">
</div>
 
 #### 3. Install .apk file of todolist app to the device from the laptop using ADB
```
.\adb install D:\Daria_HW\TodoList.apk
```
<div style="display:flex;">
<img src="Screens/Adb_install.jpg">
</div>
 
 #### 4. Take a screenshot of the opened todolist app and copy it to the laptop by one command 
```
.\adb shell screencap /storage/emulated/0/DCIM/todolist.png
```
<div style="display:flex;">
<img src="Screens/adb_shell_screencap.jpg">
</div>

```
.\adb pull /storage/emulated/0/DCIM/todolist.png todolist.png
```
<div style="display:flex;">
<img src="Screens/adb_pull.jpg">
</div>

 #### 5. List logs of todolist app to console
```
.\adb logcat -d | findstr com.android.todolist 
```

 #### 6. Copy logs of todolist app to the laptop
```
.\adb logcat -d | findstr com.android.todolist > todolist2.log
```
<div style="display:flex;">
<img src="Screens/Adb_logcat.jpg">
</div>
 
 #### 7. Delete todolist app from the device using ADB
 ```
.\adb uninstall com.android.todolist
```
<div style="display:flex;">
<img src="Screens/Adb_uninstall.jpg">
</div>
