---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 810888885c53381c274f85dc79ea2dd7bd4492c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166220"
---
# <span data-ttu-id="11172-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="11172-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="11172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11172-102">SYNOPSIS</span></span>
<span data-ttu-id="11172-103">Erstellen Sie ein neues Konto für Abendb.</span><span class="sxs-lookup"><span data-stu-id="11172-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="11172-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11172-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11172-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11172-105">DESCRIPTION</span></span>
<span data-ttu-id="11172-106">Erstellen Sie in der angegebenen Ressourcengruppe ein neues Konto für Untergruppen.</span><span class="sxs-lookup"><span data-stu-id="11172-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="11172-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11172-107">EXAMPLES</span></span>

### <span data-ttu-id="11172-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11172-108">Example 1</span></span>
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

<span data-ttu-id="11172-109">Im ResourceGroup resourceGroupName wird ein neues Konto aus Demdb mit Name databaseAccountName erstellt.</span><span class="sxs-lookup"><span data-stu-id="11172-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="11172-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11172-110">PARAMETERS</span></span>

### <span data-ttu-id="11172-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="11172-111">-ApiKind</span></span>
<span data-ttu-id="11172-112">Der Typ des zu erstellenden Db-Datenbankkontos.</span><span class="sxs-lookup"><span data-stu-id="11172-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="11172-113">Akzeptierte Werte: Sql, MongoDB, Gremlin, Table, Desser.</span><span class="sxs-lookup"><span data-stu-id="11172-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="11172-114">Standardwert: Sql</span><span class="sxs-lookup"><span data-stu-id="11172-114">Default value: Sql</span></span>

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

