# suninfo
A wrapper for PHP's native sun_info including soltice times.

## usage
```
$timestamp = time();
$latitude = -0.4319317;
$longitude = 51.5286051;
$dtz = new \DateTimeZone('Europe/London');

// get sun-info
include {path to suninfo} . '/suninfo.php';
$suninfo = new \basecamp\suninfo($timestamp, $latitude, $longitude);

print_r($suninfo->info);
foreach($suninfo->solstices as $event) {
	echo implode("\t", $event) . "\n";
}
```
