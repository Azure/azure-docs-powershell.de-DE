---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007562"
---
# Get-WAPackVM

## Synopsis
Ruft Objekte für virtuelle Maschinen ab.

## Syntax

### Leer (Standard)
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Themen sind veraltet und werden in Zukunft entfernt.
In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Get-WAPackVM** " Ruft Objekte des virtuellen Computers ab.

## Beispiele

### Beispiel 1: Abrufen eines virtuellen Computers mithilfe eines Namens
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 ab.

### Beispiel 2: Abrufen eines virtuellen Computers mithilfe einer ID
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Dieser Befehl ruft den virtuellen Computer ab, der die angegebene ID hat.

### Beispiel 3: Abrufen aller virtuellen Computer
```
PS C:\> Get-WAPackVM
```

Dieser Befehl ruft alle virtuellen Computer ab.

## Parameter

### -ID
Gibt die eindeutige ID einer virtuellen Maschine an.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen einer virtuellen Maschine an.

```yaml
Type: String
Parameter Sets: FromName
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

[Neu – WAPackVM](./New-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Neustart-WAPackVM](./Restart-WAPackVM.md)

[Lebenslauf-WAPackVM](./Resume-WAPackVM.md)

[Satz-WAPackVM](./Set-WAPackVM.md)

[Anfang-WAPackVM](./Start-WAPackVM.md)

[Stopp-WAPackVM](./Stop-WAPackVM.md)

[Suspend-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


