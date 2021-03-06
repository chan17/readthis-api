# 远程页面

远程页面接口用于特殊情况, 通过这个接口可以获取动态分析远程页面后得到的基础文章(base_articles)数据.

**远程页面**
* [获取远程页面](#获取远程页面)

## 获取远程页面

只有管理员能调用此接口.

### HTTP 请求

```
GET  /v2/remote-pages/:url
```

### URL 参数

参数名 | 值类型    | 描述
------ | -------- | -----------
url    | string   | 值需要 URL encode.
reload | string   | 重新抓取
bast   | string   | 抓取最优部分
all    | string   | 抓取全部
### 请求体

无

### 响应体

```
{
  title: string // 文章标题
  tags: string[] // 推荐的标签名数组, 可能为空
  summary: string // 文章摘要
  body: string // 文章的正文内容
  url: string // 文章的原文绝对地址(外部地址)
  iconUrl: string // 文章的图标绝对地址
  titleImageUrl: string[] // 题图的绝对地址数组, 可能为空
}
```
