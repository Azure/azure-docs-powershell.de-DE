---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: cd83d61c64e4111faf7fc6149107e172d0cf0c9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848251"
---
# Backup-AzureKeyVaultSecret

## Synopsis
Sichern eines Geheimnisses in einem schlüsseltresor

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### BySecretName (Standard)
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Backup-AzureKeyVaultSecret** " wird ein angegebener Schlüssel in einem Schlüsseldepot gesichert, indem es heruntergeladen und in einer Datei gespeichert wird.
Wenn mehrere Versionen des geheimen Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.
Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.
Sie können ein gesichertes Geheimnis in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde.

Typische Gründe für die Verwendung dieses Cmdlets sind:

- Sie möchten eine Kopie Ihres Geheimnisses hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihr Kennwort versehentlich in Ihrem schlüsseltresor löschen.
- Sie haben einem schlüsseltresor ein Kennwort hinzugefügt und möchten das Geheimnis nun in einen anderen Azure-Bereich Klonen, damit Sie es in allen Instanzen ihrer verteilten Anwendung verwenden können. Verwenden Sie das Backup-AzureKeyVaultSecret-Cmdlet, um das Geheimnis im verschlüsselten Format abzurufen, und verwenden Sie dann das Cmdlet Restore-AzureKeyVaultSecret, und geben Sie einen schlüsseltresor im zweiten Bereich an. (Beachten Sie, dass die Regionen zur gleichen geografischen Region gehören müssen.)

## Beispiele

### Beispiel 1: Sichern eines Geheimnisses mit einem automatisch generierten Dateinamen
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

Dieser Befehl ruft den geheimen Namen "MySecret" aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Geheimnisses in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.

### Beispiel 2: Sichern eines Geheimnisses zu einem angegebenen Dateinamen, Überschreiben der vorhandenen Datei ohne Aufforderung
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

Dieser Befehl ruft den geheimen Namen "MySecret" aus dem Schlüssel vaultnamed MyKeyVault ab und speichert eine Sicherungskopie dieses Geheimnisses in einer Datei mit dem Namen Backup. BLOB.

### Beispiel 3: Sichern eines zuvor abgerufenen Geheimnisses in einem angegebenen Dateinamen
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

Dieser Befehl verwendet den Tresor Namen und den Namen des $Secret Objekts, um den geheimen Schlüssel abzurufen und seine Sicherung in einer Datei mit dem Namen Backup. BLOB zu speichern.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie die Ausgabedatei überschreiben (sofern vorhanden).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des zu sichernden Schlüssels an.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Outputdatei
Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.
Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.
Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen, und es wird eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Gibt das Objekt an, dessen Name und Vault für den Sicherungsvorgang verwendet werden sollen.

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen des Schlüssel Tresors an, der das zu sichernde Geheimnis enthält.

```yaml
Type: String
Parameter Sets: BySecretName
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

## Ausgaben

### Zeichenfolge
Das Cmdlet gibt den Pfad der Ausgabedatei zurück, die die Sicherung des Schlüssels enthält.

## Notizen

## Verwandte Links

[Satz-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Wiederherstellen – AzureKeyVaultSecret](./Restore-AzureKeyVaultSecret.md)

