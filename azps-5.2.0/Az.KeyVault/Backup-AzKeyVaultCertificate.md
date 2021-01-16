---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305219"
---
# Backup-AzKeyVaultCertificate

## SYNOPSIS
Sichern eines Zertifikats in einem Schlüsseltresor

## SYNTAX

### ByCertificateName (Standard)
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Backup-AzKeyVaultCertificate"** sichern ein angegebenes Zertifikat in einem Schlüsseltresor, indem es heruntergeladen und in einer Datei gespeichert wird.
Wenn das Zertifikat über mehrere Versionen verfügt, werden alle diese Versionen in die Sicherung eingeschlossen.
Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.
Sie können ein gesichertes Zertifikat in einem beliebigen Schlüsseltresor im Abonnement wiederherstellen, von dem es gesichert wurde, solange sich der Tresor in derselben Azure-Geografie befindet.
Typische Gründe für die Verwendung dieses Cmdlets sind: 
- Sie möchten eine Offlinekopie des Zertifikats für den Fall beibehalten, dass Sie das Original versehentlich aus dem Tresor löschen.
 
- Sie haben ein Zertifikat mithilfe des Schlüsseltresor erstellt und möchten nun das Objekt in eine andere Azure-Region klonen, damit Sie es in allen Instanzen Der verteilten Anwendung verwenden können.
Verwenden Sie das **Cmdlet "Backup-AzKeyVaultCertificate",** um das Zertifikat im verschlüsselten Format abzurufen, verwenden Sie dann das Cmdlet **"Restore-AzKeyVaultCertificate",** und geben Sie einen Schlüsseltresor in der zweiten Region an.

## BEISPIELE

### Beispiel 1: Sichern eines Zertifikats mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Dieser Befehl ruft das Zertifikat namens "MyCert" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses Zertifikats in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines Zertifikats unter einem angegebenen Dateinamen
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Mit diesem Befehl wird das Zertifikat namens "MyCert" aus dem Schlüsseltresor "MyKeyVault" abgerufen und eine Sicherung des Zertifikats in einer Datei namens "Backup.blob" gespeichert.

### Beispiel 3: Sichern Sie ein zuvor abgerufenes Zertifikat unter einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Eingabeaufforderung.
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Mit diesem Befehl wird eine Sicherung des Zertifikats namens "$cert. Name im Tresor namens $cert. VaultName in eine Datei mit dem Namen "Backup.blob", und überschreiben die Datei, sofern sie bereits vorhanden ist.

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
Das Geheime, das gesichert werden soll, wird aus der Ausgabe eines Abrufanrufs pipelineiert.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

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
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Ausgabedatei.
Die Ausgabedatei zum Speichern der Sicherung des Zertifikats.
Ohne Angabe wird ein Standarddateiname generiert.

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
Parameter Sets: ByCertificateName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
