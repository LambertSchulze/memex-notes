---
category: note
tags:
  - SoftwareArchitecture
  - DesignPrinciples
created: 2024-09-23
---
> Code should be joyful to work with :-)

Die CUPID Prinzipien hat [Dan North als Kritik](https://dannorth.net/cupid-the-back-story/) an die [[SOLID Principles]] erfunden.
Er wollte Devils Advocate spielen und die extreme Meinung vertreten dass alle der Solid Prinzipien veraltet/schlecht sind.

Er selber vertritt die Meinung dass Code in so großen Blöcken gegliedert sein soll dass man sie mental gut erfassen kann.

Alles muss irgendwie halt Sinn machen.
Nicht nur für dich sondern auch für andere Programmierer.
Deshalb soll man sich an die Gepflogenheiten der Sprache in der man schreibt halten.

---
Seine fünf ausgewählten Prinzipien sind:
## [[Write simple code|Composability]]
Write small code that get's along with other code.
It can _get in your head_.
It's Consistently named.

## [[UNIX-like]]
Do one thing good.
That can be chained together.

## Predictability
Like tests in [[Test Driven Development]].
If they are so simple that you can clearly see what they do.
Observable.

## Idiomatic
> Write code like everybody writes code.
> That other people expect to see.

For libraries and in your team.

## [[Domain Driven Design|Domain based]]
Code should be written in the language that it lives in.

