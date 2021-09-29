# Versioning ([Web API Guide](../../README.md))
by [Charles Iliya Krempeaux](http://changelog.ca/)
-----

There are different ways one _could_ create a Web-based API — i.e., a HTTP or HTTPS based API — what I describe in this guide is, in general, how I recommend it is done.

Here is one thing I prefer programmers do when they create a Web-based API — **programmers should version their Web-based APIs**.

I'll explain _what_ I mean by “versioning”.
And I'll trying to explain _why_ “versioning” is desirable.

## What

This is an API without versioning:
> `GET https://api.example.com/toys`
> 
> `DELETE https://api.example.com/toys/{id}`
> 
> `GET https://api.example.com/toys/{id}`
> 
> `PATCH https://api.example.com/toys/{id}`
> 
> `PUT https://api.example.com/toys/{id}`

And this is an API with versioning:
> `GET https://api.example.com/v1/toys`
> 
> `DELETE https://api.example.com/v1/toys/{id}`
> 
> `GET https://api.example.com/v1/toys/{id}`
> 
> `PATCH https://api.example.com/v1/toys/{id}`
> 
> `PUT https://api.example.com/v1/toys/{id}`

That `v1` in the path indicates the version.
`v1` means _version one_.

If you are having trouble see the difference between the unversioned and version API, look closely at this:
```
   https://api.example.com/toys/{id}

https://api.example.com/v1/toys/{id}
                        ⇑⇑
```

This is an API at _version two_:
> `GET https://api.example.com/v2/toys`
> 
> `DELETE https://api.example.com/v2/toys/{id}`
> 
> `GET https://api.example.com/v2/toys/{id}`
> 
> `PATCH https://api.example.com/v2/toys/{id}`
> 
> `PUT https://api.example.com/v2/toys/{id}`

Again, that `v2` in the path indicates the version.
`v2` means _version two_.

You can compare all three here:
```
   https://api.example.com/toys/{id}

https://api.example.com/v1/toys/{id}
                        ⇑⇑

https://api.example.com/v2/toys/{id}
                        ⇑⇑

```

Can you guess what _version thirteen_ might look like?
> `GET https://api.example.com/v13/toys`
> 
> `DELETE https://api.example.com/v13/toys/{id}`
> 
> `GET https://api.example.com/v13/toys/{id}`
> 
> `PATCH https://api.example.com/v13/toys/{id}`
> 
> `PUT https://api.example.com/v13/toys/{id}`

## Why

The TL;DR version of why you would want to version you API is that —

You may want to change your API in the future.
But someone may have created software that depends on your old API.
It might be a _bad idea_ for your to break your previous API (because it would break this type of software).
Or you might want to give these software creators time to change their software to use your new API. (It might not happen immedidately).

Versioning of APIs can make it _easier_ to make a new version of your API (often while still keeping your old API around, at least for a while).

That's the quick explanation.
To make that make sense, I need to provide a better example.
That is coming next.

-----
[⏭️](../nouns/README.md)
