---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 675107a27774cf2fe44ef328cdb0d7a3569e8abb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918859"
---
# Remove-AzKeyVaultSecret

## SYNOPSIS
Löscht einen Geheimschlüssel in einem Schlüsseltresor.

## SYNTAX

### ByVaultName (Standard)
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das Remove-AzKeyVaultSecret-Cmdlet löscht einen Geheimschlüssel in einem Schlüsseltresor.
Wenn das Geheimnis versehentlich gelöscht wurde, kann das Geheimnis mithilfe von Undo-AzKeyVaultSecretRemoval einem Benutzer mit speziellen Berechtigungen wiederhergestellt werden.
Dieses Cmdlet hat den Wert "high" für die **ConfirmImpact-Eigenschaft.**

## BEISPIELE

### Beispiel 1: Entfernen eines Geheimschlüssels aus einem Schlüsseltresor
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

Mit diesem Befehl wird der geheime Name "FinanceSecret" aus dem Schlüsseltresor "Contoso" entfernt."

### Beispiel 2: Entfernen eines Geheimschlüssels aus einem Schlüsseltresor ohne Benutzerbestätigung
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

Mit diesem Befehl wird der geheime Name "FinanceSecret" aus dem Schlüsseltresor "Contoso" entfernt.
Der Befehl gibt die Parameter *Erzwingen* *und* Bestätigen an, daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.

### Beispiel 3: Löschen des gelöschten Geheimschlüssels aus dem Schlüsseltresor dauerhaft
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

Mit diesem Befehl wird das Geheimgeheimnis "FinanceSecret" aus dem Schlüsseltresor "Contoso" dauerhaft vorverziert.
Für die Ausführung dieses Cmdlets ist die Berechtigung "Löschen" erforderlich, die zuvor und explizit dem Benutzer für diesen Schlüsseltresor erteilt worden sein muss.

## PARAMETER

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

### -Erzwingen
Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.

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
Geheimes Schlüsseltresorobjekt

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Wenn vorhanden, entfernt das zuvor gelöschte Geheimnis endgültig.

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

### -Name
Gibt den Namen eines Geheimtipps an.
Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Geheimschlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet ein **Microsoft.Azure.Commands.KeyVault.Models.Secret-Objekt** zurückgibt.
Standardmäßig generiert dieses Cmdlet keine Ausgabe.

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

### -VaultName
Gibt den Namen des Schlüsseltresor an, zu dem das Geheimnis gehört.
Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und ihrer aktuellen Umgebung.

```yaml
Type: System.String
Parameter Sets: ByVaultName
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt. Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret

## NOTIZEN

## VERWANDTE LINKS

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Rückgängig-AzKeyVaultSecretRemoval](./Undo-AzKeyVaultSecretRemoval.md)

