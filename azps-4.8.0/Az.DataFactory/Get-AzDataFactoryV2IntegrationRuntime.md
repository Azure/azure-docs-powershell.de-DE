---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167232"
---
# <span data-ttu-id="38a03-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="38a03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38a03-102">SYNOPSIS</span></span>
<span data-ttu-id="38a03-103">Ruft Informationen zu Integrationslauf Zeit Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="38a03-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="38a03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38a03-104">SYNTAX</span></span>

### <span data-ttu-id="38a03-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="38a03-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a03-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38a03-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a03-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="38a03-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a03-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38a03-108">DESCRIPTION</span></span>
<span data-ttu-id="38a03-109">Das Get-AzDataFactoryV2IntegrationRuntime-Cmdlet ruft Informationen zu Integrationslauf Zeiten in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="38a03-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="38a03-110">Wenn Sie den Namen einer Integrationslaufzeit angeben, ruft dieses Cmdlet Informationen zu dieser Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="38a03-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="38a03-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Integrationslauf Zeiten in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="38a03-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="38a03-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38a03-112">EXAMPLES</span></span>

### <span data-ttu-id="38a03-113">Beispiel 1: Auflisten aller Integrations-Runtimes in einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="38a03-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="38a03-114">Listen Sie alle Integrations Runtimes in der Data Factory mit dem Namen "Test-DF-EU2" auf.</span><span class="sxs-lookup"><span data-stu-id="38a03-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="38a03-115">Beispiel 2: Abrufen der verwalteten dedizierten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="38a03-115">Example 2: Get managed dedicated integration runtime</span></span>
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
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="38a03-116">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="38a03-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="38a03-117">Beispiel 3: Abrufen der verwalteten dedizierten Integrationslaufzeit mit dem Detailstatus</span><span class="sxs-lookup"><span data-stu-id="38a03-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="38a03-118">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="38a03-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="38a03-119">Beispiel 4: Abrufen der selbst gehosteten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="38a03-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="38a03-120">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "Test-dediziert-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="38a03-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="38a03-121">Beispiel 5: Abrufen der selbst gehosteten Integrationslaufzeit mit dem Detailstatus</span><span class="sxs-lookup"><span data-stu-id="38a03-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="38a03-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="38a03-122">PARAMETERS</span></span>

### <span data-ttu-id="38a03-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="38a03-123">-DataFactoryName</span></span>
<span data-ttu-id="38a03-124">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="38a03-124">The data factory name.</span></span>

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

### <span data-ttu-id="38a03-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a03-125">-DefaultProfile</span></span>
<span data-ttu-id="38a03-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38a03-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38a03-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="38a03-127">-InputObject</span></span>
<span data-ttu-id="38a03-128">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="38a03-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="38a03-129">-Name</span><span class="sxs-lookup"><span data-stu-id="38a03-129">-Name</span></span>
<span data-ttu-id="38a03-130">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="38a03-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="38a03-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a03-131">-ResourceGroupName</span></span>
<span data-ttu-id="38a03-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="38a03-132">The resource group name.</span></span>

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

### <span data-ttu-id="38a03-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="38a03-133">-ResourceId</span></span>
<span data-ttu-id="38a03-134">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="38a03-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="38a03-135">-Status</span><span class="sxs-lookup"><span data-stu-id="38a03-135">-Status</span></span>
<span data-ttu-id="38a03-136">Der Detailstatus der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="38a03-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="38a03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a03-137">CommonParameters</span></span>
<span data-ttu-id="38a03-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a03-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a03-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a03-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38a03-140">INPUTS</span></span>

### <span data-ttu-id="38a03-141">System. String</span><span class="sxs-lookup"><span data-stu-id="38a03-141">System.String</span></span>

### <span data-ttu-id="38a03-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="38a03-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38a03-143">OUTPUTS</span></span>

### <span data-ttu-id="38a03-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="38a03-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="38a03-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="38a03-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="38a03-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="38a03-148">NOTES</span></span>
<span data-ttu-id="38a03-149">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="38a03-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="38a03-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38a03-150">RELATED LINKS</span></span>

[<span data-ttu-id="38a03-151">Satz-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="38a03-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38a03-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
