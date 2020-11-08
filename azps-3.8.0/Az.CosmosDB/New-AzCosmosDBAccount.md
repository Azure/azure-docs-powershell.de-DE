---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997267"
---
# <span data-ttu-id="e3ab3-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e3ab3-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e3ab3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ab3-103">Erstellen Sie ein neues CosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="e3ab3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3ab3-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3ab3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="e3ab3-106">Erstellen Sie ein neues CosmosDB-Konto in der angegebenen ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="e3ab3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="e3ab3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3ab3-108">Example 1</span></span>
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
```

<span data-ttu-id="e3ab3-109">Ein neues CosmosDB-Konto mit dem Namen databaseAccountName wird in der ResourceGroup-resourceGroupName erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="e3ab3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3ab3-110">PARAMETERS</span></span>

### <span data-ttu-id="e3ab3-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="e3ab3-111">-ApiKind</span></span>
<span data-ttu-id="e3ab3-112">Der Typ des zu erstellende Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="e3ab3-113">Akzeptierte Werte: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="e3ab3-114">Standardwert: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="e3ab3-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="e3ab3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3ab3-115">-AsJob</span></span>
<span data-ttu-id="e3ab3-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e3ab3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3ab3-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3ab3-117">-Confirm</span></span>
<span data-ttu-id="e3ab3-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ab3-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="e3ab3-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="e3ab3-120">Standardkonsistenz Stufe des Cosmos DB-Daten Bankkontos</span><span class="sxs-lookup"><span data-stu-id="e3ab3-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="e3ab3-121">Akzeptierte Werte: BoundedStaleness, ConsistentPrefix, eventuell, Sitzung, stark</span><span class="sxs-lookup"><span data-stu-id="e3ab3-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="e3ab3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ab3-122">-DefaultProfile</span></span>
<span data-ttu-id="e3ab3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ab3-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e3ab3-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="e3ab3-125">Deaktivieren von Schreibvorgängen für Metadaten-Ressourcen (Datenbanken, Container, Durchsatz) über Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="e3ab3-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="e3ab3-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="e3ab3-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="e3ab3-127">Ermöglicht automatisches Failover des Schreibbereichs in dem seltenen Fall, dass der Bereich aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="e3ab3-128">Das automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failover-Prioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="e3ab3-129">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="e3ab3-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e3ab3-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="e3ab3-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="e3ab3-131">Aktivieren von mehreren Schreib Speicherorten</span><span class="sxs-lookup"><span data-stu-id="e3ab3-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="e3ab3-132">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="e3ab3-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e3ab3-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3ab3-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="e3ab3-134">Ermöglicht virtuelles Netzwerk im Cosmos DB-Daten Bank Konto.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="e3ab3-135">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="e3ab3-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e3ab3-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="e3ab3-136">-IpRangeFilter</span></span>
<span data-ttu-id="e3ab3-137">Firewall-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-137">Firewall support.</span></span>
<span data-ttu-id="e3ab3-138">Gibt den Satz von IP-Adressen oder IP-Adressbereichen in CIDR-Form an, die als zulässige Liste von Client-IPS für ein bestimmtes Daten Bank Konto hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="e3ab3-139">-Standort</span><span class="sxs-lookup"><span data-stu-id="e3ab3-139">-Location</span></span>
<span data-ttu-id="e3ab3-140">Fügen Sie dem Cosmos DB-Daten Bank Konto einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="e3ab3-141">Array von Zeichenfolgen, geordnet nach Failover-Priorität.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-141">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="e3ab3-142">-Locationobject</span><span class="sxs-lookup"><span data-stu-id="e3ab3-142">-LocationObject</span></span>
<span data-ttu-id="e3ab3-143">Fügen Sie dem Cosmos DB-Daten Bank Konto einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="e3ab3-144">Array von PSLocation-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-144">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="e3ab3-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e3ab3-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="e3ab3-146">Bei Verwendung mit begrenzter veraltete Konsistenz stellt dieser Wert die Zeitdauer der veralteten Zeitdauer (in TimeSpan) toleriert dar.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="e3ab3-147">Angenommener Bereich für diesen Wert ist 5-86400.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="e3ab3-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="e3ab3-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="e3ab3-149">Bei Verwendung mit begrenzter veraltete Konsistenz stellt dieser Wert die Anzahl der veralteten Anforderungen dar, die toleriert werden.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="e3ab3-150">Angenommener Bereich für diesen Wert ist 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="e3ab3-151">-Name</span><span class="sxs-lookup"><span data-stu-id="e3ab3-151">-Name</span></span>
<span data-ttu-id="e3ab3-152">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3ab3-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e3ab3-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="e3ab3-154">Ob öffentlicher Endpunkt Zugriff für diesen Server zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="e3ab3-155">Mögliche Werte sind: "aktiviert", "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="e3ab3-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="e3ab3-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ab3-156">-ResourceGroupName</span></span>
<span data-ttu-id="e3ab3-157">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-157">Name of resource group.</span></span>

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

### <span data-ttu-id="e3ab3-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3ab3-158">-Tag</span></span>
<span data-ttu-id="e3ab3-159">Hashtable von Tags als Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="e3ab3-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="e3ab3-160">Verwenden Sie eine leere Zeichenfolge, um das vorhandene Tag zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-160">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="e3ab3-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3ab3-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="e3ab3-162">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-162">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="e3ab3-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e3ab3-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="e3ab3-164">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="e3ab3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ab3-165">-WhatIf</span></span>
<span data-ttu-id="e3ab3-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ab3-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3ab3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ab3-168">CommonParameters</span></span>
<span data-ttu-id="e3ab3-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ab3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ab3-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3ab3-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ab3-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3ab3-171">INPUTS</span></span>

### <span data-ttu-id="e3ab3-172">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="e3ab3-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="e3ab3-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3ab3-173">OUTPUTS</span></span>

### <span data-ttu-id="e3ab3-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e3ab3-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e3ab3-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3ab3-175">NOTES</span></span>

## <span data-ttu-id="e3ab3-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3ab3-176">RELATED LINKS</span></span>
