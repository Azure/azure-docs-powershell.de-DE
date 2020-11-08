---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173189"
---
# <span data-ttu-id="fdf33-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf33-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="fdf33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdf33-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf33-103">Entfernt einen virtuellen Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="fdf33-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="fdf33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdf33-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdf33-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdf33-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf33-106">Entfernt einen virtuellen Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="fdf33-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="fdf33-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdf33-107">EXAMPLES</span></span>

### <span data-ttu-id="fdf33-108">Beispiel 1: Entfernen eines virtuellen Netzwerk Peerings</span><span class="sxs-lookup"><span data-stu-id="fdf33-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="fdf33-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf33-109">PARAMETERS</span></span>

### <span data-ttu-id="fdf33-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdf33-110">-AsJob</span></span>
<span data-ttu-id="fdf33-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fdf33-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdf33-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf33-112">-DefaultProfile</span></span>
<span data-ttu-id="fdf33-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdf33-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf33-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fdf33-114">-Force</span></span>
<span data-ttu-id="fdf33-115">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="fdf33-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fdf33-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fdf33-116">-Name</span></span>
<span data-ttu-id="fdf33-117">Der Name des virtuellen Netzwerk Peerings.</span><span class="sxs-lookup"><span data-stu-id="fdf33-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="fdf33-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdf33-118">-PassThru</span></span>
<span data-ttu-id="fdf33-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fdf33-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fdf33-120">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="fdf33-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fdf33-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf33-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdf33-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fdf33-122">The resource group name</span></span>

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

### <span data-ttu-id="fdf33-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fdf33-123">-VirtualNetworkName</span></span>
<span data-ttu-id="fdf33-124">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="fdf33-124">The virtual network name.</span></span>

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

### <span data-ttu-id="fdf33-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fdf33-125">-Confirm</span></span>
<span data-ttu-id="fdf33-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fdf33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdf33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf33-127">-WhatIf</span></span>
<span data-ttu-id="fdf33-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdf33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdf33-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdf33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdf33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf33-130">CommonParameters</span></span>
<span data-ttu-id="fdf33-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf33-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf33-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf33-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdf33-133">INPUTS</span></span>

### <span data-ttu-id="fdf33-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fdf33-134">System.String</span></span>

## <span data-ttu-id="fdf33-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdf33-135">OUTPUTS</span></span>

### <span data-ttu-id="fdf33-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdf33-136">System.Boolean</span></span>

## <span data-ttu-id="fdf33-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdf33-137">NOTES</span></span>

## <span data-ttu-id="fdf33-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdf33-138">RELATED LINKS</span></span>

[<span data-ttu-id="fdf33-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf33-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="fdf33-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf33-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="fdf33-141">Satz-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf33-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
