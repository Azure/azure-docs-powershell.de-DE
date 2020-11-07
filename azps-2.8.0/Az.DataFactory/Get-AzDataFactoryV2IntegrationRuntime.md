---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 96c635caef26a1dc90ae2646cb4899012105f526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651764"
---
# <span data-ttu-id="32bbb-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="32bbb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="32bbb-103">Ruft Informationen zu Integrationslauf Zeit Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="32bbb-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="32bbb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32bbb-104">SYNTAX</span></span>

### <span data-ttu-id="32bbb-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="32bbb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32bbb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="32bbb-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32bbb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="32bbb-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32bbb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32bbb-108">DESCRIPTION</span></span>
<span data-ttu-id="32bbb-109">Das Get-AzDataFactoryV2IntegrationRuntime-Cmdlet ruft Informationen zu Integrationslauf Zeiten in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="32bbb-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="32bbb-110">Wenn Sie den Namen einer Integrationslaufzeit angeben, ruft dieses Cmdlet Informationen zu dieser Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="32bbb-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="32bbb-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Integrationslauf Zeiten in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="32bbb-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="32bbb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32bbb-112">EXAMPLES</span></span>

### <span data-ttu-id="32bbb-113">Beispiel 1: Auflisten aller Integrations-Runtimes in einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="32bbb-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="32bbb-114">Listen Sie alle Integrations Runtimes in der Data Factory mit dem Namen "Test-DF-EU2" auf.</span><span class="sxs-lookup"><span data-stu-id="32bbb-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="32bbb-115">Beispiel 2: Abrufen der verwalteten dedizierten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="32bbb-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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

<span data-ttu-id="32bbb-116">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="32bbb-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="32bbb-117">Beispiel 3: Abrufen der verwalteten dedizierten Integrationslaufzeit mit dem Detailstatus</span><span class="sxs-lookup"><span data-stu-id="32bbb-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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

<span data-ttu-id="32bbb-118">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="32bbb-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="32bbb-119">Beispiel 4: Abrufen der selbst gehosteten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="32bbb-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="32bbb-120">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="32bbb-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="32bbb-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="32bbb-121">PARAMETERS</span></span>

### <span data-ttu-id="32bbb-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="32bbb-122">-DataFactoryName</span></span>
<span data-ttu-id="32bbb-123">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="32bbb-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bbb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bbb-124">-DefaultProfile</span></span>
<span data-ttu-id="32bbb-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32bbb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32bbb-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="32bbb-126">-InputObject</span></span>
<span data-ttu-id="32bbb-127">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="32bbb-127">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32bbb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="32bbb-128">-Name</span></span>
<span data-ttu-id="32bbb-129">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="32bbb-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bbb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bbb-130">-ResourceGroupName</span></span>
<span data-ttu-id="32bbb-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="32bbb-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bbb-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="32bbb-132">-ResourceId</span></span>
<span data-ttu-id="32bbb-133">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="32bbb-133">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bbb-134">-Status</span><span class="sxs-lookup"><span data-stu-id="32bbb-134">-Status</span></span>
<span data-ttu-id="32bbb-135">Der Detailstatus der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="32bbb-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="32bbb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bbb-136">CommonParameters</span></span>
<span data-ttu-id="32bbb-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32bbb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bbb-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32bbb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bbb-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32bbb-139">INPUTS</span></span>

### <span data-ttu-id="32bbb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="32bbb-140">System.String</span></span>

### <span data-ttu-id="32bbb-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="32bbb-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32bbb-142">OUTPUTS</span></span>

### <span data-ttu-id="32bbb-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="32bbb-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="32bbb-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="32bbb-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="32bbb-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="32bbb-147">NOTES</span></span>
<span data-ttu-id="32bbb-148">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="32bbb-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="32bbb-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32bbb-149">RELATED LINKS</span></span>

[<span data-ttu-id="32bbb-150">Satz-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-150">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="32bbb-151">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32bbb-151">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
