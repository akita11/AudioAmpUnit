# AudioAmpUnit

Heroic社のオーディオアンプHT8693を使った10Wクラスのオーディオアンプです。（※電源電圧5Vでは3W程度） Groveコネクタからのオーディオ信号を、つないだスピーカで鳴らすことができます。イネーブル端子もGroveから制御できます。M5StackでDAC出力が使いやすいようなピン配置です。スピーカ接続端子の形状で2種類あります（プリント基板自体は両者で同一です）。なおGrove端子のピン配置は「Enable/AudioIn/VDD/GND」の順ですが、オーディオ入力とイネーブル信号の配置をソルダージャンパで入れ替え可能です。

いずれも、AudioIn信号に再生したい音声信号の電圧振幅をDAC出力から与えてください。Enabe=1とすればアンプがONとなり、Enable=0でアンプはOFFとなります。


## AudioAmpUnit（3.5mmJack)

<img src="https://github.com/akita11/AudioAmpUnit/blob/main/AudioAmpU_J.jpg" width="240px">

<img src="https://github.com/akita11/AudioAmpUnit/blob/main/AudioAmpU_J2.jpg" width="240px">

φ3.5mmプラグのついたスピーカを接続可能です。ステレオスピーカではL側のみから出力されます。


## AudioAmpUnit（ねじ端子）

<img src="https://github.com/akita11/AudioAmpUnit/blob/main/AudioAmpU_S.jpg" width="240px">

<img src="https://github.com/akita11/AudioAmpUnit/blob/main/AudioAmpU_S2.jpg" width="240px">

ねじ端子（VH3.96コネクタ）にスピーカを接続して使います。

基板形状が「[M5Stack用ADCユニット[U013]](https://www.switch-science.com/products/5221)」等と同一のため、そのケースを使うことができます。


## 設定の変更

<img src="https://github.com/akita11/AudioAmpUnit/blob/main/AudioAmpU_back.jpg" width="240px">

- 動作モード: JP1を、中央-「D」をショート（デフォルトで基板パターンでショート）＝D級動作、中央-「AB」をショート＝AB級動作（D側の基板パターンをカットしてから使ってください）
- Groveコネクタのピン割当：JP４=Grove1番ピン(Gr1)。中央-「EN」（デフォルト）=Enable、中央-「AIN」=AudioIn（EN側の基板パターンをカットしてから使ってください）
- Groveコネクタのピン割当：JP4=Grove2番ピン(Gr2)。中央-「AIN」（デフォルト）=AudioIn、中央-「EN」=Enable（AudioIn側の基板パターンをカットしてから使ってください）


## Author

Junichi Akita (akita@ifdl.jp, @akita11)
