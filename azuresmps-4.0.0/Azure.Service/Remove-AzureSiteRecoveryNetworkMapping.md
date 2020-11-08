---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006316"
---
# Remove-AzureSiteRecoveryNetworkMapping

## Synopsis
Entfernt eine Netzwerkzuordnung aus einem Website Wiederherstellungs Speicher.

## Syntax

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureSiteRecoveryNetworkMapping** entfernt eine Netzwerkzuordnung aus dem aktuellen Azure Site Recovery Vault.

## Beispiele

### Beispiel 1: Entfernen der Zuordnung zwischen einem Netzwerk und einem Wiederherstellungs Netzwerk
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.
Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.

Der zweite Befehl ruft die Zuordnung zwischen dem primären Netzwerk und dem Wiederherstellungs Netzwerk ab und speichert ihn dann in der $NetworkMapping Variablen.
Der Befehl gibt den primären Server für die Netzwerkzuordnung als erstes Element von $Servers an.
Der Befehl gibt den Server für das Wiederherstellungs Netzwerk als zweites Element von $Servers an.

Der endgültige Befehl entfernt die Netzwerkzuordnung in $NetworkMapping.

### Beispiel 2: Entfernen der Zuordnung zwischen einem Netzwerk und einem Azure Virtual Machine-Netzwerk
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Das Cmdlet "erster Befehl" Ruft Server für den aktuellen Standort Wiederherstellungs Tresor ab.
Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.

Der zweite Befehl ruft eine Zuordnung zwischen dem primären Netzwerk und einem Azure Virtual Machine-Netzwerk ab und speichert ihn dann in der $NetworkMapping-Variablen.
Der Befehl gibt den primären Server für das Netzwerk als erstes Element $Servers an.
Der Befehl gibt den *Azure* -Parameter an.
Daher ruft der Befehl die Zuordnung zu einem Azure Virtual Machine-Netzwerk ab.

Der endgültige Befehl entfernt die Netzwerkzuordnung in $NetworkMapping.

## Parameter

### -NetworkMapping
Gibt die zu entfernende Netzwerkzuordnung an.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[Neu – AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


