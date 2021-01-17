---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386279"
---
# <span data-ttu-id="907fe-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="907fe-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="907fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="907fe-102">SYNOPSIS</span></span>
<span data-ttu-id="907fe-103">Aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="907fe-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="907fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="907fe-104">SYNTAX</span></span>

### <span data-ttu-id="907fe-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="907fe-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="907fe-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="907fe-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="907fe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="907fe-107">DESCRIPTION</span></span>
<span data-ttu-id="907fe-108">Aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="907fe-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="907fe-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="907fe-109">EXAMPLES</span></span>

### <span data-ttu-id="907fe-110">Beispiel 1: Aktualisieren eines vorhandenen Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="907fe-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="907fe-111">Der oben aufgeführte Befehl aktualisiert die SKU des Kusto-Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="907fe-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="907fe-112">Beispiel 2: Aktualisieren eines vorhandenen Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="907fe-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="907fe-113">Der oben aufgeführte Befehl aktualisiert den Cluster "testnewkustocluster" in der Ressourcengruppe "testrg" mit einem vom Kunden verwalteten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="907fe-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="907fe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="907fe-114">PARAMETERS</span></span>

### <span data-ttu-id="907fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="907fe-115">-AsJob</span></span>
<span data-ttu-id="907fe-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="907fe-116">Run the command as a job</span></span>

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

### <span data-ttu-id="907fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907fe-117">-DefaultProfile</span></span>
<span data-ttu-id="907fe-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="907fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="907fe-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="907fe-120">Ein boolescher Wert, der angibt, ob die Datenträger des Cluster verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="907fe-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="907fe-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="907fe-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="907fe-122">Ein boolescher Wert, der angibt, ob die doppelte Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="907fe-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="907fe-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="907fe-123">-EnablePurge</span></span>
<span data-ttu-id="907fe-124">Ein boolescher Wert, der angibt, ob die Reinigungsvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="907fe-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="907fe-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="907fe-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="907fe-126">Ein boolescher Wert, der angibt, ob die Streamingaufnahme aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="907fe-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="907fe-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="907fe-127">-EngineType</span></span>
<span data-ttu-id="907fe-128">Der Modultyp</span><span class="sxs-lookup"><span data-stu-id="907fe-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="907fe-129">-IdentityType</span></span>
<span data-ttu-id="907fe-130">Der Typ der verwalteten Identität, die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="907fe-130">The type of managed identity used.</span></span>
<span data-ttu-id="907fe-131">Der Typ "SystemAssigned, UserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Reihe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="907fe-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="907fe-132">Mit dem Typ "Keine" werden alle Identitäten entfernt.</span><span class="sxs-lookup"><span data-stu-id="907fe-132">The type 'None' will remove all identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="907fe-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="907fe-134">Die Liste der Benutzeridentitäten, die dem Cluster "Kusto" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="907fe-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="907fe-135">Die Verweise auf benutzeridentitätswörterbücher werden ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="907fe-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="907fe-136">-InputObject</span></span>
<span data-ttu-id="907fe-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="907fe-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="907fe-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="907fe-139">Der Name des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="907fe-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="907fe-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="907fe-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="907fe-141">Die URI des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="907fe-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="907fe-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="907fe-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="907fe-143">Die Version des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="907fe-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="907fe-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="907fe-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="907fe-145">Dem Benutzer zugewiesene Identität (ARM Ressourcen-ID), der Zugriff auf den Schlüssel hat.</span><span class="sxs-lookup"><span data-stu-id="907fe-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="907fe-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="907fe-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="907fe-147">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="907fe-147">The list of language extensions.</span></span>
<span data-ttu-id="907fe-148">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="907fe-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-149">-Location</span><span class="sxs-lookup"><span data-stu-id="907fe-149">-Location</span></span>
<span data-ttu-id="907fe-150">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="907fe-150">Resource location.</span></span>

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

