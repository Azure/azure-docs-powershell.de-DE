---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146401"
---
# <span data-ttu-id="23306-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="23306-101">New-AzPeeringService</span></span>

## <span data-ttu-id="23306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23306-102">SYNOPSIS</span></span>
<span data-ttu-id="23306-103">Erstellt einen neuen Peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="23306-103">Creates a new peering service.</span></span>

## <span data-ttu-id="23306-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23306-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23306-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23306-105">DESCRIPTION</span></span>
<span data-ttu-id="23306-106">Erstellt einen Peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="23306-106">Creates peering service.</span></span>

## <span data-ttu-id="23306-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23306-107">EXAMPLES</span></span>

### <span data-ttu-id="23306-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23306-108">Example 1</span></span>
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

<span data-ttu-id="23306-109">Erstellt ein Peeringdienstobjekt mit Anbieter und Peeringspeicherort.</span><span class="sxs-lookup"><span data-stu-id="23306-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="23306-110">In Konjuction `Get-AzPeeringServiceProvider` mit und `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="23306-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="23306-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23306-111">PARAMETERS</span></span>

### <span data-ttu-id="23306-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23306-112">-AsJob</span></span>
<span data-ttu-id="23306-113">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="23306-113">Run in the background.</span></span>

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

### <span data-ttu-id="23306-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23306-114">-DefaultProfile</span></span>
<span data-ttu-id="23306-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23306-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23306-116">-Name</span><span class="sxs-lookup"><span data-stu-id="23306-116">-Name</span></span>
<span data-ttu-id="23306-117">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="23306-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="23306-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="23306-118">-PeeringLocation</span></span>
<span data-ttu-id="23306-119">Der physische Standort ist anders als in der Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="23306-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="23306-120">Verwenden Get-AzPeeringServiceLocation [-Land <country> ]</span><span class="sxs-lookup"><span data-stu-id="23306-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="23306-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="23306-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="23306-122">Der Name des Peeringdienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="23306-122">The peering service provider name.</span></span>
<span data-ttu-id="23306-123">Verwenden Get-AzPeeringServiceProvider Cmdlet für eine Liste</span><span class="sxs-lookup"><span data-stu-id="23306-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

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

### <span data-ttu-id="23306-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23306-124">-ResourceGroupName</span></span>
<span data-ttu-id="23306-125">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="23306-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="23306-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="23306-126">-Tag</span></span>
<span data-ttu-id="23306-127">Die Tags, die dem Microsoft InputObject Service zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="23306-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="23306-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23306-128">-Confirm</span></span>
<span data-ttu-id="23306-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23306-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23306-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="23306-130">-WhatIf</span></span>
<span data-ttu-id="23306-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23306-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23306-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23306-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23306-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23306-133">CommonParameters</span></span>
<span data-ttu-id="23306-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23306-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23306-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23306-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23306-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23306-136">INPUTS</span></span>

### <span data-ttu-id="23306-137">Keine</span><span class="sxs-lookup"><span data-stu-id="23306-137">None</span></span>

## <span data-ttu-id="23306-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23306-138">OUTPUTS</span></span>

### <span data-ttu-id="23306-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="23306-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="23306-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="23306-140">NOTES</span></span>

## <span data-ttu-id="23306-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="23306-141">RELATED LINKS</span></span>
