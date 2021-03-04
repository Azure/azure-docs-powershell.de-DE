---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 975395c471a08eac745bd8a9ab07cec826d5c038
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931043"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
Aktualisiert Attribute eines Geheimschlüssels in einem Schlüsseltresor.

## SYNTAX

### Standard (Standard)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Update-AzKeyVaultSecret-Cmdlet** aktualisiert bearbeitbare Attribute eines Geheimschlüssels in einem Schlüsseltresor.

## BEISPIELE

### Beispiel 1: Ändern der Attribute eines Geheimtipps
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

Die ersten vier Befehle definieren Attribute für das Ablaufdatum, das Datum NotBefore, Tags und den Kontexttyp und speichern die Attribute in Variablen.
Mit dem endgültigen Befehl werden die Attribute für den Geheimschlüssel hr im Schlüsseltresor namens ContosoVault mithilfe der gespeicherten Variablen geändert.

### Beispiel 2: Löschen der Tags und Inhaltstypen für einen Geheimtipp
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Mit diesem Befehl werden die Tags und der Inhaltstyp für die angegebene Version des Geheimschlüssels hr im Schlüsseltresor namens Contoso gelöscht.

### Beispiel 3: Deaktivieren der aktuellen Version von Geheimgeheimnissen, deren Name mit der IT beginnt
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

Der erste Befehl speichert den Zeichenfolgenwert Contoso in der $Vault Variable.
Der zweite Befehl speichert den Zeichenfolgenwert IT in der $Prefix Variable.
Der dritte Befehl verwendet das Get-AzKeyVaultSecret-Cmdlet, um die Geheimschlüssel im angegebenen Schlüsseltresor zu erhalten, und übergibt diese Geheimschlüssel dann an das **Where-Object-Cmdlet.** Das **Cmdlet Where-Object** filtert die Geheimnisse nach Namen, die mit den Zeichen IT beginnen. Der Befehl gibt die Geheim geheimen Daten, die dem Filter entsprechen, an das cmdlet Update-AzKeyVaultSecret an, wodurch diese deaktiviert werden.

### Beispiel 4: Festlegen des Inhaltstyps für alle Versionen eines Geheimtipps
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

Die ersten drei Befehle definieren Zeichenfolgenvariablen, die für die *Parameter VaultName,* *Name* und *ContentType verwendet werden.* Der vierte Befehl verwendet das Get-AzKeyVaultKey-Cmdlet, um die angegebenen Schlüssel zu erhalten, und gibt die Schlüssel an das Update-AzKeyVaultSecret-Cmdlet weiter, um deren Inhaltstyp auf XML zu setzen.

## PARAMETER

### -ContentType
Inhaltstyp von Secret
Wenn nicht angegeben, bleibt der vorhandene Wert des Inhaltstyps des Geheimen unverändert.
Entfernen Sie den vorhandenen Inhaltstypwert, indem Sie eine leere Zeichenfolge angeben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Enable
Wenn vorhanden, aktivieren Sie einen Geheimtipp, wenn der Wert wahr ist.
Deaktivieren Sie einen Geheimtipp, wenn der Wert falsch ist.
Wenn nicht angegeben, bleibt der vorhandene Wert des aktivierten/deaktivierten Zustands des Geheimen unverändert.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Läuft ab
Die Ablaufzeit eines Geheimtipps in UTC-Zeit.
Wenn nicht angegeben, bleibt der vorhandene Wert der Ablaufzeit des Geheimen unverändert.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Geheimes Objekt

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

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
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Die UTC-Zeit, vor der geheime Daten nicht verwendet werden können.
Wenn nicht angegeben, bleibt der vorhandene Wert des NotBefore-Attributs des Geheimtipps unverändert.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Das Cmdlet gibt standardmäßig kein Objekt zurück.
Wenn dieser Schalter angegeben ist, geben Sie geheimes Objekt zurück.

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

### -Tag
Eine Hashtable, die geheime Tags darstellt.
Wenn nicht angegeben, bleiben die vorhandenen Tags des geheimen Schlüssels unverändert.
Entfernen Sie ein Tag, indem Sie eine leere Hashtable angeben.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Name des Tresors.
Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Geheime Version.
Das Cmdlet erstellt den FQDN eines Geheimnamens aus dem Tresor, der aktuell ausgewählten Umgebung, des geheimen Namens und der geheimen Version.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## NOTIZEN

## VERWANDTE LINKS
