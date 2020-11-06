---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f2507d441dc04fd01217dde685deb667211f4034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505509"
---
# Get-AzureKeyVaultSecret

## Synopsis
Ruft die Geheimnisse in einem schlüsseltresor ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByVaultName (Standard)
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectVaultName
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectSecretName
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectSecretVersions
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureKeyVaultSecret** " erhält in einem schlüsseltresor Geheimnisse.
Dieses Cmdlet ruft einen bestimmten geheimen oder alle Geheimnisse in einem schlüsseltresor ab.

## Beispiele

### Beispiel 1: Abrufen aller aktuellen Versionen aller Geheimnisse in einem schlüsseltresor
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

Mit diesem Befehl werden die aktuellen Versionen aller Geheimnisse im schlüsseltresor mit dem Namen contoso abgerufen.

### Beispiel 2: Abrufen aller Versionen eines bestimmten geheimen Schlüssels
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

Dieser Befehl ruft alle Versionen des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.

### Beispiel 3: Abrufen der aktuellen Version eines bestimmten geheimen Schlüssels
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

Dieser Befehl ruft die aktuelle Version des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.

### Beispiel 4: Abrufen einer bestimmten Version eines bestimmten Geheimnisses
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

Dieser Befehl ruft eine bestimmte Version des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.

### Beispiel 5: Abrufen des nur-Text-Werts der aktuellen Version eines bestimmten geheimen Schlüssels
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Diese Befehle rufen die aktuelle Version eines geheimen namens ITSecret ab und zeigen dann den nur-Text-Wert dieses geheimen Schlüssels an.

### Beispiel 6: Abrufen aller für diesen schlüsseltresor gelöschten, aber nicht bereinigten Geheimnisse
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

Dieser Befehl ruft alle Geheimnisse ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.

### Beispiel 7: Ruft den geheimen ITSecret ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

Dieser Befehl ruft den geheimen ITSecret ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.
Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum für diesen gelöschten Schlüssel zurück.

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

### -IncludeVersions
Gibt an, dass dieses Cmdlet alle Versionen eines geheimen Schlüssels abruft.
Die aktuelle Version eines Geheimnisses ist die erste in der Liste.
Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.

Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des geheimen Schlüssels mit dem angegebenen *Namen* ab.

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Keyvault-Objekt.

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Gibt an, ob die zuvor gelöschten Geheimnisse in der Ausgabe angezeigt werden sollen.

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des abzurufenden Geheimnisses an.

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.
Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.

```yaml
Type: String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die geheime Version an.
Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.

```yaml
Type: String
Parameter Sets: BySecretName, ByInputObjectSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Zeichenfolge

## Ausgaben

### List<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret

## Notizen

## Verwandte Links

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Undo-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

[Satz-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

