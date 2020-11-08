---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005721"
---
# New-AzureStorSimpleNetworkConfig

## Synopsis
Bereitet ein Netzwerk Konfigurationsobjekt vor.

## Syntax

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureStorSimpleNetworkConfig** wird ein Netzwerk Konfigurationsobjekt für die Übergabe an das Cmdlet " **Satz-AzureStorSimpleDevice** " vorbereitet.
Setzen Sie den *Controller0IPAddress* -Parameter und den *Controller1IPAddress* -Parameter nur auf der Daten0-Schnittstelle.
Daten0 unterstützt nur drei Einstellungen: *Controller0IPAddress* , *Controller1IPAdress* und *EnableIscsi*.

## Beispiele

### Beispiel 1: Konfigurieren einer Daten0-Schnittstelle
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

Dieser Befehl erstellt die Netzwerkkonfiguration für die Daten0-Schnittstelle.
Mit diesem Befehl werden die *Controller0IPv4Address* -, *Controller1IPv4Address* -und *EnableIscsi* -Parameter angegeben.
Dieses Cmdlet kann Daten0 nur für diese drei Parameter konfigurieren.

### Beispiel 2: Konfigurieren einer anderen Schnittstelle als Daten0
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

Dieser Befehl konfiguriert die data1-Schnittstelle.

### Beispiel 3: Ändern einer Konfiguration für ein Gerät
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

Der erste Befehl erstellt eine Netzwerkkonfiguration für die Daten0-Schnittstelle.
Mit diesem Befehl werden die *Controller0IPv4Address* -, *Controller1IPv4Address* -und *EnableIscsi* -Parameter angegeben.
Der Befehl speichert das Ergebnis in der Variablen $NetworkConfigData 0.

Der zweite Befehl verwendet das Cmdlet " **Get-AzureStorSimpleDevice** " und das Cmdlet " **Where-Object** Core" zum Abrufen eines Online StorSimple-Geräts und speichert es dann in der $OnlineDevice-Variablen.

Der endgültige Befehl ändert die Konfiguration für das Gerät, das über die angegebene Geräte-ID verfügt, mithilfe des Cmdlets " **festgelegt-AzureStorSimpleDevice** ".
Der Befehl verwendet das Configuration-Objekt, das das aktuelle Cmdlet im ersten Befehl erstellt hat.

## Parameter

### -Controller0IPv4Address
Gibt die IPv4-Adresse für Controller 0 an.
Geben Sie diesen Parameter nur für die Daten0-Schnittstelle an.

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

### -Controller1IPv4Address
Gibt die IPv4-Adresse für Controller 1 an.
Geben Sie diesen Parameter nur für die Daten0-Schnittstelle an.

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

### -EnableCloud
Gibt an, ob die Benutzeroberfläche in der Cloud aktiviert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableIscsi
Gibt an, ob Internet SCSI (iSCSI) für die Schnittstelle aktiviert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterfaceAlias
Gibt den Schnittstellen Alias der Schnittstelle an, für die dieses Cmdlet Einstellungen bereitstellt.
Gültige Werte sind von Daten0 bis Daten5.

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

### -IPv4Address
Gibt die IPv4-Adresse für die Schnittstelle an.

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

### -IPv4Gateway
Gibt die IPv4-Adresse eines Gateways an.

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

### -IPv4Netmask
Gibt die IPv4-Netzmaske für die Schnittstelle an.

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

### -IPv6Gateway
Gibt das IPv6-Gateway für die Schnittstelle an.

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

### -IPv6Prefix
Gibt das IPv6-Präfix für die Schnittstelle an.

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

### -Profil
Gibt ein Azure-Profil an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### NetworkConfig
Dieses Cmdlet gibt ein NetworkConfig-Objekt zurück, das die folgenden Eigenschaften enthält: 

- **IsIscsiEnabled** ( **boolescher Wert** ) 
- **IsCloudEnabled** ( **boolescher Wert** )
- **Controller0IPv4Address** ( **IPAddress** ) 
- **Controller1IPv4Address** ( **IPAddress** ) 
- **IPv6Gateway** ( **IPAddress** ) 
- **IPv4Gateway** ( **IPAddress** ) 
- **IPv4Address** ( **IPAddress** ) 
- **IPv6Prefix** ( **Zeichenfolge** )
- **IPv4Netmask** ( **IPAddress** ) 
- **InterfaceAlias** ( **netinterface-Schnittstelle** )

## Notizen

## Verwandte Links

[Satz-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)

[Get-AzureStorSimpleDevice](./Get-AzureStorSimpleDevice.md)


