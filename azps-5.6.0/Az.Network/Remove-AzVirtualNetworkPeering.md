---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: f47b1bcc571337de8a64c591383367568cf7d67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940032"
---
# <span data-ttu-id="e57ec-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e57ec-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e57ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e57ec-102">SYNOPSIS</span></span>
<span data-ttu-id="e57ec-103">Entfernt ein virtuelles Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="e57ec-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e57ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e57ec-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e57ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e57ec-105">DESCRIPTION</span></span>
<span data-ttu-id="e57ec-106">Entfernt ein virtuelles Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="e57ec-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e57ec-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e57ec-107">EXAMPLES</span></span>

### <span data-ttu-id="e57ec-108">Beispiel 1: Entfernen eines Peerings für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e57ec-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e57ec-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e57ec-109">PARAMETERS</span></span>

### <span data-ttu-id="e57ec-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e57ec-110">-AsJob</span></span>
<span data-ttu-id="e57ec-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e57ec-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57ec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57ec-112">-DefaultProfile</span></span>
<span data-ttu-id="e57ec-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e57ec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e57ec-114">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e57ec-114">-Force</span></span>
<span data-ttu-id="e57ec-115">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="e57ec-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57ec-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e57ec-116">-Name</span></span>
<span data-ttu-id="e57ec-117">Der Name des peering virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="e57ec-117">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57ec-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e57ec-118">-PassThru</span></span>
<span data-ttu-id="e57ec-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e57ec-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e57ec-120">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e57ec-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="e57ec-122">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e57ec-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57ec-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e57ec-123">-VirtualNetworkName</span></span>
<span data-ttu-id="e57ec-124">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="e57ec-124">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57ec-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e57ec-125">-Confirm</span></span>
<span data-ttu-id="e57ec-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e57ec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e57ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e57ec-127">-WhatIf</span></span>
<span data-ttu-id="e57ec-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e57ec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e57ec-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e57ec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e57ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57ec-130">CommonParameters</span></span>
<span data-ttu-id="e57ec-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57ec-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57ec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57ec-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e57ec-133">INPUTS</span></span>

### <span data-ttu-id="e57ec-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e57ec-134">System.String</span></span>

## <span data-ttu-id="e57ec-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e57ec-135">OUTPUTS</span></span>

### <span data-ttu-id="e57ec-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e57ec-136">System.Boolean</span></span>

## <span data-ttu-id="e57ec-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e57ec-137">NOTES</span></span>

## <span data-ttu-id="e57ec-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e57ec-138">RELATED LINKS</span></span>

[<span data-ttu-id="e57ec-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e57ec-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e57ec-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e57ec-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e57ec-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e57ec-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
