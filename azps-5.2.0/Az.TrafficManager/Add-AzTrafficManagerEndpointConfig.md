---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360589"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
Fügt einem lokalen Datenverkehrs-Manager-Profilobjekt einen Endpunkt hinzu.

## SYNTAX

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzTrafficManagerEndpointConfig"** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Endpunkt hinzu.
Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.

Dieses Cmdlet wird für das lokale Profilobjekt verwendet.
Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.
Verwenden Sie zum Erstellen eines Endpunkts und Zum Commit der Änderung in einem einzigen Vorgang das New-AzTrafficManagerEndpoint Cmdlet.

## BEISPIELE

### Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Der erste Befehl ruft ein Azure Traffic -Manager-Profil mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ab.
Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variable.

Mit dem zweiten Befehl wird dem in der Datei gespeicherten Profil ein Endpunkt namens "contoso" $TrafficManagerProfile.
Der Befehl enthält Konfigurationsdaten für den Endpunkt.
Mit diesem Befehl wird nur das lokale Objekt geändert.

Der letzte Befehl aktualisiert das Datenverkehrs-Manager-Profil in Azure so, dass es mit dem lokalen Wert in der $TrafficManagerProfile.

## PARAMETERS

### -CustomHeader
Liste von benutzerdefinierten Headernamen- und Wertpaaren für Probeanforderungen.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -EndpointLocation
Gibt die Position des Endpunkts an, der in der Datenverkehrsroutingmethode "Performance" verwendet werden soll.
Dieser Parameter gilt nur für Endpunkte des Typs "ExternalEndpoints" oder "NestedEndpoints".
Sie müssen diesen Parameter angeben, wenn die Datenverkehrsroutingmethode für die Leistung verwendet wird.

Geben Sie einen Namen für die Region Azure an.
Eine vollständige Liste der Azure-Regionen finden Sie unter "Azure-Regionen http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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

### -EndpointName
Gibt den Namen des Verkehrs-Manager-Endpunkts an, den dieses Cmdlet hinzufügt.

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

### -EndpointStatus
Gibt den Status des Endpunkts an.
Gültige Werte sind: 

- Aktiviert 
- Deaktiviert 

Wenn der Status "Aktiviert" ist, wird der Endpunkt auf den Endpunktstatus untersucht und in die Datenverkehrsroutingmethode einbezogen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoMapping
Die Liste der Regionen, die bei Verwendung der Routingmethode "Geografischer" Datenverkehr diesem Endpunkt zugeordnet sind. Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation [zur Verkehrsverwaltung.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Die minimale Anzahl von Endpunkten, die im untergeordneten Profil verfügbar sein müssen, damit der geschachtelte Endpunkt im übergeordneten Profil als verfügbar betrachtet wird.
Gilt nur für Endpunkte vom Typ "NestedEndpoints".

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Gibt die Priorität an, die der Verkehrsmanager dem Endpunkt zugibt.
Dieser Parameter wird nur verwendet, wenn das Datenverkehrs-Manager-Profil mit der "for Priority Traffic-Routing"-Methode konfiguriert ist.
Gültige Werte sind ganze Zahlen zwischen 1 und 1000.
Niedrigere Werte stellen eine höhere Priorität dar.

Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und es können keine zwei Endpunkte denselben Prioritätswert verwenden.
Wenn Sie keine Prioritäten angeben, weist der Verkehrs-Manager den Endpunkten Standardwerte zu, beginnend mit einem (1), in der Reihenfolge, in der die Endpunkte im Profil aufgeführt sind.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetMapping
Die Liste der Adressbereiche oder Subnetze, die bei Verwendung der Routingmethode für den Datenverkehr im Subnetz diesem Endpunkt zugeordnet sind.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Target
Gibt den vollqualifizierten Namen des Endpunkts an.
Der Datenverkehrs-Manager gibt diesen Wert in den DNS-Antworten zurück, wenn er den Datenverkehr an diesen Endpunkt weitergibt.
Geben Sie diesen Parameter nur für den Endpunkttyp "ExternalEndpoints" an.
Geben Sie für andere Endpunkttypen stattdessen den *Parameter "TargetResourceId"* an.

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

### -TargetResourceId
Gibt die Ressourcen-ID des Ziels an.
Geben Sie diesen Parameter nur für die Endpunkttypen "AzureEndpoints" und "NestedEndpoints" an.
Geben Sie für den Endpunkttyp "ExternalEndpoints" stattdessen den *Parameter "Target"* an.

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

### -TrafficManagerProfile
Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.
Dieses Cmdlet ändert dieses lokale Objekt.
Verwenden Sie zum **Abrufen eines TrafficManagerProfile-Objekts** das Get-AzTrafficManagerProfile Cmdlet.

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

### -Type
Gibt den Endpunkttyp an, den dieses Cmdlet dem Azure Traffic Manager-Profil hinzufügt.
Gültige Werte sind: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
Gibt die Gewichtung an, die der Verkehrsmanager dem Endpunkt zugibt.
Gültige Werte sind ganze Zahlen zwischen 1 und 1000.
Der Standardwert ist "1".
Dieser Parameter wird nur verwendet, wenn das Datenverkehrs-Manager-Profil mit der "Weighted traffic-routing"-Methode konfiguriert ist.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## AUSGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


