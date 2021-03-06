---
title: 分析W
description: C++生成见解 SDK 分析W 函数参考。
ms.date: 02/12/2020
helpviewer_keywords:
- C++ Build Insights
- C++ Build Insights SDK
- AnalyzeW
- throughput analysis
- build time analysis
- vcperf.exe
ms.openlocfilehash: 64d68e4c10c0b77c3e6b08b1ec23735e38a377a1
ms.sourcegitcommit: c123cc76bb2b6c5cde6f4c425ece420ac733bf70
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "81324162"
---
# <a name="analyzew"></a>分析W

::: moniker range="<=vs-2015"

C++构建见解 SDK 与 Visual Studio 2017 及以上版本兼容。 要查看这些版本的文档，请将本文的 Visual Studio**版本**选择器控件设置为 Visual Studio 2017 或 Visual Studio 2019。 它位于此页面的目录顶部。

::: moniker-end
::: moniker range=">=vs-2017"

该`AnalyzeW`函数用于分析从 Windows （ETW） 跟踪的输入事件跟踪读取的 MSVC 事件。

## <a name="syntax"></a>语法

```cpp
enum RESULT_CODE AnalyzeW(
    const wchar_t*             inputLogFile,
    const ANALYSIS_DESCRIPTOR* analysisDescriptor);
```

### <a name="parameters"></a>参数

*输入日志文件*\
要从中读取事件的输入 ETW 跟踪。

*分析描述符*\
指向[ANALYSIS_DESCRIPTOR](../other-types/analysis-descriptor-struct.md)对象的指针。 使用此对象配置分析。

### <a name="return-value"></a>返回值

来自[RESULT_CODE](../other-types/result-code-enum.md)枚举的结果代码。

::: moniker-end
