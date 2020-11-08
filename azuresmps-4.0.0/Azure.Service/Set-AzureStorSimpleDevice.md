---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: AE8E6778-1299-4EC7-BFE0-3FB464AA7BB4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7bea5cbf2b5e10c85aaafa43203c207193040464
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005959"
---
# Set-AzureStorSimpleDevice

## Synopsis
Ändert die Gerätekonfiguration für ein Gerät.

## Syntax

### IdentifyByName (Standard)
```
Set-AzureStorSimpleDevice -DeviceName <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### IdentifyById
```
Set-AzureStorSimpleDevice -DeviceId <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureStorSimpleDevice** " ändert die Gerätekonfiguration für ein Gerät.
Wenn Sie ein Gerät zum ersten Mal einrichten, müssen Sie die Parameter *TimeZone* , *SecondaryDnsServer* und *StorSimpleNetworkConfig* angeben.
Sie müssen die Netzwerkkonfiguration für Daten0 mit controller0 und controller1 sowie IP-Adressen einbeziehen.
Es muss mindestens eine Internet-SCSI (iSCSI)-fähige Netzwerkschnittstelle vorhanden sein, um das Gerät zum ersten Mal konfigurieren zu können.

## Beispiele

### Beispiel 1: Ändern der Konfiguration für ein Gerät
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

Der erste Befehl erstellt eine Netzwerkkonfiguration für die Daten0-Schnittstelle.
Mit diesem Befehl werden die *Controller0IPv4Address* -, *Controller1IPv4Address* -und *EnableIscsi* -Parameter angegeben.
Der Befehl speichert das Ergebnis in der Variablen $NetworkConfigData 0.

Der zweite Befehl verwendet die **System. TimeZoneInfo** .NET-Klasse und die Standardsyntax, um Pacific Standard Time Zone abzurufen, und speichert dieses Objekt in der $TimeZoneInfo-Variablen.

Der dritte Befehl verwendet das Cmdlet " **Get-AzureStorSimpleDevice** " und das Cmdlet " **Where-Object** Core" zum Abrufen eines Online StorSimple-Geräts und speichert es dann in der $OnlineDevice-Variablen.

Der endgültige Befehl ändert die Konfiguration für das Gerät, das die angegebene Geräte-ID aufweist.
Der Befehl verwendet das Configuration-Objekt, das das aktuelle Cmdlet im ersten Befehl erstellt hat.
Der Befehl verwendet die in $TimeZoneInfo gespeicherte Zeitzone.

### Beispiel 2: Rohren des Konfigurationsobjekts zum Ändern eines Geräts
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 
VERBOSE: ClientRequestId: fa2f5000-169c-4feb-abbf-23f4b5c837fa_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: fae6a491-919c-44b2-93e0-0c51f202c24b_PS
VERBOSE: ClientRequestId: e1803427-a097-4d58-ab7d-14a4c39fd768_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 9e796c3d-3100-46ab-9a09-0e10c73a296f_PS
VERBOSE: ClientRequestId: 5b4cad96-31f4-4d07-a278-df5af3e06ad4_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 9061f7df-144f-4f30-858c-045d882ca392_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 2ed2fa9b-8459-4cd6-9a61-5fc25ced2815_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

In diesem Beispiel wird die gleiche Konfigurationsaktualisierung wie im ersten Beispiel durchlaufen, mit der Ausnahme, dass der endgültige Befehl das Netzwerk Konfigurationsobjekt mithilfe des Pipelineoperators an das aktuelle Cmdlet übergibt.

### Beispiel 3: Rohren des Zeitzonenobjekts zum Ändern eines Geräts
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: cfc3f3c7-a8b6-462b-96f4-124050b736fe_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 6017b76f-a771-4bf8-901e-14876e0f9962_PS
VERBOSE: ClientRequestId: 59a9275c-9005-4e8a-b68b-efa1e6c27d47_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 08e5142a-b038-4607-8690-0c5a8b948352_PS
VERBOSE: ClientRequestId: 218af244-b8f4-4a4b-817e-8f67e1323f03_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: fbd1f32d-1d74-432e-9dc0-90b46674884a_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 981cb941-252c-4898-ba9f-f19e5b8bcaa4_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

In diesem Beispiel wird die gleiche Konfigurationsaktualisierung wie im ersten Beispiel durchlaufen, mit der Ausnahme, dass der endgültige Befehl das Zeitzonenobjekt mithilfe des Pipelineoperators an das aktuelle Cmdlet übergibt.

## Parameter

### -Geräte-Nr
Gibt die Instanz-ID des StorSimple-Geräts an, das konfiguriert werden soll.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Gibt den Anzeigenamen des StorSimple-Geräts an, das konfiguriert werden soll.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den neuen Anzeigenamen des StorSimple-Geräts an.

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

### -SecondaryDnsServer
Gibt einen sekundären DNS-Server für das StorSimple-Gerät an.

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

### -StorSimpleNetworkConfig
Gibt ein Array von Netzwerk Konfigurationsobjekten für Schnittstellen auf einem Gerät an.
Verwenden Sie das New-AzureStorSimpleNetworkConfig-Cmdlet, um ein **NetworkConfig** -Objekt zu erhalten.

```yaml
Type: NetworkConfig[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TimeZone
Gibt eine Zeitzone für das Gerät an.
Mit der **GetSystemTimeZone ()** -Methode können Sie ein **TimeZoneInfo** -Objekt erstellen.
Mit diesem Befehl wird beispielsweise ein Zeit Zonen Informationsobjekt für die Pazifische Standard Zeit erstellt: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### NetworkConfig, TimeZoneInfo
Sie können ein **NetworkConfig** -Objekt oder eine **TimeZoneInfo** -Pipeline an dieses Cmdlet übergeben.

## Ausgaben

### DeviceDetails
Dieses Cmdlet gibt aktualisierte Gerätedetails für das virtuelle Gerät zurück.

## Notizen

## Verwandte Links

[Neu – AzureStorSimpleNetworkConfig](./New-AzureStorSimpleNetworkConfig.md)

[Satz-AzureStorSimpleVirtualDevice](./Set-AzureStorSimpleVirtualDevice.md)


