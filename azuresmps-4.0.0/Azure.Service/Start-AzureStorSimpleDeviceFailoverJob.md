---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005982"
---
# Start-AzureStorSimpleDeviceFailoverJob

## Synopsis
Initiiert einen Failover-Vorgang von Volumen Container Gruppen.

## Syntax

### Leer (Standard)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureStorSimpleDeviceFailoverJob** initiiert einen Failovervorgang einer oder mehrerer Volumen Container Gruppen von einem Gerät zu einem anderen.

## Beispiele

### Beispiel 1: Starten eines Failover-Auftrags für ein benanntes Gerät und benanntes Zielgerät
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Dieser Befehl ruft die Failover-Volumen Container für das Gerät mit dem Namen ChewD_App7 mit dem Cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** ab.
Der Befehl übergibt die Ergebnisse an das Cmdlet **Where-Object** , in dem die Container mit einem anderen Wert als $true für die **IsDCGroupEligibleForDR** -Eigenschaft gelöscht werden.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Where-Object` .
Das aktuelle Cmdlet startet Failover-Aufträge für die restlichen Failover-Volumen Container.
Der Befehl gibt den Gerätenamen und den Namen des Zielgeräts an.
Der Befehl gibt die Instanz-ID des Auftrags zurück, den das Cmdlet startet.

### Beispiel 2: Starten eines Failover-Auftrags für ein Gerät und Zielgerät, angegeben durch die ID
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Dieser Befehl ruft die Failover-Volumen Container für das Gerät mit dem Namen ChewD_App7 mithilfe von **Get-AzureStorSimpleFailoverVolumeContainers** ab.
Der Befehl übergibt die Ergebnisse an **Where-Object** , wodurch diese mit einem anderen Wert als $true für die **IsDCGroupEligibleForDR** -Eigenschaft gelöscht werden.
Das Cmdlet übergibt die Ergebnisse an das Cmdlet **"Select-Object"** , das das erste Objekt auswählt, das an das aktuelle Cmdlet übergeben werden soll.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Select-Object` .
Das aktuelle Cmdlet startet Failover-Aufträge für den ausgewählten Failover-Volumen Container.
Der Befehl gibt die Geräte-ID und die Zielgeräte-ID an.
Der Befehl gibt die Instanz-ID des Auftrags zurück, den das Cmdlet startet.

## Parameter

### -Geräte-Nr
Gibt die Instanz-ID des StorSimple-Geräts an, auf dem die Volumen Container Gruppen vorhanden sind.

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
Gibt den Namen des StorSimple-Geräts an, auf dem die Volumen Container Gruppen vorhanden sind.

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

### -TargetDeviceId
Gibt die Instanz-ID des StorSimple-Geräts an, für das dieses Cmdlet einen Failover für die Volumen Container Gruppen durchführt.

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

### -TargetDeviceName
Gibt den Namen des StorSimple-Geräts an, für das dieses Cmdlet einen Failover der Volumen Container Gruppen durchführt.

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

### -VolumecontainerGroups
Gibt die Liste der Volumen Container Gruppen an, für die dieses Cmdlet einen Failover zu einem anderen Gerät durchführt.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
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

### Liste\<DataContainerGroup\>
Sie können eine Liste mit Volumen Container Gruppen an dieses Cmdlet übergeben.

## Ausgaben

### Zeichenfolge

## Notizen

## Verwandte Links

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


