# A Swift Tour
-

ထုံးစံအတိုင်း Language အသစ်တစ်ခုရဲ့ ပထမဆုံး program ဟာ "Hello, world!" စာလုံးကို screen မှာ print ထုတ်တာပါပဲ။ ဒါကို Swift မှာ တစ်ကြောင်းတည်းနဲ့ ဒီလိုရေးလို့ရပါတယ်-

```swift
	println("Hello, world!")
```

အကယ်၍ C သို့မဟုတ် Objective-C တို့ကို ရေးဖူးရင် အပေါ်ကကုဒ်ကို ရင်းနှီးနေမှာပါ။ Swift မှာ အဲဒီ့ကုဒ်ဟာ ပြည့်စုံတဲ့ program တစ်ပုဒ်ပါပဲ။ input/output သို့ string handling လုပ်ဆောင်ချက်လိုမျိုးအတွက် library တွေ သီးခြား import လုပ်ပေးစရာမလိုပါဘူး။
Global scope မှာရေးထားတဲ့ ကုဒ်ဟာ program ရဲ့ entry point လိုသုံးလို့ရလို့ main function ဆိုတာမလိုပါဘူး။ ဒါ့အပြင် ကုဒ်တစ်ကြောင်းရဲ့ အဆုံးတိုင်းမှာလဲ semi colon ထည့်ပေးဖို့ မလိုပါဘူး။

ဒီ tour မှာ programming နဲ့ ပတ်သတ်တဲ့ အလုပ်တွေ ဘယ်လိုလုပ်ရမလဲဆိုတာကို ပြရင်းနဲ့ Swift နဲ့ ကုဒ်စတင်ရေးသားဖို့ လုံလောက်တဲ့ သတင်းအချက်အလက်တွေကို ပေးသွားမှာပါ။ တကယ်လို့ တစ်ခုခုကို နားမလည်တာရှိရင်လည်း စိတ်မပူပါနဲ့။ ဒီ tour မှာ မိတ်ဆက်ထားသမျှကို ဒီစာအုပ်ရဲ့ ကျန်တဲ့အပိုင်းတွေမှာ အသေးစိတ်ရှင်းပြပေးထားပါတယ်။


> မှတ်ချက်
> လေ့လာမှု့အထောက်အကူဖြစ်စေဖို့အတွက် ဒီအခန်းကကုဒ်တွေကို Xcode ရဲ့ playground မှာဖွင့်ပြီးစမ်းကြည့်ပါ။ Playgrounds ဆိုတာကုဒ်တွေကို > ရေးသားနိုင်ပြီး ရေးထားတဲ့ကုဒ်ရဲ့ ရလာဒ်ကို ချက်ခြင်းကြည့်နိုင်ပါတယ်။
> [Download Playground](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Guided> Tour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1)

--

## ရိုးရိုးတန်ဖိုးများ (Simple Values)
constant ပြုလုပ်ဖို့အတွက် `let` ကိုသုံးပြီး variable တန်ဖိုးပြုလုပ်ဖို့အတွက် `var` ကို သုံးတယ်။ constant တစ်ခုကို compile time မှာ သိဖို့မလိုပါဘူး။ ဒါပေမယ့် တန်ဖိုးအတိအကျ တစ်ကြိမ် ထည့်(assign)လုပ်ပေးထားဖို့လိုပါမယ်။ ဆိုလိုတာက တစ်ကြိမ် ဆုံးဖြတ်ပြီး အမည်ပေးကြေငြာထားတဲ့ constant တန်ဖိုးတစ်ခုကို နေရာအများအပြားမှာ ပြန်လည်အသုံးပြုနိုင်ပါတယ်။

```swift
var myVariable = 42
var myVariable = 50
let myConstant = 42
```

assign လုပ်ချင်တဲ့ constant သို့ variable ရဲ့ တန်ဖိုးတွေမှာ တူညီတဲ့ ပုံစံ(same type) ရှိဖို့တော့ လိုပါတယ်။  သို့သော် အမြဲတမ်း type ကို ကိုယ်တိုင်ကိုယ်ကျ ပြုလုပ်ပေးဖို့တော့ မလိုပါဘူး။ တန်ဖိုးတစ်ခုပေးပြီး ပြုလုပ်ထားတဲ့ constant သို့ variable တစ်ခုကို compiler က  type အတွက်  infer ပြုလုပ်ပေးပါလိမ့်မယ်။ အပေါ်က ဉပမာမှာ  `myVariable` ရဲ့ type ကို integer အဖြစ် ကောက်ချက်ချပါတယ်။ ဘာလို့လဲဆိုတော့ သူ့ရဲ့ initial တန်ဖိုးဟာ integer ဖြစ်နေလို့ပါ။