### <span data-ttu-id="907fe-151">-Name</span><span class="sxs-lookup"><span data-stu-id="907fe-151">-Name</span></span>
<span data-ttu-id="907fe-152">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="907fe-152">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="907fe-153">-NoWait</span></span>
<span data-ttu-id="907fe-154">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="907fe-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="907fe-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="907fe-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="907fe-156">Ein boolescher Wert, der angibt, ob das feature für die optimierte Autoskala aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="907fe-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="907fe-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="907fe-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="907fe-158">Maximale Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="907fe-158">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="907fe-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="907fe-160">Mindestanzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="907fe-160">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="907fe-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="907fe-162">Die Version der Vorlage wurde definiert, z. B. 1.</span><span class="sxs-lookup"><span data-stu-id="907fe-162">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907fe-163">-ResourceGroupName</span></span>
<span data-ttu-id="907fe-164">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="907fe-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-165">-Sku1</span><span class="sxs-lookup"><span data-stu-id="907fe-165">-SkuCapacity</span></span>
<span data-ttu-id="907fe-166">Die Anzahl der Instanzen des Clusters.</span><span class="sxs-lookup"><span data-stu-id="907fe-166">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="907fe-167">-SkuName</span></span>
<span data-ttu-id="907fe-168">SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="907fe-168">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="907fe-169">-SkuTier</span></span>
<span data-ttu-id="907fe-170">SKU-Stufe.</span><span class="sxs-lookup"><span data-stu-id="907fe-170">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="907fe-171">-SubscriptionId</span></span>
<span data-ttu-id="907fe-172">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="907fe-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="907fe-173">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="907fe-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="907fe-174">-Tag</span></span>
<span data-ttu-id="907fe-175">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="907fe-175">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="907fe-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="907fe-177">Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="907fe-177">The cluster's external tenants.</span></span>
<span data-ttu-id="907fe-178">Informationen zum Erstellen finden Sie im #A0 für VERTRAUENSWÜRDIGEEXTERNALTENANT-Eigenschaften und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="907fe-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907fe-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="907fe-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="907fe-180">Ressourcen-ID der öffentlichen IP-Adresse des Datenverwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="907fe-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="907fe-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="907fe-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="907fe-182">Die öffentliche IP-Adressressourcen-ID des Moduldiensts.</span><span class="sxs-lookup"><span data-stu-id="907fe-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="907fe-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="907fe-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="907fe-184">Die Subnetzressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="907fe-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="907fe-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="907fe-185">-Confirm</span></span>
<span data-ttu-id="907fe-186">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="907fe-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907fe-187">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="907fe-187">-WhatIf</span></span>
<span data-ttu-id="907fe-188">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="907fe-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="907fe-189">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="907fe-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="907fe-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907fe-190">CommonParameters</span></span>
<span data-ttu-id="907fe-191">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907fe-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907fe-192">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="907fe-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907fe-193">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="907fe-193">INPUTS</span></span>

### <span data-ttu-id="907fe-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="907fe-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="907fe-195">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="907fe-195">OUTPUTS</span></span>

### <span data-ttu-id="907fe-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="907fe-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="907fe-197">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="907fe-197">NOTES</span></span>

<span data-ttu-id="907fe-198">ALIASE</span><span class="sxs-lookup"><span data-stu-id="907fe-198">ALIASES</span></span>

<span data-ttu-id="907fe-199">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="907fe-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="907fe-200">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="907fe-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="907fe-201">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="907fe-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="907fe-202">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="907fe-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="907fe-203">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="907fe-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="907fe-204">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="907fe-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="907fe-205">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="907fe-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="907fe-206">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="907fe-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="907fe-207">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="907fe-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="907fe-208">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="907fe-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="907fe-209">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="907fe-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="907fe-210">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="907fe-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="907fe-211">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="907fe-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="907fe-212">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="907fe-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="907fe-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="907fe-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="907fe-214">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="907fe-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="907fe-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: Externe Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="907fe-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="907fe-216">`[Value <String>]`: GUID, die einen externen Mandanten darstellt.</span><span class="sxs-lookup"><span data-stu-id="907fe-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="907fe-217">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="907fe-217">RELATED LINKS</span></span>

