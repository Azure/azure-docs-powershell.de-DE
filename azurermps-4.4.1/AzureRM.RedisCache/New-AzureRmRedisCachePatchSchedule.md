---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662624"
---
# New-AzureRmRedisCachePatchSchedule

## Synopsis
Fügt einen Patch-Zeitplan hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **New-AzureRmRedisCachePatchSchedule** " wird ein Patch-Zeitplan zu einem Cache im Azure-Schlüssel-a-Cache hinzugefügt.

## Beispiele

### Beispiel 1: Erstellen und Hinzufügen eines Patch-Zeitplans für einen Cache
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

Mit diesem Befehl wird dem Cache mit dem Namen RedisCache06 ein Patch-Zeitplan hinzugefügt.
Der Parameter Entries nimmt als Wert einen Befehl auf, der zum Erstellen eines Zeitplans **New-AzureRmRedisCacheScheduleEntry** verwendet.

## Parameter

### -Einträge
Gibt ein Array von Zeitplänen an, die von diesem Cmdlet für einen Cache festgelegt werden. Verwenden Sie das New-AzureRmRedisCacheScheduleEntry-Cmdlet, um ein **PSScheduleEntry** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Caches an.

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die den Cache enthält.

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

### Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry
Dieses Cmdlet gibt den Patch-Terminplan Eintrag zurück, der für den Cache eingestellt wurde.

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website

## Verwandte Links

[Get-AzureRmRedisCachePatchSchedule](./Get-AzureRmRedisCachePatchSchedule.md)

[Neu – AzureRmRedisCacheScheduleEntry](./New-AzureRmRedisCacheScheduleEntry.md)

[Remove-AzureRmRedisCachePatchSchedule](./Remove-AzureRmRedisCachePatchSchedule.md)


