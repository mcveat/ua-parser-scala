UA Parser Scala Library
======================

This is the Scala implementation of [ua-parser](https://github.com/tobie/ua-parser).
The implementation uses the shared regex patterns and overrides from regexes.yaml.

[![Build Status](https://travis-ci.org/mcveat/ua-parser-scala.png?branch=master)](https://travis-ci.org/mcveat/ua-parser-scala)

Build:
------

    sbt package

Usage:
--------
```scala
import ua.parser.Parser

  val ua = "Mozilla/5.0 (iPhone; CPU iPhone OS 5_1_1 like Mac OS X) AppleWebKit/534.46 (KHTML, like Gecko) Version/5.1 Mobile/9B206 Safari/7534.48.3"
  val client = Parser.get.parse(ua) // you can also use CachingParser
  println(client) // Client(UserAgent(Mobile Safari,Some(5),Some(1),None),OS(iOS,Some(5),Some(1),Some(1),None),Device(iPhone))
}
```

Author:
-------

  * Piotr Adamski [@mcveat](https://twitter.com/mcveat)

  Based on the [java implementation](https://github.com/ua-parser/uap-java) by Steve Jiang [@sjiang](https://twitter.com/sjiang) and using agent data from BrowserScope
