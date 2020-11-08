---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174697"
---
# <span data-ttu-id="e67bb-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e67bb-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="e67bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e67bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e67bb-103">Aktualisieren eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="e67bb-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="e67bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e67bb-104">SYNTAX</span></span>

### <span data-ttu-id="e67bb-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e67bb-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="e67bb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e67bb-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="e67bb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e67bb-107">DESCRIPTION</span></span>
<span data-ttu-id="e67bb-108">Aktualisieren eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="e67bb-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="e67bb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e67bb-109">EXAMPLES</span></span>

### <span data-ttu-id="e67bb-110">Beispiel 1: Aktualisieren eines vorhandenen Clusters anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="e67bb-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e67bb-111">Der obige Befehl aktualisiert die SKU des Kusto-Clusters "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e67bb-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="e67bb-112">Beispiel 2: Aktualisieren eines vorhandenen Clusters anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="e67bb-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e67bb-113">Der obige Befehl aktualisiert den Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" mit einem vom Kunden verwalteten Schlüssel gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e67bb-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="e67bb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e67bb-114">PARAMETERS</span></span>

### <span data-ttu-id="e67bb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e67bb-115">-AsJob</span></span>
<span data-ttu-id="e67bb-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e67bb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e67bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67bb-117">-DefaultProfile</span></span>
<span data-ttu-id="e67bb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e67bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e67bb-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e67bb-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="e67bb-120">Ein boolescher Wert, der angibt, ob die Datenträger des Clusters verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="e67bb-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="e67bb-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="e67bb-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="e67bb-122">Ein boolescher Wert, der angibt, ob die doppelte Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e67bb-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="e67bb-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="e67bb-123">-EnablePurge</span></span>
<span data-ttu-id="e67bb-124">Ein boolescher Wert, der angibt, ob die Löschvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e67bb-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="e67bb-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="e67bb-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="e67bb-126">Ein boolescher Wert, der angibt, ob die Streaming-Aufnahme aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e67bb-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="e67bb-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e67bb-127">-IdentityType</span></span>
<span data-ttu-id="e67bb-128">Der Identity-Typ.</span><span class="sxs-lookup"><span data-stu-id="e67bb-128">The identity type.</span></span>

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

### <span data-ttu-id="e67bb-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e67bb-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="e67bb-130">Die Liste der Benutzeridentitäten, die dem Kusto-Cluster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e67bb-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="e67bb-131">Die Benutzer-ID-Wörterbuch-Schlüssel Bezüge sind arm-Ressourcen-IDs in der Form: "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="e67bb-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="e67bb-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e67bb-132">-InputObject</span></span>
<span data-ttu-id="e67bb-133">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e67bb-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e67bb-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="e67bb-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="e67bb-135">Der Name des Schlüssel Tresors.</span><span class="sxs-lookup"><span data-stu-id="e67bb-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="e67bb-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e67bb-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="e67bb-137">Der URI des Schlüsselspeichers.</span><span class="sxs-lookup"><span data-stu-id="e67bb-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="e67bb-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e67bb-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="e67bb-139">Die Version des Schlüssel Tresors.</span><span class="sxs-lookup"><span data-stu-id="e67bb-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="e67bb-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="e67bb-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="e67bb-141">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="e67bb-141">The list of language extensions.</span></span>
<span data-ttu-id="e67bb-142">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für LANGUAGEEXTENSIONVALUE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e67bb-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e67bb-143">-Standort</span><span class="sxs-lookup"><span data-stu-id="e67bb-143">-Location</span></span>
<span data-ttu-id="e67bb-144">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="e67bb-144">Resource location.</span></span>

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

