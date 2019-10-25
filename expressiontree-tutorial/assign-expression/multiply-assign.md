---
PermaID: 10010012
---

# MultiplyAssign

You can build an expression tree which contains a multiplication assignment operation using `Expression.MultiplyAssign` method. For example, you have the following code.

```csharp
int myInt;
myInt = 12;
myInt *= 5;
Console.WriteLine(myInt);
```

Here is the code that is required to build the same functionality using expression tree. 

```csharp
ParameterExpression myIntVariableExpr = Expression.Variable(typeof(int), "myInt");

BlockExpression addAssignExpr = Expression.Block(
    new ParameterExpression[] { myIntVariableExpr },
    Expression.Assign(myIntVariableExpr, Expression.Constant(12)),
    Expression.MultiplyAssign(
        myIntVariableExpr,
        Expression.Constant(5)
    )
);

Console.WriteLine(Expression.Lambda<Func<int>>(addAssignExpr).Compile()());
```

[Try it online](https://dotnetfiddle.net/Aeyne0)