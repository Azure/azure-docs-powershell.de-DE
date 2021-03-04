---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939632"
---
# <span data-ttu-id="204d1-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="204d1-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="204d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="204d1-102">SYNOPSIS</span></span>
<span data-ttu-id="204d1-103">Erstellen Sie ein neues CosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="204d1-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="204d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="204d1-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="204d1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="204d1-105">DESCRIPTION</span></span>
<span data-ttu-id="204d1-106">Erstellen Sie ein neues CosmosDB-Konto in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="204d1-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="204d1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="204d1-107">EXAMPLES</span></span>

### <span data-ttu-id="204d1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="204d1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="204d1-109">In der ResourceGroup resourceGroupName wird ein neues CosmosDB-Konto mit NamensdatenbankAccountName erstellt.</span><span class="sxs-lookup"><span data-stu-id="204d1-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="204d1-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="204d1-110">PARAMETERS</span></span>

### <span data-ttu-id="204d1-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="204d1-111">-ApiKind</span></span>
<span data-ttu-id="204d1-112">Der Typ des zu erstellenden Cosmos DB-Datenbankkontos.</span><span class="sxs-lookup"><span data-stu-id="204d1-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="204d1-113">Akzeptierte Werte: Sql, MongoDB, Gremlin, Table, Kassandra.</span><span class="sxs-lookup"><span data-stu-id="204d1-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="204d1-114">Standardwert: Sql</span><span class="sxs-lookup"><span data-stu-id="204d1-114">Default value: Sql</span></span>

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

### <span data-ttu-id="204d1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="204d1-115">-AsJob</span></span>
<span data-ttu-id="204d1-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="204d1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="204d1-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="204d1-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="204d1-118">Das Intervall (in Minuten), mit dem die Sicherung durchgeführt wird (nur für Konten mit periodischen Modussicherungen)</span><span class="sxs-lookup"><span data-stu-id="204d1-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="204d1-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="204d1-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="204d1-120">Die Uhrzeit(in Stunden), für die jede Sicherung aufbewahrt wird (nur für Konten mit periodischen Modussicherungen)</span><span class="sxs-lookup"><span data-stu-id="204d1-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="204d1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="204d1-121">-Confirm</span></span>
<span data-ttu-id="204d1-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="204d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="204d1-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="204d1-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="204d1-124">Standardkonsistenzebene des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="204d1-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="204d1-125">Akzeptierte Werte: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="204d1-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="204d1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204d1-126">-DefaultProfile</span></span>
<span data-ttu-id="204d1-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="204d1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204d1-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="204d1-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="204d1-129">Deaktivieren von Schreibvorgängen für Metadatenressourcen (Datenbanken, Container, Durchsatz) über Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="204d1-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="204d1-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="204d1-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="204d1-131">Bool, um anzugeben, ob AnalyticalStorage für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="204d1-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="204d1-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="204d1-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="204d1-133">Ermöglicht ein automatisches Failover des Schreibbereichs in dem seltenen Fall, dass die Region aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="204d1-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="204d1-134">Das automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failoverprioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="204d1-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="204d1-135">Akzeptierte Werte: false, true</span><span class="sxs-lookup"><span data-stu-id="204d1-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="204d1-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="204d1-136">-EnableFreeTier</span></span>
<span data-ttu-id="204d1-137">Bool, um anzugeben, ob FreeTier für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="204d1-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="204d1-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="204d1-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="204d1-139">Aktivieren Sie mehrere Schreibstandorte.</span><span class="sxs-lookup"><span data-stu-id="204d1-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="204d1-140">Akzeptierte Werte: false, true</span><span class="sxs-lookup"><span data-stu-id="204d1-140">Accepted values: false, true</span></span>

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

### <span data-ttu-id="204d1-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="204d1-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="204d1-142">Aktiviert das virtuelle Netzwerk im Datenbankkonto "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="204d1-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="204d1-143">Akzeptierte Werte: false, true</span><span class="sxs-lookup"><span data-stu-id="204d1-143">Accepted values: false, true</span></span>

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

