---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 61101242b100ca4b477910a0dfa339ef7f9ea81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921616"
---
# <span data-ttu-id="8732d-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8732d-101">New-AzSearchService</span></span>

## <span data-ttu-id="8732d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8732d-102">SYNOPSIS</span></span>
<span data-ttu-id="8732d-103">Erstellt einen Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8732d-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8732d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8732d-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8732d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8732d-105">DESCRIPTION</span></span>
<span data-ttu-id="8732d-106">Das **Cmdlet New-AzSearchService** erstellt einen Azure Cognitive Search-Dienst mit angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="8732d-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="8732d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8732d-107">EXAMPLES</span></span>

### <span data-ttu-id="8732d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8732d-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="8732d-109">Mit dem Befehl wird ein Azure Cognitive Search-Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="8732d-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8732d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8732d-110">PARAMETERS</span></span>

### <span data-ttu-id="8732d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8732d-111">-DefaultProfile</span></span>
<span data-ttu-id="8732d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8732d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8732d-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="8732d-113">-HostingMode</span></span>
<span data-ttu-id="8732d-114">Azure Cognitive Search Service-Hostingmodus.</span><span class="sxs-lookup"><span data-stu-id="8732d-114">Azure Cognitive Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8732d-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8732d-115">-IdentityType</span></span>
<span data-ttu-id="8732d-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="8732d-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="8732d-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="8732d-117">-IPRuleList</span></span>
<span data-ttu-id="8732d-118">(Optional) Azure Cognitive Search Service -IP-Regeln</span><span class="sxs-lookup"><span data-stu-id="8732d-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="8732d-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8732d-119">-Location</span></span>
<span data-ttu-id="8732d-120">Azure Cognitive Search Service Location.</span><span class="sxs-lookup"><span data-stu-id="8732d-120">Azure Cognitive Search Service location.</span></span>

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

### <span data-ttu-id="8732d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8732d-121">-Name</span></span>
<span data-ttu-id="8732d-122">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="8732d-122">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="8732d-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="8732d-123">-PartitionCount</span></span>
<span data-ttu-id="8732d-124">Azure Cognitive Search Service partition count.</span><span class="sxs-lookup"><span data-stu-id="8732d-124">Azure Cognitive Search Service partition count.</span></span>

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

### <span data-ttu-id="8732d-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="8732d-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="8732d-126">(Optional) Zugriff auf öffentliches Netzwerk des Azure Cognitive Search Service (Aktiviert/Deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="8732d-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="8732d-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8732d-127">-ReplicaCount</span></span>
<span data-ttu-id="8732d-128">Azure Cognitive Search Service Replica Count.</span><span class="sxs-lookup"><span data-stu-id="8732d-128">Azure Cognitive Search Service replica count.</span></span>

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

### <span data-ttu-id="8732d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8732d-129">-ResourceGroupName</span></span>
<span data-ttu-id="8732d-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8732d-130">Resource Group name.</span></span>

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

### <span data-ttu-id="8732d-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="8732d-131">-Sku</span></span>
<span data-ttu-id="8732d-132">Azure Cognitive Search Service Sku.</span><span class="sxs-lookup"><span data-stu-id="8732d-132">Azure Cognitive Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8732d-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8732d-133">-Confirm</span></span>
<span data-ttu-id="8732d-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8732d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8732d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8732d-135">-WhatIf</span></span>
<span data-ttu-id="8732d-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8732d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8732d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8732d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8732d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8732d-138">CommonParameters</span></span>
<span data-ttu-id="8732d-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8732d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8732d-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8732d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8732d-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8732d-141">INPUTS</span></span>

### <span data-ttu-id="8732d-142">Keine</span><span class="sxs-lookup"><span data-stu-id="8732d-142">None</span></span>

## <span data-ttu-id="8732d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8732d-143">OUTPUTS</span></span>

### <span data-ttu-id="8732d-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8732d-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="8732d-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8732d-145">NOTES</span></span>

## <span data-ttu-id="8732d-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8732d-146">RELATED LINKS</span></span>

[<span data-ttu-id="8732d-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8732d-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="8732d-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8732d-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="8732d-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8732d-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)