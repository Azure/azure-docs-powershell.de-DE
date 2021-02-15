---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 6824777d5df0f06705f4c10c4af248f1f8e8714a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175268"
---
# Get-AzKeyVaultSecret

## SYNOPSIS
Ruft die geheimen Daten in einem Schlüsseltresor ab.

## SYNTAX

### ByVaultName (Standard)
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectVaultName
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectSecretName
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectSecretVersions
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceIdVaultName
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceIdSecretName
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceIdSecretVersions
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzKeyVaultSecret-Cmdlet** erhält geheime Daten in einem Schlüsseltresor.
Dieses Cmdlet erhält ein bestimmtes Geheimes oder alle geheimen Daten in einem Schlüsseltresor.

## BEISPIELE

### Beispiel 1: Erhalten aller aktuellen Versionen aller geheimen Daten in einem Schlüsseltresor
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

Dieser Befehl ruft die aktuellen Versionen aller geheimen Daten im Schlüsseltresor "Contoso" ab.

### Beispiel 2: Alle Versionen eines bestimmten geheimen Schlüssels erhalten
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

Dieser Befehl ruft alle Versionen des geheimen Namens "secret1" im Schlüsseltresor "Contoso" ab.

### Beispiel 3: Erhalten der aktuellen Version eines bestimmten geheimen Schlüssels
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

Dieser Befehl ruft die aktuelle Version des geheimen Namens "secret1" im Schlüsseltresor "Contoso" ab.

### Beispiel 4: Erhalten einer bestimmten Version eines bestimmten geheimen Schlüssels
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

Dieser Befehl ruft eine bestimmte Version des geheimen Namens "secret1" im Schlüsseltresor "Contoso" ab.

### Beispiel 5: Den Nur-Text-Wert der aktuellen Version eines bestimmten geheimen Schlüssels erhalten
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

Das Cmdlet gibt das Geheime als Zeichenfolge zurück, wenn `-AsPlainText` es angewendet wird.

### Beispiel 6: Erhalten Sie alle geheimen Daten, die für diesen Schlüsseltresor gelöscht, aber nicht gelöscht wurden.
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

Dieser Befehl ruft alle geheimen Daten ab, die zuvor gelöscht, aber nicht gelöscht wurden, im Schlüsseltresor "Contoso".

### Beispiel 7: Ruft den geheimen ITSecret ab, der für diesen Schlüsseltresor gelöscht, aber nicht gelöscht wurde.
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

Dieser Befehl ruft den geheimen "geheimen1" ab, der zuvor im Schlüsseltresor "Contoso" gelöscht, aber nicht gelöscht wurde.
Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten geheimen Schlüssels zurück.

### Beispiel 8: Erhalten aller aktuellen Versionen aller geheimen Daten in einem Schlüsseltresor mithilfe von Filtern
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

Dieser Befehl ruft die aktuellen Versionen aller geheimen Daten im Schlüsseltresor "Contoso" ab, die mit "geheim" beginnen.

## PARAMETERS

### -AsPlainText
Wenn dies festgelegt ist, konvertiert das Cmdlet den geheimen Schlüssel in der sicheren Zeichenfolge als Ausgabe in die entschlüsselte Nur-Text-Zeichenfolge.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, BySecretName, ByInputObjectVaultName, ByInputObjectSecretName, ByResourceIdVaultName, ByResourceIdSecretName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -IncludeVersions
Gibt an, dass dieses Cmdlet alle Versionen eines geheimen Schlüssels erhält.
Die aktuelle Version eines Geheimen ist die erste Version in der Liste.
Wenn Sie diesen Parameter angeben, müssen Sie auch die *Parameter "Name"* und *"VaultName"* angeben.
Wenn Sie den Parameter *"IncludeVersions"* nicht angeben, ruft dieses Cmdlet die aktuelle Version des Geheimen mit dem angegebenen *Namen ab.*

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
KeyVault-Objekt.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Gibt an, ob die zuvor gelöschten geheimen Daten in der Ausgabe angezeigt werden sollen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des geheimen Schlüssels an, den Sie erhalten müssen.

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ResourceId
KeyVault-Ressourcen-ID.

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Gibt den Namen des Schlüsseltresor an, zu dem das Geheimnis gehört.
Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Gibt die geheime Version an.
Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem Namen des Schlüsseltresor, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Undo-AzKeyVaultSecretRemoval](./Undo-AzKeyVaultSecretRemoval.md)

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

