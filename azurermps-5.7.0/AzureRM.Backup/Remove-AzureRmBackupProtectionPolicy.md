---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 550a8d2a64d4e6f5b887395125daab65d1b551c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501517"
---
# Remove-AzureRmBackupProtectionPolicy

## Synopsis
Löscht eine Richtlinie aus einem Sicherungsspeicher.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmBackupProtectionPolicy** löscht eine Richtlinie aus einem Azure Backup Vault.

Bevor Sie eine Sicherungsschutz Richtlinie löschen können, darf die Richtlinie keine zugeordneten Sicherungselemente enthalten.
Bevor Sie die Richtlinie löschen, stellen Sie sicher, dass jedes zugeordnete Element einer anderen Richtlinie zugeordnet ist.
Verwenden Sie das Enable-AzureRmBackupProtection-Cmdlet, um eine andere Richtlinie einem Sicherungselement zuzuordnen.

## Beispiele

### Beispiel 1: Entfernen einer Sicherungsschutz Richtlinie
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.
Der Befehl speichert das Objekt in der $Vault Variablen.

Der zweite Befehl erstellt eine Aufbewahrungsrichtlinie für 30 Tage tägliche Aufbewahrung und speichert Sie dann in der $Daily-Variablen.

Der zweite Befehl ruft die Schutzrichtlinie mit dem Namen DailyBackup im Tresor in $Vault mit dem Cmdlet **Get-AzureRmBackupProtectionPolicy** .
Der Befehl übergibt die Richtlinie an das aktuelle Cmdlet.
Dieses Cmdlet entfernt die Richtlinie.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -ProtectionPolicy
Gibt die von diesem Cmdlet entfernte Schutzrichtlinie an.
Verwenden des Get-AzureRmBackupProtectionPolicy-Cmdlets zum Abrufen eines **AzureRmBackupProtectionPolicy**

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureRMBackupProtectionPolicy

## Ausgaben

### Keine

## Notizen

## Verwandte Links

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[Neu – AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


