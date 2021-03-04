---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: cbee0ef9ce750dbb72af5be484106ccabec79321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947984"
---
# <span data-ttu-id="5422e-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="5422e-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="5422e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5422e-102">SYNOPSIS</span></span>
<span data-ttu-id="5422e-103">Aktualisieren sie die Attribute eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5422e-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="5422e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5422e-104">SYNTAX</span></span>

### <span data-ttu-id="5422e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5422e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5422e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5422e-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5422e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5422e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5422e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5422e-108">DESCRIPTION</span></span>
<span data-ttu-id="5422e-109">Aktualisieren Sie die Eigenschaften eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5422e-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="5422e-110">Kontobereiche können nicht mit anderen Eigenschaften simulatanisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5422e-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="5422e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5422e-111">EXAMPLES</span></span>

### <span data-ttu-id="5422e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5422e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="5422e-113">Aktualisiertes DefaultConsistencyLevel auf "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations und Enabled VirtualNetwork for CosmosDB Account with name accountName.</span><span class="sxs-lookup"><span data-stu-id="5422e-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="5422e-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5422e-114">PARAMETERS</span></span>

### <span data-ttu-id="5422e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5422e-115">-AsJob</span></span>
<span data-ttu-id="5422e-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5422e-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="5422e-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="5422e-118">Das Intervall (in Minuten), mit dem die Sicherung durchgeführt wird (nur für Konten mit periodischen Modussicherungen)</span><span class="sxs-lookup"><span data-stu-id="5422e-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="5422e-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="5422e-120">Die Uhrzeit(in Stunden), für die jede Sicherung aufbewahrt wird (nur für Konten mit periodischen Modussicherungen)</span><span class="sxs-lookup"><span data-stu-id="5422e-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5422e-121">-Confirm</span></span>
<span data-ttu-id="5422e-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5422e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5422e-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="5422e-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="5422e-124">Standardkonsistenzebene des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="5422e-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="5422e-125">Akzeptierte Werte: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="5422e-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5422e-126">-DefaultProfile</span></span>
<span data-ttu-id="5422e-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5422e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="5422e-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="5422e-129">Deaktivieren von Schreibvorgängen für Metadatenressourcen (Datenbanken, Container, Durchsatz) über Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="5422e-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="5422e-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="5422e-131">Bool, um anzugeben, ob AnalyticalStorage für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5422e-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="5422e-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="5422e-133">Ermöglicht ein automatisches Failover des Schreibbereichs in dem seltenen Fall, dass die Region aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5422e-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="5422e-134">Das automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failoverprioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5422e-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="5422e-135">Akzeptierte Werte: false, true</span><span class="sxs-lookup"><span data-stu-id="5422e-135">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-136">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="5422e-136">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="5422e-137">Aktivieren Sie mehrere Schreibstandorte.</span><span class="sxs-lookup"><span data-stu-id="5422e-137">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="5422e-138">Akzeptierte Werte: false, true</span><span class="sxs-lookup"><span data-stu-id="5422e-138">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-139">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5422e-139">-EnableVirtualNetwork</span></span>
<span data-ttu-id="5422e-140">Aktiviert das virtuelle Netzwerk im Datenbankkonto "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="5422e-140">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="5422e-141">Akzeptierte Werte: false, true</span><span class="sxs-lookup"><span data-stu-id="5422e-141">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5422e-142">-InputObject</span></span>
<span data-ttu-id="5422e-143">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="5422e-143">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="5422e-144">-IpRule</span></span>
<span data-ttu-id="5422e-145">Firewallunterstützung.</span><span class="sxs-lookup"><span data-stu-id="5422e-145">Firewall support.</span></span> <span data-ttu-id="5422e-146">Gibt die Gruppe von IP-Adressen oder IP-Adressbereichen im CIDR-Formular an, die als zulässige Liste von Client-IPs für ein bestimmtes Datenbankkonto einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5422e-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="5422e-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="5422e-148">URI des KeyVault</span><span class="sxs-lookup"><span data-stu-id="5422e-148">URI of the KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-149">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5422e-149">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="5422e-150">Bei Verwendung mit der Konsistenz "Gebundene Abzeit" stellt dieser Wert die Zeitmenge der veralteten (in der Zeitspanne) tolerierten Zeit dar.</span><span class="sxs-lookup"><span data-stu-id="5422e-150">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="5422e-151">Akzeptierter Bereich für diesen Wert ist 5-86400.</span><span class="sxs-lookup"><span data-stu-id="5422e-151">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-152">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="5422e-152">-MaxStalenessPrefix</span></span>
<span data-ttu-id="5422e-153">Bei Verwendung mit der Konsistenz der gebundenen Veraltetheit stellt dieser Wert die Anzahl der veralteten Anforderungen dar, die geduldet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5422e-153">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="5422e-154">Akzeptierter Bereich für diesen Wert ist 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="5422e-154">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-155">-Name</span><span class="sxs-lookup"><span data-stu-id="5422e-155">-Name</span></span>
<span data-ttu-id="5422e-156">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="5422e-156">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-157">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="5422e-157">-NetworkAclBypass</span></span>
<span data-ttu-id="5422e-158">Ob die Umgehung von Netzwerk-Acl für dieses Konto für Synapse Link aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="5422e-158">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="5422e-159">Mögliche Werte sind: "None", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="5422e-159">Possible values include: 'None', 'AzureServices'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-160">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="5422e-160">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="5422e-161">Liste der Ressourcen-Ids, die die Umgehung von Netzwerk-Acl für Synapse Link zulassen.</span><span class="sxs-lookup"><span data-stu-id="5422e-161">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-162">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5422e-162">-PublicNetworkAccess</span></span>
<span data-ttu-id="5422e-163">Gibt an, ob der Zugriff auf öffentliche Endpunkte für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5422e-163">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="5422e-164">Mögliche Werte sind: "Aktiviert", "Deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="5422e-164">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5422e-165">-ResourceGroupName</span></span>
<span data-ttu-id="5422e-166">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5422e-166">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5422e-167">-ResourceId</span></span>
<span data-ttu-id="5422e-168">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5422e-168">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-169">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="5422e-169">-ServerVersion</span></span>
<span data-ttu-id="5422e-170">ServerVersion, gültig nur bei MongoDB-Konten.</span><span class="sxs-lookup"><span data-stu-id="5422e-170">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="5422e-171">-Tag</span></span>
<span data-ttu-id="5422e-172">Hashtable von Tags als Schlüssel-Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="5422e-172">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="5422e-173">Verwenden Sie eine leere Zeichenfolge, um vorhandene Tags zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5422e-173">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-174">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5422e-174">-VirtualNetworkRule</span></span>
<span data-ttu-id="5422e-175">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5422e-175">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-176">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5422e-176">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="5422e-177">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5422e-177">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5422e-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5422e-178">-WhatIf</span></span>
<span data-ttu-id="5422e-179">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5422e-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5422e-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5422e-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5422e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5422e-181">CommonParameters</span></span>
<span data-ttu-id="5422e-182">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5422e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5422e-183">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5422e-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5422e-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5422e-184">INPUTS</span></span>

### <span data-ttu-id="5422e-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="5422e-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="5422e-186">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5422e-186">OUTPUTS</span></span>

### <span data-ttu-id="5422e-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5422e-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5422e-188">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5422e-188">NOTES</span></span>

## <span data-ttu-id="5422e-189">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5422e-189">RELATED LINKS</span></span>
