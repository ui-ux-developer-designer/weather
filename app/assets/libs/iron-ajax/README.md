
<!---

This README is automatically generated from the comments in these files:
iron-ajax.html  iron-request.html

Edit those files, and our readme bot will duplicate them over here!
Edit this file, and the bot will squash your changes :)

The bot does some handling of markdown. Please file a bug if it does the wrong
thing! https://github.com/PolymerLabs/tedium/issues

-->

[![Build status](https://travis-ci.org/PolymerElements/iron-ajax.svg?branch=master)](https://travis-ci.org/PolymerElements/iron-ajax)

_[Demo and API docs](https://elements.polymer-project.org/elements/iron-ajax)_

## Changes in 2.0
* Promise polyfill is now a dev dependency and no longer shipped with `iron-ajax`

## &lt;iron-ajax&gt;

The `iron-ajax` element exposes network request functionality.

```html
<iron-ajax
    auto
    url="https://www.googleapis.com/youtube/v3/search"
    params='{"part":"snippet", "q":"polymer", "key": "YOUTUBE_API_KEY", "type": "video"}'
    handle-as="json"
    on-response="handleResponse"
    debounce-duration="300"></iron-ajax>
```

With `auto` set to `true`, the element performs a request whenever
its `url`, `params` or `body` properties are changed. Automatically generated
requests will be debounced in the case that multiple attributes are changed
sequentially.

Note: The `params` attribute must be double quoted JSON.

You can trigger a request explicitly by calling `generateRequest` on the
element.



## &lt;iron-request&gt;

iron-request can be used to perform XMLHttpRequests.

```html
<iron-request id="xhr"></iron-request>
...
this.$.xhr.send({url: url, body: params});
```


