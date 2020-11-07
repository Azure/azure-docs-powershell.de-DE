---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: e8f631b485c62dba2e3871d5c2deec69881097af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663177"
---
# <span data-ttu-id="a5b58-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a5b58-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="a5b58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5b58-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b58-103">Ruft eine Integration Runtime-Knoten Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="a5b58-103">Gets an integration runtime node infomation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5b58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5b58-104">SYNTAX</span></span>

### <span data-ttu-id="a5b58-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5b58-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b58-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b58-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5b58-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a5b58-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5b58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5b58-108">DESCRIPTION</span></span>
<span data-ttu-id="a5b58-109">Das Cmdlet " **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** " Ruft die Detailinformationen eines Integrationslauf Zeit Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="a5b58-109">The **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="a5b58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5b58-110">EXAMPLES</span></span>

### <span data-ttu-id="a5b58-111">Beispiel 1: Ruft die Detailinformationen eines Integrationslauf Zeit Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="a5b58-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

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

<span data-ttu-id="a5b58-112">Das Cmdlet ruft Informationen über den Knoten "Node_1" in der selbst gehosteten Integrationslaufzeit "Test-SelfHost-IR" in Data Factory "Test-DF-EU2" ab.</span><span class="sxs-lookup"><span data-stu-id="a5b58-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="a5b58-113">Beispiel 2: Ruft die Detailinformationen eines Integrationslauf Zeit Knotens zusammen mit der IP-Adresse ab.</span><span class="sxs-lookup"><span data-stu-id="a5b58-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

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

<span data-ttu-id="a5b58-114">Das Cmdlet ruft Informationen über den Knoten "Node_1" in der selbst gehosteten Integrationslaufzeit "Test-SelfHost-IR" in Data Factory "Test-DF-EU2" ab, einschließlich der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a5b58-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="a5b58-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5b58-115">PARAMETERS</span></span>

### <span data-ttu-id="a5b58-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a5b58-116">-DataFactoryName</span></span>
<span data-ttu-id="a5b58-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a5b58-117">The data factory name.</span></span>

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

### <span data-ttu-id="a5b58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b58-118">-DefaultProfile</span></span>
<span data-ttu-id="a5b58-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5b58-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b58-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5b58-120">-InputObject</span></span>
<span data-ttu-id="a5b58-121">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5b58-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="a5b58-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a5b58-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a5b58-123">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a5b58-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="a5b58-124">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a5b58-124">-IpAddress</span></span>
<span data-ttu-id="a5b58-125">Die IP-Adresse des Integrationslauf Zeit Knotens.</span><span class="sxs-lookup"><span data-stu-id="a5b58-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="a5b58-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a5b58-126">-Name</span></span>
<span data-ttu-id="a5b58-127">Der Knotenname der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a5b58-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="a5b58-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b58-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5b58-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5b58-129">The resource group name.</span></span>

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

### <span data-ttu-id="a5b58-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5b58-130">-ResourceId</span></span>
<span data-ttu-id="a5b58-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a5b58-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a5b58-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b58-132">CommonParameters</span></span>
<span data-ttu-id="a5b58-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b58-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b58-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b58-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b58-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5b58-135">INPUTS</span></span>

### <span data-ttu-id="a5b58-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b58-136">System.String</span></span>

### <span data-ttu-id="a5b58-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a5b58-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="a5b58-138">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5b58-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a5b58-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5b58-139">OUTPUTS</span></span>

### <span data-ttu-id="a5b58-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a5b58-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="a5b58-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a5b58-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a5b58-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5b58-142">NOTES</span></span>
<span data-ttu-id="a5b58-143">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="a5b58-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="a5b58-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5b58-144">RELATED LINKS</span></span>

[<span data-ttu-id="a5b58-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a5b58-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
