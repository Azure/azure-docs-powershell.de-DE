---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470691"
---
# <span data-ttu-id="c4d16-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="c4d16-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="c4d16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4d16-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d16-103">Aktualisieren Sie die Attribute eines Kundenkontos aus Durchdingungsdb.</span><span class="sxs-lookup"><span data-stu-id="c4d16-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="c4d16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4d16-104">SYNTAX</span></span>

### <span data-ttu-id="c4d16-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4d16-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d16-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d16-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d16-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d16-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d16-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4d16-108">DESCRIPTION</span></span>
<span data-ttu-id="c4d16-109">Aktualisieren Sie die Eigenschaften eines Kontos vom 8.</span><span class="sxs-lookup"><span data-stu-id="c4d16-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="c4d16-110">Kontobereiche können nicht mit anderen Eigenschaften ähnlich wie andere Eigenschaften aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4d16-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="c4d16-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4d16-111">EXAMPLES</span></span>

### <span data-ttu-id="c4d16-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4d16-112">Example 1</span></span>
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
```

<span data-ttu-id="c4d16-113">"DefaultConsistencyLevel" wurde auf "Strong", "Enabled AutomaticFailover", "Enabled multipleWriteLocations" und "Enabled VirtualNetwork forWssDB Account with name accountName" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c4d16-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="c4d16-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4d16-114">PARAMETERS</span></span>

### <span data-ttu-id="c4d16-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4d16-115">-AsJob</span></span>
<span data-ttu-id="c4d16-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c4d16-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4d16-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4d16-117">-Confirm</span></span>
<span data-ttu-id="c4d16-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4d16-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d16-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="c4d16-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="c4d16-120">Standardkonsistenzstufe des Db-Datenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="c4d16-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="c4d16-121">Akzeptierte Werte: "BoundedStaleness", "ConsistentPrefix", "Eventual", "Session", "Strong"</span><span class="sxs-lookup"><span data-stu-id="c4d16-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="c4d16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d16-122">-DefaultProfile</span></span>
<span data-ttu-id="c4d16-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4d16-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d16-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="c4d16-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="c4d16-125">Deaktivieren von Schreibvorgängen für Metadatenressourcen (Datenbanken, Container, Durchsatz) mithilfe von Kontoschlüsseln</span><span class="sxs-lookup"><span data-stu-id="c4d16-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="c4d16-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="c4d16-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="c4d16-127">Bool, um anzugeben, ob AnalyticalStorage für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c4d16-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="c4d16-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="c4d16-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="c4d16-129">Ermöglicht den automatischen Failover des Schreibbereichs für den seltenen Fall, dass die Region aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c4d16-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="c4d16-130">Der automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failoverprioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c4d16-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="c4d16-131">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="c4d16-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="c4d16-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="c4d16-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="c4d16-133">Aktivieren sie mehrere Schreibpositionen.</span><span class="sxs-lookup"><span data-stu-id="c4d16-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="c4d16-134">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="c4d16-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="c4d16-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c4d16-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="c4d16-136">Aktiviert ein virtuelles Netzwerk im Db-Datenbankkonto.</span><span class="sxs-lookup"><span data-stu-id="c4d16-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="c4d16-137">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="c4d16-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="c4d16-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4d16-138">-InputObject</span></span>
<span data-ttu-id="c4d16-139">Objekt "Buchhalterungskonto"</span><span class="sxs-lookup"><span data-stu-id="c4d16-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c4d16-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="c4d16-140">-IpRule</span></span>
<span data-ttu-id="c4d16-141">Firewallunterstützung.</span><span class="sxs-lookup"><span data-stu-id="c4d16-141">Firewall support.</span></span> <span data-ttu-id="c4d16-142">Gibt die Gruppe von IP-Adressen oder -Adressbereichen im CIDR-Formular an, die als zulässige Liste der Client-IPs für ein bestimmtes Datenbankkonto aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c4d16-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="c4d16-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="c4d16-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="c4d16-144">URI des KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4d16-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="c4d16-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c4d16-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="c4d16-146">Bei Verwendung der Konsistenz "Gebundene Veraltetheit" stellt dieser Wert den Zeitbetrag für die Veraltetheit (in der Zeitspanne) dar.</span><span class="sxs-lookup"><span data-stu-id="c4d16-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="c4d16-147">Der akzeptierte Bereich für diesen Wert beträgt 5 bis 86400.</span><span class="sxs-lookup"><span data-stu-id="c4d16-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="c4d16-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="c4d16-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="c4d16-149">Bei Verwendung der Konsistenz "Gebundene Veraltetkeit" stellt dieser Wert die Anzahl der veralteten Anforderungen dar.</span><span class="sxs-lookup"><span data-stu-id="c4d16-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="c4d16-150">Der akzeptierte Bereich für diesen Wert ist 1 bis 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="c4d16-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="c4d16-151">-Name</span><span class="sxs-lookup"><span data-stu-id="c4d16-151">-Name</span></span>
<span data-ttu-id="c4d16-152">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="c4d16-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c4d16-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c4d16-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="c4d16-154">Gibt an, ob der Zugriff auf einen öffentlichen Endpunkt für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="c4d16-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="c4d16-155">Mögliche Werte sind: 'Enabled', 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="c4d16-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="c4d16-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d16-156">-ResourceGroupName</span></span>
<span data-ttu-id="c4d16-157">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4d16-157">Name of resource group.</span></span>

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

### <span data-ttu-id="c4d16-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d16-158">-ResourceId</span></span>
<span data-ttu-id="c4d16-159">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4d16-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c4d16-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4d16-160">-Tag</span></span>
<span data-ttu-id="c4d16-161">Hashtable von Tags als Schlüssel-Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="c4d16-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="c4d16-162">Verwenden Sie eine leere Zeichenfolge, um vorhandene Tags zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c4d16-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="c4d16-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c4d16-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="c4d16-164">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c4d16-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="c4d16-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="c4d16-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="c4d16-166">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c4d16-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="c4d16-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c4d16-167">-WhatIf</span></span>
<span data-ttu-id="c4d16-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4d16-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d16-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4d16-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d16-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d16-170">CommonParameters</span></span>
<span data-ttu-id="c4d16-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d16-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d16-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4d16-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d16-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4d16-173">INPUTS</span></span>

### <span data-ttu-id="c4d16-174">Microsoft.Azure.Commands.WeitersDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="c4d16-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="c4d16-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4d16-175">OUTPUTS</span></span>

### <span data-ttu-id="c4d16-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c4d16-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c4d16-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c4d16-177">NOTES</span></span>

## <span data-ttu-id="c4d16-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c4d16-178">RELATED LINKS</span></span>
