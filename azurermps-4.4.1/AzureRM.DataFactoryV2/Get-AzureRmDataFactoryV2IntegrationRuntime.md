---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: ef5b99a27c547ec1e71c2339de8f4c9536549981
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505102"
---
# <span data-ttu-id="575a1-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="575a1-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="575a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="575a1-102">SYNOPSIS</span></span>
<span data-ttu-id="575a1-103">Ruft Informationen zu Integrationslauf Zeit Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="575a1-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="575a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="575a1-104">SYNTAX</span></span>

### <span data-ttu-id="575a1-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="575a1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="575a1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="575a1-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
```

### <span data-ttu-id="575a1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="575a1-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="575a1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="575a1-108">DESCRIPTION</span></span>
<span data-ttu-id="575a1-109">Das Get-AzureRmDataFactoryV2IntegrationRuntime-Cmdlet ruft Informationen zu Integrationslauf Zeiten in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="575a1-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="575a1-110">Wenn Sie den Namen einer Integrationslaufzeit angeben, ruft dieses Cmdlet Informationen zu dieser Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="575a1-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="575a1-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Integrationslauf Zeiten in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="575a1-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="575a1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="575a1-112">EXAMPLES</span></span>

### <span data-ttu-id="575a1-113">Beispiel 1: Auflisten aller Integrations-Runtimes in einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="575a1-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="575a1-114">Listen Sie alle Integrations Runtimes in der Data Factory mit dem Namen "Test-DF-EU2" auf.</span><span class="sxs-lookup"><span data-stu-id="575a1-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="575a1-115">Beispiel 2: Abrufen der verwalteten dedizierten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="575a1-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="575a1-116">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="575a1-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="575a1-117">Beispiel 3: Abrufen der verwalteten dedizierten Integrationslaufzeit mit dem Detailstatus</span><span class="sxs-lookup"><span data-stu-id="575a1-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="575a1-118">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="575a1-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="575a1-119">Beispiel 4: Abrufen der selbst gehosteten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="575a1-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="575a1-120">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="575a1-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="575a1-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="575a1-121">PARAMETERS</span></span>

### <span data-ttu-id="575a1-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="575a1-122">-DataFactoryName</span></span>
<span data-ttu-id="575a1-123">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="575a1-123">The data factory name.</span></span>

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

### <span data-ttu-id="575a1-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="575a1-124">-InputObject</span></span>
<span data-ttu-id="575a1-125">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="575a1-125">The integration runtime object.</span></span>

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

### <span data-ttu-id="575a1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="575a1-126">-Name</span></span>
<span data-ttu-id="575a1-127">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="575a1-127">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="575a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="575a1-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="575a1-129">The resource group name.</span></span>

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

### <span data-ttu-id="575a1-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="575a1-130">-ResourceId</span></span>
<span data-ttu-id="575a1-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="575a1-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="575a1-132">-Status</span><span class="sxs-lookup"><span data-stu-id="575a1-132">-Status</span></span>
<span data-ttu-id="575a1-133">Der Detailstatus der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="575a1-133">The integration runtime detail status.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="575a1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="575a1-134">INPUTS</span></span>

### <span data-ttu-id="575a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="575a1-135">System.String</span></span>
<span data-ttu-id="575a1-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="575a1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="575a1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="575a1-137">OUTPUTS</span></span>

### <span data-ttu-id="575a1-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="575a1-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="575a1-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="575a1-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>


## <span data-ttu-id="575a1-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="575a1-140">NOTES</span></span>
<span data-ttu-id="575a1-141">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="575a1-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="575a1-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="575a1-142">RELATED LINKS</span></span>
[<span data-ttu-id="575a1-143">Satz-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="575a1-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="575a1-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="575a1-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
