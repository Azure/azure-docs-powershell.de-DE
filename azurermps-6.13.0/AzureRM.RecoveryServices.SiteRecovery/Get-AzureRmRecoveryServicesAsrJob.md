---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: f79bc9e32ab179c10c09f3780a591182ea1d630b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663112"
---
# Get-AzureRmRecoveryServicesAsrJob

## Synopsis
Ruft die Details des angegebenen ASR-Auftrags oder der Liste der zuletzt verwendeten ASR-Aufträge im Recovery Services Vault ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByParam (Standard)
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByObject
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRecoveryServicesAsrJob** " ruft Azure Site Recovery-Aufträge ab.
Sie können dieses Cmdlet verwenden, um die ASR-Aufträge im Speicher für Wiederherstellungsdienste anzuzeigen.

## Beispiele

### Beispiel 1
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Gibt alle Aufträge für ein bestimmtes ASR-Objekt zurück (Verweis auf das ASR-Objekt wie repliziertes Element oder Wiederherstellungsplan anhand seiner ID). 

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
Gibt die Endzeit für die Aufträge an.
Dieses Cmdlet ruft alle Aufträge ab, die vor der angegebenen Zeit gestartet wurden.
Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt für diesen Parameter abzurufen.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Gibt das ASR-Auftragsobjekt an, für das aktualisierte Details abgerufen werden sollen.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Geben Sie den ASR-Auftrag nach Name an.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Startzeit
Gibt die Startzeit für die Aufträge an.
Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bundesland
Gibt den Status für einen ASR-Auftrag an.
Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- NotStarted
- InProgress
- Erfolgreich
- Anderen
- Fehlgeschlagen
- Storniert
- Ausgesetzt

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Gibt die ID des Objekts an. Wird verwendet, um nach Aufträgen für das angegebene Objekt zu suchen.

```yaml
Type: System.String
Parameter Sets: ByParam
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Ausgaben

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## Notizen

## Verwandte Links

[Neustart-AzureRmRecoveryServicesAsrJob](./Restart-AzureRmRecoveryServicesAsrJob.md)

[Lebenslauf-AzureRmRecoveryServicesAsrJob](./Resume-AzureRmRecoveryServicesAsrJob.md)

[Stopp-AzureRmRecoveryServicesAsrJob](./Stop-AzureRmRecoveryServicesAsrJob.md)