### <span data-ttu-id="e67bb-145">-Name</span><span class="sxs-lookup"><span data-stu-id="e67bb-145">-Name</span></span>
<span data-ttu-id="e67bb-146">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="e67bb-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e67bb-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e67bb-147">-NoWait</span></span>
<span data-ttu-id="e67bb-148">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e67bb-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e67bb-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="e67bb-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="e67bb-150">Ein boolescher Wert, der angibt, ob das optimierte AutoSkalieren-Feature aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e67bb-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="e67bb-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="e67bb-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="e67bb-152">Maximale Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e67bb-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="e67bb-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="e67bb-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="e67bb-154">Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e67bb-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="e67bb-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="e67bb-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="e67bb-156">Die Version der Vorlage, die beispielsweise 1 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e67bb-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="e67bb-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e67bb-157">-ResourceGroupName</span></span>
<span data-ttu-id="e67bb-158">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="e67bb-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e67bb-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e67bb-159">-SkuCapacity</span></span>
<span data-ttu-id="e67bb-160">Die Anzahl der Instanzen des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e67bb-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="e67bb-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e67bb-161">-SkuName</span></span>
<span data-ttu-id="e67bb-162">SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="e67bb-162">SKU name.</span></span>

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

### <span data-ttu-id="e67bb-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e67bb-163">-SkuTier</span></span>
<span data-ttu-id="e67bb-164">SKU-Ebene.</span><span class="sxs-lookup"><span data-stu-id="e67bb-164">SKU tier.</span></span>

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

### <span data-ttu-id="e67bb-165">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e67bb-165">-SubscriptionId</span></span>
<span data-ttu-id="e67bb-166">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e67bb-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e67bb-167">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e67bb-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e67bb-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="e67bb-168">-Tag</span></span>
<span data-ttu-id="e67bb-169">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="e67bb-169">Resource tags.</span></span>

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

### <span data-ttu-id="e67bb-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="e67bb-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="e67bb-171">Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e67bb-171">The cluster's external tenants.</span></span>
<span data-ttu-id="e67bb-172">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für TRUSTEDEXTERNALTENANT-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e67bb-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e67bb-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="e67bb-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="e67bb-174">Die Ressourcen-ID der öffentlichen IP-Adresse des Daten Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="e67bb-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="e67bb-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="e67bb-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="e67bb-176">Die Ressourcen-ID der öffentlichen IP-Adresse des Modul Diensts.</span><span class="sxs-lookup"><span data-stu-id="e67bb-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="e67bb-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="e67bb-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="e67bb-178">Die Ressourcen-ID des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="e67bb-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="e67bb-179">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e67bb-179">-Confirm</span></span>
<span data-ttu-id="e67bb-180">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e67bb-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e67bb-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e67bb-181">-WhatIf</span></span>
<span data-ttu-id="e67bb-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e67bb-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e67bb-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e67bb-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e67bb-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67bb-184">CommonParameters</span></span>
<span data-ttu-id="e67bb-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e67bb-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67bb-186">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e67bb-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67bb-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e67bb-187">INPUTS</span></span>

### <span data-ttu-id="e67bb-188">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e67bb-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e67bb-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e67bb-189">OUTPUTS</span></span>

### <span data-ttu-id="e67bb-190">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="e67bb-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="e67bb-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="e67bb-191">NOTES</span></span>

<span data-ttu-id="e67bb-192">Aliase</span><span class="sxs-lookup"><span data-stu-id="e67bb-192">ALIASES</span></span>

<span data-ttu-id="e67bb-193">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e67bb-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e67bb-194">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e67bb-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e67bb-195">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e67bb-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e67bb-196">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e67bb-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e67bb-197">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e67bb-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e67bb-198">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="e67bb-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e67bb-199">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="e67bb-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e67bb-200">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e67bb-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e67bb-201">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e67bb-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e67bb-202">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="e67bb-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e67bb-203">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e67bb-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e67bb-204">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="e67bb-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e67bb-205">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e67bb-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e67bb-206">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e67bb-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="e67bb-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="e67bb-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="e67bb-208">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="e67bb-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="e67bb-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e67bb-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="e67bb-210">`[Value <String>]`: GUID, die einen externen Mandanten darstellt.</span><span class="sxs-lookup"><span data-stu-id="e67bb-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="e67bb-211">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e67bb-211">RELATED LINKS</span></span>

