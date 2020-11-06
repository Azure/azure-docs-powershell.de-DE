---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481002"
---
# New-AzureRmRedisCache

## Synopsis
Erstellt einen Zwischenspeicher mit einem Zwischenspeicher.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **New-AzureRmRedisCache** " wird ein Azure-Teiler-Cache erstellt.

## Beispiele

### Beispiel 1: Erstellen eines Zeichenfolgen-Caches
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.

### Beispiel 2: Erstellen eines Standard mäßigen SKUs-Caches
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNonSslPort
Gibt an, ob der nicht-SSL-Port aktiviert ist.
Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort an, an dem ein a-a/a-Cache erstellt werden soll.
Gültige Werte sind: 

- Nord-Zentral-USA
- Süd-Mittelamerika
- Zentral-US
- West Europa
- Nordeuropa
- West-US
- East US
- East US 2
- Japan (Ost)
- Japan West
- Brasilien Süd
- Südostasien
- Ostasien
- Australien (Ost)
- Australien südöstlich

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxMemoryPolicy
Dieser Parameter wurde als veraltet markiert.
Verwenden Sie den *RedisConfiguration* -Parameter, um die maxmemory-Richtlinie einzurichten.
Zum Beispiel: 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des zu erstellbaren zu erstellbaren zu erstellbaren zu.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisConfiguration
Gibt die Einstellungen für die Einstellungen für die Konfiguration an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- RDB – Backup-aktiviert.
Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.
Nur Premium-Stufe.
- RDB-Speicher-Verbindungszeichenfolge.
Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.
Nur Premium-Stufe.
- RDB-Backup-Frequency.
Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.
Nur Premium-Stufe. 
- maxmemory-reserviert.
Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.
Standard-und Premium-Stufen. 
- maxmemory-Richtlinie.
Konfiguriert die vertreibungs Richtlinie für den Cache.
Alle Preisstufen. 
- Notify-Keyspace-Ereignisse.
Konfiguriert die Keyspace-Benachrichtigungen.
Standard-und Premium-Stufen. 
- Hash-Max-ziplist-Einträge.
Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.
Standard-und Premium-Stufen. 
- Hash-Max-ziplist-Wert.
Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.
Standard-und Premium-Stufen. 
- Satz-Max-intset-Einträge.
Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.
Standard-und Premium-Stufen. 
- zset-Max-ziplist-Einträge.
Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.
Standard-und Premium-Stufen. 
- zset-Max-ziplist-Wert.
Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.
Standard-und Premium-Stufen. 
- Datenbanken.
Konfiguriert die Anzahl der Datenbanken.
Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.
Standard-und Premium-Stufen.

Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisVersion
Dieser Parameter ist veraltet und wird aus zukünftigen Versionen entfernt.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, in der der "a/a-Cache" erstellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShardCount
Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- 1
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9 
- 10

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
Gibt die Größe des Zwischenspeichers für "a. a" an.
Gültige Werte sind: 

- P1
- P2
- P3
- P4
- C0
- C1
- C2
- C3
- C4
- C5
- C6
- 250MB
- 1 GB
- 2,5 GB
- 6GB
- 13GB
- 26GB
- 53GB

Der Standardwert ist 1GB oder C1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.
Gültige Werte sind: 

- Grundlegende
- Standard
- Premium

Der Standardwert ist Standard.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StaticIP
Gibt eine eindeutige IP-Adresse im Subnetz für den Cache für den "a/a-Cache" an.

Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnetz
Gibt den Namen des Subnets an, in dem der "a-Cache" bereitgestellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnet-Nr
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Eine Hashtabelle, die Tags darstellt.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
Dieser Parameter wurde als veraltet markiert.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Gibt die Ressourcen-ID des virtuellen Netzwerks an, in dem der "a-Cache" bereitgestellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Liste der Zonen.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Sie können die Eingabe an dieses Cmdlet nach Name, aber nicht nach Wert übergeben.

## Ausgaben

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys
Dieses Cmdlet gibt alle Attribute eines a-4-a-Caches einschließlich primärer und sekundärer Zugriffstasten zurück.

## Notizen

## Verwandte Links

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Satz-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


