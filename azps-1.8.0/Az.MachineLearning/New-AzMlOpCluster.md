---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819179"
---
# <span data-ttu-id="2dddd-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2dddd-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="2dddd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2dddd-102">SYNOPSIS</span></span>
<span data-ttu-id="2dddd-103">Erstellt einen neuen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddd-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="2dddd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dddd-104">SYNTAX</span></span>

### <span data-ttu-id="2dddd-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="2dddd-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dddd-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="2dddd-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dddd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dddd-107">DESCRIPTION</span></span>
<span data-ttu-id="2dddd-108">Erstellt einen neuen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddd-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="2dddd-109">Dadurch wird ein Clusterobjekt, ein Containerdienst, falls erforderlich, Anwendungs Einblicke und eine Azure Container-Registrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2dddd-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="2dddd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dddd-110">EXAMPLES</span></span>

### <span data-ttu-id="2dddd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2dddd-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="2dddd-112">Erstellt einen neuen Operations Cluster mit Azure Container Service und Kubernetes als Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="2dddd-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="2dddd-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2dddd-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="2dddd-114">Erstellt einen neuen Operations Cluster lokal.</span><span class="sxs-lookup"><span data-stu-id="2dddd-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="2dddd-115">Dadurch wird eine Azure Container-Registrierung, Anwendungs Einblicke und ein Speicherkonto erstellt, aber kein Containerdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="2dddd-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="2dddd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dddd-116">PARAMETERS</span></span>

### <span data-ttu-id="2dddd-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="2dddd-117">-AgentCount</span></span>
<span data-ttu-id="2dddd-118">Die Anzahl der Agenten Knoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddd-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="2dddd-119">-AgentVmSize</span></span>
<span data-ttu-id="2dddd-120">Die Anzahl der Agenten Knoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddd-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2dddd-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="2dddd-122">Der URI der zu verwendenden Azure Container-Registrierung, anstatt eine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2dddd-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="2dddd-123">-ClientId</span></span>
<span data-ttu-id="2dddd-124">Die ePO-Dienstprinzipal-ID des ACS-Clusters.</span><span class="sxs-lookup"><span data-stu-id="2dddd-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-125">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="2dddd-125">-ClusterType</span></span>
<span data-ttu-id="2dddd-126">Der Zuordnungs Clustertyp.</span><span class="sxs-lookup"><span data-stu-id="2dddd-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dddd-127">-DefaultProfile</span></span>
<span data-ttu-id="2dddd-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2dddd-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dddd-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dddd-129">-Description</span></span>
<span data-ttu-id="2dddd-130">Die Anzahl der Masterknoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddd-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="2dddd-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="2dddd-132">Zusätzliche Eigenschaften für die globale Dienstkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2dddd-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="2dddd-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="2dddd-134">Das Konfigurations-ETag für Updates.</span><span class="sxs-lookup"><span data-stu-id="2dddd-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2dddd-135">-InputObject</span></span>
<span data-ttu-id="2dddd-136">Die Clustereigenschaften für die Operation.</span><span class="sxs-lookup"><span data-stu-id="2dddd-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="2dddd-137">-Location</span></span>
<span data-ttu-id="2dddd-138">Der Standort des Operations Clusters.</span><span class="sxs-lookup"><span data-stu-id="2dddd-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="2dddd-139">-MasterCount</span></span>
<span data-ttu-id="2dddd-140">Die Anzahl der Masterknoten im ACS-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddd-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-141">-Name</span><span class="sxs-lookup"><span data-stu-id="2dddd-141">-Name</span></span>
<span data-ttu-id="2dddd-142">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="2dddd-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="2dddd-143">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="2dddd-143">-OrchestratorType</span></span>
<span data-ttu-id="2dddd-144">Der Orchestrator-Typ des ACS-Clusters.</span><span class="sxs-lookup"><span data-stu-id="2dddd-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dddd-145">-ResourceGroupName</span></span>
<span data-ttu-id="2dddd-146">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="2dddd-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="2dddd-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="2dddd-147">-Secret</span></span>
<span data-ttu-id="2dddd-148">Der Hauptschlüssel des Orchestrator-Diensts des ACS-Clusters.</span><span class="sxs-lookup"><span data-stu-id="2dddd-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="2dddd-149">-SslCertificate</span></span>
<span data-ttu-id="2dddd-150">Die SSL-Zertifikatsdaten im PEM-Format, die als base64-Zeichenfolge codiert sind.</span><span class="sxs-lookup"><span data-stu-id="2dddd-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="2dddd-151">-SslCName</span></span>
<span data-ttu-id="2dddd-152">Der CNAME für das SSL-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="2dddd-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="2dddd-153">-SslKey</span></span>
<span data-ttu-id="2dddd-154">Die SSL-Schlüsseldaten im PEM-Format, die als base64-Zeichenfolge codiert sind.</span><span class="sxs-lookup"><span data-stu-id="2dddd-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="2dddd-155">-SslStatus</span></span>
<span data-ttu-id="2dddd-156">SSL-Status</span><span class="sxs-lookup"><span data-stu-id="2dddd-156">SSL status.</span></span>
<span data-ttu-id="2dddd-157">Mögliche Werte sind "aktiviert" und "deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="2dddd-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2dddd-158">-StorageAccount</span></span>
<span data-ttu-id="2dddd-159">Der URI des zu verwendenden speicherkontos, anstatt eines zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2dddd-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dddd-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2dddd-160">-Confirm</span></span>
<span data-ttu-id="2dddd-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dddd-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dddd-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dddd-162">-WhatIf</span></span>
<span data-ttu-id="2dddd-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dddd-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dddd-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dddd-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dddd-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dddd-165">CommonParameters</span></span>
<span data-ttu-id="2dddd-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dddd-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dddd-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dddd-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dddd-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2dddd-168">INPUTS</span></span>

### <span data-ttu-id="2dddd-169">Keine</span><span class="sxs-lookup"><span data-stu-id="2dddd-169">None</span></span>

## <span data-ttu-id="2dddd-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2dddd-170">OUTPUTS</span></span>

### <span data-ttu-id="2dddd-171">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2dddd-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="2dddd-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="2dddd-172">NOTES</span></span>

## <span data-ttu-id="2dddd-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2dddd-173">RELATED LINKS</span></span>
