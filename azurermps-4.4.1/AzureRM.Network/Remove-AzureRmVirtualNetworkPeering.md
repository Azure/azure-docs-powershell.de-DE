---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665260"
---
# <span data-ttu-id="76669-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="76669-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="76669-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76669-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76669-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="76669-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76669-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76669-104">DESCRIPTION</span></span>

## <span data-ttu-id="76669-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76669-105">EXAMPLES</span></span>

### <span data-ttu-id="76669-106">Beispiel 1: Entfernen eines virtuellen Netzwerk Peerings</span><span class="sxs-lookup"><span data-stu-id="76669-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="76669-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="76669-107">PARAMETERS</span></span>

### <span data-ttu-id="76669-108">-Force</span><span class="sxs-lookup"><span data-stu-id="76669-108">-Force</span></span>
<span data-ttu-id="76669-109">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="76669-109">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76669-110">-Name</span><span class="sxs-lookup"><span data-stu-id="76669-110">-Name</span></span>
<span data-ttu-id="76669-111">Der Name des virtuellen Netzwerk Peerings.</span><span class="sxs-lookup"><span data-stu-id="76669-111">The virtual network peering name.</span></span>

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

### <span data-ttu-id="76669-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76669-112">-PassThru</span></span>
<span data-ttu-id="76669-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="76669-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="76669-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="76669-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76669-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76669-115">-ResourceGroupName</span></span>
<span data-ttu-id="76669-116">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="76669-116">The resource group name</span></span>

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

### <span data-ttu-id="76669-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="76669-117">-VirtualNetworkName</span></span>
<span data-ttu-id="76669-118">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="76669-118">The virtual network name.</span></span>

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

### <span data-ttu-id="76669-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76669-119">-Confirm</span></span>
<span data-ttu-id="76669-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76669-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76669-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76669-121">-WhatIf</span></span>
<span data-ttu-id="76669-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76669-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76669-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76669-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76669-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76669-124">-DefaultProfile</span></span>
<span data-ttu-id="76669-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76669-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76669-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76669-126">CommonParameters</span></span>
<span data-ttu-id="76669-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76669-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76669-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76669-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76669-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76669-129">INPUTS</span></span>

## <span data-ttu-id="76669-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76669-130">OUTPUTS</span></span>

## <span data-ttu-id="76669-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="76669-131">NOTES</span></span>

## <span data-ttu-id="76669-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76669-132">RELATED LINKS</span></span>

