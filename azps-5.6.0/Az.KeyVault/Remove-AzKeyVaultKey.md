---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 0d458d6063aa530b1f30f6a79244e7d719080bf6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918875"
---
# Remove-AzKeyVaultKey

## SYNOPSIS
Löscht einen Schlüssel in einem Schlüsseltresor.

## SYNTAX

### ByVaultName (Standard)
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByVaultName
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das Remove-AzKeyVaultKey-Cmdlet löscht einen Schlüssel in einem Schlüsseltresor.
Wenn der Schlüssel versehentlich gelöscht wurde, kann der Schlüssel mithilfe von Undo-AzKeyVaultKeyRemoval einem Benutzer mit speziellen Berechtigungen wiederhergestellt werden.
Dieses Cmdlet hat den Wert "high" für die **ConfirmImpact-Eigenschaft.**

## BEISPIELE

### Beispiel 1: Entfernen eines Schlüssels aus einem Schlüsseltresor
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

Mit diesem Befehl wird der Schlüssel "ITSoftware" aus dem Schlüsseltresor "Contoso" entfernt.

### Beispiel 2: Entfernen eines Schlüssels ohne Benutzerbestätigung
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

Mit diesem Befehl wird der Schlüssel "ITSoftware" aus dem Schlüsseltresor "Contoso" entfernt.
Der Befehl gibt den *Parameter Force* an, daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.

### Beispiel 3: Endgültiges Löschen eines gelöschten Schlüssels aus dem Schlüsseltresor
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

Mit diesem Befehl wird der Schlüssel mit dem Namen ITSoftware dauerhaft aus dem Schlüsseltresor Contoso entfernt.
Für die Ausführung dieses Cmdlets ist die Berechtigung "Löschen" erforderlich, die zuvor und explizit dem Benutzer für diesen Schlüsseltresor erteilt worden sein muss.

### Beispiel 4: Entfernen von Schlüsseln mithilfe des Pipelineoperators
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

Dieser Befehl ruft alle Schlüssel im Schlüsseltresor namens Contoso ab und übergibt sie mithilfe des Pipelineoperators an das **Where-Object-Cmdlet.**
Dieses Cmdlet übergibt die Schlüssel mit dem Wert $False für das Attribut **Enabled** an das aktuelle Cmdlet.
Dieses Cmdlet entfernt diese Tasten.

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

### -HsmName
HSM-Name. Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
KeyBundle-Objekt

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Entfernen Sie den zuvor gelöschten Schlüssel dauerhaft.

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
Gibt den Namen des zu entfernenden Schlüssels an.
Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet ein **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey-Objekt** zurückgibt.
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
Gibt den Namen des Schlüsseltresor an, aus dem der Schlüssel entfernt werden soll.
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey

## NOTIZEN

## VERWANDTE LINKS

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)

[Rückgängig-AzKeyVaultKeyRemoval](./Undo-AzKeyVaultKeyRemoval.md)

