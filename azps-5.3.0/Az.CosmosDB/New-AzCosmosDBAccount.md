---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 4e31ae75f6fcea77c179757312988a0abbbb58f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472834"
---
# <span data-ttu-id="e3c40-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e3c40-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e3c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c40-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c40-103">Erstellen Sie ein neues Konto aus Demdb.</span><span class="sxs-lookup"><span data-stu-id="e3c40-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="e3c40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3c40-104">SYNTAX</span></span>

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

## <span data-ttu-id="e3c40-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3c40-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c40-106">Erstellen Sie in der angegebenen Ressourcengruppe ein neues Konto für Untergruppen.</span><span class="sxs-lookup"><span data-stu-id="e3c40-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="e3c40-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3c40-107">EXAMPLES</span></span>

### <span data-ttu-id="e3c40-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3c40-108">Example 1</span></span>
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

<span data-ttu-id="e3c40-109">In der Ressourcengruppe "ResourceGroupGroupName" wird ein neues Serverkonto mit Name databaseAccountName erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3c40-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="e3c40-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3c40-110">PARAMETERS</span></span>

### <span data-ttu-id="e3c40-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="e3c40-111">-ApiKind</span></span>
<span data-ttu-id="e3c40-112">Der Typ des zu erstellenden Db-Datenbankkontos.</span><span class="sxs-lookup"><span data-stu-id="e3c40-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="e3c40-113">Akzeptierte Werte: Sql, MongoDB, Gremlin, Table, Desser.</span><span class="sxs-lookup"><span data-stu-id="e3c40-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="e3c40-114">Standardwert: Sql</span><span class="sxs-lookup"><span data-stu-id="e3c40-114">Default value: Sql</span></span>

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

