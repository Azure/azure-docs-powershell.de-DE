---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1520acb94ffe587fb96eaa9c2ba565bcf31cc87e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503634"
---
# Backup-AzureKeyVaultManagedStorageAccount

## Synopsis
Sichern eines von keyvault verwalteten speicherkontos

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByStorageAccountName (Standard)
```
Backup-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Backup-AzureKeyVaultManagedStorageAccount** " wird ein bestimmtes verwaltetes Speicherkonto in einem schlüsseltresor gesichert, indem es heruntergeladen und in einer Datei gespeichert wird.
Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.
Sie können ein gesichertes Speicherkonto in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde, sofern sich der Tresor im gleichen Azure-geografischen Zustand befindet.
Typische Gründe für die Verwendung dieses Cmdlets sind: 
- Sie möchten eine Offlinekopie des speicherkontos behalten, falls Sie das Original versehentlich aus dem Tresor löschen.
 
- Sie haben ein verwaltetes Speicherkonto mithilfe von Key Vault erstellt und möchten nun das Objekt in einen anderen Azure-Bereich Klonen, sodass Sie es in allen Instanzen ihrer verteilten Anwendung verwenden können.
Verwenden Sie das Cmdlet **Backup-AzureKeyVaultManagedStorageAccount** , um das verwaltete Speicherkonto im verschlüsselten Format abzurufen, und verwenden Sie dann das Cmdlet **Restore-AzureKeyVaultManagedStorageAccount** , und geben Sie einen schlüsseltresor in der zweiten Region an.

## Beispiele

### Beispiel 1: Sichern eines verwalteten speicherkontos mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Dieser Befehl ruft das verwaltete Speicherkonto namens MyMSAK aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherung dieses verwalteten speicherkontos in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines verwalteten speicherkontos mit einem angegebenen Dateinamen
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Dieser Befehl ruft das verwaltete Speicherkonto namens MyMSAK aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses verwalteten speicherkontos in einer Datei mit dem Namen Backup. BLOB.

### Beispiel 3: Sichern eines zuvor abgerufenen verwalteten speicherkontos mit einem angegebenen Dateinamen, wobei die Zieldatei ohne Aufforderung überschrieben wird.
```powershell
PS C:\> $msak = Get-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzureKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Mit diesem Befehl wird eine Sicherungskopie des verwalteten speicherkontos mit dem Namen $msak erstellt. Name im Tresor mit dem Namen $msak. Vaultname in eine Datei mit dem Namen "Backup. BLOB", wobei die Datei im Hintergrund überschrieben wird, wenn Sie bereits vorhanden ist.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Das zu sichernde Speicherkonto Bündel wird von der Ausgabe eines Abruf Anrufs in die Pipeline übertragen.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Geheimer Name.
Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Outputdatei
Ausgabedatei.
Die Ausgabedatei zum Speichern der Speicherkonto Sicherung
Wenn keine Angabe erfolgt, wird ein Standarddateiname generiert.

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
Vault-Name.
Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem
Parameter: Inputobject (ByValue)

## Ausgaben

### System. String

## Notizen

## Verwandte Links
