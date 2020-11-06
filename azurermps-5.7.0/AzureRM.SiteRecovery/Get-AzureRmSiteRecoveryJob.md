---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498781"
---
# Get-AzureRmSiteRecoveryJob

## Synopsis
Ruft die Vorgangsinformationen für den aktuellen Standort Wiederherstellungs Tresor ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByParam (Standard)
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSiteRecoveryJob** " ruft Azure Site Recovery-Aufträge ab.
Sie können dieses Cmdlet verwenden, um die Vorgangsinformationen für das aktuelle Standort Wiederherstellungs Depot anzuzeigen.

## Beispiele

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
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
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Gibt den Standort Wiederherstellungsauftrag an.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt einen eindeutigen Namen an, der den Auftrag identifiziert.

```yaml
Type: String
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
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bundesland
Gibt den Eingabestatus für einen Standort Wiederherstellungsauftrag an.
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
Type: String
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
Gibt die ID des Objekts an, das für den Auftrag vorgesehen ist.

```yaml
Type: String
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

### ASRJob
Der Parameter ' Job ' akzeptiert den Wert vom Typ ' ASRJob ' aus der Pipeline.

## Ausgaben

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]

## Notizen

## Verwandte Links

[Neustart-AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[Lebenslauf-AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[Stopp-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
