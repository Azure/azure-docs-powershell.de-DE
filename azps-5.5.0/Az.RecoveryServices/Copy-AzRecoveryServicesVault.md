---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: e456ae28bec5f5421dad9c58bc5afb58c4d0d250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169340"
---
# Copy-AzRecoveryServicesVault

## SYNOPSIS
Kopiert Daten aus einem Tresor in einer Region in einen Tresor in einer anderen Region.

## SYNTAX

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Copy-AzRecoveryServicesVault"** kopiert Daten aus einem Tresor in einer Region in einen Tresor in einer anderen Region. Derzeit wird nur das Verschieben von Daten auf Tresorebene unterstützt.

## BEISPIELE

### Beispiel 1: Kopieren von Daten aus Tresor1 in Tresor2
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

Die ersten beiden Cmdlets rufen den Wiederherstellungsdiensttresor ab – Tresor1 bzw. Tresor2.
Der zweite Befehl löst eine vollständige Datenverwaltung vom Tresor1 in den Tresor2 aus. 

### Beispiel 2: Kopieren von Daten aus Tresor1 in Tresor2 mit nur fehlgeschlagenen Elementen
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

Die ersten beiden Cmdlets rufen den Wiederherstellungsdiensttresor ab – Tresor1 bzw. Tresor2.
Der zweite Befehl löst eine Teildatenauslösung aus, die nur die Elemente enthält, die bei vorherigen Verschiebevorgängen nicht ausgeführt wurden.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt den Datendatenübertragungsvorgang (verhindert ein Bestätigungsdialogfeld), ohne eine Bestätigung für den Speicherredundanztyp des Zieltresor an bitten zu müssen. Dieser Parameter ist optional. 

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

### -RetryOnlyFailed
Wechseln Sie den Parameter, um das Verschieben von Daten nur für Container im Quelltresor auszuprobieren, die noch nicht verschoben wurden.

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

### -SourceVault
Das zu verschobende Quelltresorobjekt.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TargetVault
Das Zieltresorobjekt, in das die Daten verschoben werden müssen.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
