ZBarSDKarmv7s
=============

Just a copy of the ZBarSDK that has been recompiled for the armv7s because I'm lazy.

## Integration (taken from the [ZBarSDK website](http://zbar.sourceforge.net/iphone/sdkdoc/install.html))
The recommended installation method is to simply copy the SDK into your Xcode project:

 1. Open ZBarSDK-1.2.dmg in the Finder.

 2. Drag the ZBarSDK folder into your Xcode project. In the dialog that appears, you should choose to copy the SDK into your project by checking the box. The target that you want to link with the library should also be selected in the target list.

 3. Link the following additional frameworks to any targets that link with the ZBarSDK. You should set the first three to use weak references and configure an appropriate deployment target if you still need to support iOS 3:

	- AVFoundation.framework (weak)
	- CoreMedia.framework (weak)
	- CoreVideo.framework (weak)
	- QuartzCore.framework
	- libiconv.dylib

  If you check “Link Binary With Libraries” for the target(s), you should see all of these frameworks followed by libzbar.a.

  Note Link order may be important for some versions of Xcode; the referenced libraries should be listed before libzbar.a in the link order.

 4. Import the SDK header from your prefix header to make the barcode reader APIs available:

    - #import "ZBarSDK.h"

### Note
With the advent of iOS 7, you can use native libraries for barcode scanning now: http://www.infragistics.com/community/blogs/torrey-betts/archive/2013/10/10/scanning-barcodes-with-ios-7-objective-c.aspx
