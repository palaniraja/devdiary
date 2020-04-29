### Packaging jQuery Mobile app & iOS7+ Statusbar

iOS7+ statusbar overlapping the content is always an issue when packaging webapps with Cordova. 

#### Install cordova statusbar plugin

```
cordova plugin add org.apache.cordova.statusbar
```

#### Change config.xml 

```
<preference name="StatusBarOverlaysWebView" value="false" />
```

#### Light/White statusbar text? 

```
<preference name="StatusBarStyle" value="lightcontent" />
```

#### Change statusbar background color 
```
<preference name="StatusBarBackgroundColor" value="#000000" />
```

