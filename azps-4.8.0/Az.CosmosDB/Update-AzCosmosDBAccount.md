---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167077"
---
# <span data-ttu-id="b9907-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b9907-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b9907-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9907-102">SYNOPSIS</span></span>
<span data-ttu-id="b9907-103">Aktualisieren Sie die Attribute eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="b9907-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="b9907-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9907-104">SYNTAX</span></span>

### <span data-ttu-id="b9907-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9907-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9907-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9907-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9907-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9907-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9907-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9907-108">DESCRIPTION</span></span>
<span data-ttu-id="b9907-109">Aktualisieren Sie die Eigenschaften eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="b9907-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="b9907-110">Die Konto Regionen unerwuenscht können nicht mit anderen Eigenschaften aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b9907-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="b9907-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9907-111">EXAMPLES</span></span>

### <span data-ttu-id="b9907-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9907-112">Example 1</span></span>
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

<span data-ttu-id="b9907-113">DefaultConsistencyLevel auf "stark", aktivierte AutomaticFailover, aktivierte MultipleWriteLocations und aktivierte VirtualNetwork für CosmosDB-Konto mit Name Accountname aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b9907-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="b9907-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9907-114">PARAMETERS</span></span>

### <span data-ttu-id="b9907-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9907-115">-AsJob</span></span>
<span data-ttu-id="b9907-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b9907-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9907-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9907-117">-Confirm</span></span>
<span data-ttu-id="b9907-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9907-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9907-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="b9907-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="b9907-120">Standardkonsistenz Stufe des Cosmos DB-Daten Bankkontos</span><span class="sxs-lookup"><span data-stu-id="b9907-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="b9907-121">Akzeptierte Werte: BoundedStaleness, ConsistentPrefix, eventuell, Sitzung, stark</span><span class="sxs-lookup"><span data-stu-id="b9907-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="b9907-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9907-122">-DefaultProfile</span></span>
<span data-ttu-id="b9907-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9907-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9907-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="b9907-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="b9907-125">Deaktivieren von Schreibvorgängen für Metadaten-Ressourcen (Datenbanken, Container, Durchsatz) über Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="b9907-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="b9907-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="b9907-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="b9907-127">Bool, um anzugeben, ob AnalyticalStorage für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b9907-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="b9907-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="b9907-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="b9907-129">Ermöglicht automatisches Failover des Schreibbereichs in dem seltenen Fall, dass der Bereich aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b9907-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="b9907-130">Das automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failover-Prioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b9907-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="b9907-131">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="b9907-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b9907-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="b9907-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="b9907-133">Aktivieren von mehreren Schreib Speicherorten</span><span class="sxs-lookup"><span data-stu-id="b9907-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="b9907-134">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="b9907-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b9907-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b9907-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="b9907-136">Ermöglicht virtuelles Netzwerk im Cosmos DB-Daten Bank Konto.</span><span class="sxs-lookup"><span data-stu-id="b9907-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="b9907-137">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="b9907-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b9907-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9907-138">-InputObject</span></span>
<span data-ttu-id="b9907-139">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b9907-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b9907-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="b9907-140">-IpRule</span></span>
<span data-ttu-id="b9907-141">Firewall-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="b9907-141">Firewall support.</span></span> <span data-ttu-id="b9907-142">Gibt den Satz von IP-Adressen oder IP-Adressbereichen in CIDR-Form an, der als zulässige Liste von Client-IPS für ein bestimmtes Daten Bank Konto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9907-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="b9907-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b9907-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="b9907-144">URI des keyvaults</span><span class="sxs-lookup"><span data-stu-id="b9907-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="b9907-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b9907-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="b9907-146">Bei Verwendung mit begrenzter veraltete Konsistenz stellt dieser Wert die Zeitdauer der veralteten Zeitdauer (in TimeSpan) toleriert dar.</span><span class="sxs-lookup"><span data-stu-id="b9907-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="b9907-147">Angenommener Bereich für diesen Wert ist 5-86400.</span><span class="sxs-lookup"><span data-stu-id="b9907-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="b9907-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="b9907-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="b9907-149">Bei Verwendung mit begrenzter veraltete Konsistenz stellt dieser Wert die Anzahl der veralteten Anforderungen dar, die toleriert werden.</span><span class="sxs-lookup"><span data-stu-id="b9907-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="b9907-150">Angenommener Bereich für diesen Wert ist 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="b9907-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="b9907-151">-Name</span><span class="sxs-lookup"><span data-stu-id="b9907-151">-Name</span></span>
<span data-ttu-id="b9907-152">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b9907-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b9907-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b9907-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="b9907-154">Ob öffentlicher Endpunkt Zugriff für diesen Server zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b9907-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="b9907-155">Mögliche Werte sind: "aktiviert", "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="b9907-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="b9907-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9907-156">-ResourceGroupName</span></span>
<span data-ttu-id="b9907-157">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b9907-157">Name of resource group.</span></span>

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

### <span data-ttu-id="b9907-158">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b9907-158">-ResourceId</span></span>
<span data-ttu-id="b9907-159">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="b9907-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="b9907-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9907-160">-Tag</span></span>
<span data-ttu-id="b9907-161">Hashtable von Tags als Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="b9907-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="b9907-162">Verwenden Sie eine leere Zeichenfolge, um das vorhandene Tag zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b9907-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="b9907-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9907-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="b9907-164">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b9907-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="b9907-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b9907-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="b9907-166">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b9907-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="b9907-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9907-167">-WhatIf</span></span>
<span data-ttu-id="b9907-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9907-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9907-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9907-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9907-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9907-170">CommonParameters</span></span>
<span data-ttu-id="b9907-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9907-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9907-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9907-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9907-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9907-173">INPUTS</span></span>

### <span data-ttu-id="b9907-174">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="b9907-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="b9907-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9907-175">OUTPUTS</span></span>

### <span data-ttu-id="b9907-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b9907-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b9907-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9907-177">NOTES</span></span>

## <span data-ttu-id="b9907-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9907-178">RELATED LINKS</span></span>
