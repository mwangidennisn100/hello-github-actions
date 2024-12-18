$imgFile = "/var/www/imgs ..../" . $_GET['image'] . ".jpg";

header('Content-type: image/jpeg');
header('Content-Length: ' . filesize($imgFile));
$pipe = fopen($imgFile, 'rb');
fpassthru($pipe);
fclose($pipe)
