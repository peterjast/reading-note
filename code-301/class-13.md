# **CRUD**

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Sending Form Data

Code samples from: [Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data)

* forms can be submitted once form data is validated on the client-side

### Client/Server Architecture

* web uses client/server architecture

* client sends request to server using HTTP(hypertext transfer protocol)

* Server sends response using HTTP protocol

* HTML form is a way for users to send data to server

### Client Side: Defining How to Send Data

* form element defines how data will be sent

* attributes let you configure the request when user clicks submit

* most important attributes are action and method

### The Action Attribute

* defines where to send data

* value must be valid URL

* data is sent to current page if action attribute isn't provided

```javascript
<form action="https://example.com"> //absolute URL

<form action="/somewhere_else"> //relative URL

<form> //data sent to current page

// The names and values of the non-file form controls are sent to the server as name=value pairs joined with ampersands. The action value should be a file // on the server that can handle the incoming data, including ensuring server-side validation. The server then responds, generally handling the data and
// loading the URL defined by the action attribute, causing a new page load (or a refresh of the existing page, if the action points to the same page).
```

### The Method Attribute

* how data is sent is define by method attribute

* form data can be transmitted via different methods, most commonly, GET and POST

* HTTP consists of a header containing set of global metadata and a body containing information neccessary for server to process specific request

### The GET Method

* used by browser to request a given resource

```javascript
<form action="http://www.foo.com" method="GET">
  <div>
    <label for="say">What greeting do you want to say?</label>
    <input name="say" id="say" value="Hi">
  </div>
  <div>
    <label for="to">Who do you want to say it to?</label>
    <input name="to" id="to" value="Mom">
  </div>
  <div>
    <button>Send my greetings</button>
  </div>
</form>

// The data is appended to the URL as a series of name/value pairs. After the URL web address has ended, we include a question mark (?) followed by the    // name/value pairs, each one separated by an ampersand (&). In this case we are passing two pieces of data to the server
```

The HTTP request:

> GET /?say=Hi&to=Mom HTTP/2.0
> Host: foo.com

### The POST Method

* method used by browser to talk to server with data appended to body of HTTP request

```javascript
<form action="http://www.foo.com" method="POST">
  <div>
    <label for="say">What greeting do you want to say?</label>
    <input name="say" id="say" value="Hi">
  </div>
  <div>
    <label for="to">Who do you want to say it to?</label>
    <input name="to" id="to" value="Mom">
  </div>
  <div>
    <button>Send my greetings</button>
  </div>
</form>
```

HTTP REQUEST(No data in URL, appended to body):

> POST / HTTP/2.0
>
> Host: foo.com
>
> Content-Type: application/x-www-form-urlencoded
>
> Content-Length: 13
>
> say=Hi&to=Mom

### Viewing HTTP Requests

1. Open dev tools

1. Select Network

1. Select All

1. Select foo.name in Name tab

1. Select Headers

## Resources

[Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data)
