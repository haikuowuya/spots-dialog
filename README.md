# Spots  progress dialog

[![Maven](https://img.shields.io/badge/maven-0.1-brightgreen.svg)](http://search.maven.org/#artifactdetails%7Ccom.github.d-max%7Cspots-dialog%7C0.1%7Caar)
[![Blog Post](https://img.shields.io/badge/blog-post-yellow.svg)](http://dybarsky.blogspot.com/2015/01/spots-progress-dialog.html)

Android AlertDialog with mowing spots progress indicator packed as android library.

![Example Image1][1]

===========

###Usage

The library available in maven central repository. You can get it using:
```groovy
dependencies {
    compile 'com.github.d-max:spots-dialog:0.1+@aar'
}
```
Javadoc and sources package [classifiers][3] available too.

**Note:** The library requires minimum API level 15.

[SpotsDialog][4] class is an inheritor of a AlertDialog class. You can use it just like simple [AlertDialog][5]. For example: 
```java
AlertDialog dialog = new SpotsDialog(context);
dialog.show();
...
dialog.dismiss();
```
===========

###Customization

Use android styles to customize the dialog.
Next custom attributes provided:
* DialogTitleAppearance : style reference
* DialogTitleText : string
* DialogSpotColor : color
* DialogSpotCount : integer

**For example:**

Provide you own style resource:
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <style name="Custom" parent="android:Theme.DeviceDefault.Dialog">
        <item name="DialogTitleAppearance">@android:style/TextAppearance.Medium</item>
        <item name="DialogTitleText">Updating…</item>
        <item name="DialogSpotColor">@android:color/holo_orange_dark</item>
        <item name="DialogSpotCount">4</item>
    </style>
</resources>
```

Pass it into constuctor:
```java
new SpotsDialog(context, R.style.Custom).show();
```

Result:

![Example Image1][2]

===========

###Release notes

**[v0.1, Jan 15th 2015][6]**
* Style customization

===========

###Developed By

Maxim Dybarsky - http://d-max.info

===========

###License

	The MIT License (MIT)
	Copyright © 2015 Maxim Dybarsky

	Permission is hereby granted, free of charge, to any person obtaining a copy
	of this software and associated documentation files (the “Software”), to deal
	in the Software without restriction, including without limitation the rights
	to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the Software is
	furnished to do so, subject to the following conditions:

	The above copyright notice and this permission notice shall be included in
	all copies or substantial portions of the Software.

	THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
	THE SOFTWARE.


[1]: http://3.bp.blogspot.com/-l1UvVWiMSAg/VLa5ZfW4dDI/AAAAAAAANTc/rsWou_qb0Bc/s320/Y6HaTSw.gif
[2]: http://1.bp.blogspot.com/-GVktyphQy4U/VLa5jqIF2MI/AAAAAAAANTk/SCtC58KAYHI/s320/plYat1p.gif
[3]: http://www.gradle.org/docs/current/userguide/dependency_management.html#sub:classifiers
[4]: library/src/main/java/dmax/dialog/SpotsDialog.java
[5]: http://developer.android.com/reference/android/app/AlertDialog.html
[6]: https://github.com/d-max/spots-dialog/releases/tag/v0.1
