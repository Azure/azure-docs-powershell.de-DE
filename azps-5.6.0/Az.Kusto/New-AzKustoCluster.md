---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: c8378e9be3c92cc799eb92b9ff913be98116b019
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922411"
---
# <span data-ttu-id="0779f-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0779f-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="0779f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0779f-102">SYNOPSIS</span></span>
<span data-ttu-id="0779f-103">Erstellen oder Aktualisieren eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="0779f-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="0779f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0779f-104">SYNTAX</span></span>

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

## <span data-ttu-id="0779f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0779f-105">DESCRIPTION</span></span>
<span data-ttu-id="0779f-106">Erstellen oder Aktualisieren eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="0779f-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="0779f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0779f-107">EXAMPLES</span></span>

### <span data-ttu-id="0779f-108">Beispiel 1: Erstellen eines neuen Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="0779f-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="0779f-109">Mit dem obigen Befehl wird ein neuer Kusto-Cluster mit dem Namen "testnewkustocluster" in der Ressourcengruppe "testrg" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0779f-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="0779f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0779f-110">PARAMETERS</span></span>

### <span data-ttu-id="0779f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0779f-111">-AsJob</span></span>
<span data-ttu-id="0779f-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0779f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0779f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0779f-113">-DefaultProfile</span></span>
<span data-ttu-id="0779f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0779f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0779f-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0779f-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="0779f-116">Ein boolescher Wert, der angibt, ob die Datenträger des Clusters verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="0779f-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="0779f-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="0779f-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="0779f-118">Ein boolescher Wert, der angibt, ob die doppelte Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0779f-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="0779f-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="0779f-119">-EnablePurge</span></span>
<span data-ttu-id="0779f-120">Ein boolescher Wert, der angibt, ob die Reinigungsvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="0779f-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="0779f-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="0779f-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="0779f-122">Ein boolescher Wert, der angibt, ob die Streamingaufnahme aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0779f-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="0779f-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="0779f-123">-EngineType</span></span>
<span data-ttu-id="0779f-124">Der Motortyp</span><span class="sxs-lookup"><span data-stu-id="0779f-124">The engine type</span></span>

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

### <span data-ttu-id="0779f-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0779f-125">-IdentityType</span></span>
<span data-ttu-id="0779f-126">Der Typ der verwendeten verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="0779f-126">The type of managed identity used.</span></span>
<span data-ttu-id="0779f-127">Der Typ "SystemAssigned, UserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Reihe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="0779f-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="0779f-128">Der Typ "Keine" entfernt alle Identitäten.</span><span class="sxs-lookup"><span data-stu-id="0779f-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="0779f-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0779f-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="0779f-130">Die Liste der Benutzeridentitäten, die dem Kusto-Cluster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0779f-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="0779f-131">Die Schlüsselverweise für das Benutzeridentitätswörterbuch werden ARM Ressourcen-ID im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0779f-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="0779f-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="0779f-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="0779f-133">Der Name des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="0779f-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="0779f-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0779f-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="0779f-135">Der URI des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0779f-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="0779f-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0779f-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="0779f-137">Die Version des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="0779f-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="0779f-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="0779f-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="0779f-139">Der benutzer zugewiesene Identität (ARM-Ressourcen-ID), der Zugriff auf den Schlüssel hat.</span><span class="sxs-lookup"><span data-stu-id="0779f-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="0779f-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="0779f-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="0779f-141">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="0779f-141">The list of language extensions.</span></span>
<span data-ttu-id="0779f-142">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu den EIGENSCHAFTEN VON LANGUAGEEXTENSIONVALUE und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0779f-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="0779f-143">-Location</span><span class="sxs-lookup"><span data-stu-id="0779f-143">-Location</span></span>
<span data-ttu-id="0779f-144">Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="0779f-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="0779f-145">-Name</span><span class="sxs-lookup"><span data-stu-id="0779f-145">-Name</span></span>
<span data-ttu-id="0779f-146">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="0779f-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0779f-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0779f-147">-NoWait</span></span>
<span data-ttu-id="0779f-148">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0779f-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0779f-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="0779f-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="0779f-150">Ein boolescher Wert, der angibt, ob das optimierte Feature für die automatische Skalierung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0779f-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="0779f-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="0779f-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="0779f-152">Maximale Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="0779f-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="0779f-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="0779f-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="0779f-154">Anzahl der zulässigen Mindestinstanzen.</span><span class="sxs-lookup"><span data-stu-id="0779f-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="0779f-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="0779f-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="0779f-156">Die Version der Vorlage wurde definiert, z. B. 1.</span><span class="sxs-lookup"><span data-stu-id="0779f-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="0779f-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0779f-157">-ResourceGroupName</span></span>
<span data-ttu-id="0779f-158">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="0779f-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0779f-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0779f-159">-SkuCapacity</span></span>
<span data-ttu-id="0779f-160">Die Anzahl der Instanzen des Clusters.</span><span class="sxs-lookup"><span data-stu-id="0779f-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="0779f-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0779f-161">-SkuName</span></span>
<span data-ttu-id="0779f-162">SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="0779f-162">SKU name.</span></span>

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

