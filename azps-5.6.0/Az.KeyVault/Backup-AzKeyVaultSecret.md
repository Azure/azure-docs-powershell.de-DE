---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: ae60c2d10c8b186db22fb9fc9cd0a1e66aa1c07d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923619"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Sichern Sie einen Geheimschlüssel in einem Schlüsseltresor.

## SYNTAX

### BySecretName (Standard)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Backup-AzKeyVaultSecret** stellt einen angegebenen Geheimschlüssel in einem Schlüsseltresor sicher, indem es heruntergeladen und in einer Datei gespeichert wird.
Wenn mehrere Versionen des Geheimtipps vorhanden sind, sind alle Versionen in der Sicherung enthalten.
Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.
Sie können einen gesicherten Geheimschlüssel in jedem Schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde.
Typische Gründe für die Verwendung dieses Cmdlets sind:
- Sie möchten eine Kopie Ihres Geheimschlüssels encrown, damit Sie über eine Offlinekopie verfügen, falls Sie Ihren Geheimschlüssel versehentlich in Ihrem Schlüsseltresor löschen.
- Sie haben einem Schlüsseltresor ein Geheimnis hinzugefügt und möchten das Geheimnis nun in eine andere Azure-Region klonen, damit Sie es in allen Instanzen Ihrer verteilten Anwendung verwenden können. Verwenden Sie Backup-AzKeyVaultSecret-Cmdlet, um den Geheimschlüssel im verschlüsselten Format abzurufen, verwenden Sie dann das Restore-AzKeyVaultSecret-Cmdlet, und geben Sie einen Schlüsseltresor im zweiten Bereich an. (Beachten Sie, dass die Regionen derselben Geografie angehören müssen.)

## BEISPIELE

### Beispiel 1: Sichern eines Geheimtipps mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Dieser Befehl ruft den Geheimschlüssel "MySecret" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses Geheimschlüssels in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines Geheimtipps für einen angegebenen Dateinamen, Überschreiben der vorhandenen Datei ohne Aufforderung
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Mit diesem Befehl wird der Geheimschlüssel "MySecret" aus dem Schlüsseltresor namens "MyKeyVault" abgerufen und eine Sicherung dieses Geheimschlüssels in einer Datei mit dem Namen "Backup.blob" gespeichert.

### Beispiel 3: Sichern eines geheimen Schlüssels, der zuvor in einem angegebenen Dateinamen abgerufen wurde
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Dieser Befehl verwendet den $secret und Namen des Tresorobjekts, um den Geheimtipp abzurufen und seine Sicherung in einer Datei mit dem Namen "Backup.blob" zu speichern.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Erzwingen
Fordert Sie zur Bestätigung auf, bevor Sie die Ausgabedatei überschreiben, sofern vorhanden.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Secret to be backed up, pipelined in from the output of a retrieval call.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des zu sichernden Geheimtipps an.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Gibt die Ausgabedatei an, in der das Sicherungsblob gespeichert ist.
Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.
Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen und gibt eine Fehlermeldung zurück, dass die Sicherungsdatei bereits vorhanden ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Gibt den Namen des Schlüsseltresor an, der das zu sichernde Geheimnis enthält.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## AUSGABEN

### System.String

## NOTIZEN

## VERWANDTE LINKS

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

