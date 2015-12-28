---
layout: post
title: A First Look At TextSecure
excerpt: TextSecure is a great way to encrypt SMS messages, but understanding the cryptography...
tags: [TextSecure, libtextsecure, Signal, Open Whisper Systems]
comments: true
share: true

---

Recently I have been experimenting with Signal (TextSecure) by Open Whisper Systems. This is a messaging service which provides end-to-end encryption  without the need in paying SMS and MMS costs.

One of the great things about Signal as they have provided many libraries and a API to interact with. However in order to use it, I have found that you require an in-depth knowledge of the [axolotl library](https://github.com/WhisperSystems/libaxolotl-java). This is due to the complexity behind how it does the encryption, which at times was very confusing to understand.

I gave up on using the API as I found the documentation lacked a great deal of information. However using the [Java Library](https://github.com/AsamK/libtextsecure-java) and understanding how other people implemented applications, gave me the knowledge to further my development. I have to thank janimo for his [GO implementation of TextSecure](https://github.com/janimo/textsecure), which was one of the main ones I had used.

After producing a product for work I felt very competent in using TextSecure libraries. I hope more and more people use it as an encryption service especially as it grows and the documentation gets better. 