### <span data-ttu-id="0779f-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0779f-163">-SkuTier</span></span>
<span data-ttu-id="0779f-164">SKU-Ebene.</span><span class="sxs-lookup"><span data-stu-id="0779f-164">SKU tier.</span></span>

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

### <span data-ttu-id="0779f-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0779f-165">-SubscriptionId</span></span>
<span data-ttu-id="0779f-166">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="0779f-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0779f-167">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="0779f-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0779f-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="0779f-168">-Tag</span></span>
<span data-ttu-id="0779f-169">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="0779f-169">Resource tags.</span></span>

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

### <span data-ttu-id="0779f-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="0779f-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="0779f-171">Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="0779f-171">The cluster's external tenants.</span></span>
<span data-ttu-id="0779f-172">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für TRUSTEDEXTERNALTENANT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0779f-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0779f-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="0779f-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="0779f-174">Ressourcen-ID der öffentlichen IP-Adresse der Datenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="0779f-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="0779f-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="0779f-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="0779f-176">Ressourcen-ID der öffentlichen IP-Adresse des Moduldiensts.</span><span class="sxs-lookup"><span data-stu-id="0779f-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="0779f-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="0779f-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="0779f-178">Die Subnetzressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0779f-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="0779f-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="0779f-179">-Zone</span></span>
<span data-ttu-id="0779f-180">Die Verfügbarkeitszonen des Clusters.</span><span class="sxs-lookup"><span data-stu-id="0779f-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="0779f-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0779f-181">-Confirm</span></span>
<span data-ttu-id="0779f-182">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0779f-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0779f-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0779f-183">-WhatIf</span></span>
<span data-ttu-id="0779f-184">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0779f-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0779f-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0779f-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0779f-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0779f-186">CommonParameters</span></span>
<span data-ttu-id="0779f-187">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0779f-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0779f-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0779f-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0779f-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0779f-189">INPUTS</span></span>

## <span data-ttu-id="0779f-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0779f-190">OUTPUTS</span></span>

### <span data-ttu-id="0779f-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="0779f-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="0779f-192">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0779f-192">NOTES</span></span>

<span data-ttu-id="0779f-193">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0779f-193">ALIASES</span></span>

<span data-ttu-id="0779f-194">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0779f-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0779f-195">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="0779f-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0779f-196">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0779f-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0779f-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="0779f-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="0779f-198">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="0779f-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="0779f-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="0779f-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="0779f-200">`[Value <String>]`: GUID, die einen externen Mandanten darstellt.</span><span class="sxs-lookup"><span data-stu-id="0779f-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="0779f-201">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0779f-201">RELATED LINKS</span></span>

