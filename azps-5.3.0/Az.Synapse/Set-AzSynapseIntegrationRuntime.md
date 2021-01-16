---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470291"
---
# <span data-ttu-id="e6248-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e6248-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="e6248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6248-102">SYNOPSIS</span></span>
<span data-ttu-id="e6248-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="e6248-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6248-104">SYNTAX</span></span>

### <span data-ttu-id="e6248-105">SetByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6248-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="e6248-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e6248-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6248-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="e6248-107">SetByParentObject</span></span>
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

### <span data-ttu-id="e6248-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="e6248-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6248-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6248-109">SetByResourceId</span></span>
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

### <span data-ttu-id="e6248-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="e6248-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6248-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e6248-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="e6248-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e6248-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6248-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6248-113">DESCRIPTION</span></span>
<span data-ttu-id="e6248-114">Das **Cmdlet "Set-AzSynapseIntegrationRuntime"** aktualisiert eine Integrationslaufzeit mit bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="e6248-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="e6248-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6248-115">EXAMPLES</span></span>

### <span data-ttu-id="e6248-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6248-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="e6248-117">Das Cmdlet aktualisiert die Beschreibung der Integrationslaufzeit namens "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="e6248-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="e6248-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e6248-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="e6248-119">Das Cmdlet fügt den Arbeitsbereich zur Verwendung der Laufzeit für die gemeinsame Integration hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6248-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="e6248-120">Bei Verwendung `-SharedIntegrationRuntimeResourceId` von `-Type` Parametern muss auch das eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e6248-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="e6248-121">Beachten Sie, dass dem Arbeitsbereich die Berechtigung zur Verwendung der Integrationslaufzeit erteilt werden muss, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6248-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="e6248-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6248-122">PARAMETERS</span></span>

### <span data-ttu-id="e6248-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="e6248-123">-AuthKey</span></span>
<span data-ttu-id="e6248-124">Der Authentifizierungsschlüssel der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="e6248-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="e6248-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="e6248-126">Die Anmeldeinformationen des Katalogdatenbankadministrators der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="e6248-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="e6248-127">-CatalogPricingTier</span></span>
<span data-ttu-id="e6248-128">Die Preisstufe der Katalogdatenbank der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="e6248-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6248-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="e6248-130">Der Endpunkt des Katalogdatenbankservers der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="e6248-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="e6248-131">-DataFlowComputeType</span></span>
<span data-ttu-id="e6248-132">Der Rechentyp des Datenflussclusters, der den Datenflussauftrag ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="e6248-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="e6248-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="e6248-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="e6248-134">Die Kernanzahl des Datenflussclusters, der den Datenflussauftrag ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="e6248-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="e6248-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="e6248-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="e6248-136">Die Zeit zum Leben (in Minuten) des Datenflussclusters, der den Datenflussauftrag ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="e6248-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="e6248-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e6248-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="e6248-138">Der Self-Hosted Integration Runtime-Name, der als Proxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6248-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="e6248-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="e6248-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="e6248-140">Der Name des verknüpften Azure Blob Storage-Diensts, der auf den Stagingdatenspeicher verweist, der beim Verschieben von Daten zwischen Self-Hosted und Azure-SSIS Integration Runtime verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6248-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="e6248-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="e6248-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="e6248-142">Der Pfad im Stagingdatenspeicher, der beim Verschieben von Daten zwischen Self-Hosted und Azure-SSIS-Integrations-Runtimes verwendet wird, wird ein Standardcontainer verwendet, wenn keine Daten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e6248-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="e6248-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6248-143">-DefaultProfile</span></span>
<span data-ttu-id="e6248-144">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6248-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6248-145">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6248-145">-Description</span></span>
<span data-ttu-id="e6248-146">Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="e6248-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="e6248-147">-Edition</span></span>
<span data-ttu-id="e6248-148">Die Edition für die SSIS-Integrationslaufzeit, die "Standard" oder "Enterprise" sein könnte, ist "Standard", wenn sie nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e6248-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="e6248-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="e6248-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="e6248-150">Die express benutzerdefinierte Einrichtung für die SSIS-Integrationslaufzeit, die zum Einrichten von Konfigurationen und Komponenten von Drittanbietern ohne benutzerdefiniertes Setupskript verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6248-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="e6248-151">-Force</span><span class="sxs-lookup"><span data-stu-id="e6248-151">-Force</span></span>
<span data-ttu-id="e6248-152">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="e6248-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e6248-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6248-153">-InputObject</span></span>
<span data-ttu-id="e6248-154">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6248-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="e6248-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e6248-155">-LicenseType</span></span>
<span data-ttu-id="e6248-156">Der Lizenztyp, den Sie für SSIS IR auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="e6248-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="e6248-157">Es gibt zwei Typen: "LicenseIncluded" oder "BasePrice".</span><span class="sxs-lookup"><span data-stu-id="e6248-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="e6248-158">Wenn Sie für die Preise von Azure Hybrid Use Benefit (AHUB) qualifiziert sind, wählen Sie "BasePrice" aus.</span><span class="sxs-lookup"><span data-stu-id="e6248-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="e6248-159">Wenn nicht, wählen Sie "LicenseIncluded" aus.</span><span class="sxs-lookup"><span data-stu-id="e6248-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="e6248-160">-Location</span><span class="sxs-lookup"><span data-stu-id="e6248-160">-Location</span></span>
<span data-ttu-id="e6248-161">Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="e6248-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="e6248-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="e6248-163">Maximale Anzahl paralleler Ausführung pro Knoten für eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="e6248-164">-Name</span><span class="sxs-lookup"><span data-stu-id="e6248-164">-Name</span></span>
<span data-ttu-id="e6248-165">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="e6248-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e6248-166">-NodeCount</span></span>
<span data-ttu-id="e6248-167">Anzahl der Zielknoten der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="e6248-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="e6248-168">-NodeSize</span></span>
<span data-ttu-id="e6248-169">Die Größe des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="e6248-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="e6248-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="e6248-170">-PublicIP</span></span>
<span data-ttu-id="e6248-171">Die statischen öffentlichen IP-Adressen, die von der Integrationslaufzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6248-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="e6248-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6248-172">-ResourceGroupName</span></span>
<span data-ttu-id="e6248-173">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e6248-173">Resource group name.</span></span>

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

