# Plugin Segmented Control for Xamarin Forms and .NET Standard

[![NuGet Badge](https://buildstats.info/nuget/Plugin.SegmentedControl.Netstandard)](https://www.nuget.org/packages/Plugin.SegmentedControl.Netstandard/)

*Please star this project if you find it useful. Thank you!*

## Why
There are other Segmented Control libraries out there. This library adds two important capabilities:
- It works across all three key platforms: iOS, Android and UWP - all other libraries I've encounted lack UWP.
- It's based on .NET Standard

## Supported platforms
|Platform|Supported|Version|Renderer|
| ------------------- | :-----------: | :-----------: | :------------------: |
|Xamarin.iOS Unified|Yes|iOS 8.1+|UISegmentedControl|
|Xamarin.Android|Yes|API 18+|RadioGroup|
|Xamarin.UWP|Yes|Win10 10586+|User Control/RadioButton|

## How to used
Using this plugin is easy. 

### iOS
Add initializer to `AppDelegate`

```csharp
public override bool FinishedLaunching(UIApplication app, NSDictionary options)
{
    global::Xamarin.Forms.Forms.Init();

    SegmentedControlRenderer.Initialize();
    ...
}
```

### Android & UWP
No special needs

### Xamarin Forms

#### .NET Standard
The Xamarin Forms must use .NET Standard. I suggest using .NET Standard 1.4. 

Here is a great blog post about how to move your PCL to .NET Standard: [Building Xamarin.Forms Apps with .NET Standard](https://blog.xamarin.com/building-xamarin-forms-apps-net-standard/)

#### XAML
To get this: ![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

```xml
<control1:SegmentedControl x:Name="SegmentedControl" 
                            SelectedSegment="{Binding SegmentSelection}" 
                            OnSegmentSelected="SegmentedControl_OnValueChanged" 
                            TintColor="BlueViolet"
                            SelectedTextColor="White"
                            DisabledColor="Gray"
                            Margin="8,8,8,8">
    <control1:SegmentedControl.Children>
        <control1:SegmentedControlOption Text="Item 1"/>
        <control1:SegmentedControlOption Text="Item 2"/>
        <control1:SegmentedControlOption Text="Item 3"/>
        <control1:SegmentedControlOption Text="Item 4"/>
    </control1:SegmentedControl.Children>
</control1:SegmentedControl>

```



## Credits
For inspiration and for the Android and iOS part I'd like to thank Alex Rainman for his great work on [SegmentedControl.FormsPlugin](https://www.nuget.org/packages/SegmentedControl.FormsPlugin/).