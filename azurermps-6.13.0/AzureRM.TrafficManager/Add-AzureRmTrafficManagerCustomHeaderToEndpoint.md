---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664789"
---
# Add-AzureRmTrafficManagerCustomHeaderToEndpoint

## Synopsis
Fügt benutzerdefinierte Headerinformationen zu einem lokalen Traffic Manager-Endpunkt Objekt hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** werden benutzerdefinierte Headerinformationen zu einem lokalen Azure Traffic Manager-Endpunkt Objekt hinzugefügt.
Sie können einen Endpunkt mithilfe der Cmdlets New-AzureRmTrafficManagerEndpoint oder Get-AzureRmTrafficManagerEndpoint abrufen.

Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.
Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.

## Beispiele

### Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Endpunkt
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des Cmdlets **New-AzureRmTrafficManagerEndpoint** .
Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint-Variablen.
Der zweite Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunktbenutzer definierte Headerinformationen hinzu.
Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.

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

### -TrafficManagerEndpoint
Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.
Dieses Cmdlet ändert dieses lokale Objekt.
Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzureRmTrafficManagerEndpoint-oder New-AzureRmTrafficManagerEndpoint-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
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

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Dieses Cmdlet akzeptiert ein **TrafficManagerEndpoint** -Objekt für dieses Cmdlet.

## Ausgaben

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Dieses Cmdlet gibt ein geändertes **TrafficManagerEndpoint** -Objekt zurück.

## Notizen

## Verwandte Links

[Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[Neu – AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Satz-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
