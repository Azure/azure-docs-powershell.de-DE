---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472678"
---
# <span data-ttu-id="3f008-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="3f008-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="3f008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f008-102">SYNOPSIS</span></span>
<span data-ttu-id="3f008-103">Ruft Informationen zu Integrations-Runtime-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="3f008-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="3f008-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f008-104">SYNTAX</span></span>

### <span data-ttu-id="3f008-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f008-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f008-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f008-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f008-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3f008-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f008-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f008-108">DESCRIPTION</span></span>
<span data-ttu-id="3f008-109">Das **Cmdlet "Get-AzDataFactoryV2IntegrationRuntimeNode"** ruft die Detailinformationen eines Integrationslaufzeitknotens ab.</span><span class="sxs-lookup"><span data-stu-id="3f008-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="3f008-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f008-110">EXAMPLES</span></span>

### <span data-ttu-id="3f008-111">Beispiel 1: Ruft die Detailinformationen eines Integrationslaufzeitknotens ab.</span><span class="sxs-lookup"><span data-stu-id="3f008-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="3f008-112">Das Cmdlet ruft Informationen des Knotens "Node_1" in der selbst gehosteten Integrationslaufzeit "test-selfhost-ir" in der Daten factory "test-df-eu2" ab.</span><span class="sxs-lookup"><span data-stu-id="3f008-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="3f008-113">Beispiel 2: Ruft die Detailinformationen eines Integrationslaufzeitknotens zusammen mit der IP-Adresse ab.</span><span class="sxs-lookup"><span data-stu-id="3f008-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="3f008-114">Das Cmdlet ruft Informationen des Knotens "Node_1" in der selbst gehosteten Integrationslaufzeit "test-selfhost-ir" in der Daten factory 'test-df-eu2' ab, einschließlich der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3f008-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="3f008-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f008-115">PARAMETERS</span></span>

### <span data-ttu-id="3f008-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3f008-116">-DataFactoryName</span></span>
<span data-ttu-id="3f008-117">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="3f008-117">The data factory name.</span></span>

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

### <span data-ttu-id="3f008-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f008-118">-DefaultProfile</span></span>
<span data-ttu-id="3f008-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f008-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f008-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f008-120">-InputObject</span></span>
<span data-ttu-id="3f008-121">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3f008-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="3f008-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3f008-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="3f008-123">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3f008-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f008-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="3f008-124">-IpAddress</span></span>
<span data-ttu-id="3f008-125">Die IP-Adresse des Integrationslaufzeitknotens.</span><span class="sxs-lookup"><span data-stu-id="3f008-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="3f008-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3f008-126">-Name</span></span>
<span data-ttu-id="3f008-127">Der Name des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="3f008-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f008-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f008-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f008-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f008-129">The resource group name.</span></span>

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

### <span data-ttu-id="3f008-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f008-130">-ResourceId</span></span>
<span data-ttu-id="3f008-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3f008-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3f008-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f008-132">CommonParameters</span></span>
<span data-ttu-id="3f008-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f008-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f008-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f008-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f008-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f008-135">INPUTS</span></span>

### <span data-ttu-id="3f008-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3f008-136">System.String</span></span>

### <span data-ttu-id="3f008-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f008-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3f008-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f008-138">OUTPUTS</span></span>

### <span data-ttu-id="3f008-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="3f008-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="3f008-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="3f008-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="3f008-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f008-141">NOTES</span></span>
<span data-ttu-id="3f008-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="3f008-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="3f008-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f008-143">RELATED LINKS</span></span>

[<span data-ttu-id="3f008-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f008-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
