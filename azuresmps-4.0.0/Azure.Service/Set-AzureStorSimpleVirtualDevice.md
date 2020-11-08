---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005641"
---
# Set-AzureStorSimpleVirtualDevice

## Synopsis
Erstellt oder aktualisiert die Gerätekonfiguration eines virtuellen StorSimple-Geräts.

## Syntax

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureStorSimpleVirtualDevice** " erstellt oder aktualisiert die Gerätekonfiguration eines virtuellen Azure StorSimple-Geräts.

## Beispiele

### Beispiel 1: Aktualisieren eines virtuellen Geräts
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

Der erste Befehl verwendet die **System. TimeZoneInfo** .NET-Klasse und die Standardsyntax, um Pacific Standard Time Zone abzurufen, und speichert dieses Objekt in der $TimeZoneInfo-Variablen.

Der zweite Befehl aktualisiert das Gerät mit dem Namen Contoso23, um die in $TimeZoneInfo angegebene Zeitzone zu verwenden.
Für den Zugriff auf die Konfiguration des virtuellen Geräts benötigt der Befehl den geheimen Schlüssel.

### Beispiel 2: Aktualisieren eines virtuellen Geräts mithilfe des Pipelineoperators
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

Dieser Befehl aktualisiert das Gerät mit dem Namen Contoso23, um die vom Befehl erstellte Zeitzone zu verwenden.
Für den Zugriff auf die Konfiguration des virtuellen Geräts benötigt der Befehl den geheimen Schlüssel.
Dieser Befehl funktioniert auf die gleiche Weise wie im vorherigen Beispiel, mit der Ausnahme, dass er die Zeitzone mithilfe des Pipelineoperators an das aktuelle Cmdlet übergibt.

## Parameter

### -Administrator Password
Gibt das Administratorkennwort des virtuellen Geräts an, das konfiguriert werden soll.

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

### -DeviceName
Gibt den Namen des virtuellen Geräts an, das konfiguriert werden soll.

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

### -SecretKey
Gibt einen Dienst Verschlüsselungsschlüssel für das virtuelle Gerät an.
Dieser Schlüssel wird generiert, wenn das erste physische Gerät bei einer Ressource registriert wird.

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

### -SnapshotManagerPassword
Gibt das Kennwort des Snapshot-Managers an.

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

### TimeZoneInfo
Sie können ein **TimeZoneInfo** -Objekt an dieses Cmdlet übergeben.

## Ausgaben

### DeviceJobDetails
Dieses Cmdlet gibt aktualisierte Gerätedetails für das virtuelle Gerät zurück.

## Notizen

## Verwandte Links

[Neu – AzureStorSimpleVirtualDevice](./New-AzureStorSimpleVirtualDevice.md)

[Satz-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)


