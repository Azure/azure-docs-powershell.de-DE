---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006026"
---
# Set-AzureSBAuthorizationRule

## Synopsis
Aktualisiert die vorhandene ServiceBus-Autorisierungsregel.

## Syntax

### EntitySAS
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Namespaces
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Aktualisiert die vorhandene ServiceBus-Autorisierungsregel.

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## Beispiele

### Beispiel 1: Erneuern des Primärschlüssels für die Autorisierungsregel auf Namespaceebene
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

Der Primärschlüssel wird erneuert.

### Beispiel 2: Berechtigung zum Aktualisieren der Autorisierungsregel
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

Aktualisiert die Berechtigungen.

## Parameter

### -EntityName
Der Entitätsname, auf den die Regel angewendet werden soll.

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EntityType
Der Entitätstyp (Queue, Topic, Relay, NotificationHub).

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name der eindeutigen Autorisierungsregel.

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

### -Namespace
Der Namespacename, um die Autorisierungsregel anzuwenden.
Wenn kein Entitätsname angegeben wird, befindet sich die Regel auf der Namespaceebene.

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

### -Berechtigung
Die Autorisierungsberechtigungen (senden, verwalten, Abhören).

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Primär Primär
Der Primärschlüssel für die freigegebene zugriffssignatur.
Wird generiert, wenn Sie nicht bereitgestellt werden.

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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondaryKey
Der sekundäre Schlüssel für die freigegebene zugriffssignatur.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureSBAuthorizationRule](./Get-AzureSBAuthorizationRule.md)

[Neu – AzureSBAuthorizationRule](./New-AzureSBAuthorizationRule.md)

[Remove-AzureSBAuthorizationRule](./Remove-AzureSBAuthorizationRule.md)


