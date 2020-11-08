---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995254"
---
# <span data-ttu-id="7f69b-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="7f69b-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="7f69b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f69b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f69b-103">Aktualisieren Sie die Attribute eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="7f69b-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="7f69b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f69b-104">SYNTAX</span></span>

### <span data-ttu-id="7f69b-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f69b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f69b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f69b-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f69b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f69b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f69b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f69b-108">DESCRIPTION</span></span>
<span data-ttu-id="7f69b-109">Aktualisieren Sie die Eigenschaften eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="7f69b-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="7f69b-110">Die Konto Regionen unerwuenscht können nicht mit anderen Eigenschaften aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f69b-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="7f69b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f69b-111">EXAMPLES</span></span>

### <span data-ttu-id="7f69b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f69b-112">Example 1</span></span>
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

<span data-ttu-id="7f69b-113">DefaultConsistencyLevel auf "stark", aktivierte AutomaticFailover, aktivierte MultipleWriteLocations und aktivierte VirtualNetwork für CosmosDB-Konto mit Name Accountname aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7f69b-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="7f69b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f69b-114">PARAMETERS</span></span>

### <span data-ttu-id="7f69b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f69b-115">-AsJob</span></span>
<span data-ttu-id="7f69b-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7f69b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f69b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f69b-117">-Confirm</span></span>
<span data-ttu-id="7f69b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f69b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f69b-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="7f69b-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="7f69b-120">Standardkonsistenz Stufe des Cosmos DB-Daten Bankkontos</span><span class="sxs-lookup"><span data-stu-id="7f69b-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="7f69b-121">Akzeptierte Werte: BoundedStaleness, ConsistentPrefix, eventuell, Sitzung, stark</span><span class="sxs-lookup"><span data-stu-id="7f69b-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="7f69b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f69b-122">-DefaultProfile</span></span>
<span data-ttu-id="7f69b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f69b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f69b-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="7f69b-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="7f69b-125">Deaktivieren von Schreibvorgängen für Metadaten-Ressourcen (Datenbanken, Container, Durchsatz) über Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="7f69b-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="7f69b-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="7f69b-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="7f69b-127">Ermöglicht automatisches Failover des Schreibbereichs in dem seltenen Fall, dass der Bereich aufgrund eines Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7f69b-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="7f69b-128">Das automatische Failover führt zu einem neuen Schreibbereich für das Konto und wird basierend auf den für das Konto konfigurierten Failover-Prioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="7f69b-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="7f69b-129">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="7f69b-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="7f69b-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="7f69b-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="7f69b-131">Aktivieren von mehreren Schreib Speicherorten</span><span class="sxs-lookup"><span data-stu-id="7f69b-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="7f69b-132">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="7f69b-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="7f69b-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7f69b-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="7f69b-134">Ermöglicht virtuelles Netzwerk im Cosmos DB-Daten Bank Konto.</span><span class="sxs-lookup"><span data-stu-id="7f69b-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="7f69b-135">Akzeptierte Werte: falsch, wahr</span><span class="sxs-lookup"><span data-stu-id="7f69b-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="7f69b-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f69b-136">-InputObject</span></span>
<span data-ttu-id="7f69b-137">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="7f69b-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f69b-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="7f69b-138">-IpRangeFilter</span></span>
<span data-ttu-id="7f69b-139">Firewall-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="7f69b-139">Firewall support.</span></span>
<span data-ttu-id="7f69b-140">Gibt den Satz von IP-Adressen oder IP-Adressbereichen in CIDR-Form an, die als zulässige Liste von Client-IPS für ein bestimmtes Daten Bank Konto hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f69b-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="7f69b-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7f69b-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="7f69b-142">Bei Verwendung mit begrenzter veraltete Konsistenz stellt dieser Wert die Zeitdauer der veralteten Zeitdauer (in TimeSpan) toleriert dar.</span><span class="sxs-lookup"><span data-stu-id="7f69b-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="7f69b-143">Angenommener Bereich für diesen Wert ist 5-86400.</span><span class="sxs-lookup"><span data-stu-id="7f69b-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="7f69b-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="7f69b-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="7f69b-145">Bei Verwendung mit begrenzter veraltete Konsistenz stellt dieser Wert die Anzahl der veralteten Anforderungen dar, die toleriert werden.</span><span class="sxs-lookup"><span data-stu-id="7f69b-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="7f69b-146">Angenommener Bereich für diesen Wert ist 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="7f69b-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="7f69b-147">-Name</span><span class="sxs-lookup"><span data-stu-id="7f69b-147">-Name</span></span>
<span data-ttu-id="7f69b-148">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="7f69b-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7f69b-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="7f69b-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="7f69b-150">Ob öffentlicher Endpunkt Zugriff für diesen Server zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="7f69b-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="7f69b-151">Mögliche Werte sind: "aktiviert", "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="7f69b-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="7f69b-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f69b-152">-ResourceGroupName</span></span>
<span data-ttu-id="7f69b-153">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7f69b-153">Name of resource group.</span></span>

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

### <span data-ttu-id="7f69b-154">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7f69b-154">-ResourceId</span></span>
<span data-ttu-id="7f69b-155">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="7f69b-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="7f69b-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f69b-156">-Tag</span></span>
<span data-ttu-id="7f69b-157">Hashtable von Tags als Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="7f69b-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="7f69b-158">Verwenden Sie eine leere Zeichenfolge, um das vorhandene Tag zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7f69b-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="7f69b-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7f69b-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="7f69b-160">Array von Zeichenfolgenwerten von ACL für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7f69b-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="7f69b-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="7f69b-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="7f69b-162">Array von PSVirtualNetworkRuleObjects für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7f69b-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f69b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f69b-163">-WhatIf</span></span>
<span data-ttu-id="7f69b-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f69b-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f69b-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f69b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f69b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f69b-166">CommonParameters</span></span>
<span data-ttu-id="7f69b-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f69b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f69b-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f69b-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f69b-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f69b-169">INPUTS</span></span>

### <span data-ttu-id="7f69b-170">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="7f69b-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="7f69b-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f69b-171">OUTPUTS</span></span>

### <span data-ttu-id="7f69b-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7f69b-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7f69b-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f69b-173">NOTES</span></span>

## <span data-ttu-id="7f69b-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f69b-174">RELATED LINKS</span></span>
