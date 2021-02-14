---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147681"
---
# Backup-AzKeyVaultKey

## SYNOPSIS
Sichern eines Schlüssels in einem Schlüsseltresor

## SYNTAX

### ByKeyName (Standard)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByKeyName
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Backup-AzKeyVaultKey"** sichern einen angegebenen Schlüssel in einem Schlüsseltresor, indem es ihn herunter- und in einer Datei speichert.
Wenn mehrere Versionen des Schlüssels vorhanden sind, sind alle Versionen in der Sicherung enthalten.
Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.
Sie können einen gesicherten Schlüssel in einem beliebigen Schlüsseltresor im Abonnement wiederherstellen, von dem er gesichert wurde.
Typische Gründe für die Verwendung dieses Cmdlets sind: 
- Sie möchten eine Kopie Ihres Schlüssels einsperren, damit Sie über eine Offlinekopie verfügen, falls Sie den Schlüssel versehentlich in Ihrem Schlüsseltresor gelöscht haben.
 
- Sie haben einen Schlüssel mithilfe des Schlüsseltresor erstellt und möchten den Schlüssel jetzt in eine andere Azure-Region klonen, damit Sie ihn aus allen Instanzen Ihrer verteilten Anwendung verwenden können.
Verwenden Sie das **Cmdlet "Backup-AzKeyVaultKey",** um den Schlüssel im verschlüsselten Format abzurufen. Verwenden Sie dann das Cmdlet Restore-AzKeyVaultKey, und geben Sie einen Schlüsseltresor in der zweiten Region an.

## BEISPIELE

### Beispiel 1: Sichern eines Schlüssels mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Dieser Befehl ruft den Schlüssel namens "MyKey" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses Schlüssels in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines Schlüssels unter einem angegebenen Dateinamen
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Dieser Befehl ruft den Schlüssel namens "MyKey" aus dem Schlüsseltresornamen "MyKeyVault" ab und speichert eine Sicherung dieses Schlüssels in einer Datei namens "Backup.blob".

### Beispiel 3: Sichern eines zuvor abgerufenen Schlüssels unter einem angegebenen Dateinamen, Überschreiben der Zieldatei ohne Eingabeaufforderung
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Dieser Befehl erstellt eine Sicherung des Schlüssels namens $key. Name im Tresor namens $key. VaultName in eine Datei mit dem Namen "Backup.blob", und überschreiben die Datei, sofern sie bereits vorhanden ist.

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
Überschreiben der vorhandenen Datei

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmName
HSM-Name. Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Key bundle to back up, pipelined in from the output of a retrieval call.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des zu sichernden Schlüssels an.

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.
Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.
Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen, und es wird eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.

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
Gibt den Namen des Schlüsseltresor an, der den zu sichernden Schlüssel enthält.

```yaml
Type: System.String
Parameter Sets: ByKeyName
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

