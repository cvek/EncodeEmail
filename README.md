EncodeEmail
===========

This library allows to encode email addresses in a HTML source.
So it helps to protect your email addresses against spam robots.

To use the lib, you need to get a HTML source before sending it to client side.
Then you encode it:

    $output = HEmailEncode::encodeHtmlSrc($output);
    
For yii framework, it can be done in the CController::processOutput method:

    public function processOutput($output) {
      $output = parent::processOutput($output);
      return HEmailEncode::encodeHtmlSrc($output);
    }

It's recommended to cache the results to avoid repeating this procedure and save resources of your server.
