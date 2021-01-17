---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382918"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Erstellt einen Endpunkt in einem Datenverkehrs-Manager-Profil.

## SYNTAX

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzTrafficManagerEndpoint"** erstellt einen Endpunkt in einem Azure Traffic Manager-Profil.

Mit diesem Cmdlet wird jeder neue Endpunkt an den Datenverkehrs-Manager-Dienst gesendet.
Wenn Sie einem lokalen Traffic Manager-Profilobjekt mehrere Endpunkte hinzufügen und Änderungen in einem einzigen Vorgang commiten möchten, verwenden Sie Add-AzTrafficManagerEndpointConfig cmdlet.

## BEISPIELE

### Beispiel 1: Erstellen eines externen Endpunkts für ein Profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Mit diesem Befehl wird ein externer Endpunkt namens "contoso" im Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" erstellt.

### Beispiel 2: Erstellen eines Azure-Endpunkts für ein Profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Mit diesem Befehl wird ein Azure-Endpunkt namens "contoso" im Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" erstellt.
Der Azure-Endpunkt verweist auf die Azure Web App, deren Azure Resource Manager-ID vom URI-Pfad in *TargetResourceId angegeben wird.*
Der Befehl gibt den Parameter *"EndpointLocation"* nicht an, da die Web -App-Ressource den Speicherort liefert.

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
Die Liste der Regionen, die bei Verwendung der Routingmethode "Geografischer" Datenverkehr diesem Endpunkt zugeordnet sind. Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation zur Verkehrsverwaltung.

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
Geben Sie einen Namen für die Region Azure an.
Eine vollständige Liste der Azure-Regionen finden Sie unter "Azure-Regionen http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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

### -Name
Gibt den Namen des Verkehrs-Manager-Endpunkts an, den dieses Cmdlet erstellt.

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

### -ProfileName
Gibt den Namen eines Datenverkehrs-Manager-Profils an, dem dieses Cmdlet einen Endpunkt hinzufügt.
Verwenden Sie zum Abrufen eines Profils die cmdlets New-AzTrafficManagerProfile Get-AzTrafficManagerProfile-Cmdlets.

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

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Dieses Cmdlet erstellt einen Datenverkehrs-Manager-Endpunkt in der Gruppe, die dieser Parameter angibt.

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

### -Type
Gibt den Endpunkttyp an, den dieses Cmdlet dem Datenverkehrs-Manager-Profil hinzufügt.
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

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


