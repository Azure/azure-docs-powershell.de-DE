---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007589"
---
# Set-WAPackVMRole

## Synopsis
Ändert die Eigenschaft instanzenanzahl einer Rolle des virtuellen Computers.

## Syntax

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Diese Themen sind veraltet und werden in Zukunft entfernt.
In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Satz-WAPackVMRole** " ändert die Eigenschaft "instanzenanzahl" einer Rolle für einen virtuellen Computer.

## Beispiele

### Beispiel 1: Angeben der instanzenanzahl für eine Rolle eines virtuellen Computers
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

Der erste Befehl ruft die Rolle des virtuellen Computers mit dem Namen ContosoVMRole01 mit dem Cmdlet **Get-WAPackVMRole** ab und speichert dieses Objekt dann in der $VMRole Variablen.

Mit dem zweiten und letzten Befehl wird die neue instanzenanzahl der Rolle des virtuellen Computers festgelegt, die in $VMRole auf 3 gespeichert ist.

## Parameter

### -InstanceCount
Gibt die Anzahl der Instanzen für eine Rolle eines virtuellen Computers an.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
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

### -VMRole
Gibt eine Rolle für einen virtuellen Computer an.
Verwenden Sie zum Abrufen einer Rolle für einen virtuellen Computer das Cmdlet **Get-WAPackVMRole** .

```yaml
Type: VMRole
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

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[Neu – WAPackVMRole](./New-WAPackVMRole.md)

[Remove-WAPackVMRole](./Remove-WAPackVMRole.md)


