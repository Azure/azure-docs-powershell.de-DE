---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006130"
---
# New-AzureDns

## Synopsis
Erstellt ein Azure DNS Settings-Objekt.

## Syntax

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureDns** wird ein Azure DNS Settings-Objekt erstellt.
Sie können ein DNS-Einstellungsobjekt verwenden, wenn Sie einen virtuellen Computer mithilfe des Cmdlets **New-AzureVM** erstellen.

## Beispiele

### Beispiel 1: Erstellen eines DNS-Einstellungs Objekts
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

Mit diesem Befehl wird ein Azure DNS Settings-Objekt erstellt.
Der DNS-Server hat die angegebene Adresse und den Anzeigenamen Dns01.
Der Befehl speichert das Objekt in der $DNS-Variablen für die Verwendung durch das Cmdlet **New-AzureVM** .

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddress
Gibt die IP-Adresse des DNS-Servers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Anzeigenamen für den DNS-Server an.
Dieser Name ist nicht unbedingt ein vollständig qualifizierter Domänenname.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Add-AzureDns](./Add-AzureDns.md)

[Get-AzureDns](./Get-AzureDns.md)

[Neu – AzureVM](./New-AzureVM.md)

[Remove-AzureDns](./Remove-AzureDns.md)

[Satz-AzureDns](./Set-AzureDns.md)


