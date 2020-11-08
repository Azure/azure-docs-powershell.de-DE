---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006181"
---
# New-AzureSiteRecoveryStorageMapping

## Synopsis
Erstellt eine Zuordnung zwischen einem Azure-Speicherobjekt und einem Speicherobjekt für die Wiederherstellung.

## Syntax

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureSiteRecoveryStorageMapping** erstellt eine Zuordnung zwischen einem Azure Azure Site Recovery Managed primäres Azure-Speicherobjekt und einem Speicherobjekt für die Wiederherstellung.

## Beispiele

### Beispiel 1: Erstellen einer Zuordnung zwischen einem Speicherobjekt und einem Speicherobjekt für die Wiederherstellung
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.
Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.

Der zweite Befehl ruft den Standort Wiederherstellungs Speicher für den ersten Server im $Servers-Array ab und speichert ihn dann im $Storages.

Der endgültige Befehl erstellt eine Zuordnung zwischen dem primären Netzwerk und dem Wiederherstellungs Netzwerk.
Der Befehl gibt das primäre Speicherobjekt als erstes Element von $Storages an.
Der Befehl gibt das Speicherobjekt für die Wiederherstellung als zweites Element von $Storages an.

## Parameter

### -PrimaryStorage
Gibt den primären Speicher an, der dem Wiederherstellungs Speicher zugeordnet werden soll.
Verwenden Sie das Get-AzureSiteRecoveryStorage-Cmdlet, um ein **ASRStorage** -Objekt zu erhalten.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -RecoveryStorage
Gibt das Speicherobjekt für die Wiederherstellung an.
Dieses Cmdlet ordnet das primäre Speicherobjekt dem Speicherobjekt zu, das dieser Parameter angibt.
Verwenden **Sie Get-AzureSiteRecoveryStorage** , um ein **ASRStorage** -Objekt zu erhalten.

```yaml
Type: ASRStorage
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

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


