---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479213"
---
# Get-AzureKeyVaultKey

## Synopsis
Ruft schlüsseltresor Schlüssel ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByVaultName (Standard)
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedKey
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureKeyVaultKey** " ruft Azure Key Vault-Schlüssel ab.
Dieses Cmdlet ruft ein bestimmtes **Microsoft. Azure. Commands. keyvault. Models. keybundle** oder eine Liste aller **keybundle** -Objekte in einem schlüsseltresor oder nach Version ab.

## Beispiele

### Beispiel 1: Abrufen aller Schlüssel in einem schlüsseltresor
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen contoso ab.

### Beispiel 2: Abrufen der aktuellen Version eines Schlüssels
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

Dieser Befehl ruft die aktuelle Version des Schlüssels mit dem Namen ITPfx im schlüsseltresor mit dem Namen contoso ab.

### Beispiel 3: Abrufen aller Versionen eines Schlüssels
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

Dieser Befehl ruft alle Versionen mit dem Schlüssel "ITPfx" im Schlüssel vaultnamed Contoso ab.

### Beispiel 4: Abrufen einer bestimmten Version eines Schlüssels
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

Dieser Befehl ruft eine bestimmte Version des Schlüssels mit dem Namen ITPfx im schlüsseltresor mit dem Namen contoso ab.
Nachdem Sie diesen Befehl ausgeführt haben, können Sie verschiedene Eigenschaften des Schlüssels überprüfen, indem Sie im $Key-Objekt navigieren.

### Beispiel 5: Abrufen aller Schlüssel, die gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurden.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

Dieser Befehl ruft alle Schlüssel ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.

### Beispiel 6: Ruft den Schlüssel ITPfx ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

Dieser Befehl ruft den Schlüssel ITPfx ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.
Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Schlüssels zurück.

## Parameter

### -IncludeVersions
Gibt an, dass dieses Cmdlet alle Versionen eines Schlüssels abruft.
Die aktuelle Version eines Schlüssels ist der erste in der Liste.
Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.

Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des Schlüssels mit dem angegebenen *Namen* ab.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Gibt an, ob die zuvor gelöschten Schlüssel in der Ausgabe angezeigt werden sollen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des abzurufenden Schlüsselpakets an.

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen des Schlüsselspeichers an, aus dem dieses Cmdlet Schlüssel erhält.
Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Schlüssel Version an.
Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüssel Version.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Zeichenfolge

## Ausgaben

### Liste<Microsoft. Azure. Commands. keyvault. Models. KeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. keybundle, List<Microsoft. Azure. Commands. keyvault. Models. DeletedKeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. DeletedKeyBundle

## Notizen

## Verwandte Links

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Undo-AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

[Satz-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

