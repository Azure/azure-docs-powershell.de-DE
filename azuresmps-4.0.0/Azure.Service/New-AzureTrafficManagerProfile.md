---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006408"
---
# New-AzureTrafficManagerProfile

## Synopsis
Erstellt ein Traffic Manager-Profil.

## Syntax

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureTrafficManagerProfile** erstellt ein Microsoft Azure Traffic Manager-Profil.

Nachdem Sie ein Profil erstellt haben, in dem Sie den *LoadBalancingMethod* -Wert auf "Failover" festgelegt haben, können Sie die Failover-Reihenfolge der Endpunkte ermitteln, die Sie mit dem Add-AzureTrafficManagerEndpoint-Cmdlet zu Ihrem Profil hinzufügen.
Weitere Informationen finden Sie unten im Beispiel 2.

## Beispiele

### Beispiel 1: Erstellen eines Traffic Manager-Profils
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Mit diesem Befehl wird in der angegebenen Datenverkehrs-Manager-Domäne mit einer Round-Robin-Lastenausgleichsmethode, einem TTL-Wert von 30 Sekunden, dem http-Überwachungsprotokoll, dem Überwachungs-Port 80 und dem angegebenen Pfad ein Traffic Manager-Profil mit dem Namen "myprofil" erstellt.

### Beispiel 2: Neuanordnung von Endpunkten in der gewünschten Failover-Reihenfolge
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

In diesem Beispiel werden die zu myProfile hinzugefügten Endpunkte der gewünschten Failover-Reihenfolge neu angeordnet.

Der erste Befehl ruft das Traffic Manager-Profilobjekt mit dem Namen myProfile ab und speichert das Objekt in der $Profile Variablen.

Der zweite Befehl ordnet die Endpunkte aus dem Array Endpunkte erneut an die Reihenfolge an, in der ein Failover erfolgen soll.

Mit dem letzten Befehl wird das in $Profile gespeicherte Traffic Manager-Profil mit der neuen Endpunkt Reihenfolge aktualisiert.

## Parameter

### -Domänenname
Gibt den Domänennamen des Traffic Manager-Profils an.
Dies muss eine Unterdomäne von Trafficmanager.net sein.

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

### -LoadBalancingMethod
Gibt die Methode zum Lastenausgleich an, mit der die Verbindung verteilt werden soll.
Gültige Werte sind: 

- Leistung
- Failover
- Roundrobin

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

### -MonitorPort
Gibt den Port an, der zum Überwachen der Endpunkt Integrität verwendet wird.
Gültige Werte sind ganzzahlige Werte, die größer als 0 und kleiner oder gleich 65.535 sind.

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

### -MonitorProtocol
Gibt das Protokoll an, das zum Überwachen der Endpunkt Integrität verwendet werden soll.
Gültige Werte sind: 

- Http

- HTTPS

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

### -MonitorRelativePath
Gibt den Pfad relativ zum Endpunkt Domänennamen an, um den Integritätsstatus zu überprüfen.
Der Pfad muss die folgenden Einschränkungen erfüllen: 

- Der Pfad muss zwischen 1 und 1000 Zeichen lang sein.

- Sie muss mit einem Schrägstrich beginnen.

- Sie darf keine XML-Elemente enthalten \<\> .

- Sie darf keine doppelten Schrägstriche//aufweisen.

- Sie darf keine ungültigen HTML-Escape-Zeichen enthalten.
Beispiel:% XY.

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

### -Name
Gibt den Namen des zu erstellenden Traffic Manager-Profils an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -TTL
Gibt die DNS-Gültigkeitsdauer (Time-to-Live, TTL) an, die die lokalen DNS-Konfliktlöser darüber informiert, wie lange DNS-Einträge zwischengespeichert werden.
Gültige Werte sind ganze Zahlen von 30 bis 999.999.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition
Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt.

## Notizen

## Verwandte Links

[Deaktivieren-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


