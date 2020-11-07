---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662631"
---
# Import-AzureRmRecoveryServicesAsrVaultSettingsFile

## Synopsis
Importiert die angegebene Datei für ASR Vault-Einstellungen, um den Vault-Kontext (PowerShell-Sitzungskontext) für nachfolgende ASR-Vorgänge in der PowerShell-Sitzung festzulegen. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** " wird die Azure Site Recovery Vault-Einstellungsdatei importiert. Die Vault-Einstellungsdatei wird verwendet, um den Vault-Kontext für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen Sitzung zu definieren.

## Beispiele

### Beispiel 1
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

Importiert die angegebene Vault Settings-Datei für Wiederherstellungsdienste und gibt die Einstellungen des importierten Tresors zurück.

## Parameter

### -Path
Gibt den Pfad der ASR-Tresor-Einstellungsdatei an.
Diese Datei kann aus dem Vault-Portal für Recovery Services heruntergeladen und lokal gespeichert werden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### System. String

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesAsrVaultSettingsFile](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
