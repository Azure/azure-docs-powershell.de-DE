---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470480"
---
# <span data-ttu-id="379e5-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="379e5-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="379e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379e5-102">SYNOPSIS</span></span>
<span data-ttu-id="379e5-103">Erstellen oder aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="379e5-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="379e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="379e5-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="379e5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="379e5-105">DESCRIPTION</span></span>
<span data-ttu-id="379e5-106">Erstellen oder aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="379e5-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="379e5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="379e5-107">EXAMPLES</span></span>

### <span data-ttu-id="379e5-108">Beispiel 1: Erstellen eines neuen Kusto-Cluster</span><span class="sxs-lookup"><span data-stu-id="379e5-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="379e5-109">Mit dem oben angegebenen Befehl wird ein neuer "Kusto"-Cluster namens "testnewkustocluster" in der Ressourcengruppe "testrg" erstellt.</span><span class="sxs-lookup"><span data-stu-id="379e5-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="379e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="379e5-110">PARAMETERS</span></span>

### <span data-ttu-id="379e5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="379e5-111">-AsJob</span></span>
<span data-ttu-id="379e5-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="379e5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="379e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379e5-113">-DefaultProfile</span></span>
<span data-ttu-id="379e5-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="379e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379e5-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="379e5-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="379e5-116">Ein boolescher Wert, der angibt, ob die Datenträger des Cluster verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="379e5-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="379e5-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="379e5-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="379e5-118">Ein boolescher Wert, der angibt, ob die doppelte Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="379e5-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="379e5-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="379e5-119">-EnablePurge</span></span>
<span data-ttu-id="379e5-120">Ein boolescher Wert, der angibt, ob die Reinigungsvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="379e5-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="379e5-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="379e5-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="379e5-122">Ein boolescher Wert, der angibt, ob die Streamingaufnahme aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="379e5-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="379e5-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="379e5-123">-EngineType</span></span>
<span data-ttu-id="379e5-124">Der Modultyp</span><span class="sxs-lookup"><span data-stu-id="379e5-124">The engine type</span></span>

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

### <span data-ttu-id="379e5-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="379e5-125">-IdentityType</span></span>
<span data-ttu-id="379e5-126">Der Typ der verwalteten Identität, die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="379e5-126">The type of managed identity used.</span></span>
<span data-ttu-id="379e5-127">Der Typ "SystemAssigned, UserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Reihe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="379e5-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="379e5-128">Mit dem Typ "Keine" werden alle Identitäten entfernt.</span><span class="sxs-lookup"><span data-stu-id="379e5-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="379e5-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="379e5-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="379e5-130">Die Liste der Benutzeridentitäten, die dem Cluster "Kusto" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="379e5-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="379e5-131">Die Verweise auf benutzeridentitätswörterbücher werden ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="379e5-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="379e5-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="379e5-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="379e5-133">Der Name des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="379e5-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="379e5-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="379e5-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="379e5-135">Die URI des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="379e5-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="379e5-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="379e5-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="379e5-137">Die Version des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="379e5-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="379e5-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="379e5-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="379e5-139">Dem Benutzer zugewiesene Identität (ARM Ressourcen-ID), der Zugriff auf den Schlüssel hat.</span><span class="sxs-lookup"><span data-stu-id="379e5-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="379e5-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="379e5-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="379e5-141">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="379e5-141">The list of language extensions.</span></span>
<span data-ttu-id="379e5-142">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="379e5-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="379e5-143">-Location</span><span class="sxs-lookup"><span data-stu-id="379e5-143">-Location</span></span>
<span data-ttu-id="379e5-144">Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="379e5-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="379e5-145">-Name</span><span class="sxs-lookup"><span data-stu-id="379e5-145">-Name</span></span>
<span data-ttu-id="379e5-146">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="379e5-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379e5-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="379e5-147">-NoWait</span></span>
<span data-ttu-id="379e5-148">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="379e5-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="379e5-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="379e5-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="379e5-150">Ein boolescher Wert, der angibt, ob das feature für die optimierte Autoskala aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="379e5-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="379e5-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="379e5-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="379e5-152">Maximale Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="379e5-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="379e5-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="379e5-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="379e5-154">Mindestanzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="379e5-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="379e5-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="379e5-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="379e5-156">Die Version der Vorlage wurde definiert, z. B. 1.</span><span class="sxs-lookup"><span data-stu-id="379e5-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="379e5-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379e5-157">-ResourceGroupName</span></span>
<span data-ttu-id="379e5-158">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="379e5-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="379e5-159">-Sku1</span><span class="sxs-lookup"><span data-stu-id="379e5-159">-SkuCapacity</span></span>
<span data-ttu-id="379e5-160">Die Anzahl der Instanzen des Cluster.</span><span class="sxs-lookup"><span data-stu-id="379e5-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="379e5-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="379e5-161">-SkuName</span></span>
<span data-ttu-id="379e5-162">SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="379e5-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379e5-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="379e5-163">-SkuTier</span></span>
<span data-ttu-id="379e5-164">SKU-Stufe.</span><span class="sxs-lookup"><span data-stu-id="379e5-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379e5-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="379e5-165">-SubscriptionId</span></span>
<span data-ttu-id="379e5-166">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="379e5-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="379e5-167">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="379e5-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379e5-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="379e5-168">-Tag</span></span>
<span data-ttu-id="379e5-169">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="379e5-169">Resource tags.</span></span>

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

### <span data-ttu-id="379e5-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="379e5-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="379e5-171">Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="379e5-171">The cluster's external tenants.</span></span>
<span data-ttu-id="379e5-172">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für VERTRAUENSWÜRDIGEEXTERNALTENANT-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="379e5-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="379e5-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="379e5-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="379e5-174">Ressourcen-ID der öffentlichen IP-Adresse des Datenverwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="379e5-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="379e5-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="379e5-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="379e5-176">Die öffentliche IP-Adressressourcen-ID des Moduldiensts.</span><span class="sxs-lookup"><span data-stu-id="379e5-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="379e5-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="379e5-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="379e5-178">Die Subnetzressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="379e5-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="379e5-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="379e5-179">-Zone</span></span>
<span data-ttu-id="379e5-180">Die Verfügbarkeitszonen des Cluster.</span><span class="sxs-lookup"><span data-stu-id="379e5-180">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379e5-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="379e5-181">-Confirm</span></span>
<span data-ttu-id="379e5-182">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="379e5-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="379e5-183">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="379e5-183">-WhatIf</span></span>
<span data-ttu-id="379e5-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="379e5-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="379e5-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="379e5-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="379e5-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379e5-186">CommonParameters</span></span>
<span data-ttu-id="379e5-187">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379e5-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379e5-188">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="379e5-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379e5-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="379e5-189">INPUTS</span></span>

## <span data-ttu-id="379e5-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="379e5-190">OUTPUTS</span></span>

### <span data-ttu-id="379e5-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="379e5-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="379e5-192">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="379e5-192">NOTES</span></span>

<span data-ttu-id="379e5-193">ALIASE</span><span class="sxs-lookup"><span data-stu-id="379e5-193">ALIASES</span></span>

<span data-ttu-id="379e5-194">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="379e5-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="379e5-195">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="379e5-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="379e5-196">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="379e5-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="379e5-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="379e5-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="379e5-198">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="379e5-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="379e5-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: Externe Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="379e5-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="379e5-200">`[Value <String>]`: GUID, die einen externen Mandanten darstellt.</span><span class="sxs-lookup"><span data-stu-id="379e5-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="379e5-201">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="379e5-201">RELATED LINKS</span></span>

