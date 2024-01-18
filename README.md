# Component-Based-Architecture Implementation And Explanation In Swift

**Buongiorno**, according to midnight, **how are you, dudes**? hope things go well!!, **PIZZA was fantastic, right?** I hope you enjoyed it!

**What about sharing something cool**? They say about me that I am ***بتباكس***, but that is not correct, ***maybe I am a wizard***, but **I do not know what is your problem** to share a solution for it.

**So I decided to share one of my tricks**, any **real-world software engineer** who makes a code review will identify it...

I did not announce it, **that is true** because I like to leave things in **suspense and confuse people**,

If I tell you... where is **the suspense**?! fun would not exist In this ***boring game...*** *I don't like chaos, but I like to cause it...*

## Lighting The-Darkness In our brains:

Everything has a **unique color and taste**, including **operating systems, programming languages**, and architectural patterns. I like to jump between them, that is the reason for **gaining knowledge dude**, trying new things every day is ***super-fun***...

> She is the same and knows well how to make me high... 
> I haven't hunted for a long time, but I'll catch You : P

Anyway, If you look at a project like that [#](https://github.com/shadyelmaadawy/Opportunities-Hunter-OSX-Bot), for  **user interface architecture pattern**.. two points of **view will pop up**.
- As an **IOS Developer**, you will say **MVVM** or **VIPER** is cool,
- As a **Software Engineer** ( AS ME ), you will say **Event-Driven Architecture** is ***ideal***...
         ( FYI, I do not like this job title, *and never turned me on*, **I use it In formal conversations only** )
         
( In both cases, this project will be **finished Inevitably sooner or later**, I just thinking **About best practices and object design** and some stuff.. *Project مليان حوارات* ) 

But how? **Event-Driven Architecture** is not a **Swift  architecture pattern**, It's okay, but dose **MVVM** related to **IOS**? **NO**, you can find It In ( **C#, Java, Flutter**.. and so on ), 
**MVVM**, **It's an User-Interface Architecture Pattern**, Not an IOS Architecture, **Even MVI**, it's popular in **Android community**, a gift for them [#](https://developer.android.com/ndk/reference) for **ultra performance** when you deal with the OS, 

But maybe a **business case will force you to use** It In **IOS**, It's okay, stop ~~link architectures to environments and platforms~~, **you're software engineer!**. 
 
But does software is **limited to User-Interface?** **NO**,  There is a lot, as **Monolithic**, **Microservices**.. etc, depend on your **project scale**, you will not apply **Modular Architecture** for  ***a small-scale project!! that's not making any sense, be wise!!*** 

By the-way, do you know what **Picasso** once said?

## Learn the rules like a PRO, so you can break them like an ARTIST!

**Component-Based Architecture,** with this approach I will use **Real-World OOP concepts** that you ask about it In **Interviews and don't use In projects,**

Even though **you can find** It In a lot of **programming languages**, It's rare to see It In Egypt, because developers **negatively see things, WHY?**

Because most people will say: I can't be different, they will **laugh at me**... I don't like to be a **joke to others**... So, it's okay, **they laughed at me too**, but now they know how **ignorant** they are **in this game LOL,**

Btw, It's on of the keys to **implementing scalable software**, I used to apply It with **User interface components** most of the time, 

**From where I caught this? ملكش دعوة، بص في ورقتك**

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiKMwvg0ZkITkxe5VDUsFr6UlbPhW2fK32ivBeyAG6cA&s)

----
Let's take **Real-World Example**, ***UITextField***: [#](https://developer.apple.com/documentation/uikit/uitextfield) 

I Will just **inherit it in a new class**, 

```swift
final class BaseUITextField: UITextField { }
```

But I want to customize it, **like give it cool padding** ( ***without repeating the same code*** ) or give un-beautiful ***auto layout constraints for the height*** *'I know you did this do not worry'*, but how?! It's simple, 

I will override **three funtions**, [textRect](textRect), [borderRect](https://developer.apple.com/documentation/uikit/uitextfield/1619642-borderrect), [editingRect](https://developer.apple.com/documentation/uikit/uitextfield/1619589-editingrect)
```swift
final class BaseUITextField: UITextField {

    //MARK: - Properties
    
    var padding: UIEdgeInsets {
        return UIEdgeInsets.init(
            top: 15, left: 15, 
            bottom: 15, right: 15
        )
    }

    //MARK: - Overrides
    
    override func textRect(forBounds bounds: CGRect) -> CGRect {
        return bounds.inset(by: padding)
    }
    
    override func borderRect(forBounds bounds: CGRect) -> CGRect {
        return bounds.inset(by: padding)
    }
    
    override func editingRect(forBounds bounds: CGRect) -> CGRect {
        return bounds.inset(by: padding)
    }
}
```

No magic.. ***just 4 overrides and one variable*** solve a *real-world problem*, you can apply different things like giving them a **neat text color**, and with **one change you will affect the whole project** without the need to search in **every line of code**...

 but how do I apply this **approach In the User Interface**? 

First you need a **good UI\UX Designer** who knows how to get things done, for example, In buttons, **primary, secondary**... and so on, think about **It's as a theme**, nothing else!

This is a **simple use**, but even with this *architecture you can give them a new behavior*, **as an example**: [#](https://github.com/shadyelmaadawy/Opportunities-Hunter-OSX-Bot/blob/master/OhKit/OhKit/Custom/Logger/OhLoggerView.swift)

Life becomes easy when you **throw out your ego** and learn how to write software like a **real-world engineer** ; )

## Resources
  - [Apple.com](https://developer.apple.com/documentation/uikit/uitextfield)
 - [Opportunities-Hunter-OSX-Bot](https://github.com/shadyelmaadawy/Opportunities-Hunter-OSX-Bot/blob/master)
- [Tutorialspoint.com - An article from google search engine](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

## To infinity and beyond!

After about a year In **egyptian tech community**, and one of the wars that took **almost 6 months**, I could identify **five patterns of people**.

| Patterns    | What they have done/Or who they are    |
|  :---: | :---: |
| WHO knows how to hunt elite | They hired me  |
| WHO knows how to get things done | This is me  |
| MY FANS and THE GOOD PEOPLE out there |  ***I LOVE YOU*** ✨💜  |
| who owns the biggest job titles In SE ( **by luck** ) |  They participated in a technical interview with me  |
| noobs and the-crowd |  They throw shit and dirt in my NAME |

Today I gave **The Fourth and fifth Patterns** a new job title.. **codes-writer**, this is what you deserve dudes, In my opinion and with all modesty, you need a **software engineering literacy course**, and **I AM proof of that**.

To those who have read these lines, **do not be like the last two types**… do not follow the crowd, ***LEAD THEM! ; )***

## Credits

### Copyright (©) 2024, Shady K. Maadawy, All rights reserved. 
 [@shadudiix](https://github.com/shadyelmaadawy)

