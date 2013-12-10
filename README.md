Intro
==============

Animated Social share buttons control.<br>
Supported share buttons:<br><b>Facebook</b>,  <b>Twitter</b>,  <b>Google+</b>, <b>Tumblr</b>, <b>E-mail</b>

<img src="http://mixdesign.kz/external/AAShareBubblesAbay.png?tmp"/>&nbsp;&nbsp;
<img src="http://mixdesign.kz/external/AAShareBubbles.png?1"/>

Usage:
------
```objective-c
#import "AAShareBubbles.h"
```
```objective-c
AAShareBubbles *shareBubbles = [[AAShareBubbles alloc] initWithPoint:CGPointMake(100, 100)
                                                              radius:100
                                                              inView:self.view];
shareBubbles.delegate = self;
shareBubbles.bubbleRadius = 45; // Default is 40
shareBubbles.showFacebookBubble = YES;
shareBubbles.showTwitterBubble = YES;
shareBubbles.showMailBubble = YES;
shareBubbles.showGooglePlusBubble = YES;
shareBubbles.showTumblrBubble = YES;
[shareBubbles show];
````
#####Delegate
```objective-c
-(void)aaShareBubbles:(AAShareBubbles *)shareBubbles tappedBubbleWithType:(AAShareBubbleType)bubbleType
{
    switch (bubbleType) {
        case AAShareBubbleTypeFacebook:
            NSLog(@"Facebook");
            break;
        case AAShareBubbleTypeTwitter:
            NSLog(@"Twitter");
            break;
        case AAShareBubbleTypeMail:
            NSLog(@"Email");
            break;
        case AAShareBubbleTypeGooglePlus:
            NSLog(@"Google+");
            break;
        case AAShareBubbleTypeTumblr:
            NSLog(@"Tumblr");
            break;
        default:
            break;
    }
}
```
Requirements:
------------
`ARC`, `iOS 5+`, `Xcode 4+`

Todo:
-------
- Add more social buttons.
- Add opportunity to show bubbles in specified order.
