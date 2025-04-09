# suninfo
A wrapper for PHP's native sun_info including solstice times.

version 1.1

date: 2025-04-09

## usage
```
$timestamp = time();
$latitude = -0.4319317;
$longitude = 51.5286051;

include {path to suninfo} . '/suninfo.php';
$suninfo = new \basecamp\suninfo($timestamp, $latitude, $longitude);

print_r($suninfo->info);
foreach($suninfo->solstices as $event) {
	echo implode("\t", $event) . "\n";
}
```

See `example.php` for a better example.
