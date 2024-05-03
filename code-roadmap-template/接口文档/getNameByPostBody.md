# getNameByPostBody

## 接口信息
**获取名称**
- 请求方式: `POST`
- 请求地址: http://localhost:49066/api/h8nTaNyg/user/body/name

### 请求参数(Query)
|  参数名称   |  类型  |  描述  |
| :---------: | :----: |:----:|

### 请求参数(Body)
|  参数名称   |  类型  |  描述  |
| :---------: | :----: |:----:|
|    name     |  String   | 用户名  |

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
    public void testGetNameByPostBody(){
        TestPostClient testClient = TestPostClientUtil.getInstance(apiClientConfig.getAccessKey(),apiClientConfig.getSecretKey());
        Map<String,Object> query = new HashMap<>();
        GetNameByPostBodyRequest.RequestModel.Body body = new GetNameByPostBodyRequest.RequestModel.Body();
        body.setName("hjh");
        BaseResponse baseResponse = testClient.getNameByPostBody(query, JSONUtil.toJsonStr(body));
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

