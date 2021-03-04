---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922744"
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
Das **Cmdlet Copy-AzRecoveryServicesVault** kopiert Daten aus einem Tresor in einer Region in einen Tresor in einer anderen Region. Derzeit unterstützen wir nur das Verschieben von Daten auf Tresorebene.

## BEISPIELE

### Beispiel 1: Kopieren von Daten aus dem Tresor1 in den Tresor2
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

Die ersten beiden Cmdlets rufen den Wiederherstellungsdienste-Tresor ab – Tresor1 bzw. Tresor2.
Der zweite Befehl löst einen vollständigen Datensprung von Tresor1 in Tresor2 aus. 

### Beispiel 2: Kopieren von Daten aus Tresor1 in Tresor2 mit nur fehlgeschlagenen Elementen
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

Die ersten beiden Cmdlets rufen den Wiederherstellungsdienste-Tresor ab – Tresor1 bzw. Tresor2.
Der zweite Befehl löst einen teilweisen Datensprung von Tresor1 in Tresor2 aus, bei dem nur die Elemente enthalten sind, die bei vorherigen Verschiebevorgängen fehlgeschlagen sind.

## PARAMETER

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

### -Erzwingen
Erzwingt den Vorgang zum Verschieben von Daten (verhindert das Bestätigungsdialogfeld), ohne eine Bestätigung für den Redundanztyp des Zieltresorspeichers zu verlangen. Dieser Parameter ist optional. 

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
Parameter wechseln, um die Daten verschieben nur für Container im Quelltresor zu versuchen, die noch nicht verschoben wurden.

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
Das Quelltresorobjekt, das verschoben werden soll.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## AUSGABEN

### System.String

## NOTIZEN

## VERWANDTE LINKS
