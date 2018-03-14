# tencentyun-img
腾讯云-万象优图人脸识别检测


使用方法

use QcloudImage\CIClient;
$img = 'F:\phpStudy\WWW\test66\mayun.jpg';//需要检测的照片
			
$appid = '11111';
$secretId = '222222';
$secretKey = '33333';
$bucket = '44444';

$client = new CIClient($appid, $secretId, $secretKey, $bucket);
$client->setTimeout(5);  
$res = $client->faceDetect(array('file'=>$img),1);
$res = json_decode($res,true);
var_dump($res);
