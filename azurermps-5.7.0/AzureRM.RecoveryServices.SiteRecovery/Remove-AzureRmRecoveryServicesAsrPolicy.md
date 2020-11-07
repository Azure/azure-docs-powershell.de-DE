---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: c8ef77367c66cc479bcbab25aba427c50a38447e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663054"
---
# Remove-AzureRmRecoveryServicesAsrPolicy

## Synopsis
Löscht die angegebene ASR-Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Remove-AzureRmRecoveryServicesAsrPolicy** " hat die angegebene Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste gelöscht.

## Beispiele

### Beispiel 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

Startet das Löschen der angegebenen Replikationsrichtlinie und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.

## Parameter

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Inputobject
Das Eingabeobjekt für das Cmdlet: das ASR-Replikationsrichtlinien Objekt, das der zu löschenden Replikationsrichtlinie entspricht.

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy

## Ausgaben

### System. Object

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesAsrPolicy](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[Neu – AzureRmRecoveryServicesAsrPolicy](./New-AzureRmRecoveryServicesAsrPolicy.md)
