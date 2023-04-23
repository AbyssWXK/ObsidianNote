```java
Intent reboot = new Intent(Intent.ACTION_REBOOT);
                reboot.putExtra("nowait", 1);
                reboot.putExtra("interval", 1);
                reboot.putExtra("window", 0);
                sendBroadcast(reboot);
```
需要[系统权限](obsidian://open?vault=First&file=Android%2FPermission%2F%E7%B3%BB%E7%BB%9F%E6%9D%83%E9%99%90)