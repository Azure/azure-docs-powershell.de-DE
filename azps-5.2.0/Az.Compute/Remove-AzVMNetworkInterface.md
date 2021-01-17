---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308067"
---
# <span data-ttu-id="d8f3d-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d8f3d-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="d8f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f3d-103">Entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="d8f3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8f3d-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f3d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8f3d-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f3d-106">Das **Cmdlet "Remove-AzVMNetworkInterface"** entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="d8f3d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8f3d-107">EXAMPLES</span></span>

## <span data-ttu-id="d8f3d-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8f3d-108">PARAMETERS</span></span>

### <span data-ttu-id="d8f3d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f3d-109">-DefaultProfile</span></span>
<span data-ttu-id="d8f3d-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8f3d-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="d8f3d-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="d8f3d-112">Gibt ein Array von Netzwerkschnittstellen-IDs an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d8f3d-113">-VM</span><span class="sxs-lookup"><span data-stu-id="d8f3d-113">-VM</span></span>
<span data-ttu-id="d8f3d-114">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine Netzwerkschnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="d8f3d-115">Verwenden Sie zum Abrufen eines Objekts für einen virtuellen Computer das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="d8f3d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8f3d-116">-Confirm</span></span>
<span data-ttu-id="d8f3d-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f3d-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d8f3d-118">-WhatIf</span></span>
<span data-ttu-id="d8f3d-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8f3d-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f3d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f3d-121">CommonParameters</span></span>
<span data-ttu-id="d8f3d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f3d-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f3d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f3d-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8f3d-124">INPUTS</span></span>

### <span data-ttu-id="d8f3d-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d8f3d-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d8f3d-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8f3d-126">OUTPUTS</span></span>

### <span data-ttu-id="d8f3d-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d8f3d-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d8f3d-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8f3d-128">NOTES</span></span>

## <span data-ttu-id="d8f3d-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8f3d-129">RELATED LINKS</span></span>

[<span data-ttu-id="d8f3d-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d8f3d-130">Get-AzVM</span></span>](./Get-AzVM.md)


