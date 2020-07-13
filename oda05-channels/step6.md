Now, lets review in settings.js file in a bit more detail as you will be modifying it.

The first few functions: mockApiCall, generateJWTToken and generateToken are a starting point in case you want to enforce client authentication in your channel, so you can ignore it for this hands-on.
As we are ignoring, or not enabling client authentication, you have to make sure that 'isClientAuthEnabled' is set to false.
<pre><code>
	4 const isClientAuthEnabled = false;
</code></pre>