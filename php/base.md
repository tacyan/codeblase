# phpの基礎構文などを書く


## 呼び出し方

```
<?php
    // 関数の定義
    /*
    function 関数名(引数) {
        処理
    }
    */
    function samplefunc($a) {
        print $a;
    }

    // 関数の呼び出し
    // 関数名(引数);
    $word = "PHPのキソ";
    samplefunc($word);
?>
```

## 基礎文法

```
<?php
    $a = 0;

    while ($a < 5) {
        print '最初の$aの値は'.$a.'です。<br />';
        $a++;
        print '++演算子で$aの値は'.$a.'になりました。<br />';

        // 奇数だったらという条件
        if ($a % 2 == 1) {
            print 'continueでこの処理を中断し、次の回の繰り返しを実行<br /><br />';
            continue;
        }

        print '最後の$aの値は'.$a.'です。<br /><br />';
    }
?>
```

## 配列ループ

```
<?php
    // 図のような配列を作ります。
    $shiki = array(
                "spr" => "春",
                "sum" => "夏",
                "aut" => "秋",
                "win" => "冬",);

    // 配列の添字と値を繰り返し処理で表示します。
    foreach ($shiki as $key => $name) {
        print $key."は".$name."<br />";
    }
?>
```
## 2重ループ

```
<?php
    // 外側のループ
    for ($a = 0; $a <= 3; $a++) {
        print '■ここは外側のループです。';
        print '$aの値は'.$a.'です<br />';

        // 内側のループ
        for ($i = 0; $i <= 3; $i++) {
            print '○ここは内側のループです。';
            print '$iの値は'.$i.'です<br />';
        }
    }
?>
```

