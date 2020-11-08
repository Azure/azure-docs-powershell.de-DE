---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006029"
---
# Set-AzureRoute

## Synopsis
Erstellt eine Route in einer Route-Tabelle.

## Syntax

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRoute** " erstellt eine Route in einer Route-Tabelle.
Die neue Route wird fast sofort auf den virtuellen Computern wirksam, die der Route-Tabelle zugeordnet sind.

## Beispiele

### Beispiel 1: Hinzufügen einer virtuellen Appliance-Route für den nächsten Hop
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

Dieser Befehl erstellt eine Routentabelle mit dem Namen ApplianceRouteTable an der angegebenen Position.
Der Befehl übergibt diese Routingtabelle an das aktuelle Cmdlet.
Das aktuelle Cmdlet fügt eine Route mit dem Namen "ApplianceRoute03" hinzu, bei der es sich um einen VirtualAppliance nächsten Hop-Typ handelt.
Der Befehl gibt die IP-Adresse des nächsten Hop und das Adresspräfix für die Route an.

### Beispiel 2: Hinzufügen einer Internet Route für den nächsten Hop
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

Dieser Befehl ruft eine Routentabelle mit dem Namen ApplianceRouteTable ab.
Der Befehl übergibt diese Routingtabelle an das aktuelle Cmdlet.
Das aktuelle Cmdlet fügt eine Route mit dem Namen "InternetRoute" hinzu, die ein Internet-nächster Hop-Typ ist.
Der Befehl gibt das Adresspräfix für die Route an.

## Parameter

### -AddressPrefix
Gibt ein Adresspräfix für die neue Route an.

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

### -NextHopIpAddress
Gibt die IP-Adresse der Appliance an, bei der es sich um den nächsten Hop für Datenverkehr handelt, der diese Route verwendet.
Geben Sie diesen Wert nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.

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

### -NextHopType
Gibt den Typ des nächsten Hop für Datenverkehr an, der diese Route verwendet.
Gültige Werte sind: 

- VPNGateway
- VNETLocal
- Internet
- VirtualAppliance
- NULL

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

### -Routename
Gibt einen Namen für die neue Route an, die von diesem Cmdlet hinzugefügt wird.

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

### -Routel
Gibt die Routingtabelle an, der das Cmdlet die neue Route hinzufügt.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Remove-AzureRoute](./Remove-AzureRoute.md)


