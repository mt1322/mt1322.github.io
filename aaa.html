<html>
<head>
<style>

</style>
<?php
$csv = fopen("./KEN_ALL_ROME.csv", "r");
while($line = fgetcsv($csv)){
    $line = mb_convert_encoding($line, 'UTF8', 'ASCII,JIS,UTF-8,EUC-JP,SJIS-WIN');
    $res[] = $line[0];
}
$len = count($res);
echo $res[1];
echo $len;
$number = json_encode($res);
fclose($csv);
?> 

<script>
    var num;
    var str;
    var first = 1;
    var array = [];
    var loop = true;
    function init(){
        array=JSON.parse('<?php echo $number; ?>');
    }

    function randomGen(){
        if(first == 1){
            init();
            first = 0;
        }
        do{
            num = random(0, 9999999);
            str = String(num);
            if(num < 1000000){
                var len = str.length;
                for(var i=0; i<7-len; i++){
                    str = '0'+str;
                }
            }
            array.forEach(function (value, index) {
                if(str == value) loop = false;
            });
        }
        while(loop);
        document.getElementById('textbox').value = str;
    }

    function random(min, max) {
            return Math.floor(Math.random() * (max - min));
    }
</script>
</head>

<body>
郵便番号を入力してください。(例：1234567)
<form action="bbb.html" method="post">
<input type="text" id="textbox" name="user">
<input type="submit" value="確定">
<input type="button" value="ランダム生成" onclick="randomGen()">
</form>
住所か地名を入力してください。(例：東京都墨田区押上１丁目１−２　or　東京スカイツリー)
<form action="bbb.html" method="post">
<input type="text" name="user2">
<input type="submit" value="確定">
</body>

</html>