encdec
======
encdec is a node module that helps you baseXX encode and decode.

It defaults to using base58 encoding, but can easily be adapted for 
base16, base32, base64 - or any other base - by passing the alphabet
you want to use to the `create()` method.

Usage
-----

	var base58 = require('encdec').create() // defaults to base58
    base58.encode(1000);
    base58.decode('if');
    
    // base32 encoding
    var base32 = require('encdec').create('ABCDEFGHIJKLMNOPQRSTUVWXYZ234567');
    base32.encode(1000000);
    base32.decode('6QSA');

nodeunit
--------
[nodenunit](https://github.com/caolan/nodeunit) is used for unit testing, 
and is included in this repo as a submodule to the node_modules folder. 
To download nodeunit after cloning this repository, enter the following at
your command prompt:

    git submodule init
    git submodule update
    
The file [nodeunit](https://github.com/ianoxley/node-encdec/blob/master/nodeunit) is included as a convenience for running the nodeunit 
tests, in case you [don't want to install nodeunit as an executable](https://github.com/caolan/nodeunit#adding-nodeunit-to-your-projects).
