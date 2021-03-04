---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 2990b28e811b21940d51ce8d0fd9c7540feccfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937555"
---
# <span data-ttu-id="4aaa3-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="4aaa3-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="4aaa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaa3-103">Legt ein registriertes Präfix aus der übergeordneten Peeringressource fest oder aktualisiert es.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="4aaa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aaa3-104">SYNTAX</span></span>

### <span data-ttu-id="4aaa3-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4aaa3-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aaa3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4aaa3-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aaa3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4aaa3-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aaa3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aaa3-108">DESCRIPTION</span></span>
<span data-ttu-id="4aaa3-109">Ermöglicht das Aktualisieren eines registrierten Präfixes aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="4aaa3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aaa3-110">EXAMPLES</span></span>

### <span data-ttu-id="4aaa3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4aaa3-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="4aaa3-112">Aktualisiert das Präfix nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="4aaa3-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4aaa3-113">PARAMETERS</span></span>

### <span data-ttu-id="4aaa3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aaa3-114">-AsJob</span></span>
<span data-ttu-id="4aaa3-115">Führen Sie im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-115">Run in the background.</span></span>

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

### <span data-ttu-id="4aaa3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aaa3-116">-DefaultProfile</span></span>
<span data-ttu-id="4aaa3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aaa3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aaa3-118">-InputObject</span></span>
<span data-ttu-id="4aaa3-119">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="4aaa3-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaa3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4aaa3-120">-Name</span></span>
<span data-ttu-id="4aaa3-121">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaa3-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="4aaa3-122">-PeeringName</span></span>
<span data-ttu-id="4aaa3-123">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaa3-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4aaa3-124">-Prefix</span></span>
<span data-ttu-id="4aaa3-125">Das IPv4-Sitzungspräfix</span><span class="sxs-lookup"><span data-stu-id="4aaa3-125">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaa3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aaa3-126">-ResourceGroupName</span></span>
<span data-ttu-id="4aaa3-127">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaa3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4aaa3-128">-ResourceId</span></span>
<span data-ttu-id="4aaa3-129">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaa3-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4aaa3-130">-Confirm</span></span>
<span data-ttu-id="4aaa3-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aaa3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aaa3-132">-WhatIf</span></span>
<span data-ttu-id="4aaa3-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aaa3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aaa3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaa3-135">CommonParameters</span></span>
<span data-ttu-id="4aaa3-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaa3-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aaa3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaa3-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aaa3-138">INPUTS</span></span>

### <span data-ttu-id="4aaa3-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="4aaa3-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="4aaa3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4aaa3-140">System.String</span></span>

## <span data-ttu-id="4aaa3-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aaa3-141">OUTPUTS</span></span>

### <span data-ttu-id="4aaa3-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="4aaa3-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="4aaa3-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4aaa3-143">NOTES</span></span>

## <span data-ttu-id="4aaa3-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4aaa3-144">RELATED LINKS</span></span>
