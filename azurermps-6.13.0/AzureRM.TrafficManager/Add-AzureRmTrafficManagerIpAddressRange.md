---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477605"
---
# Add-AzureRmTrafficManagerIpAddressRange

## Synopsis
Fügt einen Adressbereich oder ein Subnetz zu einem Endpunkt Objekt des lokalen Datenverkehrs-Managers hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureRmTrafficManagerIpAddressRange** wird ein IP-Adressbereich zu einem lokalen Azure Traffic Manager-Endpunkt Objekt hinzugefügt.
Sie können einen Endpunkt mithilfe der Cmdlets New-AzureRmTrafficManagerEndpoint oder Get-AzureRmTrafficManagerEndpoint abrufen.

Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.
Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.

## Beispiele

### Beispiel 1: Hinzufügen von IP-Adressbereichen zu einem Endpunkt
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des Cmdlets **New-AzureRmTrafficManagerEndpoint** .
Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint-Variablen.
Der zweite Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 1.2.3.4 zu 5.6.7.8 hinzu.
Der dritte Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 9.10.11.0 zu 9.10.11.255 hinzu.
Der vierte Befehl überprüft, ob der Bereich der Größe des Bereichs entspricht, und fügt dann den IP-Adressbereich 12.13.14.0 zu 12.13.14.31 dem in $TrafficManagerEndpoint gespeicherten Endpunkt hinzu.
Der fünfte Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 15.16.17.18 zu 15.16.17.18 hinzu.
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

### -Letzte
Gibt die letzte IP-Adresse im Bereich an, die hinzugefügt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Gibt den Bereich des IP-Adressbereichs an, der hinzugefügt werden soll.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
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

### -First
Gibt die erste IP-Adresse im Bereich an, die hinzugefügt werden soll.

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

[Remove-AzureRmTrafficManagerIpAddressRange](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[Neu – AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Satz-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
