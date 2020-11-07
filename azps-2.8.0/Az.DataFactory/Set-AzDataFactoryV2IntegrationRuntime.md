---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651668"
---
# <span data-ttu-id="91b12-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="91b12-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="91b12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91b12-102">SYNOPSIS</span></span>
<span data-ttu-id="91b12-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="91b12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91b12-104">SYNTAX</span></span>

### <span data-ttu-id="91b12-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="91b12-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b12-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91b12-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b12-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="91b12-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b12-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="91b12-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b12-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="91b12-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b12-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="91b12-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91b12-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91b12-111">DESCRIPTION</span></span>
<span data-ttu-id="91b12-112">Das Set-AzDataFactoryV2IntegrationRuntime-Cmdlet aktualisiert eine Integrationslaufzeit mit bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="91b12-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="91b12-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91b12-113">EXAMPLES</span></span>

### <span data-ttu-id="91b12-114">Beispiel 1: Update-Integrationslauf Zeit Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="91b12-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="91b12-115">Das Cmdlet aktualisiert die Beschreibung der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="91b12-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="91b12-116">Beispiel 2: Freigeben der selbst gehosteten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="91b12-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="91b12-117">Das Cmdlet fügt die ADF hinzu, um die Common Integration Runtime zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="91b12-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="91b12-118">Bei Verwendung `-SharedIntegrationRuntimeResourceId` des Parameters `-Type` muss auch der Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="91b12-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="91b12-119">Beachten Sie, dass der Data Factory die Berechtigung erteilt werden muss, die Integrationslaufzeit zu verwenden, bevor Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91b12-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="91b12-120">Beispiel 3: Konfigurieren Sie Self-Hosted IR als Proxy für Azure-SSIS-IR in ADF.</span><span class="sxs-lookup"><span data-stu-id="91b12-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="91b12-121">Das Cmdlet Update Azure-SSIS-Integrationslaufzeit, um die selbst gehostete Integrationslaufzeit als Datenproxy zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="91b12-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="91b12-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="91b12-122">PARAMETERS</span></span>

