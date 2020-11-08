---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005930"
---
# Add-AzureInternalLoadBalancer

## Synopsis
Fügt einem Azure-Dienst ein internes Lastenausgleichsmodul hinzu.

## Syntax

### ServiceAndSlot (Standard)
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### SubnetNameOnly
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### SubnetNameAndIP
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzureInternalLoadBalancer** fügt einem Azure-Dienst eine interne Load Balancer-Konfiguration hinzu.
Bei einem virtuellen Netzwerk können Sie ein Subnetz oder die IP-Adresse des internen Load Balancer angeben.

## Beispiele

### Beispiel 1: Hinzufügen eines internen Load Balancer
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

Dieser Befehl fügt dem Dienst mit dem Namen ContosoWebsite01 ein internes Lastenausgleichsmodul mit dem Namen "ContosoILB" hinzu.

### Beispiel 2: Hinzufügen eines internen Lastenausgleichs für ein angegebenes Subnetz
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

Dieser Befehl fügt dem Dienst mit dem Namen ContosoWebsite01 ein internes Lastenausgleichsmodul mit dem Namen "ContosoILB" hinzu.
Der Befehl gibt das Subnetz mit dem Namen FrontEndSubnet an.

### Beispiel 3: Hinzufügen eines internen Lastenausgleichs für ein angegebenes Subnetz und eine Adresse
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

Dieser Befehl fügt dem Dienst mit dem Namen ContosoWebsite01 ein internes Lastenausgleichsmodul mit dem Namen "ContosoILB" hinzu.
Der Befehl gibt das Subnetz mit dem Namen FrontEndSubnet und die statische Adresse des virtuellen Netzwerks an.

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InternalLoadBalancerName
Gibt den Namen des internen Lastenausgleichs an, den dieses Cmdlet hinzufügt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ServiceName
Gibt den Namen des Diensts an, dem dieses Cmdlet ein internes Lastenausgleichsmodul hinzufügt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StaticVNetIPAddress
Gibt die IP-Adresse des virtuellen Netzwerks für ein internes Lastenausgleichsmodul an, das dieses Cmdlet hinzufügt.

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
Gibt den Namen des Subnets für ein internes Lastenausgleichsmodul an, das von diesem Cmdlet hinzugefügt wird.

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext

## Notizen

## Verwandte Links

[Get-AzureInternalLoadBalancer](./Get-AzureInternalLoadBalancer.md)

[Neu – AzureInternalLoadBalancerConfig](./New-AzureInternalLoadBalancerConfig.md)

[Remove-AzureInternalLoadBalancer](./Remove-AzureInternalLoadBalancer.md)

[Satz-AzureInternalLoadBalancer](./Set-AzureInternalLoadBalancer.md)