အကယ်၍ initial တန်ဖိုးအတွက် လုံလောက်တဲ့ အချက်အလက်မပေးရင် (သို့မဟုတ် initial တန်ဖိုးမရှိရင်) အမည်ရဲ့နောက်မှာ colon(:) ခြားပြီး type ကို သတ်မှတ်ပေးလို့ရပါတယ်။

```swift
let implicitInteger = 70
let implicitDouble = 70.0
let explicitDouble: Double = 70
```


> စမ်းသပ်ရန်
> constant တစ်ခုကို explicit type Float နဲ့ တန်ဖိုးကို 4 အဖြစ်နဲ့ ဖန်တီးပါ။


တန်ဖိုးတွေဟာ အခြား type အဖြစ် ဘယ်တော့မှ အလိုအလျောက် convert မလုပ်ပါဘူး။ အကယ်၍ တန်ဖိုးတစ်ခုကို အခြား type တစ်ခုအဖြစ် convert လုပ်ချင်ရင် ပြောင်းချင်တဲ့ type ကို ကိုယ်တိုင်ကိုယ်ကျ ပြုလုပ်ပေးရပါမယ်။

```swift
let label = "The width is"
let width = 94
let widthLabel = label + String(width)
```


> စမ်းသပ်ရန်
> နောက်ဆုံးကုဒ်လိုင်းက  `String` ကို ပြောင်းထားတာကို ဖြုတ်ပြီး စမ်းကြည့်ပါ။ ဘာ error တတ်ပါလဲ?


string ထဲမှာ နောက်ထပ် တန်ဖိုးတွေ ထပ်ထည့်ဖို့ လွယ်လွယ်လေးပဲ လုပ်နိုင်ပါတယ်။ တန်ဖိုးကို ကွင်းစကွင်းပိတ်ထဲမှာ ရေးပြီး အရှေ့မှာ backslash(\) ထည့်ရေးရပါတယ်။ ဉပမာ -

```swift
	let apples = 3
	let oranges = 5
	let appleSummary = "I have \(apples) apples."
	let fruitSummary = "I have \(apples + oranges) pieces of fruit."
```


> စမ်းသပ်ရန်
> \() ကိုသုံးပြီး string တစ်ခုထဲမှာ floating-point calculation ကို ထည့်ပါ။ နှုတ်ဆက်စကား string တစ်ခုထဲမှာ တစ်ယောက်ယောက်ရဲ့နာမည်ကို ထည့်ပါ။


arrays နဲ့ dictionaries ဖန်တီးဖို့ (`[]`) ကို သုံးပြီး index သို့မဟုတ် key ကို လေးထောင့်ကွင်းထဲမှာ ရေးပြီး သူတို့ရဲ့ elements တွေကို access လုပ်နိုင်ပါတယ်။

```swift
    var shoppingList = ["catfish", "water", "tulips", "blue paint"]
    shoppingList[1] = "bottle of water"
     
    var occupations = [
        "Malcolm": "Captain",
        "Kaylee": "Mechanic",
    ]
    occupations["Jayne"] = "Public Relations"
```


empty array သို့ dictionary ကို create လုပ်ဖို့အတွက် initializer syntax ကို သုံးပါတယ်။


```swift
    let emptyArray = [String]()
    let emptyDictionary = [String: Float]()
```


အကယ်၍ type information က inferred လုပ်နိုင်ရင် empty array တစ်ခုကို [] နဲ့ empty dictionary တစ်ခုကို [:] နဲ့ ရေးနိုင်ပါတယ်။
ဥပမာ - variable သို့မဟုတ် function တစ်ခုရဲ့ argument ထဲ ထည့်တဲ့ အချိန်မျိုးမှာ။

```swift
    shoppingList = []
    occupations = [:]
```

## Control Flow
-
