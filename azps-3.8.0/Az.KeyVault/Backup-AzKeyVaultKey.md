---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 28f4550ac850b7bcc5bab4c90ec510128a8e2ab0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847028"
---
# Backup-AzKeyVaultKey

## Synopsis
Sie können einen Schlüssel in einem schlüsseltresor sichern.

## Syntax

### ByKeyName (Standard)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Backup-AzKeyVaultKey** " wird ein angegebener Schlüssel in einem schlüsseltresor gesichert, indem er heruntergeladen und in einer Datei gespeichert wird.
Wenn mehrere Versionen des Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.
Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.
Sie können einen gesicherten Schlüssel in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde.
Typische Gründe für die Verwendung dieses Cmdlets sind: 
- Sie möchten eine Kopie Ihres Schlüssels hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihren Schlüssel versehentlich in Ihrem schlüsseltresor löschen.
 
- Sie haben einen Schlüssel mithilfe von Key Vault erstellt und möchten nun den Schlüssel in einen anderen Azure-Bereich Klonen, sodass Sie ihn aus allen Instanzen ihrer verteilten Anwendung verwenden können.
Verwenden Sie das Cmdlet **Backup-AzKeyVaultKey** , um den Schlüssel im verschlüsselten Format abzurufen, und verwenden Sie dann das Restore-AzKeyVaultKey-Cmdlet, und geben Sie einen schlüsseltresor im zweiten Bereich an.

## Beispiele

### Beispiel 1: Sichern eines Schlüssels mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Dieser Befehl ruft den Schlüssel mit dem Namen MyKey aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Schlüssels in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines Schlüssels in einem angegebenen Dateinamen
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Dieser Befehl ruft den Schlüssel mit dem Namen MyKey aus dem Schlüssel vaultnamed MyKeyVault ab und speichert eine Sicherung dieses Schlüssels in einer Datei mit dem Namen Backup. BLOB.

### Beispiel 3: Sichern Sie einen zuvor abgerufenen Schlüssel in einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Aufforderung.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Mit diesem Befehl wird eine Sicherungskopie des Schlüssels mit dem Namen $Key erstellt. Name im Tresor mit dem Namen $Key. Vaultname in eine Datei mit dem Namen "Backup. BLOB", wobei die Datei im Hintergrund überschrieben wird, wenn Sie bereits vorhanden ist.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Überschreiben der angegebenen Datei, sofern vorhanden

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

### -Inputobject
Schlüsselpaket, das von der Ausgabe eines Abruf Anrufs in eine Sicherungskopie geleitet wird.

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
Gibt den Namen des Schlüssels an, der gesichert werden soll.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Outputdatei
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

### -Vaultname
Gibt den Namen des Schlüssel Tresors an, der den zu sichernden Schlüssel enthält.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Wiederherstellen – AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

