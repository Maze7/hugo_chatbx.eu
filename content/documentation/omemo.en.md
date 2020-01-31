---
title: 'OMEMO End-To-End Encryption'
weight: 5
---

{{< external_link "https://conversations.im/omemo/" "OMEMO" >}} is a way of end-to-end encryption that offers the best usability for XMPP users. It is based on the {{< external_link "https://en.wikipedia.org/wiki/Signal_Protocol" "Signal Protocol" >}}, which implements state-of-the-art cryptography for instant messaging.

## Basics

* A key is generated per device (= XMPP Client)
* The keys are automatically published over XMPP, so that others can encrypt messages to you
* A message is encrypted to all (trusted) devices of the sender and receiver (in group chats to everyone in the group)
* The keys of others first have to be marked as trusted in your client
	- This mitigates man-in-the-middle attacks, where a stranger creates fake devices
	- Trust can be verified by comparing the fingerprint of a device key
	- Compare fingerprints over a different channel (e.g. e-mail)
	- If the fingerprints displayed in your contacts client and your own client match, you can trust this key
	- Messages you send will be encrypted to trusted devices and messages you receive form trusted devices will be displayed as secure

## Tips & Tricks

* If you are using multiple devices, be sure that all your clients trust the fingerprints of the other devices; otherwise, the different clients can't see the messages of each other
* If you trust a new fingerprint of a chat partner, be sure to do so on all your devices, as each has their own trust store
* File transfers are also encrypted like messages by OMEMO
