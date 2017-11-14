# curl-helper-php
PHP Curl Class to make curl easy to use.

Example : 
1. Include the file.

2. Create an instance of the class.

$ch = new PHPCurl();

$url = 'http://maps.googleapis.com/maps/api/geocode/json?address='.urlencode(@$location).'&sensor=false';

$curlData = array();

$ch = new PHPCurl();

$result = $ch->execute("GET", $url, $curlData);

$result = json_decode($result->body, true);

There will be two index in $result, 1. "body" which is json encoded format (if applicable), and 2nd is "bodyRaw" containing raw response from curl.



Make sure that CURL is installed and Enabled.
