# SafeCanOpenURL
This repository has an extension you can use that fixes the crash when calling canOpenURL from objc in iOS13

```
extension UIApplication {
	    @objc public func safeCanOpenURL(_ url: URL?) -> Bool {
	        guard let unWrappedUrl = url else {
	            return false
	        }
	
	        return canOpenURL(unWrappedUrl)
	    }
	}
```
