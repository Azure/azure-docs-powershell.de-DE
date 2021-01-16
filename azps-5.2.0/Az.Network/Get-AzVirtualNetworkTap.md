---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361107"
---
# <span data-ttu-id="32d6e-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="32d6e-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="32d6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="32d6e-103">Ruft die Anzapfung eines virtuellen Netzwerks ab</span><span class="sxs-lookup"><span data-stu-id="32d6e-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="32d6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32d6e-104">SYNTAX</span></span>

### <span data-ttu-id="32d6e-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="32d6e-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32d6e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32d6e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32d6e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32d6e-107">DESCRIPTION</span></span>
<span data-ttu-id="32d6e-108">Das **Cmdlet "Get-AzVirtualNetworkTap"** ruft ein Anzapfen des virtuellen Azure-Netzwerks oder eine Liste der virtuellen Azure-Netzwerktipps in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="32d6e-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="32d6e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32d6e-109">EXAMPLES</span></span>

### <span data-ttu-id="32d6e-110">Beispiel 1: Anzapfen in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="32d6e-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="32d6e-111">Dieser Befehl ruft einen VirtualNetwork-Tippverweis für bestimmte "VirtualTap1" in "ResourceGroup1" ab.</span><span class="sxs-lookup"><span data-stu-id="32d6e-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="32d6e-112">Beispiel 2: Alle tippenden virtuellen Netzwerke mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="32d6e-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="32d6e-113">Dieser Befehl ruft alle VirtualNetwork-Tippverweise ab, die mit "VirtualTap" beginnen.</span><span class="sxs-lookup"><span data-stu-id="32d6e-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="32d6e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32d6e-114">PARAMETERS</span></span>

### <span data-ttu-id="32d6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d6e-115">-DefaultProfile</span></span>
<span data-ttu-id="32d6e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32d6e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32d6e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="32d6e-117">-Name</span></span>
<span data-ttu-id="32d6e-118">Der Name des Tippens.</span><span class="sxs-lookup"><span data-stu-id="32d6e-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="32d6e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d6e-119">-ResourceGroupName</span></span>
<span data-ttu-id="32d6e-120">Der Ressourcengruppenname des Anzapfens des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="32d6e-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="32d6e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32d6e-121">-ResourceId</span></span>
<span data-ttu-id="32d6e-122">ResourceId der VirtualNetworkTap-Ressource</span><span class="sxs-lookup"><span data-stu-id="32d6e-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32d6e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32d6e-123">-Confirm</span></span>
<span data-ttu-id="32d6e-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32d6e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d6e-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="32d6e-125">-WhatIf</span></span>
<span data-ttu-id="32d6e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32d6e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32d6e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32d6e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d6e-128">CommonParameters</span></span>
<span data-ttu-id="32d6e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d6e-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32d6e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d6e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32d6e-131">INPUTS</span></span>

### <span data-ttu-id="32d6e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="32d6e-132">System.String</span></span>

## <span data-ttu-id="32d6e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32d6e-133">OUTPUTS</span></span>

### <span data-ttu-id="32d6e-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="32d6e-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="32d6e-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="32d6e-135">NOTES</span></span>

## <span data-ttu-id="32d6e-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="32d6e-136">RELATED LINKS</span></span>

[<span data-ttu-id="32d6e-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="32d6e-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="32d6e-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="32d6e-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="32d6e-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="32d6e-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