### <span data-ttu-id="204d1-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="204d1-144">-IpRule</span></span>
<span data-ttu-id="204d1-145">Firewallunterstützung.</span><span class="sxs-lookup"><span data-stu-id="204d1-145">Firewall support.</span></span> <span data-ttu-id="204d1-146">Gibt die Gruppe von IP-Adressen oder IP-Adressbereichen im CIDR-Formular an, die als zulässige Liste von Client-IPs für ein bestimmtes Datenbankkonto einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="204d1-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="204d1-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="204d1-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="204d1-148">URI des KeyVault</span><span class="sxs-lookup"><span data-stu-id="204d1-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="204d1-149">-Location</span><span class="sxs-lookup"><span data-stu-id="204d1-149">-Location</span></span>
<span data-ttu-id="204d1-150">Fügen Sie dem Datenbankkonto "Cosmos DB" einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="204d1-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="204d1-151">Array von Zeichenfolgen, nach Failoverpriorität geordnet.</span><span class="sxs-lookup"><span data-stu-id="204d1-151">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="204d1-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="204d1-152">-LocationObject</span></span>
<span data-ttu-id="204d1-153">Fügen Sie dem Datenbankkonto "Cosmos DB" einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="204d1-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="204d1-154">Array von PSLocation-Objekten.</span><span class="sxs-lookup"><span data-stu-id="204d1-154">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204d1-155">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="204d1-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="204d1-156">Bei Verwendung mit der Konsistenz "Gebundene Abzeit" stellt dieser Wert die Zeitmenge der veralteten (in der Zeitspanne) tolerierten Zeit dar.</span><span class="sxs-lookup"><span data-stu-id="204d1-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="204d1-157">Akzeptierter Bereich für diesen Wert ist 5-86400.</span><span class="sxs-lookup"><span data-stu-id="204d1-157">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="204d1-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="204d1-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="204d1-159">Bei Verwendung mit der Konsistenz der gebundenen Veraltetheit stellt dieser Wert die Anzahl der veralteten Anforderungen dar, die geduldet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="204d1-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="204d1-160">Akzeptierter Bereich für diesen Wert ist 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="204d1-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="204d1-161">-Name</span><span class="sxs-lookup"><span data-stu-id="204d1-161">-Name</span></span>
<span data-ttu-id="204d1-162">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="204d1-162">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="204d1-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="204d1-163">-NetworkAclBypass</span></span>
<span data-ttu-id="204d1-164">Ob die Umgehung von Netzwerk-Acl für dieses Konto für Synapse Link aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="204d1-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="204d1-165">Mögliche Werte sind: "None", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="204d1-165">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="204d1-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="204d1-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="204d1-167">Liste der Ressourcen-Ids, die die Umgehung von Netzwerk-Acl für Synapse Link zulassen.</span><span class="sxs-lookup"><span data-stu-id="204d1-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="204d1-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="204d1-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="204d1-169">Gibt an, ob der Zugriff auf öffentliche Endpunkte für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="204d1-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="204d1-170">Mögliche Werte sind: "Aktiviert", "Deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="204d1-170">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="204d1-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="204d1-171">-ResourceGroupName</span></span>
<span data-ttu-id="204d1-172">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="204d1-172">Name of resource group.</span></span>

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

### <span data-ttu-id="204d1-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="204d1-173">-ServerVersion</span></span>
<span data-ttu-id="204d1-174">ServerVersion, gültig nur bei MongoDB-Konten.</span><span class="sxs-lookup"><span data-stu-id="204d1-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="204d1-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="204d1-175">-Tag</span></span>
<span data-ttu-id="204d1-176">Hashtable von Tags als Schlüssel-Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="204d1-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="204d1-177">Verwenden Sie eine leere Zeichenfolge, um vorhandene Tags zu löschen.</span><span class="sxs-lookup"><span data-stu-id="204d1-177">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="204d1-178">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="204d1-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="204d1-179">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="204d1-179">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="204d1-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="204d1-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="204d1-181">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="204d1-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="204d1-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="204d1-182">-WhatIf</span></span>
<span data-ttu-id="204d1-183">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="204d1-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="204d1-184">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="204d1-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="204d1-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204d1-185">CommonParameters</span></span>
<span data-ttu-id="204d1-186">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204d1-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204d1-187">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="204d1-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204d1-188">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="204d1-188">INPUTS</span></span>

### <span data-ttu-id="204d1-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="204d1-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="204d1-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="204d1-190">OUTPUTS</span></span>

### <span data-ttu-id="204d1-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="204d1-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="204d1-192">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="204d1-192">NOTES</span></span>

## <span data-ttu-id="204d1-193">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="204d1-193">RELATED LINKS</span></span>
