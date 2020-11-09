---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301192"
---
# Get-AzRedisCacheLink

## Synopsis
Link "Geo-Replikation" für den "Mehrweg"-Cache

## Syntax

### AllLinksForCache (Standard)
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForPrimaryCache
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForSecondaryCache
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Es gibt vier verschiedene Möglichkeiten zum Abrufen von Details zur Geo-Replikationsverknüpfung. Geben Sie entweder den Parameternamen oder PrimaryServerName und/oder SecondaryServerName. Name angegeben ist, wird der gesamte Link, in dem der Cache vorhanden ist, zurückgegeben. Wenn nur PrimaryServerName angegeben ist, werden alle Verknüpfungen zurückgegeben, wobei der Cache primär ist. Wenn nur SecondaryServerName angegeben ist, werden alle Links, bei denen der Cache sekundär ist, zurückgegeben. Wenn PrimaryServerName und SecondaryServerName beide angegeben sind, wird ein bestimmter Link mit der korrekten Rolle zurückgegeben. 

## Beispiele

### Beispiel 1: Abrufen mit dem Parametersatz AllLinksForCache
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft alle Links für die Geo-Replikation für den "mycache1.

### Beispiel 2: Abrufen der Verwendung von Parametersatz AllLinksForPrimaryCache
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft georeplikations-links ab, wobei der Name des mycache1-Caches primär ist.

### Beispiel 3: Abrufen mit dem Parametersatz AllLinksForSecondaryCache
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft georeplikations-links ab, wobei der mycache2-Cache mit dem Namen "Sekundär" ist.

### Beispiel 4: Abrufen der Verwendung von Parametersatz SingleLink
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft eine einzelne georeplikations-links ab, wobei der mycache1-Cache mit dem Namen "Primär" und der "mycache2" mit dem Namen "4/4" sekundäre

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Name
Name des Zwischenspeichers mit dem Namenzeichen

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrimaryServerName
Name des primären, in Verbindung stehenden "nicht-Cache".

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryServerName
Der Name des sekundären "a/a-Cache" in Link.

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer

## Notizen

## Verwandte Links

[Neu – AzRedisCacheLink](./New-AzRedisCacheLink.md)

[Remove-AzRedisCacheLink](./Remove-AzRedisCacheLink.md)

[Get-AzRedisCache](./Get-AzRedisCache.md)

[Neu – AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)

[Satz-AzRedisCache](./Set-AzRedisCache.md)