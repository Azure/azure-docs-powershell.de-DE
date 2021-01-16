---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366902"
---
# <span data-ttu-id="e0b6e-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e0b6e-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="e0b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b6e-103">Aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="e0b6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0b6e-104">SYNTAX</span></span>

### <span data-ttu-id="e0b6e-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0b6e-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0b6e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e0b6e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0b6e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0b6e-107">DESCRIPTION</span></span>
<span data-ttu-id="e0b6e-108">Aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="e0b6e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0b6e-109">EXAMPLES</span></span>

### <span data-ttu-id="e0b6e-110">Beispiel 1: Aktualisieren eines vorhandenen Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="e0b6e-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e0b6e-111">Der oben aufgeführte Befehl aktualisiert die SKU des Kusto-Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="e0b6e-112">Beispiel 2: Aktualisieren eines vorhandenen Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="e0b6e-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e0b6e-113">Der oben aufgeführte Befehl aktualisiert den Cluster "testnewkustocluster" in der Ressourcengruppe "testrg" mit einem vom Kunden verwalteten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="e0b6e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0b6e-114">PARAMETERS</span></span>

### <span data-ttu-id="e0b6e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0b6e-115">-AsJob</span></span>
<span data-ttu-id="e0b6e-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e0b6e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e0b6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b6e-117">-DefaultProfile</span></span>
<span data-ttu-id="e0b6e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b6e-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e0b6e-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="e0b6e-120">Ein boolescher Wert, der angibt, ob die Datenträger des Cluster verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="e0b6e-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="e0b6e-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="e0b6e-122">Ein boolescher Wert, der angibt, ob die doppelte Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="e0b6e-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="e0b6e-123">-EnablePurge</span></span>
<span data-ttu-id="e0b6e-124">Ein boolescher Wert, der angibt, ob die Reinigungsvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="e0b6e-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="e0b6e-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="e0b6e-126">Ein boolescher Wert, der angibt, ob die Streamingaufnahme aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="e0b6e-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e0b6e-127">-IdentityType</span></span>
<span data-ttu-id="e0b6e-128">Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-128">The identity type.</span></span>

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

### <span data-ttu-id="e0b6e-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e0b6e-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="e0b6e-130">Die Liste der Benutzeridentitäten, die dem Cluster "Kusto" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="e0b6e-131">Die Verweise auf benutzeridentitätswörterbücher werden ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="e0b6e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b6e-132">-InputObject</span></span>
<span data-ttu-id="e0b6e-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0b6e-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="e0b6e-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="e0b6e-135">Der Name des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="e0b6e-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e0b6e-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="e0b6e-137">Die URI des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="e0b6e-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e0b6e-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="e0b6e-139">Die Version des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="e0b6e-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="e0b6e-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="e0b6e-141">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-141">The list of language extensions.</span></span>
<span data-ttu-id="e0b6e-142">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b6e-143">-Location</span><span class="sxs-lookup"><span data-stu-id="e0b6e-143">-Location</span></span>
<span data-ttu-id="e0b6e-144">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-144">Resource location.</span></span>

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

### <span data-ttu-id="e0b6e-145">-Name</span><span class="sxs-lookup"><span data-stu-id="e0b6e-145">-Name</span></span>
<span data-ttu-id="e0b6e-146">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e0b6e-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0b6e-147">-NoWait</span></span>
<span data-ttu-id="e0b6e-148">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e0b6e-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0b6e-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="e0b6e-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="e0b6e-150">Ein boolescher Wert, der angibt, ob das feature für die optimierte Autoskala aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="e0b6e-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="e0b6e-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="e0b6e-152">Maximale Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="e0b6e-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="e0b6e-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="e0b6e-154">Mindestanzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="e0b6e-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="e0b6e-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="e0b6e-156">Die Version der Vorlage wurde definiert, z. B. 1.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="e0b6e-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b6e-157">-ResourceGroupName</span></span>
<span data-ttu-id="e0b6e-158">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e0b6e-159">-Sku1</span><span class="sxs-lookup"><span data-stu-id="e0b6e-159">-SkuCapacity</span></span>
<span data-ttu-id="e0b6e-160">Die Anzahl der Instanzen des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="e0b6e-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e0b6e-161">-SkuName</span></span>
<span data-ttu-id="e0b6e-162">SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-162">SKU name.</span></span>

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

### <span data-ttu-id="e0b6e-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e0b6e-163">-SkuTier</span></span>
<span data-ttu-id="e0b6e-164">SKU-Stufe.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-164">SKU tier.</span></span>

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

### <span data-ttu-id="e0b6e-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0b6e-165">-SubscriptionId</span></span>
<span data-ttu-id="e0b6e-166">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0b6e-167">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e0b6e-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0b6e-168">-Tag</span></span>
<span data-ttu-id="e0b6e-169">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-169">Resource tags.</span></span>

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

### <span data-ttu-id="e0b6e-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="e0b6e-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="e0b6e-171">Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-171">The cluster's external tenants.</span></span>
<span data-ttu-id="e0b6e-172">Informationen zum Erstellen finden Sie im #A0 für VERTRAUENSWÜRDIGEEXTERNALTENANT-Eigenschaften und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b6e-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="e0b6e-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="e0b6e-174">Ressourcen-ID der öffentlichen IP-Adresse des Datenverwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="e0b6e-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="e0b6e-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="e0b6e-176">Die öffentliche IP-Adressressourcen-ID des Moduldiensts.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="e0b6e-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="e0b6e-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="e0b6e-178">Die Subnetzressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="e0b6e-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0b6e-179">-Confirm</span></span>
<span data-ttu-id="e0b6e-180">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b6e-181">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e0b6e-181">-WhatIf</span></span>
<span data-ttu-id="e0b6e-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b6e-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b6e-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b6e-184">CommonParameters</span></span>
<span data-ttu-id="e0b6e-185">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b6e-186">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0b6e-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b6e-187">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0b6e-187">INPUTS</span></span>

### <span data-ttu-id="e0b6e-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e0b6e-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e0b6e-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0b6e-189">OUTPUTS</span></span>

### <span data-ttu-id="e0b6e-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span><span class="sxs-lookup"><span data-stu-id="e0b6e-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="e0b6e-191">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e0b6e-191">NOTES</span></span>

<span data-ttu-id="e0b6e-192">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e0b6e-192">ALIASES</span></span>

<span data-ttu-id="e0b6e-193">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e0b6e-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0b6e-194">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0b6e-195">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0b6e-196">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b6e-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0b6e-197">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e0b6e-198">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e0b6e-199">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e0b6e-200">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="e0b6e-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e0b6e-201">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e0b6e-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0b6e-202">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e0b6e-203">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e0b6e-204">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e0b6e-205">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e0b6e-206">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="e0b6e-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="e0b6e-208">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="e0b6e-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: Externe Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="e0b6e-210">`[Value <String>]`: GUID, die einen externen Mandanten darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0b6e-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="e0b6e-211">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e0b6e-211">RELATED LINKS</span></span>

