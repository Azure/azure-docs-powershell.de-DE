---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007674"
---
# <span data-ttu-id="1be52-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1be52-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="1be52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1be52-102">SYNOPSIS</span></span>
<span data-ttu-id="1be52-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="1be52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1be52-104">SYNTAX</span></span>

### <span data-ttu-id="1be52-105">SetByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1be52-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be52-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1be52-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be52-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="1be52-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be52-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="1be52-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be52-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1be52-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be52-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="1be52-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be52-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1be52-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be52-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1be52-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1be52-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1be52-113">DESCRIPTION</span></span>
<span data-ttu-id="1be52-114">Das Cmdlet " **Satz-AzSynapseIntegrationRuntime** " aktualisiert eine Integrationslaufzeit mit bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="1be52-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="1be52-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1be52-115">EXAMPLES</span></span>

### <span data-ttu-id="1be52-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1be52-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="1be52-117">Das Cmdlet aktualisiert die Beschreibung der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="1be52-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="1be52-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1be52-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="1be52-119">Das Cmdlet fügt den Arbeitsbereich hinzu, um die Common Integration Runtime zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1be52-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="1be52-120">Bei Verwendung `-SharedIntegrationRuntimeResourceId` des Parameters `-Type` muss auch der Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1be52-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="1be52-121">Beachten Sie, dass dem Arbeitsbereich die Berechtigung erteilt werden muss, die Integrationslaufzeit zu verwenden, bevor Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1be52-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="1be52-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="1be52-122">PARAMETERS</span></span>

