---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 3d0f7267d1dbe899de0e0414c52a395985f09bfd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412536"
---
# Add-AzKeyVaultKey

## SYNOPSIS
Erstellt einen Schlüssel in einem Schlüsseltresor oder importiert einen Schlüssel in einen Schlüsseltresor.

## SYNTAX

### InteractiveCreate (Standard)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzKeyVaultKey"** erstellt einen Schlüssel in einem Schlüsseltresor im Azure Key Vault oder importiert einen Schlüssel in einen Schlüsseltresor.
Verwenden Sie dieses Cmdlet zum Hinzufügen von Schlüsseln mit einer der folgenden Methoden:
- Erstellen Sie einen Schlüssel in einem Hardwaresicherheitsmodul (Hardware Security Module, HSM) im Key Vault-Dienst.
- Erstellen Sie einen Schlüssel in der Software im Schlüsseltresordienst.
- Importieren Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul (Hardware Security Module, HSM) in HSMs im Key Vault-Dienst.
- Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.
- Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer in Hardwaresicherheitsmodule (Hardware Security Module, HSMs) im Key Vault-Dienst.
Für jede dieser Vorgänge können Sie Schlüsselattribute bereitstellen oder Standardeinstellungen akzeptieren.
Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel in Ihrem Schlüsseltresor hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben. Sie können auf die vorherigen Werte zugreifen, indem Sie den versionsspezifischen URI für diese Version des Schlüssels verwenden. Informationen zu Schlüsselversionen und der URI-Struktur finden Sie [in](http://go.microsoft.com/fwlink/?linkid=518560) der Rest-API-Dokumentation zu Schlüsseln und Geheimen Schlüsseln.
Hinweis: Um einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul zu importieren, müssen Sie zuerst mithilfe des Azure Key Vault BYOK Toolset ein "BYOK"-Paket (eine Datei mit der Dateinamenerweiterung BYOK) generieren. Weitere Informationen finden Sie unter "Generieren und Übertragen HSM-Protected [Schlüssel für den Azure Key Vault".](http://go.microsoft.com/fwlink/?LinkId=522252)
Als bewährte Methode sollten Sie Ihren Schlüssel nach dem Erstellen oder Aktualisieren sichern, indem Sie das cmdlet Backup-AzKeyVaultKey verwenden. Es gibt keine rückgängig gemachten Funktionen. Wenn Sie also versehentlich Ihren Schlüssel löschen oder ihn löschen und dann Ihre Meinung ändern, kann der Schlüssel nur wiederhergestellt werden, wenn Sie über eine Sicherung verfügen, die Sie wiederherstellen können.

## BEISPIELE

### Beispiel 1: Erstellen eines Schlüssels
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Mit diesem Befehl wird ein softwaregeschützter Schlüssel namens "ITSoftware" im Schlüsseltresor "Contoso" erstellt.

### Beispiel 2: Erstellen eines HSM-geschützten Schlüssels
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Mit diesem Befehl wird ein HSM-geschützter Schlüssel im Schlüsseltresor "Contoso" erstellt.

### Beispiel 3: Erstellen eines Schlüssels mit Nicht-Standardwerten
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Der erste Befehl speichert die Werte zum Entschlüsseln und Überprüfen in der $KeyOperations Variable.
Der zweite Befehl erstellt ein in UTC definiertes **DateTime-Objekt** mithilfe des **Get-Date-Cmdlets.**
Dieses Objekt gibt eine Uhrzeit in zwei Jahren in der Zukunft an. Der Befehl speichert dieses Datum in der $Expires Variable. Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.
Der dritte Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein **DateTime-Objekt.** Dieses Objekt gibt die aktuelle UTC-Uhrzeit an. Der Befehl speichert dieses Datum in der $NotBefore Variable.
Der letzte Befehl erstellt einen Schlüssel namens ITHsmNonDefault, bei dem es sich um einen HSM-geschützten Schlüssel handelt. Der Befehl gibt Werte für zulässige Schlüsselvorgänge an, die $KeyOperations. Der Befehl gibt Zeiten für die in den vorherigen Befehlen erstellten Parameter *"Expires"* und *"NotBefore"* sowie Tags für hohen Schweregrad und IT an. Der neue Schlüssel ist deaktiviert. Sie können es mithilfe des **Cmdlets "Set-AzKeyVaultKey"** aktivieren.

### Beispiel 4: Importieren eines HSM-geschützten Schlüssels
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Mit diesem Befehl wird der Schlüssel "ITByok" von dem vom *Parameter "KeyFilePath"* angegebenen Speicherort importiert. Der importierte Schlüssel ist ein HSM-geschützter Schlüssel.
Um einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul zu importieren, müssen Sie zuerst mithilfe des Azure Key Vault BYOK Toolset ein "BYOK"-Paket (eine Datei mit der Dateinamenerweiterung BYOK) generieren.
Weitere Informationen finden Sie unter "Generieren und Übertragen HSM-Protected [Schlüssel für den Azure Key Vault".](http://go.microsoft.com/fwlink/?LinkId=522252)

### Beispiel 5: Importieren eines softwaregeschützten Schlüssels
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Password Variable. Weitere Informationen erhalten Sie, wenn Sie " `Get-Help
ConvertTo-SecureString` eingeben" aus.
Der zweite Befehl erstellt ein Softwarekennwort im Contoso-Schlüsseltresor. Der Befehl gibt den Speicherort für den Schlüssel und das Kennwort an, die in der Datei $Password.

### Beispiel 6: Importieren eines Schlüssels und Zuweisen von Attributen
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Password Variable.
Der zweite Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein **DateTime-Objekt** und speichert dieses Objekt dann in der $Expires Variable.
Der dritte Befehl erstellt die $tags Variable zum Festlegen von Tags für hohen Schweregrad und IT.
Der endgültige Befehl importiert einen Schlüssel als HSM-Schlüssel von der angegebenen Position. Der Befehl gibt die in der Datei gespeicherte $Expires und das Kennwort an und wendet die in $Password gespeicherten Tags $tags.

## PARAMETERS

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

### -Destination
Gibt an, ob der Schlüssel als softwaregeschützter Oder HSM-geschützter Schlüssel im Schlüsseltresordienst hinzugefügt werden soll.
Gültige Werte sind: HSM und Software.
Hinweis: Wenn Sie HSM als Ziel verwenden möchten, müssen Sie über einen Schlüsseltresor verfügen, der HSMs unterstützt. Weitere Informationen zu den Dienststufen und -funktionen für den Azure Key Vault finden Sie auf der Website "Preise für [den Azure Key Vault".](http://go.microsoft.com/fwlink/?linkid=512521)
Dieser Parameter ist erforderlich, wenn Sie einen neuen Schlüssel erstellen. Wenn Sie einen Schlüssel mithilfe des Parameters *"KeyFilePath"* importieren, ist dieser Parameter optional:
- Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel mit der Dateinamenerweiterung BYOK importiert, wird dieser Schlüssel als HSM-geschützter Schlüssel importiert. Das Cmdlet kann diesen Schlüssel nicht als softwaregeschützten Schlüssel importieren.
- Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel mit der Dateinamenerweiterung PFX importiert, importiert es den Schlüssel als softwaregeschützten Schlüssel.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Gibt an, dass der hinzugefügte Schlüssel auf den anfänglichen Status "Deaktiviert" festgelegt ist. Jeder Versuch, den Schlüssel zu verwenden, ist fehlgeschlagen. Verwenden Sie diesen Parameter, wenn Sie Schlüssel vorab laden, die Sie später aktivieren möchten.

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

### -Expires
Gibt die Ablaufzeit als **"DateTime"-Objekt** für den Schlüssel an, den dieses Cmdlet hinzufügt. Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC). Verwenden Sie das Get-Date-Cmdlet, um **ein "DateTime"-Objekt** zu erhalten.  Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus. Wenn Sie diesen Parameter nicht angeben, läuft der Schlüssel nicht ab.

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
Vault-Objekt.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Gibt ein Kennwort für die importierte Datei als **SecureString-Objekt** an. Verwenden Sie zum **Abrufen eines SecureString-Objekts** **das Cmdlet ConvertTo-SecureString.** Weitere Informationen erhalten Sie, wenn Sie " `Get-Help ConvertTo-SecureString` eingeben" aus. Sie müssen dieses Kennwort angeben, um eine Datei mit der Dateinamenerweiterung PFX zu importieren.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Gibt den Pfad einer lokalen Datei an, die Schlüsselmaterial enthält, das von diesem Cmdlet importiert wird.
Die gültigen Dateinamenerweiterungen sind BYOK und PFX.
- Wenn es sich bei der Datei um eine byok-Datei handelt, wird der Schlüssel nach dem Import automatisch durch HSMs geschützt, und Sie können diesen Standard nicht überschreiben.
- Handelt es sich bei der Datei um eine PFX-Datei, wird der Schlüssel nach dem Import automatisch durch Software geschützt. Um diesen Standard außer Kraft zu setzen, legen Sie den *Zielparameter* auf HSM fest, damit der Schlüssel HSM-geschützt ist.
Wenn Sie diesen Parameter angeben, ist der *Zielparameter* optional.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Gibt ein Array von Vorgängen an, die mit dem von diesem Cmdlet hinzugefügten Schlüssel ausgeführt werden können.
Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.
Bei den zulässigen Werten für diesen Parameter handelt es sich um eine durch Kommas getrennte Liste von Schlüsselvorgängen gemäß der [JSON Web Key (JWK)-Spezifikation:](http://go.microsoft.com/fwlink/?LinkID=613300)
- Verschlüsseln
- Entschlüsseln
- Umbruch
- Entpacken
- Signieren
- Überprüfen

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Schlüssels an, der dem Schlüsseltresor hinzugefügt werden soll. Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung. Der Name muss eine Zeichenfolge von 1 bis 63 Zeichen lang sein, die nur 0-9, a-z, A-Z und - (das Strichsymbol) enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Gibt die Uhrzeit als **"DateTime"-Objekt** an, vor dem der Schlüssel nicht verwendet werden kann. Dieser Parameter verwendet UTC. Verwenden Sie das Get-Date-Cmdlet, um **ein "DateTime"-Objekt** zu erhalten.  Wenn Sie diesen Parameter nicht angeben, kann der Schlüssel sofort verwendet werden.

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

### -ResourceId
Vault Resource Id.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
RSA-Schlüsselgröße, in Bits. Wenn nichts angegeben wird, stellt der Dienst einen sicheren Standardwert zur Verfügung.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"}

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
Gibt den Namen des Schlüsseltresor an, dem dieses Cmdlet den Schlüssel hinzufügt. Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

