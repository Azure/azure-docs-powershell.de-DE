---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469507"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
Aktualisiert die Attribute eines Geheimschlüssels in einem Schlüsseltresor.

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
Das **Cmdlet "Update-AzKeyVaultSecret"** aktualisiert bearbeitbare Attribute eines geheimen Schlüssels in einem Schlüsseltresor.

## BEISPIELE

### Beispiel 1: Ändern der Attribute eines geheimen Schlüssels
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

Die ersten vier Befehle definieren Attribute für das Ablaufdatum, das NotBefore-Datum, Tags und den Kontexttyp und speichern die Attribute in Variablen.
Der letzte Befehl ändert die Attribute für den geheimen Namen "HR" im Schlüsseltresor "ContosoVault" unter Verwendung der gespeicherten Variablen.

### Beispiel 2: Löschen der Tags und des Inhaltstyps eines geheimen Schlüssels
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Mit diesem Befehl werden die Tags und der Inhaltstyp für die angegebene Version des geheimen Namens "HR" im Schlüsseltresor "Contoso" gelöscht.

### Beispiel 3: Deaktivieren der aktuellen Version von geheimen Daten, deren Name mit der IT beginnt
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

Der erste Befehl speichert den Zeichenfolgenwert "Contoso" in der $Vault Variable.
Der zweite Befehl speichert den Zeichenfolgenwert IT in der $Prefix Variable.
Der dritte Befehl verwendet das Get-AzKeyVaultSecret-Cmdlet, um die geheimen Daten im angegebenen Schlüsseltresor zu erhalten, und übergibt diese anschließend an das **Where-Object-Cmdlet.** Das **Cmdlet "Where-Object"** filtert die geheimen Daten nach Namen, die mit den Zeichen IT beginnen. Der Befehl gibt die geheimen Daten, die dem Filter entsprechen, Update-AzKeyVaultSecret an das Cmdlet weiter, wodurch sie deaktiviert werden.

### Beispiel 4: Festlegen des Inhaltstyps für alle Versionen eines geheimen Schlüssels
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

Die ersten drei Befehle definieren Zeichenfolgenvariablen, die für die Parameter *VaultName,* *Name* und *ContentType verwendet werden.* Der vierte Befehl verwendet das Get-AzKeyVaultKey-Cmdlet, um die angegebenen Schlüssel zu erhalten, und gibt die Schlüssel an das cmdlet Update-AzKeyVaultSecret weiter, um den Inhaltstyp auf XML zu setzen.

## PARAMETERS

### -ContentType
Inhaltstyp des Geheimen
Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Inhaltstyps des Geheimen unverändert.
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
Wenn vorhanden, aktivieren Sie einen geheimen Wert, wenn der Wert wahr ist.
Deaktivieren Sie einen geheimen Wert, wenn der Wert falsch ist.
Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Status "Aktiviert/Deaktiviert" des Geheimen unverändert.

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

### -Expires
Die Ablaufzeit eines Geheimen in UTC.
Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert der Ablaufzeit des Geheimen unverändert.

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
Das Cmdlet erstellt den FQDN eines Geheimen aus dem Namen des Tresors, die aktuell ausgewählte Umgebung und den geheimen Namen.

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
Die UTC-Zeit, vor der der geheime Schlüssel nicht verwendet werden kann.
Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Attributs "NotBefore" des Geheimen unverändert.

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
Das Cmdlet gibt das Objekt standardmäßig nicht zurück.
Wenn dieser Schalter angegeben ist, geben Sie das geheime Objekt zurück.

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
Wenn nichts angegeben wird, bleiben die vorhandenen Tags des geheimen Schlüssels unverändert.
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
Das Cmdlet erstellt den FQDN eines Geheimen aus dem Tresornamen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
