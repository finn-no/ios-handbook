# Using modern frameworks

Swift has some really interesting frameworks but the information is sometimes scattered over different pages and Apple's own documentation not always deep enough. This page serves as a collection of useful blogs / books regarding specific areas / frameworks.

## SwiftUI

Since SwiftUI is continuously evolving, it's highly possible to bump into issues where a view is not backwards compatible (e.g. `AsyncImageView` was only introduced in iOS 15). Fortunately there are several solutions on the internet, 

- Apple [made](https://developer.apple.com/tutorials/swiftui) a nice examples page.

- Paul Hudson has an [extensive introduction](https://www.hackingwithswift.com/quick-start/swiftui/) to SwiftUI. 

- John Sundell dedicated a whole [category](https://www.swiftbysundell.com/discover/swiftui/) to SwiftUI.

- Majid wrote a few interesting articles. [This](https://swiftwithmajid.com/2019/11/19/you-have-to-change-mindset-to-use-swiftui/) one can serve as a great starting point. There are some really interesing entries on the [categories](https://swiftwithmajid.com/categories/) page.

- Alex Grebenyuk did a very good [explanation](https://kean.blog/post/swiftui-layout-system) on SwiftUI layout system.

- Samuel Défago wrote a thorough [article](http://defagos.github.io/understanding_swiftui_layout_behaviors/) about SwiftUI layout behaviours. It's worth a read.

## Async / await

- There's a basic introduction about the new concurrency related features on [Apple's site](https://docs.swift.org/swift-book/LanguageGuide/Concurrency.html).

- Andy Ibanez wrote a detailed [series](https://www.andyibanez.com/posts/modern-concurrency-in-swift-introduction/) about async / await. This one is definitely recommended.

- You can find a whole [discovery section](https://www.swiftbysundell.com/discover/concurrency/) on John Sundell's site about async / await.

- Avander Lee also wrote a few articles with useful examples. [This](https://www.avanderlee.com/swift/async-await/) is a good starting point.

- There are some interesting articles on Donny Wals's [concurrency related pages](https://www.donnywals.com/category/swift-concurrency/).

- Apple recently [published](https://www.swift.org/blog/swift-async-algorithms/) a great algorithms extension for async / await.

## Combine

- Antoine Van Der Lee has a few great blog posts about Combine. You can start with [this](https://www.avanderlee.com/swift/combine/) and continue on related ones describing some specifig use cases.

- Donny Wals has also has several posts connected to Combine. [This](https://www.donnywals.com/an-introduction-to-combine/) is a great place to get an overview, then it's possible to cherry pick individual topics on [this page](https://www.donnywals.com/category/combine/).

- John Sundell has a nice [discovery page](https://www.swiftbysundell.com/discover/combine/) covering a lot of interesting topics around Combine.

## Practical usage

If you're wondering about how to combine all of these frameworks / techniques in an app, you can check [this repository](https://github.schibsted.io/finn/ios-app/tree/onboarding-attila). The files you want to check can be found in the folder `Classes/Wishlist`.