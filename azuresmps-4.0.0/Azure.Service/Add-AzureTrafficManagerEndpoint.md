---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006582"
---
# Add-AzureTrafficManagerEndpoint

## Synopsis
Fügt einen Endpunkt zu einem Traffic Manager-Profil hinzu.

## Syntax

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureTrafficManagerEndpoint** wird ein Endpunkt zu einem Microsoft Azure Traffic Manager-Profil hinzugefügt.
Nachdem Sie einen Endpunkt hinzugefügt haben, übergeben Sie das Ergebnis mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureTrafficManagerProfile** ".
Dieses Cmdlet stellt eine Verbindung mit Azure her, um Ihre Änderungen zu speichern.

## Beispiele

### Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

Der erste Befehl verwendet das Cmdlet " **Get-AzureTrafficManagerProfile** ", um das Profil mit dem Namen ContosoProfile abzurufen, und speichert es dann in der $TrafficManagerProfile-Variablen.

Mit dem zweiten Befehl wird ein Endpunkt zu Traffic Manager-Profil hinzugefügt, das in $TrafficManagerProfile gespeichert ist.
Der Endpunkt hat den Domänennamen Contoso02App.couldapp.net.
Der Befehl gibt auch an, ob er aktiviert ist und welchen Typ er hat.
Der Befehl übergibt das Profilobjekt an das Cmdlet " **Satz-AzureTrafficManagerProfile** ", um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.

### Beispiel 2: Hinzufügen eines Endpunkts mit einer angegebenen Position und Gewichtung
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Mit diesem Befehl wird ein Endpunkt zu einem Traffic Manager-Profil hinzugefügt.
Der Endpunkt hat den Domänennamen Contoso02App.couldapp.net.
Der Befehl gibt auch an, ob er aktiviert ist und welchen Typ er hat.
Mit dem Befehl werden auch die Gewichtung und die Position für den Endpunkt angegeben.
Der Befehl übergibt das Profilobjekt an **AzureTrafficManagerProfile** , um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.

## Parameter

### -Domänenname
Gibt den Domänennamen des hinzuzufügenden Endpunkts an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort des vom Cmdlet hinzugefügten Endpunkts an.
Dies muss eine Azure-Position sein.

Dieser Parameter muss einen Wert für Endpunkte des Typs "Any" oder des Typs "Trafficmanager" in einem Profil enthalten, bei dem die Load Balancing-Methode auf "Leistung" festgesetzt ist.
Mögliche Werte sind die Namen der Azure-Region, wie unter aufgeführt https://azure.microsoft.com/regions/ .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Gibt die Mindestanzahl von Endpunkten an, die das verschachtelte Profil Online haben muss, damit dieser Endpunkt als Online betrachtet werden kann.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -Status
Gibt den Status des Überwachungs Endpunkts an.
Gültige Werte sind: 

- Aktiviert
- Deaktiviert

Wenn Sie den Wert enabled angeben, überwacht Traffic Manager den Endpunkt, und die Load-Balancing-Methode berücksichtigt ihn beim Verwalten von Datenverkehr.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Gibt das Traffic Manager-Profilobjekt an, dem der Endpunkt hinzugefügt werden soll.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Typ
Gibt den Typ des Endpunkts an.
Gültige Werte sind: 

- CloudService
- AzureWebsite
- Trafficmanager

- Alle 

Wenn mehr als ein AzureWebsite-Endpunkt vorhanden ist, müssen sich die Endpunkte in unterschiedlichen Rechenzentren befinden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gewicht
Gibt die Gewichtung des vom Cmdlet hinzugefügten Endpunkts an.
Der gültige Wertebereich für diesen Parameter ist \[ 1.000 \] .

Dieser Parameter wird nur für Roundrobin-Lastenausgleichsrichtlinien verwendet.

```yaml
Type: Int32
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

### Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition
Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt, das Informationen über das aktualisierte Profil enthält.

## Notizen

## Verwandte Links

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Satz-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


