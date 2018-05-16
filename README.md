# Minimal Ruby and NodeJS/NPM/Yarn built on top of Alpine Linux Docker Image (Approx. 53MB)
Self explanatory, ruby build on top of nodejs and alpine image

This will be a great base image for people working with rails applications.
You could get away from using therubyracer gem by using a pre-built nodejs for the javascript V8 engine.

Hope this will help others in the future.

### Gem dependencies
When you install gems, there are gems with specific native dependencies.

You have to add the respective alpine package before installing the respective gems.
```
apk --update add ${packages}
```

The few known dependencies are:
* ffi: libffi-dev
* nokogiri: libxml2 libxslt libxml2-dev libxslt-dev
* rmagick: imagemagick imagemagick-dev
* raindrops: linux-headers
* pg: postgresql-client postgresql-dev

p.s.: there are also a few native compilation dependencies that you have to keep in mind.
* g++
* make


### Supported Docker versions

This image is officially supported on Docker version 1.11.2.

Support for older versions (down to 1.6) is provided on a best-effort basis.

### Thanks

@Daniel-ltw for the original [ruby-node-alpine](https://github.com/Daniel-ltw/ruby-node-alpine) image which this image is based on.
