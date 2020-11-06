---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481654"
---
# Set-AzureRmRedisCache

## Synopsis
Ändert einen "a-a-Cache".

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmRedisCache** " ändert einen Azure-a-a-Cache.

## Beispiele

### Beispiel 1: Ändern eines Zeichenfolgen-Caches
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
```

Mit diesem Befehl wird die maxmemory-Richtlinie für den Namen "myCache" für den "a-Cache" aktualisiert.

## Parameter

### -EnableNonSslPort
Gibt an, ob der nicht-SSL-Port aktiviert ist.
Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).

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

### -MaxMemoryPolicy
Dieser Parameter wurde als veraltet markiert.
Verwenden Sie den *RedisConfiguration* -Parameter, um die maxmemory-Richtlinie einzurichten.
Zum Beispiel: 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### -Name
Gibt den Namen des zu aktualisierbaren "zu aktualisierbaren Speichers" an.

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
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.

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

### -ShardCount
Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.

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

### -SKU
Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.
Gültige Werte sind: 

- Grundlegende
- Standard
- Premium

Der Standardwert ist Standard.

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

### -TenantSettings
Dieser Parameter wurde als veraltet markiert.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys
Gibt alle Attribute eines "4-a-Cache" zurück, einschließlich primärer und sekundärer Zugriffstasten.

## Notizen

## Verwandte Links

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Neu – AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)


