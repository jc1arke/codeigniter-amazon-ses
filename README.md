CodeIgniter Amazon SES
======================
A CodeIgniter library to interact with Amazon Web Services (AWS) Simple Email Service (SES). This library was designed with the standard CodeIgniter email class in mind. As a result, most methods look the same, ensuring a minimal learning curve.

NOTE: this code is still under heavy development and currently provides only the very basics of the AWS SES API (don't you like acronyms?), sending email.

Requirements
------------
1. PHP 5.1+
2. CodeIgniter 2.0+ (http://codeigniter.com)
3. libcurl
4. Phil Sturgeon's CodeIgniter cURL library (http://github.com/philsturgeon/codeigniter-curl)
5. Amazon Web Services account (http://aws.amazon.com)

Documentation
-------------

### Configuration
This library expects a configuration file to function correctly. A template for this file is provided with the library. 

### Recipients

####$this->amazon_ses->to()
Set the "To" address(es) for a message.

####$this->amazon_ses->cc()
Set the "CC" address(es) (carbon copy) for a message.

####$this->amazon_ses->bcc()
Set the "BCC" address(es) (blind carbon copy) for a message.

These three methods expect valid e-mail addresses as a string, array or comma separated list.

###Message

####$this->amazon_ses->subject()
Set the subject for a message

####$this->amazon_ses->$this->amazon_ses->message()
Set the message to ben sent

####$this->amazon_ses->send()
Sends the message. Returns true on success.

###Misc

####$this->amazon_ses->debug()
Sends the message in debug mode. In debug mode, the send() methods returns the actual API response instead of a boolean. Call this method before calling the send method.

####$this->amazon_ses->destroy()
Preserves recipient after the message has been successfully send. When you call this method, all recipients will be preserved during the objects life. This makes it possible to sent an additional message without re-specifying the recipients.

Contributing
------------
I am a firm believer of social coding, so <strike>if</strike> when you find a bug, please fork my code on GitHub (http://github.com/joelcox/codeigniter-amazon-ses) and squash it. I will be happy to merge it back in to the code base (and add you to the "Thanks to" section). If you're not too comfortable using Git or messing with the inner workings of this library, please open a new issue (http://github.com/joelcox/codeigniter-amazon-ses/issues). 

Thanks to
---------
* Phil Sturgeon (http://philsturgeon.co.uk), for creating the CodeIgniter cURL library (http://github.com/philsturgeon/codeigniter-curl) and thus taking care of all the cURL hassle.