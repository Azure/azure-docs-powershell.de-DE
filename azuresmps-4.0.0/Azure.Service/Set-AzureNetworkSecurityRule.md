---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006006"
---
# Set-AzureNetworkSecurityRule

## Synopsis
Fügt eine Netzwerk Sicherheitsregel in einer Netzwerksicherheitsgruppe hinzu oder ändert diese.

## Syntax

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureNetworkSecurityRule** " fügt eine Azure Network Security-Regel in einer Netzwerksicherheitsgruppe hinzu oder ändert diese.

## Beispiele

## Parameter

### – Aktion
Gibt die Aktion für eine Netzwerk Sicherheitsregel an.
Gültige Werte sind: allow und Deny.

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

### -DestinationAddressPrefix
Gibt die CIDR-Adresse (classlos InterDomain Routing) des Ziel-IP-Bereichs für die Netzwerk Sicherheitsregel an.
Ein Sternchen (*) gibt eine beliebige IP-Adresse an.

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

### -DestinationPortRange
Gibt einen Ziel Portbereich für die Netzwerk Sicherheitsregel an.
Gültige Werte bestehen aus ganzen Zahlen von 0 bis 65535.
Sie können einen einzelnen Wert angeben oder einen Bereich im Format LowerNumber-HigherNumber angeben.
Ein Bindestrich trennt die beiden Werte.

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
Gibt den Namen für die Netzwerk Sicherheitsregel an, die von diesem Cmdlet hinzugefügt oder geändert wird.

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

### -NetworkSecurityGroup
Gibt die Netzwerksicherheitsgruppe an, die von diesem Cmdlet geändert wird.
Verwenden Sie das Get-AzureNetworkSecurityGroup-Cmdlet, um ein **INetworkSecurityGroup** -Objekt zu erhalten.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Priorität
Gibt die Priorität für die Netzwerk Sicherheitsregel an.
Gültige Werte sind: ganze Zahlen von 100 bis 4096.

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

### -Protokoll
Gibt das Protokoll für die Netzwerk Sicherheitsregel an.
Gültige Werte sind: 

- TCP 
- UDP 
- *

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

### -SourceAddressPrefix
Gibt die CIDR-Adresse des Quell-IP-Bereichs für die Netzwerk Sicherheitsregel an.
Ein Sternchen (*) gibt eine beliebige IP-Adresse an.

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

### -SourcePortRange
Gibt einen Quellportbereich für die Netzwerk Sicherheitsregel an.
Gültige Werte bestehen aus ganzen Zahlen von 0 bis 65535.
Sie können einen einzelnen Wert angeben oder einen Bereich im Format LowerNumber-HigherNumber angeben.
Ein Bindestrich trennt die beiden Werte.

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

### -Typ
Gibt den Verbindungstyp für die Netzwerk Sicherheitsregel an.
Gültige Werte sind: ein-und ausgehende Daten.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


