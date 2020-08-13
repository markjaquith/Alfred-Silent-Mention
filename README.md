# Alfred Silent Mention
Alfred 4 Workflow to silently type `@usernames`, `domains.com`, or `#hashtags` without them being linked or parsed.

<img width="704" alt="Screen Shot 2020-08-13 at 5 04 14 PM" src="https://user-images.githubusercontent.com/353790/90187047-2b991e80-dd87-11ea-97cf-0066a7fcc579.png">

For example, you can type `@stop` on Twitter without poor [Doug Bowman](https://twitter.com/stop) getting a notification.
Or you could type `WordPress.com` or `Amazon.com` in Slack without a big stupid preview loading in.

## Installation
Download the Workflow file, and run it to add it to Alfred. Customize the keyword if you want (default is `silent`).

## Usage
Invoke Alfred, then type `silent @username` or `silent amazon.com` or `silent #hashtag` and hit return. The thing you typed will be pasted into the frontmost app, but will **not** be seen as a username mention, a domain link, or a valid hashtag.

## How It Works
It works by inserting a "zero-width space" character (which is like a space, but without any width) in a location that breaks the parsing. So, to Twitter, it looks like `WordPress .com`, but to a human's eyes, it is just `WordPress​.com` (that one has a zero-width space in it).

## Works On
* Twitter
* Slack
* iMessage
* GitHub
* Probably a lot more things!
