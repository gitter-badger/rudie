
# rudie

[![Join the chat at https://gitter.im/rudieIOS/Lobby](https://badges.gitter.im/rudieIOS/Lobby.svg)](https://gitter.im/rudieIOS/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Bridge between iOS devices and MiaoMiao with Nightscout integration

**Expect code during the weekend, notice will be posted on the facebook groups and elsewhere**

Since us iOS users are somewhat limited in our options I figured it was time to up the game a bit. Welcome. Rudie is in its early stages yet. It integrates initially with [Nightscout](http://www.nightscout.info/wiki/welcome/nightscout-for-ios-optional),  and there's plenty of guides there on how to set things up for things to work.  I like Heroku. You might not. Guides are available on the Nightscout foundation site. It's also worth noting which apps they support. 

Want to participate - just get in touch. I primarily code in other languages so here and there there are improvements to be made I'm sure. But the fact of the matter is that it's trivial to read and interpret the data from the miaomiao. If you want to build something for yourself - start by cloning RxBluetoothKit, run their example app (you need to turn on auto managing to use your credentials). Start scanning, connect to the miao miao. The Service with two Characteristics is the one you want. 

One is Tx (transmit) and one is Rc (Receive).
(click the top one, turn notification on, click the bottom one and put in d305 and send. On Success send f0. Watch your data scroll by in the upper characteristic.

The actual flow to fetch data is trivial. When the code is up just have a look into MiaoMiao.swift (or if I refactor, wherever it ends up). In fact I encourage everyone with experience with coding to look into it, I've tried to ensure that the state machine and the interpretation is as close to *common* syntax as possible.
Oh and my friend the UI designer is on vacation so live with a somewhat bizarre selection of fonts. 

Yeah, and since we have watches here there'll be a watch app as well. For now this is a stop gap and proof that getting stuck in ancient tech stacks is less than optimal.

### CAVEAT EMPTOR
Libre isn't perfect. Everyone who has been a long term user knows that. This means that even though your miaomiao may work perfectly the readings may be off. Since I've been gathering data on this for about 18 months I can safely say that apart from their general quality issues they also have substantial margins of error, especially in the first 24-48 hours of application. **Be aware**

### Post scriptum
[Just for you, and you know who you are.](https://www.youtube.com/watch?v=sVzvRsl4rEM)
