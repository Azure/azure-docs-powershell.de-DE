---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005640"
---
# Set-AzureTrafficManagerEndpoint

## Synopsis
Aktualisiert die Eigenschaften eines Endpunkts in einem Traffic Manager-Profil.

## Syntax

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureTrafficManagerEndpoint** " aktualisiert die Eigenschaften eines Endpunkts in einem Microsoft Azure Traffic Manager-Profil.
Wenn der Endpunkt im aktuellen Profil nicht vorhanden ist, wird dieser vom Cmdlet erstellt.
Nachdem Sie einen Endpunkt hinzugefügt haben, übergeben Sie das Ergebnis mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureTrafficManagerProfile** ".
Dieses Cmdlet stellt eine Verbindung mit Azure her, um Ihre Änderungen zu speichern.

## Beispiele

### Beispiel 1: Aktualisieren eines Endpunkts für ein Profil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Der erste Befehl verwendet das Cmdlet " **Get-AzureTrafficManagerProfile** ", um das Profil mit dem Namen ContosoProfile abzurufen, und speichert es dann in der $TrafficManagerProfile-Variablen.

Mit dem zweiten Befehl wird der Endpunkt im Profil des Datenverkehrs-Managers aktualisiert, der in $TrafficManagerProfile gespeichert ist.
Der Endpunkt hat den Domänennamen ContosoApp02.cloudapp.net.
Der Befehl gibt auch den Status, den Typ, die Gewichtung und die Position des Endpunkts an.
Der Befehl übergibt das geänderte Profil an das Cmdlet " **Satz-AzureTrafficManagerProfile** ", um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.

## Parameter

### -Domänenname
Gibt den Domänennamen des zu ändernden Endpunkts an.

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
Mögliche Werte sind die Namen der Azure-Region, wie unter aufgeführt  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .

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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Gibt das Traffic Manager-Profilobjekt an, für das der Endpunkt geändert werden soll.

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

Required: False
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

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


