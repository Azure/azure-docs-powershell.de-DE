---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007613"
---
# Remove-WAPackVMSubnet

## Synopsis
Entfernt Subnetz-Objekte des virtuellen Computers.

## Syntax

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Diese Themen sind veraltet und werden in Zukunft entfernt.
In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .

Das Cmdlet **Remove-WAPackVMSubnet** entfernt Subnetzmasken virtueller Maschinen.

## Beispiele

### Beispiel 1: Entfernen eines virtuellen Computer-Subnets
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

Der erste Befehl ruft das Subnetz des virtuellen Computers mit dem Namen ContosoVMSubnet01 mit dem Cmdlet **Get-WAPackVMSubnet** ab und speichert dieses Objekt dann in der $VMSubnet Variablen.

Mit dem zweiten Befehl wird das in $VMSubnet gespeicherte Virtual Machine-Subnetz entfernt.
Der Befehl fordert Sie zur Bestätigung auf.

### Beispiel 2: Entfernen einer virtuellen Maschine ohne Bestätigung
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

Der erste Befehl ruft den clouddienst mit dem Namen ContosoVMSubnet02 mit dem Cmdlet **Get-WAPackVMSubnet** ab und speichert dieses Objekt dann in der $VMSubnet Variablen.

Mit dem zweiten Befehl wird das in $VMSubnet gespeicherte Virtual Machine-Subnetz entfernt.
Dieser Befehl enthält den Parameter *Force* .
Der Befehl fordert Sie nicht zur Bestätigung auf.

## Parameter

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

```yaml
Type: SwitchParameter
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

### -VMSubnet
Gibt ein Subnetz eines virtuellen Computers an.
Um ein Subnetz eines virtuellen Computers zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVMSubnet** .

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[Neu – WAPackVMSubnet](./New-WAPackVMSubnet.md)