### <span data-ttu-id="e3c40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3c40-115">-AsJob</span></span>
<span data-ttu-id="e3c40-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e3c40-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3c40-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3c40-117">-Confirm</span></span>
<span data-ttu-id="e3c40-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3c40-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c40-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="e3c40-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="e3c40-120">Standardkonsistenzstufe des Db-Datenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="e3c40-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="e3c40-121">Akzeptierte Werte: "BoundedStaleness", "ConsistentPrefix", "Eventual", "Session", "Strong"</span><span class="sxs-lookup"><span data-stu-id="e3c40-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="e3c40-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c40-122">-DefaultProfile</span></span>
<span data-ttu-id="e3c40-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3c40-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c40-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e3c40-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="e3c40-125">Deaktivieren von Schreibvorgängen für Metadatenressourcen (Datenbanken, Container, Durchsatz) mithilfe von Kontoschlüsseln</span><span class="sxs-lookup"><span data-stu-id="e3c40-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="e3c40-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="e3c40-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="e3c40-127">Bool, um anzugeben, ob AnalyticalStorage für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e3c40-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="e3c40-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="e3c40-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="e3c40-129">Ermöglicht den automatischen Failover des Schreibbereichs für den seltenen Fall, dass die Region aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e3c40-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="e3c40-130">Der automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failoverprioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e3c40-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="e3c40-131">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="e3c40-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e3c40-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="e3c40-132">-EnableFreeTier</span></span>
<span data-ttu-id="e3c40-133">Bool, um anzugeben, ob FreeTier für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e3c40-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="e3c40-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="e3c40-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="e3c40-135">Aktivieren sie mehrere Schreibpositionen.</span><span class="sxs-lookup"><span data-stu-id="e3c40-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="e3c40-136">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="e3c40-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e3c40-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3c40-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="e3c40-138">Aktiviert ein virtuelles Netzwerk mit dem Db-Datenbankkonto von Db.</span><span class="sxs-lookup"><span data-stu-id="e3c40-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="e3c40-139">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="e3c40-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e3c40-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e3c40-140">-IpRule</span></span>
<span data-ttu-id="e3c40-141">Firewallunterstützung.</span><span class="sxs-lookup"><span data-stu-id="e3c40-141">Firewall support.</span></span> <span data-ttu-id="e3c40-142">Gibt die Gruppe von IP-Adressen oder -Adressbereichen im CIDR-Formular an, die als liste zulässiger Client-IPs für ein bestimmtes Datenbankkonto aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3c40-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="e3c40-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="e3c40-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="e3c40-144">URI von KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3c40-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="e3c40-145">-Location</span><span class="sxs-lookup"><span data-stu-id="e3c40-145">-Location</span></span>
<span data-ttu-id="e3c40-146">Fügen Sie dem Db-Datenbankkonto von Db einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3c40-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="e3c40-147">Array von Zeichenfolgen, geordnet nach Failoverpriorität.</span><span class="sxs-lookup"><span data-stu-id="e3c40-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="e3c40-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="e3c40-148">-LocationObject</span></span>
<span data-ttu-id="e3c40-149">Fügen Sie dem Db-Datenbankkonto von Db einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3c40-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="e3c40-150">Array von PSLocation-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e3c40-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="e3c40-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e3c40-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="e3c40-152">Bei Verwendung der Konsistenz "Gebundene Veraltetheit" stellt dieser Wert den Zeitbetrag für die Veraltetheit (in der Zeitspanne) dar.</span><span class="sxs-lookup"><span data-stu-id="e3c40-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="e3c40-153">Der akzeptierte Bereich für diesen Wert beträgt 5 bis 86400.</span><span class="sxs-lookup"><span data-stu-id="e3c40-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="e3c40-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="e3c40-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="e3c40-155">Bei Verwendung der Konsistenz "Gebundene Veraltetkeit" stellt dieser Wert die Anzahl der veralteten Anforderungen dar.</span><span class="sxs-lookup"><span data-stu-id="e3c40-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="e3c40-156">Der akzeptierte Bereich für diesen Wert ist 1 bis 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="e3c40-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="e3c40-157">-Name</span><span class="sxs-lookup"><span data-stu-id="e3c40-157">-Name</span></span>
<span data-ttu-id="e3c40-158">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="e3c40-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3c40-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e3c40-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="e3c40-160">Gibt an, ob der Zugriff auf einen öffentlichen Endpunkt für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e3c40-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="e3c40-161">Mögliche Werte sind: 'Enabled', 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="e3c40-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="e3c40-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c40-162">-ResourceGroupName</span></span>
<span data-ttu-id="e3c40-163">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3c40-163">Name of resource group.</span></span>

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

### <span data-ttu-id="e3c40-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="e3c40-164">-ServerVersion</span></span>
<span data-ttu-id="e3c40-165">ServerVersion, gilt nur für MongoDB-Konten.</span><span class="sxs-lookup"><span data-stu-id="e3c40-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="e3c40-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3c40-166">-Tag</span></span>
<span data-ttu-id="e3c40-167">Hashtable von Tags als Schlüssel-Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="e3c40-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="e3c40-168">Verwenden Sie eine leere Zeichenfolge, um vorhandene Tags zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e3c40-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="e3c40-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3c40-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="e3c40-170">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e3c40-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="e3c40-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e3c40-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="e3c40-172">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e3c40-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="e3c40-173">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e3c40-173">-WhatIf</span></span>
<span data-ttu-id="e3c40-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3c40-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c40-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3c40-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c40-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c40-176">CommonParameters</span></span>
<span data-ttu-id="e3c40-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c40-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c40-178">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3c40-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c40-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3c40-179">INPUTS</span></span>

### <span data-ttu-id="e3c40-180">Microsoft.Azure.Commands.WeitersDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="e3c40-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="e3c40-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3c40-181">OUTPUTS</span></span>

### <span data-ttu-id="e3c40-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e3c40-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e3c40-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e3c40-183">NOTES</span></span>

## <span data-ttu-id="e3c40-184">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e3c40-184">RELATED LINKS</span></span>
 
