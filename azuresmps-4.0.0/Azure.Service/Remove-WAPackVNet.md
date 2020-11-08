---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007612"
---
# Remove-WAPackVNet

## Synopsis
Entfernt virtuelle Netzwerkobjekte.

## Syntax

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Themen sind veraltet und werden in Zukunft entfernt.
In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .

Das Cmdlet **Remove-WAPackVNet** entfernt virtuelle Netzwerkobjekte.

## Beispiele

### Beispiel 1: Entfernen eines virtualisierten Netzwerks
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

Der erste Befehl ruft das virtualisierte Netzwerk mit dem Namen ContosoVNet01 mit dem Cmdlet **Get-WAPackVNet** ab und speichert dieses Objekt dann in der $VNet Variablen.
Der zweite Befehl entfernt das virtualisierte Netzwerk, das in $VNet gespeichert ist.
Der Befehl fordert Sie zur Bestätigung auf.

### Beispiel 2: Entfernen eines virtualisierten Netzwerks ohne Bestätigung
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

Der erste Befehl ruft den clouddienst mit dem Namen ContosoVNet02 mit dem Cmdlet **Get-WAPackVNet** ab und speichert dieses Objekt dann in der $VNet Variablen.
Der zweite Befehl entfernt das virtualisierte Netzwerk, das in $VNet gespeichert ist.
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

### -VNet
Gibt ein virtualisiertes Netzwerk an.
Verwenden Sie das Cmdlet " **Get-WAPackVNet** ", um ein virtualisiertes Netzwerk zu erhalten.

```yaml
Type: VMNetwork
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

[Get-WAPackVNet](./Get-WAPackVNet.md)

[Neu – WAPackVNet](./New-WAPackVNet.md)


