---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006461"
---
# Import-AzureVM

## Synopsis
Importiert einen Azure Virtual Machine-Zustand aus einer Datei.

## Syntax

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Import-AzureVM** " wird der zuvor gespeicherte Zustand eines virtuellen Computers aus einer XML-Datei importiert.
Dieses Cmdlet ist nützlich, wenn Sie anschließend einen virtuellen Computer aus den importierten Daten erstellen möchten.

Beim Ausführen von " **Export-AzureVM** ", gefolgt von " **Remove-AzureVM** " und dann " **Import-AzureVM** ", um einen virtuellen Computer neu zu erstellen, kann die resultierende virtuelle Maschine eine andere IP-Adresse als das Original aufweisen.

## Beispiele

### Beispiel 1: Importieren eines Zustands eines virtuellen Computers
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

Dieser Befehl importiert den Zustand einer virtuellen Maschine aus der VMstate.xml-Datei und erstellt dann einen virtuellen Computer im angegebenen clouddienst.

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

### -Path
Gibt den Pfad der Datei mit dem Zustand des zuvor gespeicherten virtuellen Computers an.

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

[Export-AzureVM](./Export-AzureVM.md)

[Neu – AzureVM](./New-AzureVM.md)


