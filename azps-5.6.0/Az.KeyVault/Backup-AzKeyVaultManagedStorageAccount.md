---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938672"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Stellt ein von KeyVault verwaltetes Speicherkonto sichern.

## SYNTAX

### ByStorageAccountName (Standard)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Backup-AzKeyVaultManagedStorageAccount** stellt ein angegebenes verwaltetes Speicherkonto in einem Schlüsseltresor bereit, indem es heruntergeladen und in einer Datei gespeichert wird.
Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.
Sie können ein gesichertes Speicherkonto in einem beliebigen Schlüsseltresor im Abonnement wiederherstellen, von dem es gesichert wurde, solange sich der Tresor in derselben Azure-Geographie befindet.
Typische Gründe für die Verwendung dieses Cmdlets sind: 
- Sie möchten eine Offlinekopie des Speicherkontos beibehalten, falls Sie das Original versehentlich aus dem Tresor löschen.
 
- Sie haben mit dem Schlüsseltresor ein verwaltetes Speicherkonto erstellt und möchten das Objekt nun in eine andere Azure-Region klonen, sodass Sie es in allen Instanzen Ihrer verteilten Anwendung verwenden können.
Verwenden Sie das **Cmdlet Backup-AzKeyVaultManagedStorageAccount,** um das verwaltete Speicherkonto im verschlüsselten Format abzurufen, verwenden Sie dann das **Cmdlet Restore-AzKeyVaultManagedStorageAccount,** und geben Sie einen Schlüsseltresor in der zweiten Region an.

## BEISPIELE

### Beispiel 1: Sichern eines verwalteten Speicherkontos mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Dieser Befehl ruft das verwaltete Speicherkonto mit dem Namen MyMSAK aus dem Schlüsseltresor "MyKeyVault" ab und speichert eine Sicherung dieses verwalteten Speicherkontos in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines verwalteten Speicherkontos auf einen angegebenen Dateinamen
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Mit diesem Befehl wird das verwaltete Speicherkonto mit dem Namen MyMSAK aus dem Schlüsseltresor "MyKeyVault" abgerufen und eine Sicherung dieses verwalteten Speicherkontos in einer Datei mit dem Namen "Backup.blob" gespeichert.

### Beispiel 3: Sichern Sie ein zuvor abgerufenes verwaltetes Speicherkonto auf einen angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Aufforderung.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Mit diesem Befehl wird eine Sicherung des verwalteten Speicherkontos namens $msak. Name im Tresor namens $msak. VaultName in eine Datei mit dem Namen "Backup.blob", und überschreiben Sie die Datei automatisch, wenn sie bereits vorhanden ist.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Überschreiben der angegebenen Datei, wenn sie vorhanden ist

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

### -InputObject
Speicherkontobündel, das gesichert werden soll, das aus der Ausgabe eines Abrufaufrufs in pipelineiniert wird.

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
Das Cmdlet erstellt den FQDN eines Geheimnamens aus dem Tresor, der aktuell ausgewählten Umgebung und des geheimen Namens.

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

### -OutputFile
Ausgabedatei.
Die Ausgabedatei zum Speichern der Speicherkontosicherung.
Wenn nicht angegeben, wird ein Standarddateiname generiert.

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
Name des Tresors.
Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## AUSGABEN

### System.String

## NOTIZEN

## VERWANDTE LINKS
