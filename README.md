# oil-sardine


A WebDAV client for Java applications, using [OkHttp](https://github.com/square/okhttp) as HTTP client.
This is a fork of [Grizzly Labs' fork](https://github.com/thegrizzlylabs/sardine-android) of the [Sardine library](https://github.com/lookfirst/sardine). 

The goal is to have a pure Java library that is as lean as possible, without dependencies on Kotlin Standard library, JAXB or Apache's HttpClient. 
If you are looking for a WebDAV client for Android, you better go to Grizzly Labs, if you are looking for a WebDAV client for Java applications and dependencies on large libraries is not a issue, you better go to Sardine. 

You still need: 
- an okhttp version without Kotlin, e.g. okhttp-3.9.0.jar  
- a compatible okio library, e.g. okio-1.13.0.jar
- the simple xml library, e.g. simple-xml-2.7.1.jar


## Getting started


- Create a `Sardine` client:
```
Sardine sardine = new OkHttpSardine();
sardine.setCredentials("username", "password");
```

- Use the client to make requests to your WebDAV server:
```
List<DavResource> resources = sardine.list("http://webdav.server.com");
```

## Legacy

Originally forked from [Grizzly Labs' fork](https://github.com/thegrizzlylabs/sardine-android) of the [Sardine library](https://github.com/lookfirst/sardine). 
All Android dependencies and libraries that require the Kotlin standard library have been removed.

[Apache HTTP Client](http://hc.apache.org/) was replaced by [OkHttp](https://github.com/square/okhttp) and [Okio](https://github.com/square/okio)

JAXB was replaced by [SimpleXml](http://simple.sourceforge.net/)
