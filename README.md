# Get-File-extension-from-URL-or-String
This String Extension will get you the file name and extension of the file


```swift
//Get file extension form string or URL
extension String {
    
    func fileName() -> String {
        return NSURL(fileURLWithPath: self).deletingPathExtension?.lastPathComponent ?? ""
    }
    
    func fileExtension() -> String {
        return NSURL(fileURLWithPath: self).pathExtension ?? ""
    }
}

```

* Call it lIke below

```swift

let URLString = "Document.pdf"

//call it

URLString.fileName() //Output :- Document.pdf
URLString.fileExtension() //Output :- pdf

```
