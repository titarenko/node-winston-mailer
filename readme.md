An email transport based on mailer for [winston][0].

## Installation

``` sh
npm i winston
npm i winston-mailer
```

## Usage
``` js
var winston = require('winston');

//
// Requiring `winston-mailer` will expose 
// `winston.transports.Mail`
//

require('winston-mailer');

winston.add(winston.transports.Mail, options);
```

The Mail transport uses [nodemailer][1] behind the scenes. Options are the following:

* __to:__ The address(es) you want to send to. *[required]*
* __from:__ The 'from' address (default: `winston@hostname`).
* __smtp:__ Options for [nodemailer][1] [smtp][2] transport.
* __level:__ Level of messages that this transport should log.
* __silent:__ Boolean flag indicating whether to suppress output.
* __maxBufferItems__ Max errors that will be buffered (default 100).
* __maxBufferTimeSpan__ Max miliseconds errors will be buffered (default 60000).

[0]: https://github.com/flatiron/winston
[1]: https://github.com/andris9/Nodemailer
[2]: https://github.com/andris9/nodemailer-smtp-transport
