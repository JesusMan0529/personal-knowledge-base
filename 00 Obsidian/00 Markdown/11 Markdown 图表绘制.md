#Markdown
#### 常见的 Markdown 图表工具

**Mermaid**

Mermaid 是最流行的 Markdown 图表工具之一，它允许你使用简单的文本语法生成各种图表。

**支持图表类型**

- 流程图 (Flowchart)
- 序列图 (Sequence Diagram)
- 类图 (Class Diagram)
- 状态图 (State Diagram)
- 甘特图 (Gantt Chart)
- 饼图 (Pie Chart)

#### 流程图

```mermaid
graph TB
    A[开始] --> B{条件判断}
    B -->|Yes| C[执行操作A]
    B -->|No| D[执行操作B]
    C --> E[结束]
    D --> E
```

**流程图方向**

- `TB`：从上到下
- `BT`：从下到上
- `RL`：从右到左
- `LR`：从左到右

**节点形状**

- `A[方形]`：矩形
- `B(圆角矩形)`：圆角矩形
- `C{菱形}`：菱形（决策）
- `D((圆形))`：圆形
- `E>旗帜形]`：旗帜形

**连接线类型**

- `-->` 实线箭头
- `-.->` 虚线箭头
- `==>` 粗实线箭头
- `---` 实线
- `-.-` 虚线

#### 时序图和甘特图

##### 时序图

```mermaid
sequenceDiagram
    participant A as 用户
    participant B as 系统
    participant C as 数据库
    
    A->>B: 登录请求 
    B->>C: 验证用户信息
    C-->>B: 返回验证结果
    B-->>A: 登录成功/失败
```

**时序图语法要点**

- `participant` 定义参与者
- `->>` 实线箭头
- `-->>` 虚线箭头
- `note` 添加注释

##### 甘特图

```mermaid
gantt
    title 项目开发计划
    dateFormat YYYY-MM-DD
    section 设计阶段
    需求分析: done, des1, 2024-01-01, 2024-01-15
    UI设计: active, des2, 2024-01-10, 30d
    section 开发阶段
    前端开发: dev1, after des2, 45d
    后端开发: dev2, 2024-02-01, 60d
    section 测试阶段
    单元测试: test1, after dev1, 15d
    集成测试: test2, after dev2, 10d
```

**通用结构**

`任务名称: 状态, 任务ID, 开始时间, 结束时间`

**甘特图语法要点**

- `title` 设置标题
- `dateFormat` 定义日期格式
- `section` 定义阶段
- 任务状态：`done`（已完成）、`active`（进行中）、`crit`（关键）

#### 饼图

```mermaid
pie
    title 浏览器市场份额
    "Chrome" : 65
    "Safari" : 15
    "Firefox" : 10
    "其他" : 10
```


#### 图表类型

1. 流程图（graph）
2. 时序图（sequenceDiagram）
3. 甘特图（gantt）
4. 饼图（pie）
5. 类图（classDiagram）
```mermaid
classDiagram
    class 用户 {
        用户名: string
        密码: string
        登录()
    }
    
    class 订单 {
        订单号: int
        创建日期: date
        计算总价()
    }
    
    用户 --> 订单
```

#### 参考官方文档

- [Mermaid 官方文档](https://mermaid.js.org/)