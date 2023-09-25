# AnimeFace_Detector
Anime face detection program using OpenCV

## 概要
[こちら](https://github.com/nagadomi/lbpcascade_animeface)にあげられているアニメ顔の検出フィルタをつかったアニメ顔検出プログラム.  
幾万と先人たちのプログラムがあるので今更感が否めないが, 動画ファイルを使っているものをあまり見かけないのとOpenCVをつかった自分のポートフォリオになるので公開する.  

## 実行例
画像形式もあるが, 概要にある理由から省略.  
出力はmp4形式だが, ここでは出力されたものをgifに変換したものを載せる.  

- 実行例  
![output](https://github.com/KKawaguchi1219/AnimeFace_Detector/blob/pic/output.gif)

## 余談
google colaboratoryにて同様のプログラムを実行すると何故か編集途中でエラーが出る.  

```
エラー内容

 start
541 frames
 95%|█████████▌| 514/540 [02:33<00:07,  3.35it/s]
---------------------------------------------------------------------------
error                                     Traceback (most recent call last)
<ipython-input-10-737162b9a893> in <cell line: 20>()
     21     ret, frame = video.read()
     22     img = frame
---> 23     img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
     24     face_list = cascade.detectMultiScale(img_gray)
     25 

error: OpenCV(4.8.0) /io/opencv/modules/imgproc/src/color.cpp:182: error: (-215:Assertion failed) !_src.empty() in function 'cvtColor'
```
パッケージのバージョンが原因なのか私のプログラム自体が悪さをしているのかわからないが, 自前のAnaconda環境だとちゃんとプログラムが走ったので取り敢えず見なかったことにしている.  
