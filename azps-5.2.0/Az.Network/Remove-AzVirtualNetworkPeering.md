---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300592"
---
# <span data-ttu-id="221d3-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="221d3-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="221d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="221d3-102">SYNOPSIS</span></span>
<span data-ttu-id="221d3-103">Entfernt ein virtuelles Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="221d3-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="221d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="221d3-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="221d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="221d3-105">DESCRIPTION</span></span>
<span data-ttu-id="221d3-106">Entfernt ein virtuelles Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="221d3-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="221d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="221d3-107">EXAMPLES</span></span>

### <span data-ttu-id="221d3-108">Beispiel 1: Entfernen eines virtuellen Netzwerk peerings</span><span class="sxs-lookup"><span data-stu-id="221d3-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="221d3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="221d3-109">PARAMETERS</span></span>

### <span data-ttu-id="221d3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="221d3-110">-AsJob</span></span>
<span data-ttu-id="221d3-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="221d3-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="221d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="221d3-112">-DefaultProfile</span></span>
<span data-ttu-id="221d3-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="221d3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="221d3-114">-Force</span><span class="sxs-lookup"><span data-stu-id="221d3-114">-Force</span></span>
<span data-ttu-id="221d3-115">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="221d3-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="221d3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="221d3-116">-Name</span></span>
<span data-ttu-id="221d3-117">Der Name des virtuellen Netzwerk-Peerings.</span><span class="sxs-lookup"><span data-stu-id="221d3-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="221d3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="221d3-118">-PassThru</span></span>
<span data-ttu-id="221d3-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="221d3-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="221d3-120">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="221d3-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="221d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="221d3-121">-ResourceGroupName</span></span>
<span data-ttu-id="221d3-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="221d3-122">The resource group name</span></span>

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

### <span data-ttu-id="221d3-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="221d3-123">-VirtualNetworkName</span></span>
<span data-ttu-id="221d3-124">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="221d3-124">The virtual network name.</span></span>

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

### <span data-ttu-id="221d3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="221d3-125">-Confirm</span></span>
<span data-ttu-id="221d3-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="221d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="221d3-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="221d3-127">-WhatIf</span></span>
<span data-ttu-id="221d3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="221d3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="221d3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="221d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="221d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="221d3-130">CommonParameters</span></span>
<span data-ttu-id="221d3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="221d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="221d3-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="221d3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="221d3-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="221d3-133">INPUTS</span></span>

### <span data-ttu-id="221d3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="221d3-134">System.String</span></span>

## <span data-ttu-id="221d3-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="221d3-135">OUTPUTS</span></span>

### <span data-ttu-id="221d3-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="221d3-136">System.Boolean</span></span>

## <span data-ttu-id="221d3-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="221d3-137">NOTES</span></span>

## <span data-ttu-id="221d3-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="221d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="221d3-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="221d3-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="221d3-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="221d3-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="221d3-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="221d3-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
