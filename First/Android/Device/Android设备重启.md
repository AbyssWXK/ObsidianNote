```java
Intent reboot = new Intent(Intent.ACTION_REBOOT);
                reboot.putExtra("nowait", 1);
                reboot.putExtra("interval", 1);
                reboot.putExtra("window", 0);
                sendBroadcast(reboot);
```
需要[[系统权限]]