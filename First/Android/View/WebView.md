加载网页方式
[HTML5](obsidian://open?vault=First&file=Android%2FOther%2FHTML5)
```java
mWebView.loadUrl(url);  
//系统默认会通过手机浏览器打开网页，为了能够直接通过WebView显示网页，则必须设置  
mWebView.setWebViewClient(new WebViewClient(){  
    @Override  
    public boolean shouldOverrideUrlLoading(WebView view, WebResourceRequest request) {  
        return super.shouldOverrideUrlLoading(view, request);  
    }  
});
```
[goback](https://blog.csdn.net/qq_20451879/article/details/54316824)
