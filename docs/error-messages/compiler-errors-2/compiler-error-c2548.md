---
title: 编译器错误 C2548
ms.date: 11/04/2016
f1_keywords:
- C2548
helpviewer_keywords:
- C2548
ms.assetid: 01e9c835-9bf3-4020-9295-5ee448c519f3
ms.openlocfilehash: f89208314c1d2e8ddb5100da72aa600a411b4608
ms.sourcegitcommit: 16fa847794b60bf40c67d20f74751a67fccb602e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2019
ms.locfileid: "74756794"
---
# <a name="compiler-error-c2548"></a>编译器错误 C2548

"class：： member"：缺少参数参数的默认参数

默认参数列表缺少参数。 如果在参数列表中的任意位置提供默认参数，则必须为所有后续参数定义默认参数。

## <a name="example"></a>示例

下面的示例生成 C2548：

```cpp
// C2548.cpp
// compile with: /c
void func( int = 1, int, int = 3);  // C2548

// OK
void func2( int, int, int = 3);
void func3( int, int = 2, int = 3);
```
