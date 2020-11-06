---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501777"
---
# <span data-ttu-id="a9fe7-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="a9fe7-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="a9fe7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fe7-103">Ruft die Zugriffstasten ab, die einem Operations Cluster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9fe7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9fe7-104">SYNTAX</span></span>

### <span data-ttu-id="a9fe7-105">Besorgen Sie sich die Schlüssel des Operations Clusters aus Cmdlet-Eingabeparametern.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="a9fe7-106">Besorgen Sie sich die Schlüssel des Operations Clusters aus einer OperationalizationCluster-Instanzen Definition.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="a9fe7-107">Besorgen Sie sich die Schlüssel des Operational Clusters aus einer Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="a9fe7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9fe7-108">DESCRIPTION</span></span>
<span data-ttu-id="a9fe7-109">Die Schlüssel für das Speicherkonto, die Container Registrierung und andere Dienste, die dem Zuordnungs Cluster zugeordnet sind, werden beim Abrufen der Clustereigenschaften nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="a9fe7-110">Ein bestimmter Aufruf zum Abrufen der Schlüssel muss vorgenommen werden, da es sich um vertrauliche Informationen handelt.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="a9fe7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9fe7-111">EXAMPLES</span></span>

### <span data-ttu-id="a9fe7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9fe7-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="a9fe7-113">Gibt die geheimen Schlüssel für die Dienste zurück, die dem Cluster für die Operation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="a9fe7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9fe7-114">PARAMETERS</span></span>

### <span data-ttu-id="a9fe7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9fe7-115">-InputObject</span></span>
<span data-ttu-id="a9fe7-116">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="a9fe7-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a9fe7-117">-Name</span></span>
<span data-ttu-id="a9fe7-118">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fe7-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9fe7-120">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe7-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a9fe7-121">-ResourceId</span></span>
<span data-ttu-id="a9fe7-122">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="a9fe7-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9fe7-123">INPUTS</span></span>

### <span data-ttu-id="a9fe7-124">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a9fe7-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="a9fe7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a9fe7-125">System.String</span></span>


## <span data-ttu-id="a9fe7-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9fe7-126">OUTPUTS</span></span>

### <span data-ttu-id="a9fe7-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="a9fe7-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="a9fe7-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9fe7-128">NOTES</span></span>

## <span data-ttu-id="a9fe7-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9fe7-129">RELATED LINKS</span></span>

