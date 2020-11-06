---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504889"
---
# <span data-ttu-id="66a19-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="66a19-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="66a19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66a19-102">SYNOPSIS</span></span>
<span data-ttu-id="66a19-103">Startet ein Update für die Systemdienste des Operations Clusters.</span><span class="sxs-lookup"><span data-stu-id="66a19-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66a19-104">SYNTAX</span></span>

### <span data-ttu-id="66a19-105">Starten Sie ein Systemdienst Update aus Cmdlet-Eingabeparametern.</span><span class="sxs-lookup"><span data-stu-id="66a19-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="66a19-106">Starten Sie ein Systemdienst Update aus einer PSOperationalizationCluster-Instanzen Definition.</span><span class="sxs-lookup"><span data-stu-id="66a19-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="66a19-107">Starten Sie ein Systemdienst Update über eine Azure Resouce-ID.</span><span class="sxs-lookup"><span data-stu-id="66a19-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="66a19-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66a19-108">DESCRIPTION</span></span>
<span data-ttu-id="66a19-109">Die Systemdienste können unabhängig vom Operations Cluster aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="66a19-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="66a19-110">Verwenden Sie dieses Cmdlet, um ein Update für die Systemdienste zu starten.</span><span class="sxs-lookup"><span data-stu-id="66a19-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="66a19-111">Wenn kein Update verfügbar ist, wird ein Update weiterhin gestartet und wird erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="66a19-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="66a19-112">Nach Abschluss des Updates meldet es, wenn es gestartet, abgeschlossen und erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="66a19-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="66a19-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66a19-113">EXAMPLES</span></span>

### <span data-ttu-id="66a19-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66a19-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="66a19-115">Startet ein Systemdienst Update für den angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="66a19-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="66a19-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="66a19-116">PARAMETERS</span></span>

### <span data-ttu-id="66a19-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66a19-117">-InputObject</span></span>
<span data-ttu-id="66a19-118">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="66a19-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66a19-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66a19-119">-Confirm</span></span>
<span data-ttu-id="66a19-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66a19-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a19-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66a19-121">-Name</span></span>
<span data-ttu-id="66a19-122">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="66a19-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a19-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a19-123">-ResourceGroupName</span></span>
<span data-ttu-id="66a19-124">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="66a19-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a19-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="66a19-125">-ResourceId</span></span>
<span data-ttu-id="66a19-126">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="66a19-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a19-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a19-127">-WhatIf</span></span>
<span data-ttu-id="66a19-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66a19-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a19-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66a19-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="66a19-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66a19-130">INPUTS</span></span>

### <span data-ttu-id="66a19-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="66a19-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="66a19-132">System. String</span><span class="sxs-lookup"><span data-stu-id="66a19-132">System.String</span></span>


## <span data-ttu-id="66a19-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66a19-133">OUTPUTS</span></span>

### <span data-ttu-id="66a19-134">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="66a19-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="66a19-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="66a19-135">NOTES</span></span>

## <span data-ttu-id="66a19-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66a19-136">RELATED LINKS</span></span>

