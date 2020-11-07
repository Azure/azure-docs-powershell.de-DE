---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820335"
---
# <span data-ttu-id="9f2a2-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9f2a2-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="9f2a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2a2-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="9f2a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f2a2-104">SYNTAX</span></span>

### <span data-ttu-id="9f2a2-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f2a2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2a2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2a2-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2a2-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2a2-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2a2-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9f2a2-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2a2-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9f2a2-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2a2-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9f2a2-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f2a2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f2a2-111">DESCRIPTION</span></span>
<span data-ttu-id="9f2a2-112">Das Set-AzDataFactoryV2IntegrationRuntime-Cmdlet aktualisiert eine Integrationslaufzeit mit bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="9f2a2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f2a2-113">EXAMPLES</span></span>

### <span data-ttu-id="9f2a2-114">Beispiel 1: Update-Integrationslauf Zeit Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="9f2a2-115">Das Cmdlet aktualisiert die Beschreibung der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="9f2a2-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="9f2a2-116">Beispiel 2: Freigeben der selbst gehosteten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="9f2a2-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="9f2a2-117">Das Cmdlet fügt die ADF hinzu, um die Common Integration Runtime zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="9f2a2-118">Bei Verwendung `-SharedIntegrationRuntimeResourceId` des Parameters `-Type` muss auch der Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="9f2a2-119">Beachten Sie, dass der Data Factory die Berechtigung erteilt werden muss, die Integrationslaufzeit zu verwenden, bevor Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="9f2a2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f2a2-120">PARAMETERS</span></span>

### <span data-ttu-id="9f2a2-121">-Authentifizierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="9f2a2-121">-AuthKey</span></span>
<span data-ttu-id="9f2a2-122">Der Authentifizierungsschlüssel der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="9f2a2-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="9f2a2-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="9f2a2-124">Die Anmeldeinformationen für den Katalogdaten Bank Administrator der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="9f2a2-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="9f2a2-125">-CatalogPricingTier</span></span>
<span data-ttu-id="9f2a2-126">Die Preisstufe der Katalogdatenbank der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="9f2a2-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f2a2-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="9f2a2-128">Der Katalogdatenbankserver-Endpunkt der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="9f2a2-129">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9f2a2-129">-DataFactoryName</span></span>
<span data-ttu-id="9f2a2-130">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-130">The data factory name.</span></span>

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

### <span data-ttu-id="9f2a2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2a2-131">-DefaultProfile</span></span>
<span data-ttu-id="9f2a2-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f2a2-133">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f2a2-133">-Description</span></span>
<span data-ttu-id="9f2a2-134">Die Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="9f2a2-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="9f2a2-135">-Edition</span></span>
<span data-ttu-id="9f2a2-136">Die Edition für die SSIS-Integrationslaufzeit, die Standard oder Enterprise sein kann, Standard ist Standard, wenn Sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="9f2a2-137">-Force</span><span class="sxs-lookup"><span data-stu-id="9f2a2-137">-Force</span></span>
<span data-ttu-id="9f2a2-138">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9f2a2-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f2a2-139">-InputObject</span></span>
<span data-ttu-id="9f2a2-140">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="9f2a2-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9f2a2-141">-LicenseType</span></span>
<span data-ttu-id="9f2a2-142">Der Lizenztyp, den Sie für die SSIS-IR auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="9f2a2-143">Es gibt zwei Typen: LicenseIncluded oder Grundpr..</span><span class="sxs-lookup"><span data-stu-id="9f2a2-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="9f2a2-144">Wenn Sie für die Azure Hybrid use Benefit (AHUB)-Preise qualifiziert sind, wählen Sie Grundpr. aus.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="9f2a2-145">Wenn dies nicht der Fall ist, wählen Sie LicenseIncluded aus.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="9f2a2-146">-Standort</span><span class="sxs-lookup"><span data-stu-id="9f2a2-146">-Location</span></span>
<span data-ttu-id="9f2a2-147">Der Speicherort der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="9f2a2-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="9f2a2-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="9f2a2-149">Maximale parallele Ausführungsanzahl pro Knoten für eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="9f2a2-150">-Name</span><span class="sxs-lookup"><span data-stu-id="9f2a2-150">-Name</span></span>
<span data-ttu-id="9f2a2-151">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="9f2a2-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9f2a2-152">-NodeCount</span></span>
<span data-ttu-id="9f2a2-153">Die Anzahl der Zielknoten der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="9f2a2-154">-Knoten</span><span class="sxs-lookup"><span data-stu-id="9f2a2-154">-NodeSize</span></span>
<span data-ttu-id="9f2a2-155">Die Knoten Größe der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="9f2a2-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2a2-156">-ResourceGroupName</span></span>
<span data-ttu-id="9f2a2-157">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-157">The resource group name.</span></span>

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

### <span data-ttu-id="9f2a2-158">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9f2a2-158">-ResourceId</span></span>
<span data-ttu-id="9f2a2-159">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9f2a2-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="9f2a2-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="9f2a2-161">Der SAS-URI des Azure-BLOB-Containers, der das benutzerdefinierte Setupskript enthält.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="9f2a2-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2a2-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="9f2a2-163">Die Ressourcen-ID der freigegebenen selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="9f2a2-164">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="9f2a2-164">-Subnet</span></span>
<span data-ttu-id="9f2a2-165">Der Name des Subnets in der VNet.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="9f2a2-166">-Typ</span><span class="sxs-lookup"><span data-stu-id="9f2a2-166">-Type</span></span>
<span data-ttu-id="9f2a2-167">Der Typ der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="9f2a2-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="9f2a2-168">-VNetId</span></span>
<span data-ttu-id="9f2a2-169">Die ID des VNet, dem die Integrationslaufzeit Beitritt.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="9f2a2-170">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f2a2-170">-Confirm</span></span>
<span data-ttu-id="9f2a2-171">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f2a2-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f2a2-172">-WhatIf</span></span>
<span data-ttu-id="9f2a2-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9f2a2-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2a2-174">CommonParameters</span></span>
<span data-ttu-id="9f2a2-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f2a2-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2a2-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f2a2-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2a2-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f2a2-177">INPUTS</span></span>

### <span data-ttu-id="9f2a2-178">System. String</span><span class="sxs-lookup"><span data-stu-id="9f2a2-178">System.String</span></span>

### <span data-ttu-id="9f2a2-179">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9f2a2-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9f2a2-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f2a2-180">OUTPUTS</span></span>

### <span data-ttu-id="9f2a2-181">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9f2a2-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9f2a2-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f2a2-182">NOTES</span></span>

## <span data-ttu-id="9f2a2-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f2a2-183">RELATED LINKS</span></span>

[<span data-ttu-id="9f2a2-184">Satz-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9f2a2-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
