adb shell am broadcast 后面的参数有：  
```
[-a <ACTION>]  
[-d <DATA_URI>]  
[-t <MIME_TYPE>]   
[-c <CATEGORY> [-c <CATEGORY>] ...]   
[-e|--es <EXTRA_KEY> <EXTRA_STRING_VALUE> ...]   
[--ez <EXTRA_KEY> <EXTRA_BOOLEAN_VALUE> ...]   
[-e|--ei <EXTRA_KEY> <EXTRA_INT_VALUE> ...]   
[-n <COMPONENT>]  
[-f <FLAGS>] [<URI>]
```

adb shell am broadcast -a com.android.test --es test_string "this is test string" --ei test_int 100 --ez test_boolean true