### <span data-ttu-id="1be52-123">-Authentifizierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="1be52-123">-AuthKey</span></span>
<span data-ttu-id="1be52-124">Der Authentifizierungsschlüssel der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="1be52-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="1be52-126">Die Anmeldeinformationen für den Katalogdaten Bank Administrator der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="1be52-127">-CatalogPricingTier</span></span>
<span data-ttu-id="1be52-128">Die Preisstufe der Katalogdatenbank der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1be52-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="1be52-130">Der Katalogdatenbankserver-Endpunkt der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="1be52-131">-DataFlowComputeType</span></span>
<span data-ttu-id="1be52-132">Compute-Typ des Datenfluss Clusters, der den Datenfluss Auftrag ausführt.</span><span class="sxs-lookup"><span data-stu-id="1be52-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="1be52-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="1be52-134">Kernanzahl des Datenfluss Clusters, der den Datenfluss Auftrag ausführt.</span><span class="sxs-lookup"><span data-stu-id="1be52-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="1be52-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="1be52-136">Zeit zum Leben (in Minuten) Einstellung des Datenfluss Clusters, der den Datenfluss Auftrag ausführt.</span><span class="sxs-lookup"><span data-stu-id="1be52-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1be52-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="1be52-138">Der Name der Self-Hosted-Integrationslaufzeit, der als Proxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1be52-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="1be52-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="1be52-140">Der Azure BLOB Storage-verknüpfte Dienstname, der auf den Stagingdaten-Datenspeicher verweist, der beim Verschieben von Daten zwischen Self-Hosted und Azure-SSIS-Integrationslaufzeit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1be52-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="1be52-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="1be52-142">Der Pfad im Staging-Datenspeicher, der beim Verschieben von Daten zwischen Self-Hosted-und Azure-SSIS-Integrations Runtime verwendet werden soll, wird ein Standardcontainer verwendet, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="1be52-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be52-143">-DefaultProfile</span></span>
<span data-ttu-id="1be52-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1be52-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be52-145">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1be52-145">-Description</span></span>
<span data-ttu-id="1be52-146">Die Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="1be52-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="1be52-147">-Edition</span></span>
<span data-ttu-id="1be52-148">Die Edition für die SSIS-Integrationslaufzeit, die Standard oder Enterprise sein kann, Standard ist Standard, wenn Sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1be52-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="1be52-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="1be52-150">Das Express-benutzerdefinierte Setup für die SSIS-Integrationslaufzeit, das zum Einrichten von Konfigurationen und Komponenten von Drittanbietern ohne benutzerdefiniertes Setupskript verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1be52-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-151">-Force</span><span class="sxs-lookup"><span data-stu-id="1be52-151">-Force</span></span>
<span data-ttu-id="1be52-152">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="1be52-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1be52-153">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1be52-153">-InputObject</span></span>
<span data-ttu-id="1be52-154">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="1be52-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1be52-155">-LicenseType</span></span>
<span data-ttu-id="1be52-156">Der Lizenztyp, den Sie für die SSIS-IR auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="1be52-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="1be52-157">Es gibt zwei Typen: LicenseIncluded oder Grundpr..</span><span class="sxs-lookup"><span data-stu-id="1be52-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="1be52-158">Wenn Sie für die Azure Hybrid use Benefit (AHUB)-Preise qualifiziert sind, wählen Sie Grundpr. aus.</span><span class="sxs-lookup"><span data-stu-id="1be52-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="1be52-159">Wenn dies nicht der Fall ist, wählen Sie LicenseIncluded aus.</span><span class="sxs-lookup"><span data-stu-id="1be52-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-160">-Standort</span><span class="sxs-lookup"><span data-stu-id="1be52-160">-Location</span></span>
<span data-ttu-id="1be52-161">Die Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="1be52-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="1be52-163">Maximale parallele Ausführungsanzahl pro Knoten für eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-164">-Name</span><span class="sxs-lookup"><span data-stu-id="1be52-164">-Name</span></span>
<span data-ttu-id="1be52-165">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="1be52-166">-NodeCount</span></span>
<span data-ttu-id="1be52-167">Die Anzahl der Zielknoten der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-168">-Knoten</span><span class="sxs-lookup"><span data-stu-id="1be52-168">-NodeSize</span></span>
<span data-ttu-id="1be52-169">Die Knoten Größe der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="1be52-170">-PublicIP</span></span>
<span data-ttu-id="1be52-171">Die statischen öffentlichen IP-Adressen, die von der Integrationslaufzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1be52-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be52-172">-ResourceGroupName</span></span>
<span data-ttu-id="1be52-173">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1be52-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-174">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1be52-174">-ResourceId</span></span>
<span data-ttu-id="1be52-175">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="1be52-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="1be52-177">Der SAS-URI des Azure-BLOB-Containers, der das benutzerdefinierte Setupskript enthält.</span><span class="sxs-lookup"><span data-stu-id="1be52-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="1be52-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="1be52-179">Die Ressourcen-ID der freigegebenen selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-180">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="1be52-180">-Subnet</span></span>
<span data-ttu-id="1be52-181">Der Name des Subnets in der VNet.</span><span class="sxs-lookup"><span data-stu-id="1be52-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-182">-Typ</span><span class="sxs-lookup"><span data-stu-id="1be52-182">-Type</span></span>
<span data-ttu-id="1be52-183">Der Typ der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1be52-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="1be52-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="1be52-184">-VNetId</span></span>
<span data-ttu-id="1be52-185">Die ID des VNet, dem die Integrationslaufzeit beitreten soll.</span><span class="sxs-lookup"><span data-stu-id="1be52-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1be52-186">-WorkspaceName</span></span>
<span data-ttu-id="1be52-187">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1be52-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-188">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1be52-188">-WorkspaceObject</span></span>
<span data-ttu-id="1be52-189">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="1be52-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1be52-190">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1be52-190">-Confirm</span></span>
<span data-ttu-id="1be52-191">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1be52-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be52-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be52-192">-WhatIf</span></span>
<span data-ttu-id="1be52-193">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1be52-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be52-194">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1be52-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be52-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be52-195">CommonParameters</span></span>
<span data-ttu-id="1be52-196">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be52-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be52-197">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1be52-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be52-198">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1be52-198">INPUTS</span></span>

### <span data-ttu-id="1be52-199">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1be52-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1be52-200">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1be52-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1be52-201">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1be52-201">OUTPUTS</span></span>

### <span data-ttu-id="1be52-202">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1be52-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1be52-203">Notizen</span><span class="sxs-lookup"><span data-stu-id="1be52-203">NOTES</span></span>

## <span data-ttu-id="1be52-204">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1be52-204">RELATED LINKS</span></span>
