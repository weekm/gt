<?php
$url=$_GET['url'];
$UserAgent = 'Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.0; SLCC1; .NET CLR 2.0.50727; .NET CLR 3.0.04506; .NET CLR 3.5.21022; .NET CLR 1.0.3705; .NET CLR 1.1.4322)';  
$curl = curl_init();    //创建一个新的CURL资源  
curl_setopt($curl, CURLOPT_URL, $url);  //设置URL和相应的选项  
curl_setopt($curl, CURLOPT_HEADER, 0);  //0表示不输出Header，1表示输出  
curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);  //设定是否显示头信息,1显示，0不显示。  
//如果成功只将结果返回，不自动输出任何内容。如果失败返回FALSE  
curl_setopt($curl, CURLOPT_SSL_VERIFYPEER, false);  
curl_setopt($curl, CURLOPT_SSL_VERIFYHOST, false);  
curl_setopt($curl, CURLOPT_ENCODING, '');   //设置编码格式，为空表示支持所有格式的编码  
//header中“Accept-Encoding: ”部分的内容，支持的编码格式为："identity"，"deflate"，"gzip"。  
curl_setopt($curl, CURLOPT_USERAGENT, $UserAgent);  
curl_setopt($curl, CURLOPT_FOLLOWLOCATION, 1);  
//设置这个选项为一个非零值(象 “Location: “)的头，服务器会把它当做HTTP头的一部分发送(注意这是递归的，PHP将发送形如 “Location: “的头)。  
$data = curl_exec($curl);   
//echo $data;  
//echo curl_errno($curl); //返回0时表示程序执行成功  
curl_close($curl);  //关闭cURL资源，并释放系统资源  
$a="\"bid\": \"";
$b="\",";
$x=".*";
if (preg_match("/".$a . $x . $b."/", $data,$matches)) {
    $sub_a=substr($matches[0],8);
    $sub_b=substr($sub_a,0,strlen($sub_a)-2);
    // echo "查找到匹配的字符串 ".$sub_b;
    echo "https://weibo.com/2286908003/".$sub_b."?from-page_1002062286908003_profi1e&wvr=6&mod=weibotime";
}
?>
