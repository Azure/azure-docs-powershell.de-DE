---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469859"
---
# <span data-ttu-id="e440c-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="e440c-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="e440c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e440c-102">SYNOPSIS</span></span>
<span data-ttu-id="e440c-103">Erstellt einen neuen dedizierten Eventhub-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e440c-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="e440c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e440c-104">SYNTAX</span></span>

### <span data-ttu-id="e440c-105">ClusterPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e440c-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e440c-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e440c-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e440c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e440c-107">DESCRIPTION</span></span>
<span data-ttu-id="e440c-108">Das New-AzEventHubCluster erstellt den dedizierten Eventhub-Cluster in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e440c-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="e440c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e440c-109">EXAMPLES</span></span>

### <span data-ttu-id="e440c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e440c-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="e440c-111">Erstellt einen dedizierten "Eventhub-Cluster-5557"-Cluster in der Ressourcengruppe "RSG-Cluster27651" mit Standort-Südzentralus und Kapazität als 1.</span><span class="sxs-lookup"><span data-stu-id="e440c-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="e440c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e440c-112">PARAMETERS</span></span>

### <span data-ttu-id="e440c-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="e440c-113">-Capacity</span></span>
<span data-ttu-id="e440c-114">Clusterkapazität (CU), kurvig, zulässiger Wert = 1</span><span class="sxs-lookup"><span data-stu-id="e440c-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="e440c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e440c-115">-DefaultProfile</span></span>
<span data-ttu-id="e440c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e440c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e440c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e440c-117">-Location</span></span>
<span data-ttu-id="e440c-118">Standort des Clusters</span><span class="sxs-lookup"><span data-stu-id="e440c-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e440c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e440c-119">-Name</span></span>
<span data-ttu-id="e440c-120">Clustername</span><span class="sxs-lookup"><span data-stu-id="e440c-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e440c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e440c-121">-ResourceGroupName</span></span>
<span data-ttu-id="e440c-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e440c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e440c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e440c-123">-ResourceId</span></span>
<span data-ttu-id="e440c-124">Ressourcen-ID des Clusters</span><span class="sxs-lookup"><span data-stu-id="e440c-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="e440c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e440c-125">-Tag</span></span>
<span data-ttu-id="e440c-126">Hashtables, die Ressourcentags für Clustern darstellt</span><span class="sxs-lookup"><span data-stu-id="e440c-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e440c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e440c-127">-Confirm</span></span>
<span data-ttu-id="e440c-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e440c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e440c-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e440c-129">-WhatIf</span></span>
<span data-ttu-id="e440c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e440c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e440c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e440c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e440c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e440c-132">CommonParameters</span></span>
<span data-ttu-id="e440c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e440c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e440c-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e440c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e440c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e440c-135">INPUTS</span></span>

### <span data-ttu-id="e440c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e440c-136">System.String</span></span>

### <span data-ttu-id="e440c-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e440c-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e440c-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e440c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e440c-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e440c-139">OUTPUTS</span></span>

### <span data-ttu-id="e440c-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="e440c-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="e440c-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e440c-141">NOTES</span></span>

## <span data-ttu-id="e440c-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e440c-142">RELATED LINKS</span></span>
