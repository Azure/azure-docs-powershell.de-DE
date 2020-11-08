---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006200"
---
# New-AzureRemoteAppVNet

## Synopsis
Erstellt ein virtuelles Azure RemoteApp-Netzwerk.

## Syntax

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureRemoteAppVNet** wird ein virtuelles Azure RemoteApp-Netzwerk erstellt.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Netzwerks
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

Dieser Befehl erstellt ein virtuelles Netzwerk mit dem Namen ContosoVNet.

Wenn Sie den Status des Vorgangs ermitteln möchten, verwenden Sie das Cmdlet **Get-AzureRemoteAppOperationResult** mit der nach Verfolgungs-ID, die dieses Cmdlet zurückgibt.

## Parameter

### -DnsServerIpAddress
Gibt ein Array der IPv4-Adressen der DNS-Server an.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Gatewaytype
Gibt den Typ des zu verwendenden Gateway-Routings an.
Die zulässigen Werte für diesen Parameter sind: StaticRouting oder DynamicRouting.

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LocalNetworkAddressSpace
Gibt ein Array von Zeichenfolgen an, mit denen der lokale Netzwerk Adressraum in der CIDR-Notation (classly InterDomain Routing) angegeben wird.
Dieser Adressraum darf sich nicht mit dem virtuellen Netzwerk Adressraum überlappen, den der *VirtualNetworkAddressSpace* -Parameter angibt.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort an, an dem das virtuelle Netzwerk erstellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -VirtualNetworkAddressSpace
Gibt ein Array von Zeichenfolgen an, die den virtuellen Netzwerk Adressraum in der CIDR-Notation angeben.
Dieser muss sich im privaten IP-Adressbereich befinden und kann sich nicht mit dem lokalen Netzwerk Adressraum überlappen, der vom *LocalNetworkAddressSpace* -Parameter angegeben wird.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VNetName
Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnDeviceIpAddress
Gibt die Adresse des VPN-Geräts (virtuelles privates Netzwerk) an.
Dies muss eine öffentlich zugängliche Adresse sein.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRemoteAppOperationResult](./Get-AzureRemoteAppOperationResult.md)

[Get-AzureRemoteAppVNet](./Get-AzureRemoteAppVNet.md)

[Remove-AzureRemoteAppVNet](./Remove-AzureRemoteAppVNet.md)

[Satz-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


