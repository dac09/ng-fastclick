# NOTE
Forked version with a fix for disabling fastclick with the class `needsclick`. Although this is supposed to be a normal fast click feature, it doesn't seem to work in the official library at the time of writing.

Uses my [fork of FT's Fastclick](https://github.com/dac09/fastclick)

This helps with e.g. select boxes on iOS 8 by adding the required class. Older versions of iOS don't seem to show this problem.
You can use it on any dom element though.
#### Example
```
<select class="needsfix">
	<option value="1">One</option>
	<option value="2">Two</option>
</select>
```
This will disable fast click for the select box, so that it does not autoclose or jump to the next input on iOS 8 (Cordova/Phonegap and Safari).


# ng-fastclick + needsclick fix

This is a very thin (3 line!) Angular wrapper around the [FT's](https://github.com/ftlabs) fantastic [FastClick](https://github.com/ftlabs/fastclick)

## Installation

In your Angular project, run `bower install --save ng-fastclick` to save the
module. Then, in your HTML, add:

``` html
<script src="/path/to/bower_components/ng-fastclick/dist/index.min.js"></script>
```

And lastly, in your Angular module, include `ng-fastclick` as a dependency:

``` javascript
angular.module('my-app', ['ng-fastclick'])
```

