# slack_builder
[![Build Status](https://travis-ci.org/botdio/slack_builder.svg?branch=master)](https://travis-ci.org/botdio/slack_builder)
use builder design pattern to compose the slack simple Markdown text, in chain style

## examples:

```
new SlackBuilder("abc") => abc
new SlackBuilder().text("abc") => abc
new SlackBuilder("abc").b() => *abc*
new SlackBuilder("abc").b("def") => abc *def*
new SlackBuilder("abc").i() => _abc_
new SlackBuilder("abc").br().text('def') => abc\ndef
new SlackBuilder("abc").del() => ~abc~
new SlackBuilder("abc").code("hello,world") => abc `hello,world`
new SlackBuilder("abc").pre("hello\nworld") => abc ```hello\nworld```
new SlackBuilder("abc").comment("hello\nworld") => abc >>> hello\nworld
```

find more examples in test.js.