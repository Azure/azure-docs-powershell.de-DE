---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663566"
---
# <span data-ttu-id="6cab4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="6cab4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="6cab4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cab4-102">SYNOPSIS</span></span>
<span data-ttu-id="6cab4-103">Überprüft, ob Updates für die Systemdienste verfügbar sind, die mit einem Operations Cluster verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="6cab4-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cab4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cab4-104">SYNTAX</span></span>

### <span data-ttu-id="6cab4-105">Testen Sie die Verfügbarkeit von Updates über Cmdlet-Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="6cab4-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="6cab4-106">Testen Sie die Verfügbarkeit von Updates anhand einer OperationalizationCluster-Instanzen Definition.</span><span class="sxs-lookup"><span data-stu-id="6cab4-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="6cab4-107">Testen Sie die Verfügbarkeit von Updates über eine Azure Resouce-ID.</span><span class="sxs-lookup"><span data-stu-id="6cab4-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="6cab4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cab4-108">DESCRIPTION</span></span>
<span data-ttu-id="6cab4-109">System Dienste erhalten Updates unabhängig vom Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="6cab4-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="6cab4-110">Wenn Sie dieses Cmdlet verwenden, kann der Benutzer wissen, ob Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="6cab4-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="6cab4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cab4-111">EXAMPLES</span></span>

### <span data-ttu-id="6cab4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cab4-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="6cab4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6cab4-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="6cab4-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6cab4-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="6cab4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cab4-115">PARAMETERS</span></span>

### <span data-ttu-id="6cab4-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6cab4-116">-InputObject</span></span>
<span data-ttu-id="6cab4-117">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="6cab4-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cab4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6cab4-118">-Name</span></span>
<span data-ttu-id="6cab4-119">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="6cab4-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cab4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cab4-120">-ResourceGroupName</span></span>
<span data-ttu-id="6cab4-121">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="6cab4-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cab4-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6cab4-122">-ResourceId</span></span>
<span data-ttu-id="6cab4-123">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="6cab4-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6cab4-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cab4-124">INPUTS</span></span>

### <span data-ttu-id="6cab4-125">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="6cab4-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="6cab4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6cab4-126">System.String</span></span>


## <span data-ttu-id="6cab4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cab4-127">OUTPUTS</span></span>

### <span data-ttu-id="6cab4-128">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="6cab4-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="6cab4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cab4-129">NOTES</span></span>

## <span data-ttu-id="6cab4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cab4-130">RELATED LINKS</span></span>

