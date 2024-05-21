# Spy pixel

This is an example of html template with a spy pixel.

A spy pixel is a mechanism to have a read receipt on your mails.

## How to use

1. Open an http server on your computer. You can do this with Python:
```python
python -m http.server 14789
```
2. Write your message on the `message.html` tempalte.
3. Change the IP address and the port of the image URL to match with your http server.
4. Open the message.html in a browser
5. Copy and paste the browser content in your mail editor
6. Send the mail

Now you just have to wait for a request reaching your http server. It means that your message has been read.

## Disclamer

A lot of mail servers like Gmail, Exchange etc... open the images and store it in a cache. It mean that:
- the IP address reaching you http server isn't always your recipient IP address,
- your http server is not always reached if the recipient re-open your mail.

## What next

This repository is a base of a concept. Unfortunately, it would be difficult to track many mails with it.

The next step of this approach is to create a server able to track each email separately, maybe using url parametres `http://url?id=lol` ?
