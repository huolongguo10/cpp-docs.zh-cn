---
title: __vmx_vmresume
ms.date: 09/02/2019
f1_keywords:
- __vmx_vmresume
helpviewer_keywords:
- __vmx_vmresume intrinsic
- VMRESUME instruction
ms.assetid: 233fe1b6-c727-493a-a484-1b2363732281
ms.openlocfilehash: 34d0e6814dd00da07076e644513400bd5be36bd3
ms.sourcegitcommit: 6e1c1822e7bcf3d2ef23eb8fac6465f88743facf
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70219453"
---
# <a name="__vmx_vmresume"></a>__vmx_vmresume

**Microsoft 专用**

通过使用当前虚拟机控件结构 (VMCS) 恢复 VMX 非根操作。

## <a name="syntax"></a>语法

```C
unsigned char __vmx_vmresume(
   void);
```

## <a name="return-value"></a>返回值

|值|含义|
|-----------|-------------|
|0|操作成功。|
|1|操作失败，当前 VMCS 的 `VM-instruction error field` 中提供了扩展状态。|
|2|操作失败，无可用状态。|

## <a name="remarks"></a>备注

应用程序可以通过使用 [__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md) 或 `__vmx_vmresume` 函数执行 VM 输入操作。 `__vmx_vmlaunch` 函数只可用于启动状态为 `Clear`的 VMCS，而 `__vmx_vmresume` 函数只可用于启动状态为 `Launched`的 VMCS。 因此，使用 [__vmx_vmclear](../intrinsics/vmx-vmclear.md) 函数将 VMCS 的启动状态设置为 `Clear`，然后对第一个 VM 输入操作使用 `__vmx_vmlaunch` 函数，对后续 VM 输入操作使用 `__vmx_vmresume` 函数。

`__vmx_vmresume` 函数等同于 `VMRESUME` 计算机指令。 此函数支持主机的虚拟机监视器与来宾操作系统及其应用程序进行交互。 有关详细信息，请在 [Intel Corporation](https://software.intel.com/articles/intel-sdm) 站点搜索 PDF 文档“适用于 IA-32 Intel 架构的 Intel 虚拟化技术规范”，文档编号 C97063-002。

## <a name="requirements"></a>要求

|内部函数|体系结构|
|---------------|------------------|
|`__vmx_vmresume`|X64|

**标头文件**\<intrin.h >

**结束 Microsoft 专用**

## <a name="see-also"></a>请参阅

[编译器内部函数](../intrinsics/compiler-intrinsics.md)\
[__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md)\
[__vmx_vmclear](../intrinsics/vmx-vmclear.md)
