---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 8f9f16b0f5ea4b36cfe8247eed2ed6e88ecd4853
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929867"
---
# Get-AzRecoveryServicesAsrJob

## SYNOPSIS
Ruft die Details des angegebenen ASR-Auftrags oder die Liste der zuletzt verwendeten ASR-Aufträge im Wiederherstellungsdienste-Tresor ab.

## SYNTAX

### ByParam (Standard)
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzRecoveryServicesAsrJob-Cmdlet** ruft Azure-Websitewiederherstellungsaufträge ab.
Sie können dieses Cmdlet verwenden, um die ASR-Aufträge im Recovery Services-Tresor anzeigen.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Gibt alle Aufträge für ein bestimmtes ASR-Objekt zurück (verweisen Sie auf das ASR-Objekt, z. B. repliziertes Element oder den Wiederherstellungsplan nach seiner ID.) 

### Beispiel 2

Ruft die Details des angegebenen ASR-Auftrags oder die Liste der zuletzt verwendeten ASR-Aufträge im Wiederherstellungsdienste-Tresor ab. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrJob -Job $Job
```

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
Gibt die Endzeit für die Aufträge an.
Dieses Cmdlet ruft alle Aufträge ab, die vor dem angegebenen Zeitpunkt begonnen haben.
Um ein **DateTime-Objekt** für diesen Parameter zu erhalten, verwenden Sie das Get-Date Cmdlet.
Weitere Informationen finden Sie unter `Get-Help Get-Date` .

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
Gibt das ASR-Auftragsobjekt an, für das aktualisierte Details angezeigt werden.

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

### -StartTime
Gibt die Startzeit für die Aufträge an.
Dieses Cmdlet ruft alle Aufträge ab, die nach dem angegebenen Zeitpunkt gestartet wurden.

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

### -State
Gibt den Zustand für einen ASR-Auftrag an.
Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.
Die zulässigen Werte für diesen Parameter sind:

- NotStarted
- InProgress
- Erfolgreich
- Sonstige
- Fehlgeschlagen
- Storniert
- Angehalten

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
Gibt die ID des -Objekts an. Wird verwendet, um nach Aufträgen für das angegebene Objekt zu suchen.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## NOTIZEN

## VERWANDTE LINKS

[Restart-AzRecoveryServicesAsrJob](./Restart-AzRecoveryServicesAsrJob.md)

[Resume-AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[Stop-AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
