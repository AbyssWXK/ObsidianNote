  获取radioManager服务
```java
RadioManager radioManager =  
        (RadioManager) SettingApplication.getContext().getSystemService(Context.RADIO_SERVICE);
```

获取模块列表，一个设备可能有多个收音机模块
```java
List<RadioManager.ModuleProperties> mModules = new ArrayList<>();  
radioManager.listModules(mModules);
```
根据模块获取收音机控制器
```java
RadioManager.ModuleProperties module = null;  
for (RadioManager.ModuleProperties mp : mModules) {  
    LogUtils.d(TAG, "ModuleProperties " + mp);  
    LogUtils.d(TAG, "ModuleProperties " + mp.getImplementor());  
    module = mp;  
}  
RadioTuner mRadioTuner = radioManager.openTuner(module.getId(), null /*config*/, true,  
        mCallback , null /* handler */);
```
需求仅关闭收音机
```java
mRadioTuner.setMute(true);  
```