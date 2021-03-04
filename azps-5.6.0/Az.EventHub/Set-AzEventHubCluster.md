---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3fb0030d6475ab3fb41f78ab1dc1a54870ed2f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942776"
---
# <span data-ttu-id="f4522-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="f4522-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="f4522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4522-102">SYNOPSIS</span></span>
<span data-ttu-id="f4522-103">Aktualisiert das Tag für den angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="f4522-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="f4522-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4522-104">SYNTAX</span></span>

### <span data-ttu-id="f4522-105">ClusterPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4522-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4522-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4522-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4522-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4522-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4522-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4522-108">DESCRIPTION</span></span>
<span data-ttu-id="f4522-109">Das Set-AzEventHubCluster cmdlet aktualisiert Tags des angegebenen Clusters</span><span class="sxs-lookup"><span data-stu-id="f4522-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="f4522-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4522-110">EXAMPLES</span></span>

### <span data-ttu-id="f4522-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4522-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="f4522-112">Aktualisiert Tags des angegebenen Clusters.</span><span class="sxs-lookup"><span data-stu-id="f4522-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="f4522-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4522-113">PARAMETERS</span></span>

### <span data-ttu-id="f4522-114">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="f4522-114">-Capacity</span></span>
<span data-ttu-id="f4522-115">Clusterkapazität (CU), curerntrly, zulässiger Wert = 1</span><span class="sxs-lookup"><span data-stu-id="f4522-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4522-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4522-116">-DefaultProfile</span></span>
<span data-ttu-id="f4522-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4522-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4522-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4522-118">-InputObject</span></span>
<span data-ttu-id="f4522-119">Clustername</span><span class="sxs-lookup"><span data-stu-id="f4522-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4522-120">-Location</span><span class="sxs-lookup"><span data-stu-id="f4522-120">-Location</span></span>
<span data-ttu-id="f4522-121">Standort des Clusters</span><span class="sxs-lookup"><span data-stu-id="f4522-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4522-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f4522-122">-Name</span></span>
<span data-ttu-id="f4522-123">Clustername</span><span class="sxs-lookup"><span data-stu-id="f4522-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4522-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4522-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4522-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f4522-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4522-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4522-126">-ResourceId</span></span>
<span data-ttu-id="f4522-127">Ressourcen-ID des Clusters</span><span class="sxs-lookup"><span data-stu-id="f4522-127">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4522-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4522-128">-Tag</span></span>
<span data-ttu-id="f4522-129">Hashtables, die ressourcentag für Cluster darstellt</span><span class="sxs-lookup"><span data-stu-id="f4522-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4522-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4522-130">-Confirm</span></span>
<span data-ttu-id="f4522-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4522-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4522-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4522-132">-WhatIf</span></span>
<span data-ttu-id="f4522-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4522-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4522-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4522-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4522-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4522-135">CommonParameters</span></span>
<span data-ttu-id="f4522-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4522-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4522-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4522-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4522-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4522-138">INPUTS</span></span>

### <span data-ttu-id="f4522-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f4522-139">System.String</span></span>

### <span data-ttu-id="f4522-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f4522-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f4522-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="f4522-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="f4522-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4522-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4522-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4522-143">OUTPUTS</span></span>

### <span data-ttu-id="f4522-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="f4522-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="f4522-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4522-145">NOTES</span></span>

## <span data-ttu-id="f4522-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4522-146">RELATED LINKS</span></span>
