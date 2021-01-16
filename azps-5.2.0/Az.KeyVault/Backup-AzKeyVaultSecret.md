---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305736"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Ein Geheimschlüssel in einem Schlüsseltresor wird sichern.

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
Das **Cmdlet "Backup-AzKeyVaultSecret"** sichern einen angegebenen Geheimschlüssel in einem Schlüsseltresor, indem es ihn herunter- und in einer Datei speichert.
Wenn mehrere Versionen des geheimen Schlüssels vorhanden sind, sind alle Versionen in der Sicherung enthalten.
Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.
Sie können einen gesicherten Geheimschlüssel für jeden Schlüsseltresor in dem Abonnement wiederherstellen, von dem es gesichert wurde.
Typische Gründe für die Verwendung dieses Cmdlets sind:
- Sie möchten eine Kopie Ihres geheimen Schlüssels einsperren, damit Sie über eine Offlinekopie verfügen, falls Sie ihr Geheimes versehentlich in Ihrem Schlüsseltresor löschen.
- Sie haben einem Schlüsseltresor ein Geheimnis hinzugefügt und möchten es nun in eine andere Azure-Region klonen, damit Sie es in allen Instanzen Ihrer verteilten Anwendung verwenden können. Verwenden Sie das Backup-AzKeyVaultSecret-Cmdlet, um den geheimen Schlüssel im verschlüsselten Format abzurufen. Verwenden Sie dann das Cmdlet Restore-AzKeyVaultSecret, und geben Sie einen Schlüsseltresor in der zweiten Region an. (Beachten Sie, dass die Regionen derselben Geografie angehören müssen.)

## BEISPIELE

### Beispiel 1: Sichern eines geheimen Schlüssels mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Dieser Befehl ruft den geheimen Namen "MySecret" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses Geheimschlüssels in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines Geheimtipps für einen angegebenen Dateinamen, Überschreiben der vorhandenen Datei ohne Eingabeaufforderung
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Dieser Befehl ruft den geheimen Namen "MySecret" aus dem Schlüsseltresor "MyKeyVault" ab und speichert eine Sicherung dieses Geheimschlüssels in einer Datei mit dem Namen "Backup.blob".

### Beispiel 3: Sichern eines geheimen Schlüssels, der zuvor unter einem angegebenen Dateinamen abgerufen wurde
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Dieser Befehl verwendet den $secret und Den Namen des $secret objekts, um den geheimen Schlüssel abzurufen, und speichert seine Sicherung in einer Datei namens "Backup.BLOB".

## PARAMETERS

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

### -Force
Fordert Sie zur Bestätigung auf, bevor Sie die Ausgabedatei überschreiben, sofern diese vorhanden ist.

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
Das Geheime, das gesichert werden soll, wird aus der Ausgabe eines Abrufanrufs pipelineiert.

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
Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.
Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.
Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen und eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.

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

### -Confirm
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

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