### <span data-ttu-id="91b12-123">-Authentifizierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="91b12-123">-AuthKey</span></span>
<span data-ttu-id="91b12-124">Der Authentifizierungsschlüssel der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="91b12-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="91b12-126">Die Anmeldeinformationen für den Katalogdaten Bank Administrator der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="91b12-127">-CatalogPricingTier</span></span>
<span data-ttu-id="91b12-128">Die Preisstufe der Katalogdatenbank der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91b12-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="91b12-130">Der Katalogdatenbankserver-Endpunkt der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="91b12-131">-DataFactoryName</span></span>
<span data-ttu-id="91b12-132">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="91b12-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="91b12-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="91b12-134">Der Name der Self-Hosted-Integrationslaufzeit, der als Proxy verwendet wird</span><span class="sxs-lookup"><span data-stu-id="91b12-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="91b12-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="91b12-136">Der Namen des Azure BLOB-Speicher-verknüpften Diensts, der auf den Stagingdaten-Speicher verweist, der beim Verschieben von Daten zwischen Self-Hosted und Azure-SSIS-Integrationslaufzeit verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="91b12-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="91b12-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="91b12-138">Der Pfad im Staging-Datenspeicher, der beim Verschieben von Daten zwischen Self-Hosted-und Azure-SSIS-Integrations Runtime verwendet werden soll, wird ein Standardcontainer verwendet, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="91b12-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b12-139">-DefaultProfile</span></span>
<span data-ttu-id="91b12-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91b12-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b12-141">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91b12-141">-Description</span></span>
<span data-ttu-id="91b12-142">Die Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-142">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="91b12-143">-Edition</span></span>
<span data-ttu-id="91b12-144">Die Edition für die SSIS-Integrationslaufzeit, die Standard oder Enterprise sein kann, Standard ist Standard, wenn Sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="91b12-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-145">-Force</span><span class="sxs-lookup"><span data-stu-id="91b12-145">-Force</span></span>
<span data-ttu-id="91b12-146">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="91b12-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="91b12-147">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91b12-147">-InputObject</span></span>
<span data-ttu-id="91b12-148">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="91b12-148">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="91b12-149">-LicenseType</span></span>
<span data-ttu-id="91b12-150">Der Lizenztyp, den Sie für die SSIS-IR auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="91b12-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="91b12-151">Es gibt zwei Typen: LicenseIncluded oder Grundpr..</span><span class="sxs-lookup"><span data-stu-id="91b12-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="91b12-152">Wenn Sie für die Azure Hybrid use Benefit (AHUB)-Preise qualifiziert sind, wählen Sie Grundpr. aus.</span><span class="sxs-lookup"><span data-stu-id="91b12-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="91b12-153">Wenn dies nicht der Fall ist, wählen Sie LicenseIncluded aus.</span><span class="sxs-lookup"><span data-stu-id="91b12-153">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-154">-Standort</span><span class="sxs-lookup"><span data-stu-id="91b12-154">-Location</span></span>
<span data-ttu-id="91b12-155">Der Speicherort der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-155">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="91b12-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="91b12-157">Maximale parallele Ausführungsanzahl pro Knoten für eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-158">-Name</span><span class="sxs-lookup"><span data-stu-id="91b12-158">-Name</span></span>
<span data-ttu-id="91b12-159">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-159">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="91b12-160">-NodeCount</span></span>
<span data-ttu-id="91b12-161">Die Anzahl der Zielknoten der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-161">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-162">-Knoten</span><span class="sxs-lookup"><span data-stu-id="91b12-162">-NodeSize</span></span>
<span data-ttu-id="91b12-163">Die Knoten Größe der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-163">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b12-164">-ResourceGroupName</span></span>
<span data-ttu-id="91b12-165">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91b12-165">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-166">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="91b12-166">-ResourceId</span></span>
<span data-ttu-id="91b12-167">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="91b12-167">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="91b12-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="91b12-169">Der SAS-URI des Azure-BLOB-Containers, der das benutzerdefinierte Setupskript enthält.</span><span class="sxs-lookup"><span data-stu-id="91b12-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="91b12-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="91b12-171">Die Ressourcen-ID der freigegebenen selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-171">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-172">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="91b12-172">-Subnet</span></span>
<span data-ttu-id="91b12-173">Der Name des Subnets in der VNet.</span><span class="sxs-lookup"><span data-stu-id="91b12-173">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-174">-Typ</span><span class="sxs-lookup"><span data-stu-id="91b12-174">-Type</span></span>
<span data-ttu-id="91b12-175">Der Typ der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91b12-175">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="91b12-176">-VNetId</span></span>
<span data-ttu-id="91b12-177">Die ID des VNet, dem die Integrationslaufzeit Beitritt.</span><span class="sxs-lookup"><span data-stu-id="91b12-177">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b12-178">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91b12-178">-Confirm</span></span>
<span data-ttu-id="91b12-179">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91b12-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b12-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b12-180">-WhatIf</span></span>
<span data-ttu-id="91b12-181">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91b12-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="91b12-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b12-182">CommonParameters</span></span>
<span data-ttu-id="91b12-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b12-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b12-184">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b12-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b12-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91b12-185">INPUTS</span></span>

### <span data-ttu-id="91b12-186">System. String</span><span class="sxs-lookup"><span data-stu-id="91b12-186">System.String</span></span>

### <span data-ttu-id="91b12-187">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="91b12-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="91b12-188">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91b12-188">OUTPUTS</span></span>

### <span data-ttu-id="91b12-189">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="91b12-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="91b12-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="91b12-190">NOTES</span></span>

## <span data-ttu-id="91b12-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91b12-191">RELATED LINKS</span></span>

[<span data-ttu-id="91b12-192">Satz-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="91b12-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
