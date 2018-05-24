JS命名规范

原则：
1. 命名清晰、精炼、见名知义。 *****
2. 复用常见命名词, 依循已成型命名词汇(is/can/get/set)/结构(驼峰)。 ****
3. 非常见业务命名汇，对应英文词汇，要求尽量简约（英文简写）而不失其义（重）。 **
4. 特殊情况(第三条不能满足，第一条)，可使用 中文简写结构： ***
    例如： 百度地图 => baidudt
           前端客   => qianduank
    描述： 前两个汉中文全拼 + 首字母
5. 其它视情况而定。

命名结构

### 变量(驼峰结构)/常量(MAX_HEIGHT 结构)
- 量词 + 名词 ： maxPrice、 minPrice
- 判断型/询问性(boolean)前缀：
    - can + 动作： canJump == 能否
    - is + 值： isLogin == 是否是某个值
    - has + 值： hasChild == 是否存在

- 方法名
    - 整体结构：
        - onXXX onClick 事件名方法(监听)
        - getXXX ( action方法/普通方法 )
        - callGetXXX (api 调用 )
    - 常见动作类词汇：
        - 获取 get / load
        - 设值： set / update
        - 打开关闭
            open / close
        - 删除
            del / delete
        - 提交
            commit 、 submit
        -  jump
        -  loop
        -  scroll

原则规范：
- 方法具有行为性，除常见定型结构， 整体结构应遵循 动 + 名 结合方式。
-