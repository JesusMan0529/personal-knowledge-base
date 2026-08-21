#Markdown
## 行内代码

`printf()` 函数

## 特殊字符转义

**使用双反引号包围单反引号**

``使用双反引号包围 `单反引号` ``

```包含 `` 双反引号的代码``` 

规则：外层反引号的数量必须**多于**内容中连续反引号的最大数量。

## 代码区块

**缩进式代码块**

代码区块使用 **4 个空格**或者一个**制表符（Tab 键）**。

正常文本段落

	这是缩进式代码块
    每行前面有四个空格
    保持代码的原始格式

继续正常文本

**三反引号代码块**

```
多行代码内容
可以包含空行
保持原有缩进

注意事项：不指定语言时不支持语法高亮。
```

**JavaScript**
```javascript
const users = [
    { name: "Alice", age: 25 },
    { name: "Bob", age: 30 }
];

const adults = users.filter(user => user.age >= 18);
console.log(adults);
```

**Python**
```python
def calculate_area(radius):
    """计算圆的面积"""
    import math
    return math.pi * radius ** 2

# 使用函数
area = calculate_area(5)
print(f"圆的面积是: {area:.2f}")
```

**SQL**
```sql
SELECT u.name, u.email, COUNT(o.id) as order_count
FROM users u
LEFT JOIN orders o ON u.id = o.user_id
WHERE u.created_at >= '2024-01-01'
GROUP BY u.id, u.name, u.email
ORDER BY order_count DESC
LIMIT 10;
```

## 代码差异对比

**Diff 语法**
```diff
function calculateTotal(items) {
-	let total = 0;
+   let total = 0.0;
    
    for (let item of items) {
-       total += item.price;
+       total += parseFloat(item.price);
    }
    
+   // 保留两位小数
+   total = Math.round(total * 100) / 100;
    return total;
}
```
```diff
@@ -1,5 +1,8 @@
 function greetUser(name) {
-    console.log("Hello " + name);
+    if (!name) {
+        throw new Error("Name is required");
+    }
+    console.log(`Hello, ${name}!`);
 }
```