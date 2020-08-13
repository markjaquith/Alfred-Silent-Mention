# Alfred Silent Mention
[Alfred 4][alfred] workflow to silently type `@usernames`, `domains.com`, or `#hashtags` without them being linked or parsed by Twitter, Slack, iMessage, and more.

<img width="704" alt="Screen Shot 2020-08-13 at 5 04 14 PM" src="https://user-images.githubusercontent.com/353790/90187047-2b991e80-dd87-11ea-97cf-0066a7fcc579.png">

For example, you can type `@stop` on Twitter without poor [Doug Bowman][stop] getting a notification.
Or you could type `WordPress.com` or `Amazon.com` in Slack without a big annoying preview loading in.

## Installation
1. Have [Alfred][alfred] installed.
2. Have the [Alfred Powerpack][powerpack] installed.
3. [Download the Silent Mention workflow file][download], and double-click it to add it to Alfred.
4. Customize the keyword if you want (default is `silent`).

## Usage
Invoke Alfred, then type `silent @username` or `silent amazon.com` or `silent #hashtag` and hit return. The thing you typed will be pasted into the frontmost app, but will **not** be seen as a username mention, a domain link, or a valid hashtag.

## How It Works
It works by inserting an invisible `U+2060` [Word Joiner][word-joiner] character in a location that breaks the parsing. `U+2060` is a special character that means “the things on either side of me should stay stuck together”. So, to Twitter, it looks like `WordPress<U+2060>.com` or `@<U+2060>stop, but to a human's eyes, it is just `WordPress⁠.com` or `@⁠stop`.

## Works On
* Twitter
* Slack
* iMessage
* GitHub
* And more

[download]: https://github.com/markjaquith/Alfred-Silent-Mention/raw/main/Silent%20Mention.alfredworkflow
[stop]: https://twitter.com/stop
[alfred]: https://www.alfredapp.com/
[powerpack]: https://www.alfredapp.com/powerpack/
[word-joiner]: https://en.wikipedia.org/wiki/Word_joiner
