---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: c14854da187101f3b15db178c656005942c1bff0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504237"
---
# Add-AzureRmTrafficManagerCustomHeaderToProfile

## Synopsis
Fügt benutzerdefinierte Kopfzeileninformationen zu einem lokalen Traffic Manager-Profilobjekt hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureRmTrafficManagerCustomHeaderToProfile** werden benutzerdefinierte Headerinformationen zu einem lokalen Azure Traffic Manager-Profilobjekt hinzugefügt.
Sie können ein Profil mithilfe der Cmdlets New-AzureRmTrafficManagerProfile oder Get-AzureRmTrafficManagerProfile abrufen.

Dieses Cmdlet funktioniert für das lokale Profilobjekt.
Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.

## Beispiele

### Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Profil
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzureRmTrafficManagerProfile** ab.
Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.
Mit dem zweiten Befehl werden benutzerdefinierte Headerinformationen zu dem in $TrafficManagerProfile gespeicherten Profil hinzugefügt.
Der endgültige Befehl aktualisiert das Profil im Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.

## Parameter

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

### -Name
Gibt den Namen der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.

```yaml
Type: System.String
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
Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.

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

### -Wert
Gibt den Wert der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt für dieses Cmdlet.

## Ausgaben

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Dieses Cmdlet gibt ein geändertes **TrafficManagerProfile** -Objekt zurück.

## Notizen

## Verwandte Links

[Remove-AzureRmTrafficManagerCustomHeaderFromProfile](./Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Satz-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)
