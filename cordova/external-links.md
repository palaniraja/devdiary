###External links

Tapping any links eg., **http / https / tel:** doesn't work as expected?


####Update config.xml
```
<access origin="*" />
<access origin="tel:*" launch-external="yes" />
```

####Add target blank in links
```
<a href="http://outgoingdomain.com/links/" target="_blank"></a>
```

####Edit MainViewController.m file
```
- (BOOL)webView:(UIWebView *)theWebView shouldStartLoadWithRequest:(NSURLRequest *)request navigationType:(UIWebViewNavigationType)navigationType
{
    NSURL *url = [request URL];
    // Intercept the external http requests and forward to Safari.app
    // Otherwise forward to the PhoneGap WebView
    if ([[url scheme] isEqualToString:@"http"] || [[url scheme] isEqualToString:@"https"]) {
        [[UIApplication sharedApplication] openURL:url]; return NO;
    }
    else {
        return [ super webView:theWebView shouldStartLoadWithRequest:request navigationType:navigationType ];
    }
}
```
