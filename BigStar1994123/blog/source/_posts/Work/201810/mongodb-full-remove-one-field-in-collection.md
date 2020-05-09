---
title: 在 MongoDB Collection 內完全移除一個 Field
tags:
  - 工作
  - MongoDB
category:
  - 工作日誌
  - 2018
  - 10月
date: 2018-10-25 14:58:22
---
# Remove mongodb field from collections #

```
{ 
    name: 'book',
    tags: {
        words: ['abc','123'],
        lat: 33,
        long: 22
    }
}
```

db.example.update({}, {$unset: {tags.words:1}}, false, true);  
remove words

```
  { 
      name: 'book',
      tags: {
          lat: 33,
          long: 22
      }
  }
```

[StackOverflow : How to remove a field completely from a MongoDB document?](https://stackoverflow.com/questions/6851933/how-to-remove-a-field-completely-from-a-mongodb-document)