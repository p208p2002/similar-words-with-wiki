# 維基關鍵字配對
- 使用維基百科資料配對關鍵字

# 使用
- 下載維基資料包放置在wikidata底下
> [維基資料包下載](https://github.com/p208p2002/key-match-with-wiki/releases/tag/0.0.1)

- 引入KeyMatch
```python
from KeyMatch import KeyMatch
km = KeyMatch()
```

- 切割檔案，進行預處理(只有在第一次使用需要)

```python
km.split(jsonDataPath = jsonFile, blackFlags = blackFlags)
# jsonDataPath:str 欲切割的wikijson file
# blackFlags:list 欲過濾的詞性
# 詞性列表 https://gist.github.com/luw2007/6016931
```
> 也有[切割好的檔案](https://github.com/p208p2002/key-match-with-wiki/releases/tag/0.0.2)，放置在splitdata底下即可使用

- 進行關鍵字配對

```python
km.match(key = key, blackWords = blackWords)
# key:str 關鍵字
# blackWords:list 過濾字
```

- 取得結果

```python
km.getTop(n)
# n:int 筆數
```

# 範例輸出
```
# key = 台灣

[('臺灣', 7), ('誌', 6), ('仙', 5), ('木本植物', 4), ('嘉義', 3), ('天', 3), ('植物', 3), ('嘉義市', 2), ('本地', 2), ('破', 2), ('澳洲', 2), ('腺葉野', 2), ('櫻', 2), ('廣州', 2), ('腺葉', 2), ('稠李', 2), ('拉漢', 2), ('種子植物', 2), ('名稱', 2), ('墨點', 2), ('櫻桃', 2), ('劉業經', 2), ('黑星櫻', 2), ('李惠林', 2), ('
刺葉桂櫻', 2), ('震央', 2), ('面臨', 2), ('中部地區', 1), ('開採', 1), ('日本時代', 1), ('嘉義車站', 1), ('北門車站', 1), ('檜意森活村', 1), ('嘉義市立博物館', 1), ('嘉義市立文化中心', 1), ('文化局', 1), ('交趾陶', 1), ('館', 1), ('文化中心', 1), ('文化創意產業', 1)]
```
```
# key = 蔡依林

[('歌曲', 256), ('專輯', 242), ('巡迴演唱', 192), ('上海站', 164), ('臺灣歌手', 154), ('音樂', 116), ('臺灣', 111), ('演唱會', 88), ('歌手', 80), ('表演', 74), ('MV', 64), ('zh', 60), ('單曲', 59), ('排行榜', 57), ('嘉賓', 51), ('錄音室專輯', 50), ('唱片', 46), ('演唱', 45), ('羅志祥', 42), ('場次', 40), ('周杰倫', 37), ('Play', 34), ('上海', 34), ('藝人', 33), ('張惠妹', 31), ('唱片公司', 30), ('媒體', 30), ('舞蹈', 30), ('冠軍', 29), ('收錄於', 29), ('臺北', 28), ('電影', 27), ('E', 26), ('級', 26), ('S', 25), ('女歌手', 25), ('舞曲', 25), ('香港', 24), ('美國', 23), ('安可', 23)]
```



