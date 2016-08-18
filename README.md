# \<app-cookie-document\>

> Cookie Web Component for Polymer extending app-storage

Cookie Web Component for Polymer extending app-storage

```html
<app-cookie-document
  key="test_cookie"
  data="hello world!"
  time="2"
  format="h">
</app-cookie-document>
```

## Usage

Add the library using the Javascript package manager [Bower](http://bower.io/):

```shell
$ bower install --save app-cookie-document
```

Or clone this repository inside your project folder using Git:

```shell
$ git clone https://github.com/CityOfAuburnAL/polymer-cookie.git
```

## Properties

### key

Type: String

Set the cookie name

### data

type: String

The cookie value, notifies

### sessionOnly

type: Boolean

Default value: false

Set to true if you want the cookie to end with the user session. Overrides time and format settings when true.

### path

type: String

Default value: ''

The cookie path.

The path must be absolute.
If not specified, defaults to the current path of the current document location.

### domain

type: String

Default value: ''

The cookie domain.

(e.g., 'example.com' or 'subdomain.example.com').
If not specified, defaults to the host portion of the current document location
(but not including subdomains). Contrary to earlier specifications,
leading dots in domain names are ignored. If a domain is specified,
subdomains are always included.

### time

type: Number

Default value: 1

The expiration time related to the 'format' value.
Set to -1 to never expire the cookie

### format

type: String

Default value: 'd'

The expiration format time

*   's' : seconds
*   'm' : minutes
*   'h' : hours
*   'd' : days

### secure

type: Boolean

Default value: false

Cookie to only be transmitted over secure protocol as https

### http-only

type: Boolean

Default value: false

The HTTPOnly cookie attribute can help to mitigate this attack by
preventing access to cookie value through Javascript. Read more about
[Cookies and Security](https://www.nczonline.net/blog/2009/05/12/cookies-and-security/).

## Methods

### save

Write the cookie

```js
this.$$('app-cookie-document').save('key').then(...);
```

### destroy

Destroy the cookie

```js
this.$$('app-cookie-document').destroy().then(...);
```

## Rendering in a demo page

### Install Polymer CLI

Install the Polymer CLI to serve the demo locally with:

```shell
$ npm install -g polymer-cli
```

### Run the demo

First install all the project dependencies with:

```shell
$ bower install
```

Then, run Polymer serve from the repo directory with:

```shell
$ polymer serve
```

Then open localhost:8080/components/polymer-cookie/demo/ in your browser.

For more information about Polymer CLI have a look at the
[official documentation](https://www.polymer-project.org/1.0/start/first-element/intro)

## Contributing

1.  Fork it!
2.  Create your feature branch: `git checkout -b my-new-feature`
3.  Commit your changes: `git commit -m 'Add some feature'`
4.  Push to the branch: `git push origin my-new-feature`
5.  Submit a pull request :D

## Contributors

A special thanks to polymer-cookie team:

*   [@cameronwp](https://github.com/cameronwp)
*   [@MeTaNoV](https://github.com/MeTaNoV)
*   [@ymahnovskyy](https://github.com/ymahnovskyy)
*   [@web-padawan](https://github.com/web-padawan)

The expires get and _setCookie is largely based on their project.

## Changelog

Changelog available [here](https://github.com/CityOfAuburnAL/polymer-cookie/blob/master/CHANGELOG.md)

## License

[MIT License](https://github.com/CityOfAuburnAL/polymer-cookie/blob/master/LICENSE)
© City of Auburn
