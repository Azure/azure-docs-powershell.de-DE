---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 8fadba097b602bd84c8eb36d75f5b7a331e2280b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928888"
---
# <span data-ttu-id="3a524-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3a524-101">Set-AzSearchService</span></span>

## <span data-ttu-id="3a524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a524-102">SYNOPSIS</span></span>
<span data-ttu-id="3a524-103">Aktualisieren sie einen Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="3a524-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3a524-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a524-104">SYNTAX</span></span>

### <span data-ttu-id="3a524-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a524-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a524-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a524-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a524-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a524-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a524-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a524-108">DESCRIPTION</span></span>
<span data-ttu-id="3a524-109">Das **Cmdlet Set-AzSearchService** ändert einen Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="3a524-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3a524-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a524-110">EXAMPLES</span></span>

### <span data-ttu-id="3a524-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a524-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="3a524-112">Im Beispiel werden die Partitionsanzahl und die Replikatanzahl des Azure Cognitive Search-Diensts in 2 geändert.</span><span class="sxs-lookup"><span data-stu-id="3a524-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="3a524-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3a524-113">PARAMETERS</span></span>

### <span data-ttu-id="3a524-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a524-114">-DefaultProfile</span></span>
<span data-ttu-id="3a524-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a524-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a524-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3a524-116">-IdentityType</span></span>
<span data-ttu-id="3a524-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="3a524-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a524-118">-InputObject</span></span>
<span data-ttu-id="3a524-119">Suchdiensteingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="3a524-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="3a524-120">-IPRuleList</span></span>
<span data-ttu-id="3a524-121">(Optional) Azure Cognitive Search Service -IP-Regeln</span><span class="sxs-lookup"><span data-stu-id="3a524-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3a524-122">-Name</span></span>
<span data-ttu-id="3a524-123">Name des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="3a524-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="3a524-124">-PartitionCount</span></span>
<span data-ttu-id="3a524-125">Anzahl der Suchdienstpartitionen.</span><span class="sxs-lookup"><span data-stu-id="3a524-125">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="3a524-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="3a524-127">(Optional) Zugriff auf öffentliches Netzwerk des Azure Cognitive Search Service (Aktiviert/Deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="3a524-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3a524-128">-ReplicaCount</span></span>
<span data-ttu-id="3a524-129">Anzahl der Suchdienstreplikate.</span><span class="sxs-lookup"><span data-stu-id="3a524-129">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a524-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a524-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a524-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a524-132">-ResourceId</span></span>
<span data-ttu-id="3a524-133">Suchdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3a524-133">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a524-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a524-134">-Confirm</span></span>
<span data-ttu-id="3a524-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a524-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a524-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a524-136">-WhatIf</span></span>
<span data-ttu-id="3a524-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a524-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a524-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a524-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a524-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a524-139">CommonParameters</span></span>
<span data-ttu-id="3a524-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a524-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a524-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a524-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a524-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a524-142">INPUTS</span></span>

### <span data-ttu-id="3a524-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3a524-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="3a524-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3a524-144">System.String</span></span>

## <span data-ttu-id="3a524-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a524-145">OUTPUTS</span></span>

### <span data-ttu-id="3a524-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3a524-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="3a524-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3a524-147">NOTES</span></span>

## <span data-ttu-id="3a524-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3a524-148">RELATED LINKS</span></span>

[<span data-ttu-id="3a524-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3a524-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="3a524-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3a524-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="3a524-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3a524-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)