### <span data-ttu-id="11172-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11172-115">-AsJob</span></span>
<span data-ttu-id="11172-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="11172-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11172-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11172-117">-Confirm</span></span>
<span data-ttu-id="11172-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11172-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11172-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="11172-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="11172-120">Standardkonsistenzstufe des Db-Datenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="11172-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="11172-121">Akzeptierte Werte: "BoundedStaleness", "ConsistentPrefix", "Eventual", "Session", "Strong"</span><span class="sxs-lookup"><span data-stu-id="11172-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="11172-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11172-122">-DefaultProfile</span></span>
<span data-ttu-id="11172-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11172-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11172-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="11172-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="11172-125">Deaktivieren von Schreibvorgängen für Metadatenressourcen (Datenbanken, Container, Durchsatz) mithilfe von Kontoschlüsseln</span><span class="sxs-lookup"><span data-stu-id="11172-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="11172-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="11172-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="11172-127">Bool, um anzugeben, ob AnalyticalStorage für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="11172-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="11172-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="11172-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="11172-129">Ermöglicht den automatischen Failover des Schreibbereichs für den seltenen Fall, dass die Region aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="11172-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="11172-130">Der automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failoverprioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="11172-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="11172-131">Akzeptierte Werte: FALSCH, WAHR</span><span class="sxs-lookup"><span data-stu-id="11172-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="11172-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="11172-132">-EnableFreeTier</span></span>
<span data-ttu-id="11172-133">Bool, um anzugeben, ob FreeTier für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="11172-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="11172-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="11172-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="11172-135">Aktivieren sie mehrere Schreibpositionen.</span><span class="sxs-lookup"><span data-stu-id="11172-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="11172-136">Akzeptierte Werte: FALSCH, WAHR</span><span class="sxs-lookup"><span data-stu-id="11172-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="11172-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="11172-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="11172-138">Aktiviert ein virtuelles Netzwerk mit dem Db-Datenbankkonto von Db.</span><span class="sxs-lookup"><span data-stu-id="11172-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="11172-139">Akzeptierte Werte: FALSCH, WAHR</span><span class="sxs-lookup"><span data-stu-id="11172-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="11172-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="11172-140">-IpRule</span></span>
<span data-ttu-id="11172-141">Firewallunterstützung.</span><span class="sxs-lookup"><span data-stu-id="11172-141">Firewall support.</span></span> <span data-ttu-id="11172-142">Gibt die Gruppe von IP-Adressen oder -Adressbereichen im CIDR-Formular an, die als liste zulässiger Client-IPs für ein bestimmtes Datenbankkonto aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11172-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="11172-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="11172-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="11172-144">URI von KeyVault</span><span class="sxs-lookup"><span data-stu-id="11172-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="11172-145">-Location</span><span class="sxs-lookup"><span data-stu-id="11172-145">-Location</span></span>
<span data-ttu-id="11172-146">Fügen Sie dem Datenbankkonto "Dbs" einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="11172-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="11172-147">Array von Zeichenfolgen, geordnet nach Failoverpriorität.</span><span class="sxs-lookup"><span data-stu-id="11172-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="11172-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="11172-148">-LocationObject</span></span>
<span data-ttu-id="11172-149">Fügen Sie dem Datenbankkonto "Dbs" einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="11172-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="11172-150">Array von PSLocation-Objekten.</span><span class="sxs-lookup"><span data-stu-id="11172-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="11172-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="11172-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="11172-152">Bei Verwendung der Konsistenz "Gebundene Veraltetheit" stellt dieser Wert den Zeitbetrag für die Veraltetheit (in der Zeitspanne) dar.</span><span class="sxs-lookup"><span data-stu-id="11172-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="11172-153">Der akzeptierte Bereich für diesen Wert beträgt 5 bis 86400.</span><span class="sxs-lookup"><span data-stu-id="11172-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="11172-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="11172-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="11172-155">Bei Verwendung der Konsistenz "Gebundene Veraltetkeit" stellt dieser Wert die Anzahl der veralteten Anforderungen dar.</span><span class="sxs-lookup"><span data-stu-id="11172-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="11172-156">Der akzeptierte Bereich für diesen Wert ist 1 bis 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="11172-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="11172-157">-Name</span><span class="sxs-lookup"><span data-stu-id="11172-157">-Name</span></span>
<span data-ttu-id="11172-158">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="11172-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="11172-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="11172-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="11172-160">Gibt an, ob der Zugriff auf einen öffentlichen Endpunkt für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="11172-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="11172-161">Mögliche Werte sind: "Enabled", "Disabled".</span><span class="sxs-lookup"><span data-stu-id="11172-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="11172-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11172-162">-ResourceGroupName</span></span>
<span data-ttu-id="11172-163">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="11172-163">Name of resource group.</span></span>

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

### <span data-ttu-id="11172-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="11172-164">-ServerVersion</span></span>
<span data-ttu-id="11172-165">ServerVersion, gilt nur für MongoDB-Konten.</span><span class="sxs-lookup"><span data-stu-id="11172-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="11172-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="11172-166">-Tag</span></span>
<span data-ttu-id="11172-167">Hashtable von Tags als Schlüssel-Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="11172-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="11172-168">Verwenden Sie eine leere Zeichenfolge, um vorhandene Tags zu löschen.</span><span class="sxs-lookup"><span data-stu-id="11172-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="11172-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="11172-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="11172-170">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="11172-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="11172-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="11172-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="11172-172">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="11172-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="11172-173">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="11172-173">-WhatIf</span></span>
<span data-ttu-id="11172-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11172-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11172-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11172-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11172-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11172-176">CommonParameters</span></span>
<span data-ttu-id="11172-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11172-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11172-178">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11172-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11172-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11172-179">INPUTS</span></span>

### <span data-ttu-id="11172-180">Microsoft.Azure.Commands.WeitersDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="11172-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="11172-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11172-181">OUTPUTS</span></span>

### <span data-ttu-id="11172-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="11172-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="11172-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="11172-183">NOTES</span></span>

## <span data-ttu-id="11172-184">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="11172-184">RELATED LINKS</span></span>
