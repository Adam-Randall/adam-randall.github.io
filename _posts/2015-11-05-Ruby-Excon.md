---
layout: post
title: Excon - The HTTP Ruby Gem
excerpt: "Excon is a excellent and easy way to make HTTP calls within Ruby. I found it to be a excellent tool when needing to make calls within a Ruby on Rails application."
modified: 2015-05-31
tags: [Excon, Ruby On Rails, Ruby, ROR]
comments: true
share: true

---

Within Ruby, the Excon Gem makes it easy to make HTTP calls. With one line of code you can make a request.

Firstly install the gem (or include it in your Gemfile):

```
sudo gem install 'excon'
```

Make a get request, inputting the server you are calling:

```
response = Excon.get("http://websitetoget.com")
```

You can then check the response.code to see if the request was successful (200 response code).<br>
You can also check response.body to see what JSON is received (if some is parse back). 

Alternatively, posting JSON is just as easy:

```
response =  Excon.new("http://websitetoget.com",
```
```
    headers: {"Content-Type" => "application/json", "Accept" => "*/*"},
```
```
    body: {name: "Joe Blogs", description: "I am JSON"}.to_json
)
```

As you can see above, I am setting a header with a content type of JSON and parsing through a JSON string containing a name and description.

To do this in Java or other languages could take several lines of code and requires you to check for exceptions along the way. However this gem leaves you saving time and allows for fast rapid development.