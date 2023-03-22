# 題目6. 季節判定
### 問題描述：
試撰寫一程式，可輸入月份，然後判斷其所屬的季節（ 3~5 月為春季，6~8 月為夏季， 9~11 月為秋季， 12~2 月為冬季）。

### 輸入說明：
輸入月份。
### 輸出說明：
輸出該月份的季節， 3~5 月為春季(Spring)， 6~8 月為夏季(Summer)， 9~11 月為秋季(Autumn)， 12~2 月為冬季(Winter)。

### 範例：
#### 輸入範例:
3

10

#### 輸出範例:
Spring

Autumn

### 解答
```
#include <iostream>
using namespace std;
int main()
{
    int start1 = 0, start2 = 0, end1 = 0, end2 = 0, time = 0, cash = 0;
    cin >> start1 >> start2;
    cin >> end1 >> end2;

    time = (end1 * 60 + end2) - (start1 * 60 + start2);

    if (time <= 120 && time > 0) {

        cash = (time / 30) * 30;
    }
    else if (time > 120 && time <= 240) {

        cash = 120 + (time - 120) / 30 * 40;

    }
    else {

        cash = 120 + 160 + (time - 240) / 30 * 60;

    }

    cout << cash << endl;

    return 0;
}
```
