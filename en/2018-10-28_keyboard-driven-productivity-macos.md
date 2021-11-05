![](https://thepracticaldev.s3.amazonaws.com/i/ospp8ymq4hwaifnt0tcn.jpeg)

Picture: Kinesis Advantage2 keyboard, https://www.kinesis-ergo.com/shop/advantage2/ . All rights reserved by Kinesis, it’s their trademarks, etc. Looks pretty cool, but I have some doubts on ⇧⌥⌘ shortcuts ergonomics

This article was originally posted on Medium.com, https://medium.com/@true.neu/keyboard-driven-productivity-in-macos-def201b6c8fa

# So hey, fellow developer.

Or a devops, or sysadm, it doesn’t really matter.

Have you ever wondered how much time and effort do you waste when reaching out to your pointer device throughout the day?

Let’s make a wild assumption that you change your application in focus 100 times a day. From terminal emulator to IDE, then to messenger, then to browser, and back to terminal emulator, 25 cycles, and you do not use ⌘⇥ to do so. So each time you have to:

- Remove your hand from home row of your keyboard
- Reach to the mouse
- Find the current pointer location
- Point to the application you need and click
- Return you hand to the home row.

Assuming each individual action takes about 0.5 seconds, we have 2.5 seconds in total. Times 100, it’s a bit more than 4 minutes spent only to change focus. You might argue that it’s not a lot, compared to a standard 8-hour long workday. Well, add to that every time you need to reach mouse to change active tab in your browser, or click a menu item, or start an application, or to focus searchbar in the browser, or copy text from a terminal emulator. You probably won’t like your findings.

---

# Now what can you do to fix this?

Though I’ll be talking about software I use personally (namely macOS, Jetbrains IDEs, iTerm and Google Chrome), you may find a lot of things useful even if our favorites are not the same. For example,

## Keyboard

### Touch typing

There’s no arguing or pros and cons about that. If you don’t know how to touch type and using hunt-and-peck technique, or just memorized where each key is located and your hands resemble piano player’s hands, you’re either slow, or making a lot of typos, or (the most common case) both. There are exceptions of course, but in general you should learn to touch type as soon as possible.

To put this a little bit into perspective, an average touch typer such as myself, types at 40-60 wpm. An average hunt-and-peck typer would have speed at 27–37 wpm (https://blog.typing.com/hunt-and-peck/). This, of course, doesn’t mean you’ll produce twice as much code you’re producing today; but you’d half the time needed to respond to your colleagues in Slack. If you type 200 words each day (just a bit more than twice this paragraph), you’ll have 2.5 minutes more left to think about the function naming.

### Keyboard layout

Think if your current keyboard layout is optimal for what you’re doing. Chances are you’re using standard QWERTY. As a person that doesn’t like his fingers to travel much away from the home row, frequently uses parenthesis, brackets and other characters which usually require pressing Shift + a digit, I opted for Programmer Dvorak layout (https://www.kaufmann.no/roland/dvorak/). You might find regular Dvorak or Colemak more appealing.

I must say that there are some disadvantages of choosing a non-standard keyboard layout.

You’ll have to learn it, it takes time and dedication, though it’s not as hard as learning to touch type for the first time, as you know the general technique already.
You’ll have troubles typing on QWERTY keyboard, especially in case of Dvorak. Colemak is much more forgiving in that aspect, as it diverges not so drastically. Personally, I don’t think it matters much, as I don’t usually push people off their seats and type e-mails impersonating them. But you might have a different perspective on this one.
You have to decide what to do with your shortcuts. For example, macOS has this peculiar ‘Dvorak + QWERTY-⌘’ layout, which changes your ⌘ layer to still use QWERTY, so ⌘C and ⌘V are in their old place. I don’t like this way, because well, okay, what do we do with ⌃ shortcuts then? ⌃⌘? And anyway, when your brain is trying to cope with new layout, it’s better to go all-in and let your C and V be on the same key regardless of modifiers pressed.
What software could you make use of to customize this aspect of your setup? Well, to make your own, redistributable keyboard layout, there’s Ukelele (https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=ukelele). Karabiner-Elements can also be of great use (https://pqrs.org/osx/karabiner/), and will be mentioned later on.

### Other keyboard mods

There are a couple of other low-level modifications I like to use. Most of common UNIX-like shortcuts like ⌃w, ⌃a, ⌃e work out of the box in macOS. But not ⌥ ones. I don’t really like Option layer in macOS, as it yields symbols which are used less often than I change my jobs. But good news, we can remap, for instance, ⌥D to forward delete a word system-wide. You can find an extensive list for such modifications at https://github.com/ttscoff/KeyBindings.

Another one is inspired by Nikita Prokopov’s blog post, http://tonsky.me/blog/cursor-keys/. The basic idea is that you remap your Caps Lock key to fn, and map fn+JKLI to you cursor keys. So whenever you have to navigate using arrow keys, you don’t have to move your hands away from home row at all. I went a bit further and also mapped fn+SDFE to ⌃a/PgDown/⌃e/PgUp.

Are you using standard macOS behaviour (so-called Character Picker) to type accents by holding a letter key like ‘a’, ‘o’, ‘e’, ‘c’? No? Well me neither. Let’s switch it off, or we won’t be able to type ‘aaaaaaaaaaaaaaaaaaaa’ as a commit message with just one keypress. Take a look at this link: http://m10lmac.blogspot.com/2011/07/os-x-107-lion-getting-rid-of-character.htmtl

And the last, but not the least, is one of standard Karabiner-Elements modifications to map Caps Lock to “hyper-modifier” (⇧⌥⌃⌘), which is normally not used at all in any kind of applications. As Caps Lock is already taken by arrows mod, I map it to right ⌥.

## Shortcuts

You should take a look at the most useful shortcuts for your applications and learn to take advantage of them. Whenever there’s two ways to do something, where one is with mouse, always opt for another one. Whenever there’s only one, spend some time to find out the right one. Without the mouse. In case you didn’t figure.

### System

Don’t forget about system-wide shortcuts, such as focus the menu bar or the dock. Another one, surprisingly useful for multi-window applications such as Adium is “Move focus to next window”.

I’m sure you’re using Spotlight, it’s a nice way of finding/running things on your computer. However, I’ve replaced my Spotlight completely with Alfred. Unlike most of the soft I’m talking about, it’s not free, but it has an especially cool feature: Workflows. Practically, it’s Automator from a different perspective: you set a trigger and a bunch of actions to follow, which can also utilize the input provided in Alfred’s omnibar. The Workflow I use the most is pretty stupid: it triggers on ⇧⌥⌃⌘letter, and launches a specific application. I have iTerm on ‘a’, Chrome on ‘d’, IDEA on ‘g’ and so on. That enables me to switch focus between applications really fast (because remember, I mapped ⇧⌥⌃⌘ to right ⌥?)

Alfred has an extensive list of features which don’t bring a lot of value to the topic, but nevertheless I’ll mention my favorite one: Clipboard History. Whenever I press ⌥⌘V, I get a list of things that were in my clipboard recently, with omnibar active. That saves a lot of browser tab switches, when you have to copy-paste 5–6 values between tabs; instead of doing it one by one, you can do so in bulks.

### IDE

If you’re using a powerful text editor or an IDE, chances are you can shortcut nearly any action available. For instance, there are one hour long videos on just using IntelliJ IDEA shortcuts, such as https://www.youtube.com/watch?v=eq3KiAH4IBI. There’s not much to say about this, you just have to force yourself to use a shortcut whenever possible until it becomes second nature. Here are some of my favorites for IDEA, if it helps: Extend/Shrink selection, Recent files, Recent projects, Git/VCS commands, Jump to Navigation bar, Focus Project tool window, VCS tool window, Parameter info, Jump to definition, Show usages, Search for File/Symbol, Find in path, Replace in path, and of course Find action.

### Browser

If you use Google Chrome, there’s a great extension for it called Vimium (https://chrome.google.com/webstore/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=en). It enables you to control nearly every action in your browser with keyboard: opening and scrolling pages, following links, shortcutting Next/Prev buttons on paged views, etc. There are extensions like this for Firefox and Safari as well, but they’re not nearly as powerful. However, if you can’t stand Google Chrome, it may be worth to check them out (https://github.com/philc/vimium/wiki/Alternative-Vimium-for-Other-Browser).

### Terminal

To navigate through terminal emulator’s input, don’t use arrow keys or ⌃f/⌃b if you have to move the cursor further than a couple of symbols. Throw in some ⌥f/⌥b to move by word boundaries. All in all, learning typical UNIX shortcuts to move around text and edit it won’t hurt.

I’m sure that from time to time, you have to copy something from your terminal emulator window. iTerm has a couple of nice features: first, you can define shortcuts to move selection boundaries left or right, and second, you can enable so-called Shell Integration, that makes your local shell a bit more intelligent knowing it’s input and output is controlled by iTerm.

First one enables you to use the following pattern to select and copy text from arbitrary piece of terminal’s output: ⌘f (Find) + beginning of the piece you’d like to copy + (in my case) ⌥⇧→ (actually, ⇪⌥⇧l if we take into account everything I said before) + ⌘c.

Second one enables you to copy all the output from the previous command, or current command you’re currently typing in, with a single shortcut.

Also, if you use iTerm and don’t have tmux integration enabled, please please please enable it right now. If for some reason you tried and didn’t like it, that’s okay, fair enough. It’s just, I personally don’t see any reason to use another different set of shortcuts that don’t make sense anywhere outside screen or tmux, but that’s me. Some people still love vim for some reason, you know.

Learning everything new and unusual takes time. But if you’re successful in not letting yourself use old, slow but familiar way, soon new and fast habits will become your second nature. I don’t really move my hands away from home row anymore, and that feels great. I don’t spend time on useless muscular activity (I have table tennis and bass guitar for useful muscular activity, thank you very much), and it just looks cool. Seriously. It’s almost like I don’t move my hands at all, but everything works as it should.

This article was written without touching mouse a single time (though I’d punish some design decisions on Medium. Like really, you have all this free space on the left and right, but no buttons to insert an image or make a header?..)

### Bonus level

I notice that I sometimes start to suffer from syndromes I’d describe as ‘pre-RSI’. Wrist soreness, mild pain, etc. So… if you use more than one keyboard, Karabiner-Elements by default mirrors any modifiers pressed on one keyboard to all the others. That means you may seamlessly use two keyboards at the same time. You know, almost like split keyboards. Which is exactly what I do: my left hand types on laptop’s keyboard, and my right one uses standard Apple Wired. This way both my arms are straight without having to curve wrists at unnatural angles.

Well yeah, that’s it. See you at the home row!
