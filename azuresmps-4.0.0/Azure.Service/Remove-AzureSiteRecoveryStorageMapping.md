---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006315"
---
# Remove-AzureSiteRecoveryStorageMapping

## Synopsis
Entfernt eine Speicherobjekt Zuordnung für einen Standort Wiederherstellungs Tresor.

## Syntax

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureSiteRecoveryStorageMapping** entfernt eine Speicherobjekt Zuordnung für das aktuelle Azure Site Recovery Vault.

## Beispiele

### Beispiel 1: Entfernen der Zuordnung zwischen einem Netzwerk und einem Wiederherstellungs Netzwerk
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.
Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.

Der zweite Befehl ruft die Zuordnung zwischen zwei Speicherobjekten ab und speichert Sie dann in der $StorageMapping Variablen.
Der Befehl gibt den primären Server für die Netzwerkzuordnung als erstes Element von $Servers an.
Der Befehl gibt den Server für das Wiederherstellungs Netzwerk als zweites Element von $Servers an.

Der endgültige Befehl entfernt die Zuordnung in $StorageMapping.

## Parameter

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

### -StorageMapping
Gibt eine Netzwerkzuordnung an.
Verwenden Sie zum Abrufen eines **ASRStorageMapping** das Cmdlet **Get-AzureSiteRecoveryStorage** .

```yaml
Type: ASRStorageMapping
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

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)


