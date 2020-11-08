---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005767"
---
# Get-AzureStorSimpleFailoverVolumeContainers

## Synopsis
Ruft die Volumen Container Gruppen für das Geräte Failover ab.

## Syntax

### IdentifyById
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleFailoverVolumeContainers** " Ruft die Volumen Container Gruppen für das Geräte Failover ab.
Übergeben Sie eine einzelne **VolumeContainer** -Gruppe oder ein Array von **VolumeContainer** -Gruppen an das Cmdlet **Start-AzureStorSimpleDeviceFailover** .
Für Failover können nur Gruppen mit dem Wert $true für die **IsDCGroupEligibleForDR** -Eigenschaft ausgewählt werden.

## Beispiele

### Beispiel 1: Abrufen von Failover-Volumen Containern
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

Dieser Befehl ruft Failover-Volumen Container ab.
Für das Geräte Failover können nur die DCGroups verwendet werden, die den Wert $true für die **IsDCGroupEligibleForDR** -Eigenschaft aufweisen.

## Parameter

### -Geräte-Nr
Gibt die Instanz-ID des StorSimple-Geräts an, auf dem das Cmdlet ausgeführt werden soll.

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
Gibt den Namen des StorSimple-Geräts an, auf dem das Cmdlet ausgeführt werden soll.

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

## Ausgaben

### IList\<DataContainerGroup\>
Dieses Cmdlet gibt eine Liste von **VolumeContainer** -Gruppen zurück.

## Notizen

## Verwandte Links

[Anfang-AzureStorSimpleDeviceFailoverJob](./Start-AzureStorSimpleDeviceFailoverJob.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


