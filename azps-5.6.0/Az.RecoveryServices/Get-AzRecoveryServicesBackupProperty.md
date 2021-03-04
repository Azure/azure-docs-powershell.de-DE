---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 2cabaaedbd384237cd8be1469ea5f28cbc1e951f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934720"
---
# Get-AzRecoveryServicesBackupProperty

## SYNOPSIS
Ruft Sicherungseigenschaften ab.

## SYNTAX

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzRecoveryServicesBackupProperty-Cmdlet** ruft Sicherungseigenschaften für einen Recovery Services-Tresor ab.

## BEISPIELE

### Beispiel 1
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

Holen Sie sich die Sicherungstresoreigenschaft für den Tresor.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Vault
Gibt den Namen des Tresors an.
Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties

## NOTIZEN

## VERWANDTE LINKS
