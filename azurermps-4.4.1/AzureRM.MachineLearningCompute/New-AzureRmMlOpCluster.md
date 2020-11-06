---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500829"
---
# <span data-ttu-id="f5100-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5100-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="f5100-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5100-102">SYNOPSIS</span></span>
<span data-ttu-id="f5100-103">Erstellt einen neuen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="f5100-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5100-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5100-104">SYNTAX</span></span>

### <span data-ttu-id="f5100-105">Erstellen Sie einen neuen Einsatz Cluster aus einer OperationalizationCluster-Instanzen Definition.</span><span class="sxs-lookup"><span data-stu-id="f5100-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f5100-106">Erstellen eines neuen Operations Clusters aus Cmdlet-Eingabeparametern</span><span class="sxs-lookup"><span data-stu-id="f5100-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f5100-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5100-107">DESCRIPTION</span></span>
<span data-ttu-id="f5100-108">Erstellt einen neuen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="f5100-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="f5100-109">Dadurch wird ein Clusterobjekt, ein Containerdienst, falls erforderlich, Anwendungs Einblicke und eine Azure Container-Registrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5100-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="f5100-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5100-110">EXAMPLES</span></span>

### <span data-ttu-id="f5100-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5100-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="f5100-112">Erstellt einen neuen Operations Cluster mit Azure Container Service und Kubernetes als Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="f5100-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="f5100-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f5100-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="f5100-114">Erstellt einen neuen Operations Cluster lokal.</span><span class="sxs-lookup"><span data-stu-id="f5100-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="f5100-115">Dadurch wird eine Azure Container-Registrierung, Anwendungs Einblicke und ein Speicherkonto erstellt, aber kein Containerdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5100-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="f5100-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5100-116">PARAMETERS</span></span>

### <span data-ttu-id="f5100-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="f5100-117">-AgentCount</span></span>
<span data-ttu-id="f5100-118">Die Anzahl der Agenten Knoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f5100-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="f5100-119">-AgentVmSize</span></span>
<span data-ttu-id="f5100-120">Die Anzahl der Agenten Knoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f5100-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5100-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="f5100-122">Der URI der zu verwendenden Azure Container-Registrierung, anstatt eine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5100-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5100-123">-InputObject</span></span>
<span data-ttu-id="f5100-124">Die Clustereigenschaften für die Operation.</span><span class="sxs-lookup"><span data-stu-id="f5100-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-125">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="f5100-125">-ClusterType</span></span>
<span data-ttu-id="f5100-126">Der Zuordnungs Clustertyp.</span><span class="sxs-lookup"><span data-stu-id="f5100-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5100-127">-Confirm</span></span>
<span data-ttu-id="f5100-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5100-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5100-129">-Description</span></span>
<span data-ttu-id="f5100-130">Die Anzahl der Masterknoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f5100-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="f5100-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="f5100-132">Zusätzliche Eigenschaften für die globale Dienstkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5100-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="f5100-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="f5100-134">Das Konfigurations-ETag für Updates.</span><span class="sxs-lookup"><span data-stu-id="f5100-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="f5100-135">-Location</span></span>
<span data-ttu-id="f5100-136">Der Standort des Operations Clusters.</span><span class="sxs-lookup"><span data-stu-id="f5100-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="f5100-137">-MasterCount</span></span>
<span data-ttu-id="f5100-138">Die Anzahl der Masterknoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f5100-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-139">-Name</span><span class="sxs-lookup"><span data-stu-id="f5100-139">-Name</span></span>
<span data-ttu-id="f5100-140">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="f5100-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-141">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="f5100-141">-OrchestratorType</span></span>
<span data-ttu-id="f5100-142">Der Orchestrator-Typ des ACS-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f5100-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5100-143">-ResourceGroupName</span></span>
<span data-ttu-id="f5100-144">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="f5100-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-145">-ClientID</span><span class="sxs-lookup"><span data-stu-id="f5100-145">-ClientId</span></span>
<span data-ttu-id="f5100-146">Die ePO-Dienstprinzipal-ID des ACS-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f5100-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="f5100-147">-Secret</span></span>
<span data-ttu-id="f5100-148">Der Hauptschlüssel des Orchestrator-Diensts des ACS-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f5100-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="f5100-149">-SslCName</span></span>
<span data-ttu-id="f5100-150">Der CNAME für das SSL-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="f5100-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5100-151">-SslCertificate</span></span>
<span data-ttu-id="f5100-152">Die SSL-Zertifikatsdaten im PEM-Format, die als base64-Zeichenfolge codiert sind.</span><span class="sxs-lookup"><span data-stu-id="f5100-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="f5100-153">-SslKey</span></span>
<span data-ttu-id="f5100-154">Die SSL-Schlüsseldaten im PEM-Format, die als base64-Zeichenfolge codiert sind.</span><span class="sxs-lookup"><span data-stu-id="f5100-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="f5100-155">-SslStatus</span></span>
<span data-ttu-id="f5100-156">SSL-Status</span><span class="sxs-lookup"><span data-stu-id="f5100-156">SSL status.</span></span>
<span data-ttu-id="f5100-157">Mögliche Werte sind "aktiviert" und "deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="f5100-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5100-158">-StorageAccount</span></span>
<span data-ttu-id="f5100-159">Der URI des zu verwendenden speicherkontos, anstatt eines zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5100-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5100-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5100-160">-WhatIf</span></span>
<span data-ttu-id="f5100-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5100-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5100-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5100-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f5100-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5100-163">INPUTS</span></span>

### <span data-ttu-id="f5100-164">Keine</span><span class="sxs-lookup"><span data-stu-id="f5100-164">None</span></span>


## <span data-ttu-id="f5100-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5100-165">OUTPUTS</span></span>

### <span data-ttu-id="f5100-166">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="f5100-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="f5100-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5100-167">NOTES</span></span>

## <span data-ttu-id="f5100-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5100-168">RELATED LINKS</span></span>

