---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665400"
---
# <span data-ttu-id="24838-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="24838-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="24838-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24838-102">SYNOPSIS</span></span>
<span data-ttu-id="24838-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="24838-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24838-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24838-104">SYNTAX</span></span>

### <span data-ttu-id="24838-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="24838-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="24838-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24838-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="24838-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="24838-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="24838-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24838-108">DESCRIPTION</span></span>
<span data-ttu-id="24838-109">Das Get-AzureRmDataFactoryV2IntegrationRuntimeMetric-Cmdlet ruft metrische Daten zur Integrationslaufzeit in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="24838-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="24838-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24838-110">EXAMPLES</span></span>

### <span data-ttu-id="24838-111">Beispiel 1: Abrufen der Integrationslauf Zeit Metrik</span><span class="sxs-lookup"><span data-stu-id="24838-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="24838-112">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="24838-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="24838-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="24838-113">PARAMETERS</span></span>

### <span data-ttu-id="24838-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="24838-114">-DataFactoryName</span></span>
<span data-ttu-id="24838-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="24838-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24838-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24838-116">-InputObject</span></span>
<span data-ttu-id="24838-117">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="24838-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24838-118">-Name</span><span class="sxs-lookup"><span data-stu-id="24838-118">-Name</span></span>
<span data-ttu-id="24838-119">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="24838-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24838-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24838-120">-ResourceGroupName</span></span>
<span data-ttu-id="24838-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24838-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24838-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="24838-122">-ResourceId</span></span>
<span data-ttu-id="24838-123">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="24838-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="24838-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24838-124">INPUTS</span></span>

### <span data-ttu-id="24838-125">System. String</span><span class="sxs-lookup"><span data-stu-id="24838-125">System.String</span></span>
<span data-ttu-id="24838-126">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="24838-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="24838-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24838-127">OUTPUTS</span></span>

### <span data-ttu-id="24838-128">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="24838-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="24838-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="24838-129">NOTES</span></span>

## <span data-ttu-id="24838-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24838-130">RELATED LINKS</span></span>
[<span data-ttu-id="24838-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="24838-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

