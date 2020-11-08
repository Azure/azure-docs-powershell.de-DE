---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173759"
---
# <span data-ttu-id="de0ac-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="de0ac-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="de0ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="de0ac-103">Erstellen oder Aktualisieren eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="de0ac-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="de0ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de0ac-104">SYNTAX</span></span>

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

## <span data-ttu-id="de0ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de0ac-105">DESCRIPTION</span></span>
<span data-ttu-id="de0ac-106">Erstellen oder Aktualisieren eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="de0ac-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="de0ac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de0ac-107">EXAMPLES</span></span>

### <span data-ttu-id="de0ac-108">Beispiel 1: Erstellen eines neuen Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="de0ac-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="de0ac-109">Der obige Befehl erstellt einen neuen Kusto-Cluster mit dem Namen "testnewkustocluster" in der Ressourcengruppe "testrg".</span><span class="sxs-lookup"><span data-stu-id="de0ac-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="de0ac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de0ac-110">PARAMETERS</span></span>

### <span data-ttu-id="de0ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de0ac-111">-AsJob</span></span>
<span data-ttu-id="de0ac-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="de0ac-112">Run the command as a job</span></span>

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

### <span data-ttu-id="de0ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0ac-113">-DefaultProfile</span></span>
<span data-ttu-id="de0ac-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de0ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de0ac-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="de0ac-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="de0ac-116">Ein boolescher Wert, der angibt, ob die Datenträger des Clusters verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="de0ac-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="de0ac-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="de0ac-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="de0ac-118">Ein boolescher Wert, der angibt, ob die doppelte Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="de0ac-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="de0ac-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="de0ac-119">-EnablePurge</span></span>
<span data-ttu-id="de0ac-120">Ein boolescher Wert, der angibt, ob die Löschvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="de0ac-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="de0ac-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="de0ac-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="de0ac-122">Ein boolescher Wert, der angibt, ob die Streaming-Aufnahme aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="de0ac-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="de0ac-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="de0ac-123">-IdentityType</span></span>
<span data-ttu-id="de0ac-124">Der Identity-Typ.</span><span class="sxs-lookup"><span data-stu-id="de0ac-124">The identity type.</span></span>

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

### <span data-ttu-id="de0ac-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="de0ac-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="de0ac-126">Die Liste der Benutzeridentitäten, die dem Kusto-Cluster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="de0ac-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="de0ac-127">Die Benutzer-ID-Wörterbuch-Schlüssel Bezüge sind arm-Ressourcen-IDs in der Form: "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="de0ac-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="de0ac-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="de0ac-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="de0ac-129">Der Name des Schlüssel Tresors.</span><span class="sxs-lookup"><span data-stu-id="de0ac-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="de0ac-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="de0ac-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="de0ac-131">Der URI des Schlüsselspeichers.</span><span class="sxs-lookup"><span data-stu-id="de0ac-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="de0ac-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="de0ac-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="de0ac-133">Die Version des Schlüssel Tresors.</span><span class="sxs-lookup"><span data-stu-id="de0ac-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="de0ac-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="de0ac-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="de0ac-135">Die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="de0ac-135">The list of language extensions.</span></span>
<span data-ttu-id="de0ac-136">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für LANGUAGEEXTENSIONVALUE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="de0ac-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="de0ac-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="de0ac-137">-Location</span></span>
<span data-ttu-id="de0ac-138">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="de0ac-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="de0ac-139">-Name</span><span class="sxs-lookup"><span data-stu-id="de0ac-139">-Name</span></span>
<span data-ttu-id="de0ac-140">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="de0ac-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="de0ac-141">-Nowait</span><span class="sxs-lookup"><span data-stu-id="de0ac-141">-NoWait</span></span>
<span data-ttu-id="de0ac-142">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="de0ac-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="de0ac-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="de0ac-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="de0ac-144">Ein boolescher Wert, der angibt, ob das optimierte AutoSkalieren-Feature aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="de0ac-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="de0ac-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="de0ac-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="de0ac-146">Maximale Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="de0ac-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="de0ac-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="de0ac-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="de0ac-148">Anzahl zulässiger Instanzen.</span><span class="sxs-lookup"><span data-stu-id="de0ac-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="de0ac-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="de0ac-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="de0ac-150">Die Version der Vorlage, die beispielsweise 1 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="de0ac-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="de0ac-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0ac-151">-ResourceGroupName</span></span>
<span data-ttu-id="de0ac-152">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="de0ac-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="de0ac-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="de0ac-153">-SkuCapacity</span></span>
<span data-ttu-id="de0ac-154">Die Anzahl der Instanzen des Clusters.</span><span class="sxs-lookup"><span data-stu-id="de0ac-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="de0ac-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="de0ac-155">-SkuName</span></span>
<span data-ttu-id="de0ac-156">SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="de0ac-156">SKU name.</span></span>

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

