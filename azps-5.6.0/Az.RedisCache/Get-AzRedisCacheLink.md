---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 9b1957054c243de8776f0063e236f9e19980af54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933760"
---
# Get-AzRedisCacheLink

## SYNOPSIS
Link zur Georeplikation für Den Redis Cache.

## SYNTAX

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

## BESCHREIBUNG
Es gibt vier verschiedene Möglichkeiten zum Erhalten von Linkdetails für die Georeplikation. Geben Sie entweder den Parameter Name oder PrimaryServerName und/oder SecondaryServerName an. Der Name wird angegeben, und alle Verknüpfungen, für die cache vorhanden ist, werden zurückgegeben. Wenn nur PrimaryServerName angegeben wird, werden alle Links zurückgegeben, für die der Cache primär ist. Wenn nur SecondaryServerName angegeben wird, werden alle Links zurückgegeben, für die der Cache sekundär ist. Wenn PrimaryServerName und SecondaryServerName beide angegeben werden, wird ein bestimmter Link mit der richtigen Rolle zurückgegeben. 

## BEISPIELE

### Beispiel 1: Verwenden des Parametersatzs AllLinksForCache
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft alle Georeplikationslinks für Den Redis Cache mit dem Namen mycache1 ab.

### Beispiel 2: Verwenden des Parametersatzs AllLinksForPrimaryCache
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft Georeplikationslinks ab, bei denen der Redis Cache mit dem Namen mycache1 primär ist.

### Beispiel 3: Verwenden des Parametersatzs AllLinksForSecondaryCache
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft Verknüpfungen zur Georeplikation ab, wobei der Redis Cache mit dem Namen mycache2 sekundär ist.

### Beispiel 4: Verwenden des Parametersatzs SingleLink
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Dieser Befehl ruft eine einzelne Georeplikationsverknüpfung ab, wobei der Redis Cache mit dem Namen mycache1 primär und der Redis Cache mit dem Namen mycache2 sekundär ist.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Name des Redis-Caches.

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
Name des primären Redis-Caches in Link.

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
Name des sekundären Redis-Caches in Link.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer

## NOTIZEN

## VERWANDTE LINKS

[New-AzRedisCacheLink](./New-AzRedisCacheLink.md)

[Remove-AzRedisCacheLink](./Remove-AzRedisCacheLink.md)

[Get-AzRedisCache](./Get-AzRedisCache.md)

[New-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)