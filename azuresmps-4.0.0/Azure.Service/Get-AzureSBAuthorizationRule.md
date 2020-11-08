---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005820"
---
# Get-AzureSBAuthorizationRule

## Synopsis
Ruft Service Bus-Autorisierungsregeln ab.


## Syntax

### EntitySAS
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Namespaces
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Ruft Service Bus-Autorisierungsregeln ab.

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## Beispiele

### Beispiel 1: Abrufen der Autorisierungsregel auf Namespaceebene
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

Ruft alle verfügbaren Autorisierungsregeln für MyNamespace ab.

### Beispiel 2: Abrufen der Autorisierungsregel für eine Warteschlange
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

Ruft alle verfügbaren Autorisierungsregeln einer myentity-Warteschlange für MyNamespace ab.

### Beispiel 3: Abrufen der Autorisierungsregel nach Namen
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

Ruft eine Autorisierungsregel namens myrule auf MyNamespace-Ebene ab.

### Beispiel 4: Abrufen der Autorisierungsregel nach Berechtigung
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

Ruft alle Autorisierungsregeln ab, die über die Berechtigung Senden auf Namespaceebene verfügen.

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

Required: False
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
Die Autorisierungsberechtigungen zum Filtern (senden, verwalten, Abhören).
Dies verwendet exakte Übereinstimmung.

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureSBAuthorizationRule](./New-AzureSBAuthorizationRule.md)

[Remove-AzureSBAuthorizationRule](./Remove-AzureSBAuthorizationRule.md)

[Satz-AzureSBAuthorizationRule](./Set-AzureSBAuthorizationRule.md)