### <span data-ttu-id="de0ac-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="de0ac-157">-SkuTier</span></span>
<span data-ttu-id="de0ac-158">SKU-Ebene.</span><span class="sxs-lookup"><span data-stu-id="de0ac-158">SKU tier.</span></span>

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

### <span data-ttu-id="de0ac-159">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="de0ac-159">-SubscriptionId</span></span>
<span data-ttu-id="de0ac-160">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="de0ac-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="de0ac-161">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="de0ac-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="de0ac-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="de0ac-162">-Tag</span></span>
<span data-ttu-id="de0ac-163">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="de0ac-163">Resource tags.</span></span>

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

### <span data-ttu-id="de0ac-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="de0ac-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="de0ac-165">Die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="de0ac-165">The cluster's external tenants.</span></span>
<span data-ttu-id="de0ac-166">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für TRUSTEDEXTERNALTENANT-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="de0ac-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de0ac-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="de0ac-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="de0ac-168">Die Ressourcen-ID der öffentlichen IP-Adresse des Daten Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="de0ac-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="de0ac-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="de0ac-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="de0ac-170">Die Ressourcen-ID der öffentlichen IP-Adresse des Modul Diensts.</span><span class="sxs-lookup"><span data-stu-id="de0ac-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="de0ac-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="de0ac-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="de0ac-172">Die Ressourcen-ID des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="de0ac-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="de0ac-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="de0ac-173">-Zone</span></span>
<span data-ttu-id="de0ac-174">Die Verfügbarkeits Zonen des Clusters.</span><span class="sxs-lookup"><span data-stu-id="de0ac-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="de0ac-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de0ac-175">-Confirm</span></span>
<span data-ttu-id="de0ac-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de0ac-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de0ac-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de0ac-177">-WhatIf</span></span>
<span data-ttu-id="de0ac-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de0ac-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de0ac-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de0ac-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de0ac-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0ac-180">CommonParameters</span></span>
<span data-ttu-id="de0ac-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0ac-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0ac-182">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de0ac-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0ac-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de0ac-183">INPUTS</span></span>

## <span data-ttu-id="de0ac-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de0ac-184">OUTPUTS</span></span>

### <span data-ttu-id="de0ac-185">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="de0ac-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="de0ac-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="de0ac-186">NOTES</span></span>

<span data-ttu-id="de0ac-187">Aliase</span><span class="sxs-lookup"><span data-stu-id="de0ac-187">ALIASES</span></span>

<span data-ttu-id="de0ac-188">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de0ac-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de0ac-189">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de0ac-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de0ac-190">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="de0ac-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de0ac-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: die Liste der Spracherweiterungen.</span><span class="sxs-lookup"><span data-stu-id="de0ac-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="de0ac-192">`[Name <LanguageExtensionName?>]`: Der Name der Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="de0ac-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="de0ac-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: die externen Mandanten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="de0ac-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="de0ac-194">`[Value <String>]`: GUID, die einen externen Mandanten darstellt.</span><span class="sxs-lookup"><span data-stu-id="de0ac-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="de0ac-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de0ac-195">RELATED LINKS</span></span>

