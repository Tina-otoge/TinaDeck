#![Tina Deck](https://raw.githubusercontent.com/Shookaite/TinaDeck/master/logo/hibiki_v1-title.png)
Client-side overrides suite for *[Twitter Inc.'s TweetDeck](https://tweetdeck.twitter.com/ "Open Tweetdeck")*.

## Summary
* [What does it do](#wtf)
* [Installation](#install)
* [What are the different files ?](#files)
* [Miscellaneous](#misc)

## <i id="wtf"></i>What does it do
*Tina Deck* adds some animations, shadows, and some features to *Twitter TweetDeck*.
#### Main features :
* **You can hide a user's profile content on profile cards**, this feature was designed to help you looking at your friends's headers, because profile content often obstructs them so you have to open your friends's profile on *Twitter Web*. This trick was achieved using CSS only so it shouldn't slow your browser nor your computer.  
Demo :  
![profile card content hiding feature](http://i.imgur.com/uDggjhY.gif)
* The loading picture animation has been changed.  
[Demo](https://twitter.com/Shookaite/status/639832880621977601)
* Some items have now a shadow and that make everything softer.
* Many more incoming

## <i id="install"></i>Installation
Those steps may differ depending on your browser and its version.  
Considering you're surely using a mainstream browser, **you first need Stylish**. [Stylish add-on for Chrome](https://chrome.google.com/webstore/detail/fjnbnpbmkenffdnngjfgmeleoegfcffe) // [Stylish extension for Firefox](https://addons.mozilla.org/en-US/firefox/addon/stylish/?src=external-userstyleshome) (Chromium-based browsers like Opera and Vivaldi normally supports the Chrome add-on one)

#### Simplest and faster way : Instructions
1. Click on the CSS file you want to install in the GitHub explorer.  
![demo](http://i.imgur.com/pqWhT1A.png)
2. Click on the "raw" button to show only what you need, the source code.  
![demo](http://i.imgur.com/ihMmXtI.png)
3. Copy all the content of the file. You can use the shortcuts <kbd>CTRL+A</kbd> to select all the content and then <kbd>CTRL+C</kbd> to copy it to clipboard.
4. Go to <https://tweetdeck.twitter.com>
5. Left-click on the Stylish button in your browser's toolbar
6. Select *Write new style* > *For tweetdeck.twitter.com...*  
![example](http://i.imgur.com/Qwx3zwp.png)
7. A text input box prompting you to enter some CSS code should be in front of you now. Just paste the content of the *Tina Deck* file you copied earlier from the clipboard. You can use the shortcut <kbd>CTRL+V</kbd> for that. If the text box is pre-filled with some code, remove it before pasting, it will prevent some -not severe- errors to happen.
8. Choose a name for your override (I recommend something that helps you recognizing it like *Tina Deck core file* if it's *main.css*) and then click on *save* and go back to *TweetDeck*, your new style override should be installed !  


## <i id="files"></i> What are the different files ?
For now the only files in *Tina Deck* are [main.css](https://github.com/Shookaite/TinaDeck/blob/master/main.css) and [favs-are-back.css](https://github.com/Shookaite/TinaDeck/blob/master/favs-are-back.css) I'm sure you guessed it, main.css is the main *Tina Deck* file. It contains all the main features and is pretty light so it shouldn't slow down your browsing experience and favs-are-back is a little script to put stars back in TweetDeck. Maybe in the future, if it's needed, when adding some very specific features, I'll release them as complementary files, that way you'll be able to choose what features you want or not.

## <i id="misc"></i> Miscellaneous
If you want to disable or modify some of the *TinaDeck*'s features, feel free to modify the files.  
Here's some basic tips if you're not used to CSS.
* If you want to modify a color, for example, shadows color, you can enter pre-defined values by simply typing the name of a color. For example, here's the feature that makes the avatars glowing when hovering them in profile cards  :  
<blockquote>.prf-card-inner .prf-img:hover img {box-shadow:-webkit-box-shadow: 0 0 8px 6px #55acee!important;box-shadow: 0 0 8px 6px #55acee!important;} /* avatar is glowing blue when hovering it in profile card \*/</blockquote>
Here the color is set using an hexadecimal value, it's a shiny blue and it's equal to the **#55acee** parts. Let's imagine that you want pink instead. Then replace **#55acee** by the word **pink**, it'll work just fine ! (of course every colors work, you can type **red**, **yellow**, or anything)  
* Now let's have a look at the transitions delay. First off what are transitions delays ? That's the time taked by an item to change from a CSS value from another. For example in the feature that allows you to make profile contents disappear by hovering the closing button, the content disappears smoothly and reappears smoothly too. Now let's imagine that you want it to disappears fastly. You can. Check those lines :  
<blockquote>/* Global transition delay */
.avatar, div.is-open .compose, .prf-carn-inner .prf-img img, .prf-card-inner {transition:1s;}</blockquote>  
There are several items selected, and them all have the same value **transition:1s**. For our example you will change it to **transition:0.2s** to have very fast transitions. Feel free to put the value that fits you the most !
