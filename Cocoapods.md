# Create library in cocoapods

## Step

1. `$ pod lib create [your library name]`
1. create github repository   
    ```
    $ git add .
    $ git commit -m "commit message"
    $ git remote add origin https://github.com/[User Name]/[ライブラリ名].git
    $ git push origin master
    ```
1. replace file `/Pod/Classes/ReplaceMe.swift`
1. open and develop `/Example/[ライブラリ名].xcworkspace`
1. check your library
    ```
    $ cd Example
    $ pod install
    ```
1. edit podspec
1. edit Readme.md
1. add tag
    ```
    $ git tag 0.1.0
    $ git push origin 0.1.0
    ```
1. if you want to check `$ pod lib lint SampleLib.podspec`
1. derivery `$ pod trunk push SampleLib.podspec`

## Sample

### podspec

```
#
# Be sure to run `pod lib lint SampleLib.podspec' to ensure this is a
# valid spec before submitting.
#
# Any lines starting with a # are optional, but their use is encouraged
# To learn more about a Podspec see http://guides.cocoapods.org/syntax/podspec.html
#

Pod::Spec.new do |s|
  s.name             = "SampleLib"
  s.version          = "0.1.0"
  s.summary          = "A short description of SampleLib."

# This description is used to generate tags and improve search results.
#   * Think: What does it do? Why did you write it? What is the focus?
#   * Try to keep it short, snappy and to the point.
#   * Write the description between the DESC delimiters below.
#   * Finally, don't worry about the indent, CocoaPods strips it!
  s.description      = <<-DESC
                       DESC

  s.homepage         = "https://github.com/<GITHUB_USERNAME>/SampleLib"
  # s.screenshots     = "www.example.com/screenshots_1", "www.example.com/screenshots_2"
  s.license          = 'MIT'
  s.author           = { "[作成者名]" => "[メールアドレス]" }
  s.source           = { :git => "https://github.com/<GITHUB_USERNAME>/SampleLib.git", :tag => s.version.to_s }
  # s.social_media_url = 'https://twitter.com/<TWITTER_USERNAME>'

  s.platform     = :ios, '8.0'
  s.requires_arc = true

  s.source_files = 'Pod/Classes/**/*'
  s.resource_bundles = {
    'SampleLib' => ['Pod/Assets/*.png']
  }

  # s.public_header_files = 'Pod/Classes/**/*.h'
  # s.frameworks = 'UIKit', 'MapKit'
  # s.dependency 'AFNetworking', '~> 2.3'
end
```










