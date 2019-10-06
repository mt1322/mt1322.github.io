<html>
<head>
<style>
#map {
    width:500px;
    height:500px;
}
</style>
</head>
<body>
<?php
$check = 0;
$error = false;
if($_REQUEST['user'] != null) $check = 1;
else if ($_REQUEST['user2'] != null) $check = 2;
switch($check){
    case 0:
        echo 'Error(郵便番号か住所を入力してください。)';
        $error = true;
        break;
    case 1:
        if(!preg_match("/^[0-9]{7}$/" ,$_REQUEST['user'])){
            echo 'Error(7文字の数字を入力してください。)';
            $error = true;
        }
        else{
            $url = 'http://zipcloud.ibsnet.co.jp/api/search?zipcode='.$_REQUEST['user'];
            $json = file_get_contents($url); //json取得
            $json = mb_convert_encoding($json, 'UTF8', 'ASCII,JIS,UTF-8,EUC-JP,SJIS-WIN');
            $arr = json_decode($json,true); //jsonを配列に格納
            echo $_REQUEST['user'], '</br>';
            if($arr["results"][0]["address1"] == ''){
                echo 'Error(存在しない郵便番号です。)';
                $error = true;
            }

            $res[0] = $arr["results"][0]["address1"];
            $res[1] = $arr["results"][0]["address2"];
            $res[2] = $arr["results"][0]["address3"];
            foreach($res as $key=>$value){ //番地を除いた住所を表示
                echo $value;
            }

            /*$url2 = 'http://maps.googleapis.com/maps/api/geocode/json?sensor=false&language=ja&address='.$_REQUEST['user'];
            $json2 = file_get_contents($url2);
            $json2 = mb_convert_encoding($json2, 'UTF8', 'ASCII,JIS,UTF-8,EUC-JP,SJIS-WIN');
            $arr2 = json_decode($json2,true);
            $lat = $arr2['results'][0]['geometry']['location']['lat'];
            $lng = $arr2['results'][0]['geometry']['location']['lng'];
            echo $lat;
            echo $lng;
            */

            $url2 = "http://www.geocoding.jp/api/?q=".$_REQUEST['user'];
            $xml = simplexml_load_file($url2);
            $lat = $xml->coordinate->lat;
            $lng = $xml->coordinate->lng;

        }
        break;
    case 2:
        if(preg_match("/^[0-9]{7}$/" ,$_REQUEST['user2'])){
            echo 'Error(正しい住所を入力してください。)';
            $error = true;
        }
        else{
            $url2 = "http://www.geocoding.jp/api/?q=".$_REQUEST['user2'];
            $xml = simplexml_load_file($url2);
            if($xml->error == 001){
                    echo 'Error(正しい住所を入力してください。)';
                    $error = true;
            }
            else{
                echo $_REQUEST['user2'];
                $lat = $xml->coordinate->lat;
                $lng = $xml->coordinate->lng;
            }
        }
        break;
    default:
        break;
}
?>
</br>
<button onclick="history.back()">戻る</button>
<script src="//maps.googleapis.com/maps/api/js?key=AIzaSyA8rFw8SLuiNgw68v0nf8KdM-LNWFoig88&callback=initMap" async></script>
<script>
var map;
var marker;
var lat = parseFloat("<?php echo $lat; ?>"); //取得した緯度
var lng = parseFloat("<?php echo $lng; ?>"); //取得した経度
function initMap() {
    var error = "<?php echo $error; ?>";
    if(!error){　//$error = falseならマップ表示
        map = new google.maps.Map(document.getElementById('map'), {
            center: {
                lat: lat,
                lng: lng
            },
            zoom: 16
        });
        if(parseInt("<?php echo $check; ?>") == 2){ //住所が入力された場合マーカー表示
            marker = new google.maps.Marker({
            position: {
                lat: lat,
                lng: lng
            },
            map: map,
            });
        }
    }
}
</script>
<div id="map"></div>
</body>
</html>