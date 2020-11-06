---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503422"
---
# <span data-ttu-id="85b64-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="85b64-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="85b64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85b64-102">SYNOPSIS</span></span>
<span data-ttu-id="85b64-103">Ändert einen "a-a-Cache".</span><span class="sxs-lookup"><span data-stu-id="85b64-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85b64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85b64-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85b64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85b64-105">DESCRIPTION</span></span>
<span data-ttu-id="85b64-106">Das Cmdlet " **Satz-AzureRmRedisCache** " ändert einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="85b64-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="85b64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85b64-107">EXAMPLES</span></span>

### <span data-ttu-id="85b64-108">Beispiel 1: Ändern eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="85b64-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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

<span data-ttu-id="85b64-109">Mit diesem Befehl wird die maxmemory-Richtlinie für den Namen "myCache" für den "a-Cache" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="85b64-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="85b64-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="85b64-110">PARAMETERS</span></span>

### <span data-ttu-id="85b64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b64-111">-DefaultProfile</span></span>
<span data-ttu-id="85b64-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85b64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b64-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="85b64-113">-EnableNonSslPort</span></span>
<span data-ttu-id="85b64-114">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="85b64-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="85b64-115">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="85b64-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="85b64-116">-Name</span><span class="sxs-lookup"><span data-stu-id="85b64-116">-Name</span></span>
<span data-ttu-id="85b64-117">Gibt den Namen des zu aktualisierbaren "zu aktualisierbaren Speichers" an.</span><span class="sxs-lookup"><span data-stu-id="85b64-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="85b64-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="85b64-118">-RedisConfiguration</span></span>
<span data-ttu-id="85b64-119">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="85b64-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="85b64-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="85b64-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85b64-121">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85b64-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="85b64-122">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="85b64-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="85b64-123">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="85b64-123">Premium tier only.</span></span>
- <span data-ttu-id="85b64-124">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="85b64-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="85b64-125">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="85b64-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="85b64-126">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="85b64-126">Premium tier only.</span></span>
- <span data-ttu-id="85b64-127">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="85b64-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="85b64-128">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="85b64-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="85b64-129">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="85b64-129">Premium tier only.</span></span> 
- <span data-ttu-id="85b64-130">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="85b64-130">maxmemory-reserved.</span></span>
<span data-ttu-id="85b64-131">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="85b64-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="85b64-132">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="85b64-133">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="85b64-133">maxmemory-policy.</span></span>
<span data-ttu-id="85b64-134">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="85b64-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="85b64-135">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-135">All pricing tiers.</span></span> 
- <span data-ttu-id="85b64-136">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="85b64-136">notify-keyspace-events.</span></span>
<span data-ttu-id="85b64-137">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="85b64-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="85b64-138">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="85b64-139">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="85b64-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="85b64-140">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="85b64-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="85b64-141">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="85b64-142">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="85b64-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="85b64-143">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="85b64-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="85b64-144">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="85b64-145">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="85b64-145">set-max-intset-entries.</span></span>
<span data-ttu-id="85b64-146">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="85b64-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="85b64-147">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="85b64-148">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="85b64-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="85b64-149">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="85b64-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="85b64-150">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="85b64-151">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="85b64-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="85b64-152">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="85b64-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="85b64-153">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="85b64-154">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="85b64-154">databases.</span></span>
<span data-ttu-id="85b64-155">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="85b64-155">Configures the number of databases.</span></span>
<span data-ttu-id="85b64-156">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="85b64-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="85b64-157">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="85b64-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="85b64-158">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="85b64-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="85b64-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b64-159">-ResourceGroupName</span></span>
<span data-ttu-id="85b64-160">Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="85b64-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="85b64-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="85b64-161">-ShardCount</span></span>
<span data-ttu-id="85b64-162">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="85b64-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="85b64-163">-Size</span><span class="sxs-lookup"><span data-stu-id="85b64-163">-Size</span></span>
<span data-ttu-id="85b64-164">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="85b64-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="85b64-165">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="85b64-165">Valid values are:</span></span> 
- <span data-ttu-id="85b64-166">P1</span><span class="sxs-lookup"><span data-stu-id="85b64-166">P1</span></span>
- <span data-ttu-id="85b64-167">P2</span><span class="sxs-lookup"><span data-stu-id="85b64-167">P2</span></span>
- <span data-ttu-id="85b64-168">P3</span><span class="sxs-lookup"><span data-stu-id="85b64-168">P3</span></span>
- <span data-ttu-id="85b64-169">P4</span><span class="sxs-lookup"><span data-stu-id="85b64-169">P4</span></span>
- <span data-ttu-id="85b64-170">C0</span><span class="sxs-lookup"><span data-stu-id="85b64-170">C0</span></span>
- <span data-ttu-id="85b64-171">C1</span><span class="sxs-lookup"><span data-stu-id="85b64-171">C1</span></span>
- <span data-ttu-id="85b64-172">C2</span><span class="sxs-lookup"><span data-stu-id="85b64-172">C2</span></span>
- <span data-ttu-id="85b64-173">C3</span><span class="sxs-lookup"><span data-stu-id="85b64-173">C3</span></span>
- <span data-ttu-id="85b64-174">C4</span><span class="sxs-lookup"><span data-stu-id="85b64-174">C4</span></span>
- <span data-ttu-id="85b64-175">C5</span><span class="sxs-lookup"><span data-stu-id="85b64-175">C5</span></span>
- <span data-ttu-id="85b64-176">C6</span><span class="sxs-lookup"><span data-stu-id="85b64-176">C6</span></span>
- <span data-ttu-id="85b64-177">250MB</span><span class="sxs-lookup"><span data-stu-id="85b64-177">250MB</span></span>
- <span data-ttu-id="85b64-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="85b64-178">1GB</span></span>
- <span data-ttu-id="85b64-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="85b64-179">2.5GB</span></span>
- <span data-ttu-id="85b64-180">6GB</span><span class="sxs-lookup"><span data-stu-id="85b64-180">6GB</span></span>
- <span data-ttu-id="85b64-181">13GB</span><span class="sxs-lookup"><span data-stu-id="85b64-181">13GB</span></span>
- <span data-ttu-id="85b64-182">26GB</span><span class="sxs-lookup"><span data-stu-id="85b64-182">26GB</span></span>
- <span data-ttu-id="85b64-183">53GB der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="85b64-183">53GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b64-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="85b64-184">-Sku</span></span>
<span data-ttu-id="85b64-185">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="85b64-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="85b64-186">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="85b64-186">Valid values are:</span></span> 
- <span data-ttu-id="85b64-187">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="85b64-187">Basic</span></span>
- <span data-ttu-id="85b64-188">Standard</span><span class="sxs-lookup"><span data-stu-id="85b64-188">Standard</span></span>
- <span data-ttu-id="85b64-189">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="85b64-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="85b64-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="85b64-190">-Tag</span></span>
<span data-ttu-id="85b64-191">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="85b64-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="85b64-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="85b64-192">-TenantSettings</span></span>
<span data-ttu-id="85b64-193">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="85b64-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="85b64-194">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85b64-194">-Confirm</span></span>
<span data-ttu-id="85b64-195">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85b64-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85b64-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85b64-196">-WhatIf</span></span>
<span data-ttu-id="85b64-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85b64-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85b64-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85b64-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85b64-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b64-199">CommonParameters</span></span>
<span data-ttu-id="85b64-200">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b64-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b64-201">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b64-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b64-202">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85b64-202">INPUTS</span></span>

### <span data-ttu-id="85b64-203">System. String</span><span class="sxs-lookup"><span data-stu-id="85b64-203">System.String</span></span>

### <span data-ttu-id="85b64-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="85b64-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="85b64-205">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="85b64-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="85b64-206">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="85b64-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="85b64-207">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85b64-207">OUTPUTS</span></span>

### <span data-ttu-id="85b64-208">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="85b64-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="85b64-209">Notizen</span><span class="sxs-lookup"><span data-stu-id="85b64-209">NOTES</span></span>

## <span data-ttu-id="85b64-210">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85b64-210">RELATED LINKS</span></span>

[<span data-ttu-id="85b64-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="85b64-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="85b64-212">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="85b64-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="85b64-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="85b64-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


