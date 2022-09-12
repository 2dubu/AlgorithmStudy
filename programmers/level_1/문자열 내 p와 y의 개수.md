## 문제 설명

문자열 s의 길이가 4 혹은 6이고, 숫자로만 구성돼있는지 확인해주는 함수, solution을 완성하세요. 예를 들어 s가 "a234"이면 False를 리턴하고 "1234"라면 True를 리턴하면 됩니다.대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요. 'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다. 단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.

예를 들어 s가 "pPoooyY"면 true를 return하고 "Pyy"라면 false를 return합니다.

</br>

## 제한 사항

- 문자열 s의 길이 : 50 이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.

</br>

## 예시

**입출력 예**

|     s     | answer |
| :-------: | :----: |
| "pPoooyY" |  true  |
|   "Pyy"   | false  |

##### 입출력 예 설명

**입출력 예 #1**
'p'의 개수 2개, 'y'의 개수 2개로 같으므로 true를 return 합니다.

**입출력 예 #2**
'p'의 개수 1개, 'y'의 개수 2개로 다르므로 false를 return 합니다.

</br>

## Solution

```swift
func solution(_ s:String) -> Bool {
    
    var count = 0
    
    for i in s.lowercased() {
        if i == "p" {
            count += 1
        } else if i == "y" {
            count -= 1
        }
    }
    
    return count == 0
}
```