### <span data-ttu-id="e6248-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6248-174">-ResourceId</span></span>
<span data-ttu-id="e6248-175">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="e6248-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="e6248-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="e6248-177">Der SAS-URI des Azure-BLOB-Containers, der das benutzerdefinierte Setupskript enthält.</span><span class="sxs-lookup"><span data-stu-id="e6248-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="e6248-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="e6248-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="e6248-179">Die Ressourcen-ID der freigegebenen selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e6248-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="e6248-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e6248-180">-Subnet</span></span>
<span data-ttu-id="e6248-181">Der Name des Subnetzes im VNet.</span><span class="sxs-lookup"><span data-stu-id="e6248-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="e6248-182">-Type</span><span class="sxs-lookup"><span data-stu-id="e6248-182">-Type</span></span>
<span data-ttu-id="e6248-183">Der Integrationslaufzeittyp.</span><span class="sxs-lookup"><span data-stu-id="e6248-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="e6248-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="e6248-184">-VNetId</span></span>
<span data-ttu-id="e6248-185">Die ID des VNets, dem die Integrationslaufzeit hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e6248-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="e6248-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6248-186">-WorkspaceName</span></span>
<span data-ttu-id="e6248-187">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e6248-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e6248-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6248-188">-WorkspaceObject</span></span>
<span data-ttu-id="e6248-189">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e6248-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e6248-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6248-190">-Confirm</span></span>
<span data-ttu-id="e6248-191">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6248-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6248-192">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e6248-192">-WhatIf</span></span>
<span data-ttu-id="e6248-193">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6248-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6248-194">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6248-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6248-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6248-195">CommonParameters</span></span>
<span data-ttu-id="e6248-196">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6248-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6248-197">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6248-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6248-198">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6248-198">INPUTS</span></span>

### <span data-ttu-id="e6248-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6248-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e6248-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e6248-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e6248-201">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6248-201">OUTPUTS</span></span>

### <span data-ttu-id="e6248-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e6248-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e6248-203">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e6248-203">NOTES</span></span>

## <span data-ttu-id="e6248-204">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e6248-204">RELATED LINKS</span></span>
