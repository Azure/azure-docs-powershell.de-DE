---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005789"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## Synopsis
Downloadet einen Azure Site Recovery Plan im XML-Format.

## Syntax

### ByRPObject (Standard)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSiteRecoveryRecoveryPlanFile** " downloadet einen Azure Site Recovery Plan im XML-Format.
Sie können diese Datei verwenden, um den Wiederherstellungsplan zu aktualisieren und dann auf den Website Wiederherstellungsserver hochzuladen.

Ein Wiederherstellungsplan sammelt virtuelle Computer in einer Gruppe, um Failover und Wiederherstellung zu verwenden.

## Beispiele

### Beispiel 1: Abrufen einer Wiederherstellungsplan Datei
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Dieser Befehl verwendet das Cmdlet " **Get-AzureSiteRecoveryRecoveryPlan** ", um den Wiederherstellungsplan abzurufen, und speichert ihn dann in der $RecoveryPlan-Variablen.

Der zweite Befehl verwendet das **GetAzureSiteRecoveryRecoveryPlanFile** -Cmdlet, um die XML-Datei für den Website Wiederherstellungsplan in $RecoveryPlan abzurufen.
Der Befehl speichert die XML-Datei unter dem angegebenen Pfad.

## Parameter

### -ID
Gibt die ID des abzurufenden Wiederherstellungsplans an.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Gibt den vollständigen Pfad zum Speichern der XML-Wiederherstellungsplan-Datei an.

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

### -RecoveryPlan
Gibt ein **ASRRecoveryPlan** -Objekt an, aus dem der Wiederherstellungsplan abgerufen werden soll.
Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryRecoveryPlan** , um ein **ASRRecoveryPlan** -Objekt abzurufen.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
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

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


