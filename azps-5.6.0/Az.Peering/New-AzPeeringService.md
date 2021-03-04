---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 1fc1d2f9269bf48d6f6dfd79caa8e34b3de51fee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937640"
---
# <span data-ttu-id="0bc00-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="0bc00-101">New-AzPeeringService</span></span>

## <span data-ttu-id="0bc00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bc00-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc00-103">Erstellt einen neuen Peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="0bc00-103">Creates a new peering service.</span></span>

## <span data-ttu-id="0bc00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bc00-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc00-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bc00-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc00-106">Erstellt einen Peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="0bc00-106">Creates peering service.</span></span>

## <span data-ttu-id="0bc00-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bc00-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc00-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bc00-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="0bc00-109">Erstellt ein Peeringdienstobjekt mit Anbieter- und Peeringspeicherort.</span><span class="sxs-lookup"><span data-stu-id="0bc00-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="0bc00-110">Verwenden sie in der Konjuktion `Get-AzPeeringServiceProvider` mit und `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="0bc00-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="0bc00-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0bc00-111">PARAMETERS</span></span>

### <span data-ttu-id="0bc00-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bc00-112">-AsJob</span></span>
<span data-ttu-id="0bc00-113">Führen Sie im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="0bc00-113">Run in the background.</span></span>

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

### <span data-ttu-id="0bc00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc00-114">-DefaultProfile</span></span>
<span data-ttu-id="0bc00-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bc00-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bc00-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0bc00-116">-Name</span></span>
<span data-ttu-id="0bc00-117">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="0bc00-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc00-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="0bc00-118">-PeeringLocation</span></span>
<span data-ttu-id="0bc00-119">Der physische Speicherort, der sich von der Azure-Region ab unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="0bc00-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="0bc00-120">Verwenden Get-AzPeeringServiceLocation [-Land <country> ]</span><span class="sxs-lookup"><span data-stu-id="0bc00-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc00-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="0bc00-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="0bc00-122">Der Name des Peeringdienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="0bc00-122">The peering service provider name.</span></span>
<span data-ttu-id="0bc00-123">Verwenden Get-AzPeeringServiceProvider cmdlets für eine Liste</span><span class="sxs-lookup"><span data-stu-id="0bc00-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc00-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bc00-125">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="0bc00-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc00-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="0bc00-126">-Tag</span></span>
<span data-ttu-id="0bc00-127">Die Tags, die dem Microsoft InputObject Service zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0bc00-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc00-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0bc00-128">-Confirm</span></span>
<span data-ttu-id="0bc00-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bc00-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc00-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc00-130">-WhatIf</span></span>
<span data-ttu-id="0bc00-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bc00-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc00-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bc00-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc00-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc00-133">CommonParameters</span></span>
<span data-ttu-id="0bc00-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc00-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc00-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bc00-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc00-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bc00-136">INPUTS</span></span>

### <span data-ttu-id="0bc00-137">Keine</span><span class="sxs-lookup"><span data-stu-id="0bc00-137">None</span></span>

## <span data-ttu-id="0bc00-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bc00-138">OUTPUTS</span></span>

### <span data-ttu-id="0bc00-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="0bc00-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="0bc00-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0bc00-140">NOTES</span></span>

## <span data-ttu-id="0bc00-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0bc00-141">RELATED LINKS</span></span>
