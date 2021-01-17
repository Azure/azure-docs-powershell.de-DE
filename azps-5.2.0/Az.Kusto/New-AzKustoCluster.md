---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359048"
---
# <span data-ttu-id="d5fa8-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d5fa8-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="d5fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fa8-103">Erstellen oder aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="d5fa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5fa8-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5fa8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fa8-106">Erstellen oder aktualisieren Sie einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="d5fa8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="d5fa8-108">Beispiel 1: Erstellen eines neuen Kusto-Cluster</span><span class="sxs-lookup"><span data-stu-id="d5fa8-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d5fa8-109">Mit dem oben angegebenen Befehl wird ein neuer "Kusto"-Cluster namens "testnewkustocluster" in der Ressourcengruppe "testrg" erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="d5fa8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5fa8-110">PARAMETERS</span></span>

### <span data-ttu-id="d5fa8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5fa8-111">-AsJob</span></span>
<span data-ttu-id="d5fa8-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d5fa8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d5fa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fa8-113">-DefaultProfile</span></span>
<span data-ttu-id="d5fa8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5fa8-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d5fa8-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="d5fa8-116">Ein boolescher Wert, der angibt, ob die Datenträger des Cluster verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="d5fa8-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="d5fa8-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="d5fa8-118">Ein boolescher Wert, der angibt, ob die doppelte Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="d5fa8-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="d5fa8-119">-EnablePurge</span></span>
<span data-ttu-id="d5fa8-120">Ein boolescher Wert, der angibt, ob die Reinigungsvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="d5fa8-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="d5fa8-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="d5fa8-122">Ein boolescher Wert, der angibt, ob die Streamingaufnahme aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="d5fa8-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d5fa8-123">-IdentityType</span></span>
<span data-ttu-id="d5fa8-124">Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-124">The identity type.</span></span>

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

### <span data-ttu-id="d5fa8-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d5fa8-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="d5fa8-126">Die Liste der Benutzeridentitäten, die dem Cluster "Kusto" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="d5fa8-127">Die Verweise auf benutzeridentitätswörterbücher werden ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="d5fa8-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="d5fa8-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="d5fa8-129">Der Name des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="d5fa8-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d5fa8-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="d5fa8-131">Die URI des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="d5fa8-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d5fa8-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="d5fa8-133">Die Version des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="d5fa8-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="d5fa8-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="d5fa8-135">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-135">The list of language extensions.</span></span>
<span data-ttu-id="d5fa8-136">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5fa8-137">-Location</span><span class="sxs-lookup"><span data-stu-id="d5fa8-137">-Location</span></span>
<span data-ttu-id="d5fa8-138">Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="d5fa8-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="d5fa8-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d5fa8-139">-Name</span></span>
<span data-ttu-id="d5fa8-140">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d5fa8-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5fa8-141">-NoWait</span></span>
<span data-ttu-id="d5fa8-142">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d5fa8-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d5fa8-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d5fa8-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="d5fa8-144">Ein boolescher Wert, der angibt, ob das feature für die optimierte Autoskala aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="d5fa8-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="d5fa8-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="d5fa8-146">Maximale Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="d5fa8-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="d5fa8-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="d5fa8-148">Mindestanzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="d5fa8-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="d5fa8-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="d5fa8-150">Die Version der Vorlage wurde definiert, z. B. 1.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="d5fa8-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5fa8-151">-ResourceGroupName</span></span>
<span data-ttu-id="d5fa8-152">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d5fa8-153">-Sku1</span><span class="sxs-lookup"><span data-stu-id="d5fa8-153">-SkuCapacity</span></span>
<span data-ttu-id="d5fa8-154">Die Anzahl der Instanzen des Cluster.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="d5fa8-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d5fa8-155">-SkuName</span></span>
<span data-ttu-id="d5fa8-156">SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-156">SKU name.</span></span>

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

### <span data-ttu-id="d5fa8-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d5fa8-157">-SkuTier</span></span>
<span data-ttu-id="d5fa8-158">SKU-Stufe.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-158">SKU tier.</span></span>

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

### <span data-ttu-id="d5fa8-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5fa8-159">-SubscriptionId</span></span>
<span data-ttu-id="d5fa8-160">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5fa8-161">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d5fa8-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5fa8-162">-Tag</span></span>
<span data-ttu-id="d5fa8-163">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-163">Resource tags.</span></span>

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

### <span data-ttu-id="d5fa8-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="d5fa8-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="d5fa8-165">Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-165">The cluster's external tenants.</span></span>
<span data-ttu-id="d5fa8-166">Informationen zum Erstellen finden Sie im #A0 für VERTRAUENSWÜRDIGEEXTERNALTENANT-Eigenschaften und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5fa8-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="d5fa8-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="d5fa8-168">Ressourcen-ID der öffentlichen IP-Adresse des Datenverwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="d5fa8-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="d5fa8-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="d5fa8-170">Die öffentliche IP-Adressressourcen-ID des Moduldiensts.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="d5fa8-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="d5fa8-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="d5fa8-172">Die Subnetzressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="d5fa8-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="d5fa8-173">-Zone</span></span>
<span data-ttu-id="d5fa8-174">Die Verfügbarkeitszonen des Cluster.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="d5fa8-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5fa8-175">-Confirm</span></span>
<span data-ttu-id="d5fa8-176">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5fa8-177">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d5fa8-177">-WhatIf</span></span>
<span data-ttu-id="d5fa8-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5fa8-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5fa8-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fa8-180">CommonParameters</span></span>
<span data-ttu-id="d5fa8-181">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fa8-182">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5fa8-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fa8-183">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5fa8-183">INPUTS</span></span>

## <span data-ttu-id="d5fa8-184">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5fa8-184">OUTPUTS</span></span>

### <span data-ttu-id="d5fa8-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span><span class="sxs-lookup"><span data-stu-id="d5fa8-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="d5fa8-186">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5fa8-186">NOTES</span></span>

<span data-ttu-id="d5fa8-187">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d5fa8-187">ALIASES</span></span>

<span data-ttu-id="d5fa8-188">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d5fa8-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5fa8-189">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5fa8-190">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5fa8-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="d5fa8-192">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="d5fa8-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: Externe Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="d5fa8-194">`[Value <String>]`: GUID, die einen externen Mandanten darstellt.</span><span class="sxs-lookup"><span data-stu-id="d5fa8-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="d5fa8-195">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5fa8-195">RELATED LINKS</span></span>

