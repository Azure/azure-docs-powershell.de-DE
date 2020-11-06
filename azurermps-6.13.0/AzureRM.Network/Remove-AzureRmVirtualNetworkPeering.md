---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 73e4fb2dde10739176a1adfe55c22529e8ccdaaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482230"
---
# <span data-ttu-id="2fe19-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2fe19-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="2fe19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fe19-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe19-103">Entfernt einen virtuellen Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="2fe19-103">Removes a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fe19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fe19-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fe19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fe19-105">DESCRIPTION</span></span>
<span data-ttu-id="2fe19-106">Entfernt einen virtuellen Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="2fe19-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="2fe19-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fe19-107">EXAMPLES</span></span>

### <span data-ttu-id="2fe19-108">Beispiel 1: Entfernen eines virtuellen Netzwerk Peerings</span><span class="sxs-lookup"><span data-stu-id="2fe19-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="2fe19-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fe19-109">PARAMETERS</span></span>

### <span data-ttu-id="2fe19-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fe19-110">-AsJob</span></span>
<span data-ttu-id="2fe19-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2fe19-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fe19-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe19-112">-DefaultProfile</span></span>
<span data-ttu-id="2fe19-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fe19-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe19-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2fe19-114">-Force</span></span>
<span data-ttu-id="2fe19-115">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2fe19-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fe19-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2fe19-116">-Name</span></span>
<span data-ttu-id="2fe19-117">Der Name des virtuellen Netzwerk Peerings.</span><span class="sxs-lookup"><span data-stu-id="2fe19-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="2fe19-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fe19-118">-PassThru</span></span>
<span data-ttu-id="2fe19-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2fe19-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2fe19-120">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2fe19-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2fe19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe19-121">-ResourceGroupName</span></span>
<span data-ttu-id="2fe19-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2fe19-122">The resource group name</span></span>

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

### <span data-ttu-id="2fe19-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2fe19-123">-VirtualNetworkName</span></span>
<span data-ttu-id="2fe19-124">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="2fe19-124">The virtual network name.</span></span>

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

### <span data-ttu-id="2fe19-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fe19-125">-Confirm</span></span>
<span data-ttu-id="2fe19-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fe19-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe19-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fe19-127">-WhatIf</span></span>
<span data-ttu-id="2fe19-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fe19-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fe19-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fe19-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe19-130">CommonParameters</span></span>
<span data-ttu-id="2fe19-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe19-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe19-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe19-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fe19-133">INPUTS</span></span>

### <span data-ttu-id="2fe19-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2fe19-134">System.String</span></span>

## <span data-ttu-id="2fe19-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fe19-135">OUTPUTS</span></span>

### <span data-ttu-id="2fe19-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fe19-136">System.Boolean</span></span>

## <span data-ttu-id="2fe19-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fe19-137">NOTES</span></span>

## <span data-ttu-id="2fe19-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fe19-138">RELATED LINKS</span></span>
