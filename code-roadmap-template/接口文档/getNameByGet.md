# getNameByGet

## 接口信息
**获取名称**
- 请求方式: `GET`
- 请求地址: http://localhost:49066/api/h1nTWNyg/user/getName

### 请求参数(Query)
|  参数名称   |  类型  |  描述  |
| :---------: | :----: |:----:|
|    name     |  String   | 用户名  |

### 请求参数(Body)
|  参数名称   |  类型  |  描述  |
| :---------: | :----: |:----:|

### 响应参数
|  参数名称   |  类型  |  描述  |
| :---------: | :----: |:----:|
|    code     |  int   | 状态码  |
|    data     | String | 响应数据 |
|   message   | String | 响应描述 |

### 请求示例
~~~java
@Resource
    private ApiClientConfig apiClientConfig;

    @Test
    public void testUserGetName(){
        TestGetClient testGetClient = TestGetClientUtil.getInstance(apiClientConfig.getAccessKey(),apiClientConfig.getSecretKey());
        Map<String,Object> query = new HashMap<>();
        query.put("name","hjh");
        BaseResponse baseResponse = testGetClient.userGetName(query,"");
        System.out.println(baseResponse);
    }
~~~

### 响应示例

#### 成功响应示例
~~~json
{"code":"2000","data":"hjh123","msg":"The operation was successful","description":""}
~~~

#### 失败响应示例
~~~json
{}
~~~

