---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 247a066da4d6a8a84587e451850954df40ba7be4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946229"
---
# <span data-ttu-id="46440-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="46440-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="46440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46440-102">SYNOPSIS</span></span>
<span data-ttu-id="46440-103">Entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="46440-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="46440-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46440-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46440-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46440-105">DESCRIPTION</span></span>
<span data-ttu-id="46440-106">Das **Cmdlet Remove-AzVMNetworkInterface** entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="46440-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="46440-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46440-107">EXAMPLES</span></span>

## <span data-ttu-id="46440-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46440-108">PARAMETERS</span></span>

### <span data-ttu-id="46440-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46440-109">-DefaultProfile</span></span>
<span data-ttu-id="46440-110">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46440-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46440-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="46440-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="46440-112">Gibt ein Array von Netzwerkschnittstellen-IDs an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="46440-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="46440-113">-VM</span><span class="sxs-lookup"><span data-stu-id="46440-113">-VM</span></span>
<span data-ttu-id="46440-114">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine Netzwerkschnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="46440-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="46440-115">Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46440-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="46440-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46440-116">-Confirm</span></span>
<span data-ttu-id="46440-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46440-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46440-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46440-118">-WhatIf</span></span>
<span data-ttu-id="46440-119">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46440-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46440-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46440-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46440-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46440-121">CommonParameters</span></span>
<span data-ttu-id="46440-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46440-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46440-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46440-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46440-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46440-124">INPUTS</span></span>

### <span data-ttu-id="46440-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46440-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="46440-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46440-126">OUTPUTS</span></span>

### <span data-ttu-id="46440-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46440-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="46440-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46440-128">NOTES</span></span>

## <span data-ttu-id="46440-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46440-129">RELATED LINKS</span></span>

[<span data-ttu-id="46440-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="46440-130">Get-AzVM</span></span>](./Get-AzVM.md)


