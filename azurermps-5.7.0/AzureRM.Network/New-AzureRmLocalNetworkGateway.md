---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 6db2d9defaed434aa74f64d6f13af4f029edf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662936"
---
# New-AzureRmLocalNetworkGateway

## Synopsis
Erstellt ein lokales Netzwerk Gateway

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.

Das Cmdlet **New-AzureRmLocalNetworkGateway** erstellt das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf dem Namen, dem Ressourcengruppennamen, dem Speicherort und der IP-Adresse des Gateways sowie dem Adresspräfix des lokalen Netzwerks, das eine Verbindung zu Azure herstellt.

## Beispiele

### 1: Erstellen eines lokalen Netzwerkgateways
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

Erstellt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" an der Position "West US" mit der IP-Adresse "23.99.221.164" und dem Adresspräfix "10.5.51.0/24" auf-Prem.

## Parameter

### -AddressPrefix
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ASN
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BgpPeeringAddress
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayIpAddress
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
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

### -Name
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PeerWeight
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, zu der das lokale Netzwerkgateway gehört.

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

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway

## Notizen

## Verwandte Links

[Get-AzureRmLocalNetworkGateway](./Get-AzureRmLocalNetworkGateway.md)

[Remove-AzureRmLocalNetworkGateway](./Remove-AzureRmLocalNetworkGateway.md)

[Satz-AzureRmLocalNetworkGateway](./Set-AzureRmLocalNetworkGateway.md)
