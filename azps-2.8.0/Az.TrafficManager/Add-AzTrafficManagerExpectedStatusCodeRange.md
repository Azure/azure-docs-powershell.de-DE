---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: c2758304f0140f5737a01611b18acf1449d0bb77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824604"
---
# Add-AzTrafficManagerExpectedStatusCodeRange

## Synopsis
Fügt einen erwarteten Statuscodebereich zu einem lokalen Traffic Manager-Profilobjekt hinzu.

## Syntax

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzTrafficManagerExpectedStatusCodeRange** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Bereich von erwarteten Statuscodes hinzu.
Sie können ein Profil mithilfe der Cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile abrufen.

Dieses Cmdlet funktioniert für das lokale Profilobjekt.
Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.

## Beispiele

### Beispiel 1: Hinzufügen eines erwarteten Statuscode Bereichs zu einem Profil
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzTrafficManagerProfile** ab.
Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.
Mit dem zweiten Befehl wird dem in $TrafficManagerProfile gespeicherten Profil ein erwarteter Statuscodebereich hinzugefügt.
Der endgültige Befehl aktualisiert das Profil im Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Max
Gibt den höchsten Wert im Statuscodebereich an, der hinzugefügt werden soll.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Min
Gibt den niedrigsten Wert im Statuscodebereich an, der hinzugefügt werden soll.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Gibt ein lokales **TrafficManagerProfile** -Objekt an.
Dieses Cmdlet ändert dieses lokale Objekt.
Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## Ausgaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## Notizen

## Verwandte Links

[Remove-AzTrafficManagerExpectedStatusCodeRange](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Satz-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)
