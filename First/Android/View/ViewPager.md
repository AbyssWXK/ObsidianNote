参考[CSND ViewPager和Fragment](https://www.jianshu.com/p/ad810a0bef6b)
ViewPager2禁止滑动
调用setUserInputEnabled方法，设置是否滑动
//true:滑动，false：禁止滑动
java: viewPager2.setUserInputEnabled(false);
kotlin: viewPager2.isUserInputEnabled = false

ViewPager2去除滑动效果
viewPager2.setCurrentItem(position,false)