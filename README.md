# Kruiz Control

This is a Fork of [Kruiz Control](https://github.com/Kruiser8/Kruiz-Control), with modifications for the [@HangoutHere Twitch](https://twitch.tv/hangouthere) stream!

When Kruiz Control upstream updates, the `master` branch here should be unchanged, and this `hangouthere` branch should contain only the [differences](https://github.com/hangouthere/Kruiz-Control/compare/master...hangouthere) that are our tweaks!

# Features:

* Utilities (`triggers/_utils.txt`):
    * System TTS Voice output normalized for consistent usage
    * Read a list, newline separated, into a variable (`_listData_`) for future use
    * Import a list read from disk into a named KC-List
    * Check if the incoming user is one we don't want to allow (ie, bots), and set in a variable
    * Compare all values of Array1 to Array2, and store in a List (_CompareArrays_) for easy access
        * Useful for comparing all words in a message against a set of keywords, instead of hardcoding them into an `OnKeyword` trigger
    * `Chat Send` a random entry from a list on disk easily
* Greetings (`triggers/greetings.txt`): On every incoming message, check for common greetings and respond both in chat and TTS!
* LOLs (`triggers/lols.txt`): Similar to *Greetings*, will "lol" back at the chatter (no TTS).
* Support Messaging (`triggers/interval_support.txt`):
    * At some interval, output a message to chat to garner support from viewers
    * Picks at random from Twitter/Discord/Instagram/General support messaging!
    * Only outputs if a viewer has chatted recently to avoid a wall of bot text for new viewers
* Randomized Responses to common commands (`triggers/randomListCommands.txt`):
    * `!thanksWatching` - Thanks chatters for watching, used at the end of a stream
    * `!discord` - Random Response to invite chatters to Discord
    * `!twitter` - Random Response to invite chatters to follow on Twitter
    * `!instagram` - Random Response to invite chatters to follow on Instagram
    * `!support` - Random Response to emplore chatters to support you.
    * `!lurk` - Random Response to thank chatters for Lurking
    * `!unlurk`/`back` - Random Response to welcome chatters back
    * `!brb`/`brb` - Random Response emploring chatters to hurry back
* StreamLabs Randomized Responses (`triggers/streamlabs.txt`):
    * Various event handling with randomized responses to the chatter/streamer
    * Supports Bits, Donations, Raids, and Follows
* Misc Commands (`triggers/misc.txt`):
    * Time/Date command (!time or !date) for quick current time information!