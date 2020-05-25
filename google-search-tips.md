|   运算符   |            功能            |                  语法                  |              实例              |
| :--------: | :------------------------: | :------------------------------------: | :----------------------------: |
|    " "     |          完全匹配          |               "keyword"                |       "google 高级搜索"        |
|  +/space   |          同时匹配          | keyword1+keyword2 或 keyword1 keyword2 | github+google 或 github google |
|     -      |          排除匹配          |       keyword1+space+-+keyword2        |          github -The           |
|     OR     |           或匹配           |    keyword1+space+OR+space+keyword2    |         github OR bing         |
|     *      |          模糊匹配          |    keyword1+space+*+space+keyword2     |           搜索 * 名            |
|    site    |          站内搜索          |      site+space+url+space+keyword      |     site zhihu.com google      |
|   inurl    |   url 搜索(一个 keyword)   |             inurl:+keyword             |            inurl:go            |
|  allinurl  |   url 搜索(多个 keyword)   |       allinurl+keyword1+keyword2       |        allinurl:go com         |
|  intitle   |  title 搜索(一个 keyword)  |            intitle:keyword             |        intitle:whatever        |
| allintitle |  title 搜索(多个 keyword)  |   allintitle:keyword1+space+keyword2   |       allintitle:grpc go       |
|   intext   |  body 搜索(一个 keyword)   |             intext:keyword             |          intext:grpc           |
| allintext  |  body 搜索(多个 keyword)   |      allintext:keyword1+keyword2       |       allintext:gprc go        |
|  related   |        匹配相关网站        |           related:+space+url           |  related: https://gitlat.com   |
|    link    |          外链搜索          |               link:+url                |         link:zhihu.com         |
|  filetype  |          匹配文件          |       filetype:+fileType+keyword       |        filetype:pdf SEO        |
|   cache    | 查找 google 服务器上的缓存 |               cache:+url               |      cache:www.zhihu.com       |
|   define   |           查单词           |            define:+keyword             |        define:function         |



在 工具 中可以调制时间与语言