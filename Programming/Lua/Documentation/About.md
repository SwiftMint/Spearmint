# What is Lua?[^1]

|Logo|
|-|
|<img width="57.1" height="57.1" alt="Lua-Logo svg" src="https://github.com/user-attachments/assets/e1ca6ad0-e8f0-4ca9-b37d-b6f223e487ed" />|

Lua is a powerful, efficient, lightweight, embeddable scripting language. It supports several programming styles: procedural, object-oriented, functional, data-driven, and data description.

Lua combines simple procedural syntax with powerful data description constructs based on associative arrays and extensible semantics. Lua is dynamically typed, runs by interpreting bytecode with a register-based virtual machine, and has automatic memory management with incremental garbage collection, making it ideal for configuration, scripting, and rapid prototyping.

# Where does Lua come from?[^2]

Lua is designed, implemented, and maintained by a team at PUC-Rio, the Pontifical Catholic University of Rio de Janeiro in Brazil. Lua was born and raised in Tecgraf, formerly the Computer Graphics Technology Group of PUC-Rio. Lua is now housed at LabLua, a laboratory of the Department of Computer Science of PUC-Rio.

# What's in a name?[^3]

"Lua" (pronounced LOO-ah) means "Moon" in Portuguese. As such, it is neither an acronym nor an abbreviation, but a noun. More specifically, "Lua" is a name, the name of the Earth's moon and the name of the language. Like most names, it should be written in lower case with an initial capital, that is, "Lua". Please do not write it as "LUA", which is both ugly and confusing, because then it becomes an acronym with different meanings for different people. So, please, write "Lua" right!

# Joining the community[^4]

There are several meeting places for the Lua community where you can go to learn and help others and contribute in other ways. One of the focal points is the mailing list, which is very active and friendly.

You can meet part of the Lua community in person by attending a Lua Workshop.

# Supporting Lua[^5]

You can help to support the Lua project by buying a book published by Lua.org and by making a donation.

You can also help to spread the word about Lua by buying Lua products at Zazzle.

Lua.org is an Amazon Associate and we get commissions for qualifying purchases made through links in this site.

# Why choose Lua?[^6]

## Lua is a proven, robust language[^7]

Lua has been used in many industrial applications (e.g., Adobe's Photoshop Lightroom), with an emphasis on embedded systems (e.g., the Ginga middleware for digital TV in Brazil) and games (e.g., World of Warcraft and Angry Birds). Lua is currently the leading scripting language in games. Lua has a solid reference manual and there are several books about it. Several versions of Lua have been released and used in real applications since its creation in 1993. Lua featured in HOPL III, the Third ACM SIGPLAN History of Programming Languages Conference, in 2007. Lua won the Front Line Award 2011 from the Game Developers Magazine.

## Lua is fast[^8]

Lua has a deserved reputation for performance. To claim to be "as fast as Lua" is an aspiration of other scripting languages. Several benchmarks show Lua as the fastest language in the realm of interpreted scripting languages. Lua is fast not only in fine-tuned benchmark programs, but in real life too. Substantial fractions of large applications have been written in Lua.

If you need even more speed, try LuaJIT, an independent implementation of Lua using a just-in-time compiler.

## Lua is portable[^9]

Lua is distributed in a small package and builds out-of-the-box in all platforms that have a standard C compiler. Lua runs on all flavors of Unix and Windows, on mobile devices (running Android, iOS, BREW, Symbian, Windows Phone), on embedded microprocessors (such as ARM and Rabbit, for applications like Lego MindStorms), on IBM mainframes, etc.

For specific reasons why Lua is a good choice also for constrained devices, read this summary by Mike Pall. See also a poster created by Timm Müller.

## Lua is embeddable[^10]

Lua is a fast language engine with small footprint that you can embed easily into your application. Lua has a simple and well documented API that allows strong integration with code written in other languages. It is easy to extend Lua with libraries written in other languages. It is also easy to extend programs written in other languages with Lua. Lua has been used to extend programs written not only in C and C++, but also in Java, C#, Smalltalk, Fortran, Ada, Erlang, and even in other scripting languages, such as Perl and Ruby.

## Lua is powerful (but simple)[^11]

A fundamental concept in the design of Lua is to provide meta-mechanisms for implementing features, instead of providing a host of features directly in the language. For example, although Lua is not a pure object-oriented language, it does provide meta-mechanisms for implementing classes and inheritance. Lua's meta-mechanisms bring an economy of concepts and keep the language small, while allowing the semantics to be extended in unconventional ways.

## Lua is small[^12]

Adding Lua to an application does not bloat it, thus also contributing to its security. The tarball for Lua 5.5.0, which contains source code and documentation, takes 388K compressed and 1.5M uncompressed. The source contains around 32000 lines of C. On 64-bit Linux, the Lua interpreter built with all standard Lua libraries takes 293K and the Lua library takes 484K.

## Lua is free[^13]

Lua is free open-source software, distributed under a very liberal license (the well-known MIT license). It may be used for any purpose, including commercial purposes, at absolutely no cost. Just download it and use it.

See all of the Lua documentation @ [Lua | Docs](https://www.lua.org/docs.html)!

 [^1]: [**Header**: What is Lua?](https://www.lua.org/about.html#:~:text=%C2%B7%20getting%20started-,What%20is%20Lua%3F,-Lua%20is%20a)
 [^2]: [**Header**: Where does Lua come from?](https://www.lua.org/about.html#:~:text=Where%20does%20Lua%20come%20from%3F)
 [^3]: [**Header**: What's in a name?](https://www.lua.org/about.html#:~:text=of%20PUC%2DRio.-,What%27s%20in%20a%20name%3F,-%22Lua%22%20(pronounced%20LOO))
 [^4]: [**Header**: Joining the community](https://www.lua.org/about.html#:~:text=Joining%20the%20community)
 [^5]: [**Header**: Supporting Lua](https://www.lua.org/about.html#:~:text=Lua%20Workshop.-,Supporting%20Lua,-You%20can%20help)
 [^6]: [**Header**: Why choose Lua?](https://www.lua.org/about.html#:~:text=in%20this%20site.-,Why%20choose%20Lua%3F,-Lua%20is%20a)
 [^7]: [**Subheader**: Lua is fast](https://www.lua.org/about.html#:~:text=Lua%20is%20a%20proven%2C%20robust%20language)
 [^8]: [**Subheader**: Lua is portable](https://www.lua.org/about.html#:~:text=Developers%20Magazine.-,Lua%20is%20fast,-Lua%20has%20a)
 [^9]: [**Subheader**: Lua is portable](https://www.lua.org/about.html#:~:text=in%2Dtime%20compiler.-,Lua%20is%20portable,-Lua%20is%20distributed)
[^10]: [**Subheader**: Lua is embeddable](https://www.lua.org/about.html#:~:text=by%20Timm%20M%C3%BCller.-,Lua%20is%20embeddable,-Lua%20is%20a)
[^11]: [**Subheader**: Lua is powerful (but simple)](https://www.lua.org/about.html#:~:text=Lua%20is%20powerful%20(but%20simple))
[^12]: [**Subheader**: Lua is small](https://www.lua.org/about.html#:~:text=in%20unconventional%20ways.-,Lua%20is%20small,-Adding%20Lua%20to)
[^13]: [**Subheader**: Lua is free ](https://www.lua.org/about.html#:~:text=library%20takes%20484K.-,Lua%20is%20free,-Lua%20is%20free)
