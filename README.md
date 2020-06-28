# sample-ios-project-cocoapods-renovate-debug-source

## Demo Issue updating Cocoapods dependency
Sample project with automated dependency updates for Cocoapods using Renovatebot.
1. Created sample repo [sample-ios-project-cocoapods-renovate-debug-source](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source.git)
2. Create a sample XCode Project [sample-ios-project](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source/tree/master/sample-ios-project)
3. Did `pod init` and added a pod dependency
   * Added at top:
     * `platform :ios, '11.2'`
   * Added Dependency:
     * `pod 'Analytics', '3.8.1'`
4. Connect Renovate using [renovate](https://github.com/marketplace/renovate) to the repo [sample-ios-project-cocoapods-renovate-debug-source](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source).
5. Renovate created a [pr 1](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source/pull/1) with renovate config which I merged.
6. Renovate created a [pr 2](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source/pull/2) to Update dependency Analytics 3.8.1 to 3.9.0.
   * Successfully dependency update for renovate bot.
   * Job log [here](https://app.renovatebot.com/dashboard#github/asoneji/sample-ios-project-cocoapods-renovate-debug-source/195269364)
7. Add Source
   * Added Source:
     * `source 'https://github.com/CocoaPods/Specs.git'`
     * [pod source doc](https://guides.cocoapods.org/syntax/podfile.html#source)
8. Renovate updated [pr 2](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source/pull/2) to Update dependency Analytics 3.8.1 to 3.9.0.
   * [Error](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source/pull/2#issuecomment-650665348)
   ```
   Analyzing dependencies
   Cloning spec repo `cocoapods` from `https://github.com/CocoaPods/Specs.git`
   ```
   * Job log [here](https://app.renovatebot.com/dashboard#github/asoneji/sample-ios-project-cocoapods-renovate-debug-source/195279974)


**Note**: If I remove `Source` from podfile the [pr 2](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-debug-source/pull/2) again will behave successfully dependency update for renovate bot. Adding source impacts all PR's.
