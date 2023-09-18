+++
draft = false
date = 2023-09-17
title = "SwiftUI Note"
description = ""
tags = ["SwiftUI","IOS development","Internship","Weekly Diary"]
+++

* [SwiftUI](#swift_ui)

## SwiftUI

1. Structure
```swift
import SwiftUI
// main function for constructing the UI component
struct ContentView: View {
    var body: some View {
        VStack {
            Text("Hello world")
        }
    }
}

// this function is for preview in Xcode
struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
```

2. Button
```swift
    Button(action: {
        // action after pressing button
    }){
       // looks for the button
       Image(systemName:"chevron.left")
            // if you want to frame a image, 
            // you need this resizable
            .resizable()
            .frame(width:10, height:12)
    }
```

3. Stacks
```swift
// HStack is for horizontal alignment
HStack(alignment: .center, spacing: 10) {
    Text("something")
    // font can be customized and you may need
    // to download some font style that you like
    .font(Font.custom("some font",size: 17))

    // Spacer here for spliting the element in HStack
    // evenly
    Spacer()

    Image(systemName:"chevron.left")
            .resizable()
            .frame(width:10, height:12)
}
.padding()

// VStack is for vertical alignment
VStack(alignment: .leading) {
    Section {
        // some element
    }
    Spacer()
    Section {
        // other element
    }
}

// ZStack is for putting something on the 
// original page. for example, you are trying
// to add a comment on a tweet and the app pops out
// another 'page'
ZStack{
    VStack{

    }
}
// you can even add some blur to make it looks good
.blur(radius: 6)
```

4. Binding and State
```swift
struct ParentView: View {
    @State private var text = ""

    var body: some View {
        VStack {
            ChildView(text: $text)
            Text("Entered: \(text)")
        }
    }
}

struct ChildView: View {
    @Binding var text: String

    var body: some View {
        TextField("Enter something", text: $text)
    }
}
```
By using `@State`, SwiftUI allows you to update and rerender (eg. A counter changes)
For `@Binding`, it allows to refer to another view's `@State`,which doesn't need to 
replicate the data.
