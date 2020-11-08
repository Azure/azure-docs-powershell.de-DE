---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167119"
---
# <span data-ttu-id="c9412-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c9412-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="c9412-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9412-102">SYNOPSIS</span></span>
<span data-ttu-id="c9412-103">Entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c9412-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c9412-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9412-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9412-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9412-105">DESCRIPTION</span></span>
<span data-ttu-id="c9412-106">Das Cmdlet **Remove-AzVMNetworkInterface** entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c9412-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c9412-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9412-107">EXAMPLES</span></span>

## <span data-ttu-id="c9412-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9412-108">PARAMETERS</span></span>

### <span data-ttu-id="c9412-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9412-109">-DefaultProfile</span></span>
<span data-ttu-id="c9412-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9412-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9412-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="c9412-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="c9412-112">Gibt ein Array von Netzwerkschnittstellen-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c9412-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9412-113">-VM</span><span class="sxs-lookup"><span data-stu-id="c9412-113">-VM</span></span>
<span data-ttu-id="c9412-114">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine Netzwerkschnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="c9412-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="c9412-115">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9412-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9412-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9412-116">-Confirm</span></span>
<span data-ttu-id="c9412-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9412-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9412-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9412-118">-WhatIf</span></span>
<span data-ttu-id="c9412-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9412-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9412-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9412-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9412-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9412-121">CommonParameters</span></span>
<span data-ttu-id="c9412-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9412-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9412-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9412-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9412-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9412-124">INPUTS</span></span>

### <span data-ttu-id="c9412-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c9412-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c9412-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9412-126">OUTPUTS</span></span>

### <span data-ttu-id="c9412-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c9412-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c9412-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9412-128">NOTES</span></span>

## <span data-ttu-id="c9412-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9412-129">RELATED LINKS</span></span>

[<span data-ttu-id="c9412-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c9412-130">Get-AzVM</span></span>](./Get-AzVM.md)


