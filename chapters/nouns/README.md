# Nouns ([Web API Guide](../../README.md))
by [Charles Iliya Krempeaux](http://changelog.ca/)
-----

There are different ways one _could_ create a Web-based API — i.e., a HTTP or HTTPS based API — what I describe in this guide is, in general, how I recommend it is done.

Here is one thing I prefer programmers do when they create a Web-based API — **the path of a Web-based API URI should represent a noun**.

I'll explain _what_ I mean by "path" and "noun". And I'll try explaining _why_ this is desirable.

## Web URI Path

Web URIs look like these:

* `http://example.com/`
* `http://example.com/apple/banana/cherry`
* `http://example.com/path/to/something.txt`
* `http://example.com/toys?q=action+figures`
* `https://www.example.com/hello-world#reference`
* `https://search.example.com/ultimate/combo?apple=one&banana=two&cherry=three#reference`

For each of these the paths are:

* `/`
* `/apple/banana/cherry`
* `/path/to/something.txt`
* `/toys`
* `/hello-world`
* `/ultimate/combo`

Let's compare the path and the URI for each of these, to make it easier to see which part is the path:
```
http://example.com/
                  /
                  ⇑
                 path
```

```
http://example.com/apple/banana/cherry
                  /apple/banana/cherry
                  ⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑
                  path
```

```
http://example.com/path/to/something.txt
                  /path/to/something.txt
                  ⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑
                  path
```

```
http://example.com/toys?q=action+figures
                  /toys
                  ⇑⇑⇑⇑⇑
                  path
```

```
https://www.example.com/hello-world#reference                  /
                       /hello-world
                       ⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑
                       path
```

```
https://search.example.com/ultimate/combo?apple=one&banana=two&cherry=three#reference
                          /ultimate/combo
                          ⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑⇑
                          path
```





-----
[⏭️](../nouns/README.md)
