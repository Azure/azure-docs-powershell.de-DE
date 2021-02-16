---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170454"
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
Das **Cmdlet "Backup-AzKeyVaultManagedStorageAccount"** sichern ein angegebenes verwaltetes Speicherkonto in einem Schlüsseltresor, indem es heruntergeladen und in einer Datei gespeichert wird.
Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.
Sie können ein gesichertes Speicherkonto in einem beliebigen Schlüsseltresor in dem Abonnement wiederherstellen, von dem es gesichert wurde, solange sich der Tresor in derselben Geografie von Azure befindet.
Typische Gründe für die Verwendung dieses Cmdlets sind: 
- Sie möchten eine Offlinekopie des Speicherkontos für den Fall beibehalten, dass Sie das Original versehentlich aus dem Tresor löschen.
 
- Sie haben mit dem Schlüsseltresor ein Konto für verwalteten Speicher erstellt und möchten nun das Objekt in eine andere Azure-Region klonen, damit Sie es in allen Instanzen der verteilten Anwendung verwenden können.
Verwenden Sie das Cmdlet **"Backup-AzKeyVaultManagedStorageAccount",** um das verwaltete Speicherkonto im verschlüsselten Format abzurufen, verwenden Sie dann das Cmdlet **"Restore-AzKeyVaultManagedStorageAccount",** und geben Sie einen Schlüsseltresor in der zweiten Region an.

## BEISPIELE

### Beispiel 1: Sichern eines verwalteten Speicherkontos mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Dieser Befehl ruft das verwaltete Speicherkonto "MyMSAK" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses verwalteten Speicherkontos in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines verwalteten Speicherkontos unter einem angegebenen Dateinamen
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Dieser Befehl ruft das verwaltete Speicherkonto "MyMSAK" aus dem Schlüsseltresor "MyKeyVault" ab und speichert eine Sicherung dieses verwalteten Speicherkontos in einer Datei namens "Backup.blob".

### Beispiel 3: Sichern sie ein zuvor abgerufenes Konto für verwalteten Speicher unter einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Eingabeaufforderung.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Dieser Befehl erstellt eine Sicherung des verwalteten Speicherkontos namens $msak. Name im Tresor namens $msak. VaultName in eine Datei mit dem Namen "Backup.blob", und überschreiben die Datei, sofern sie bereits vorhanden ist.

## PARAMETERS

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

### -InputObject
Das Speicherkontobündel, das gesichert werden soll, wird über die Ausgabe eines Abrufaufrufs pipelineiert.

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
Das Cmdlet erstellt den FQDN eines Geheimen aus dem Namen des Tresors, die aktuell ausgewählte Umgebung und den geheimen Namen.

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
Wenn nichts angegeben wird, wird ein Standarddateiname generiert.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
