---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846923"
---
# <span data-ttu-id="f69ae-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f69ae-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="f69ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f69ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f69ae-103">Ändert einen "a-a-Cache".</span><span class="sxs-lookup"><span data-stu-id="f69ae-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="f69ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f69ae-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f69ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f69ae-105">DESCRIPTION</span></span>
<span data-ttu-id="f69ae-106">Das Cmdlet " **Satz-AzRedisCache** " ändert einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="f69ae-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="f69ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f69ae-107">EXAMPLES</span></span>

### <span data-ttu-id="f69ae-108">Beispiel 1: Ändern eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="f69ae-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="f69ae-109">Mit diesem Befehl wird die maxmemory-Richtlinie für den Namen "myCache" für den "a-Cache" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f69ae-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="f69ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f69ae-110">PARAMETERS</span></span>

### <span data-ttu-id="f69ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69ae-111">-DefaultProfile</span></span>
<span data-ttu-id="f69ae-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f69ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="f69ae-113">-EnableNonSslPort</span></span>
<span data-ttu-id="f69ae-114">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f69ae-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="f69ae-115">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="f69ae-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f69ae-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="f69ae-117">Geben Sie die TLS-Version an, die von Clients zum Herstellen einer Verbindung mit dem Cache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f69ae-117">Specify the TLS version required by clients to connect to cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f69ae-118">-Name</span></span>
<span data-ttu-id="f69ae-119">Gibt den Namen des zu aktualisierbaren "zu aktualisierbaren Speichers" an.</span><span class="sxs-lookup"><span data-stu-id="f69ae-119">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69ae-120">-RedisConfiguration</span></span>
<span data-ttu-id="f69ae-121">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="f69ae-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="f69ae-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f69ae-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f69ae-123">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f69ae-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="f69ae-124">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f69ae-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="f69ae-125">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="f69ae-125">Premium tier only.</span></span>
- <span data-ttu-id="f69ae-126">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f69ae-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="f69ae-127">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="f69ae-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="f69ae-128">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="f69ae-128">Premium tier only.</span></span>
- <span data-ttu-id="f69ae-129">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="f69ae-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="f69ae-130">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="f69ae-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="f69ae-131">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="f69ae-131">Premium tier only.</span></span> 
- <span data-ttu-id="f69ae-132">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="f69ae-132">maxmemory-reserved.</span></span>
<span data-ttu-id="f69ae-133">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f69ae-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="f69ae-134">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f69ae-135">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f69ae-135">maxmemory-policy.</span></span>
<span data-ttu-id="f69ae-136">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="f69ae-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="f69ae-137">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-137">All pricing tiers.</span></span> 
- <span data-ttu-id="f69ae-138">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f69ae-138">notify-keyspace-events.</span></span>
<span data-ttu-id="f69ae-139">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="f69ae-140">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="f69ae-141">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="f69ae-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="f69ae-142">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f69ae-143">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f69ae-144">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="f69ae-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="f69ae-145">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f69ae-146">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f69ae-147">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="f69ae-147">set-max-intset-entries.</span></span>
<span data-ttu-id="f69ae-148">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f69ae-149">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f69ae-150">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="f69ae-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="f69ae-151">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f69ae-152">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f69ae-153">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="f69ae-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="f69ae-154">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f69ae-155">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f69ae-156">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="f69ae-156">databases.</span></span>
<span data-ttu-id="f69ae-157">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="f69ae-157">Configures the number of databases.</span></span>
<span data-ttu-id="f69ae-158">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f69ae-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="f69ae-159">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="f69ae-160">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="f69ae-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69ae-161">-ResourceGroupName</span></span>
<span data-ttu-id="f69ae-162">Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="f69ae-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="f69ae-163">-ShardCount</span></span>
<span data-ttu-id="f69ae-164">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="f69ae-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-165">-Size</span><span class="sxs-lookup"><span data-stu-id="f69ae-165">-Size</span></span>
<span data-ttu-id="f69ae-166">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="f69ae-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="f69ae-167">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f69ae-167">Valid values are:</span></span> 
- <span data-ttu-id="f69ae-168">P1</span><span class="sxs-lookup"><span data-stu-id="f69ae-168">P1</span></span>
- <span data-ttu-id="f69ae-169">P2</span><span class="sxs-lookup"><span data-stu-id="f69ae-169">P2</span></span>
- <span data-ttu-id="f69ae-170">P3</span><span class="sxs-lookup"><span data-stu-id="f69ae-170">P3</span></span>
- <span data-ttu-id="f69ae-171">P4</span><span class="sxs-lookup"><span data-stu-id="f69ae-171">P4</span></span>
- <span data-ttu-id="f69ae-172">P5</span><span class="sxs-lookup"><span data-stu-id="f69ae-172">P5</span></span>
- <span data-ttu-id="f69ae-173">C0</span><span class="sxs-lookup"><span data-stu-id="f69ae-173">C0</span></span>
- <span data-ttu-id="f69ae-174">C1</span><span class="sxs-lookup"><span data-stu-id="f69ae-174">C1</span></span>
- <span data-ttu-id="f69ae-175">C2</span><span class="sxs-lookup"><span data-stu-id="f69ae-175">C2</span></span>
- <span data-ttu-id="f69ae-176">C3</span><span class="sxs-lookup"><span data-stu-id="f69ae-176">C3</span></span>
- <span data-ttu-id="f69ae-177">C4</span><span class="sxs-lookup"><span data-stu-id="f69ae-177">C4</span></span>
- <span data-ttu-id="f69ae-178">C5</span><span class="sxs-lookup"><span data-stu-id="f69ae-178">C5</span></span>
- <span data-ttu-id="f69ae-179">C6</span><span class="sxs-lookup"><span data-stu-id="f69ae-179">C6</span></span>
- <span data-ttu-id="f69ae-180">250MB</span><span class="sxs-lookup"><span data-stu-id="f69ae-180">250MB</span></span>
- <span data-ttu-id="f69ae-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="f69ae-181">1GB</span></span>
- <span data-ttu-id="f69ae-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="f69ae-182">2.5GB</span></span>
- <span data-ttu-id="f69ae-183">6GB</span><span class="sxs-lookup"><span data-stu-id="f69ae-183">6GB</span></span>
- <span data-ttu-id="f69ae-184">13GB</span><span class="sxs-lookup"><span data-stu-id="f69ae-184">13GB</span></span>
- <span data-ttu-id="f69ae-185">26GB</span><span class="sxs-lookup"><span data-stu-id="f69ae-185">26GB</span></span>
- <span data-ttu-id="f69ae-186">53GB</span><span class="sxs-lookup"><span data-stu-id="f69ae-186">53GB</span></span>
- <span data-ttu-id="f69ae-187">120GB der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="f69ae-187">120GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="f69ae-188">-Sku</span></span>
<span data-ttu-id="f69ae-189">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="f69ae-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="f69ae-190">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f69ae-190">Valid values are:</span></span> 
- <span data-ttu-id="f69ae-191">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="f69ae-191">Basic</span></span>
- <span data-ttu-id="f69ae-192">Standard</span><span class="sxs-lookup"><span data-stu-id="f69ae-192">Standard</span></span>
- <span data-ttu-id="f69ae-193">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="f69ae-193">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="f69ae-194">-Tag</span></span>
<span data-ttu-id="f69ae-195">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f69ae-195">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="f69ae-196">-TenantSettings</span></span>
<span data-ttu-id="f69ae-197">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="f69ae-197">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69ae-198">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f69ae-198">-Confirm</span></span>
<span data-ttu-id="f69ae-199">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f69ae-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f69ae-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f69ae-200">-WhatIf</span></span>
<span data-ttu-id="f69ae-201">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f69ae-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f69ae-202">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f69ae-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f69ae-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69ae-203">CommonParameters</span></span>
<span data-ttu-id="f69ae-204">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69ae-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69ae-205">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f69ae-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69ae-206">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f69ae-206">INPUTS</span></span>

### <span data-ttu-id="f69ae-207">System. String</span><span class="sxs-lookup"><span data-stu-id="f69ae-207">System.String</span></span>

### <span data-ttu-id="f69ae-208">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f69ae-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f69ae-209">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f69ae-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f69ae-210">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f69ae-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f69ae-211">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f69ae-211">OUTPUTS</span></span>

### <span data-ttu-id="f69ae-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f69ae-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="f69ae-213">Notizen</span><span class="sxs-lookup"><span data-stu-id="f69ae-213">NOTES</span></span>

## <span data-ttu-id="f69ae-214">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f69ae-214">RELATED LINKS</span></span>

[<span data-ttu-id="f69ae-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f69ae-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="f69ae-216">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f69ae-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f69ae-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f69ae-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


