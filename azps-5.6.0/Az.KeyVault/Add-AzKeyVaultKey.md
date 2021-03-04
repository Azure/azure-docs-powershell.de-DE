---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b853e688330eda17f037381fc5105626e16d93fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919912"
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
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveCreate
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveImport
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
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
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectCreate
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectImport
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
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
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdCreate
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdImport
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Add-AzKeyVaultKey-Cmdlet** erstellt einen Schlüssel in einem Schlüsseltresor im Azure Key Vault, oder importiert einen Schlüssel in einen Schlüsseltresor.
Verwenden Sie dieses Cmdlet zum Hinzufügen von Schlüsseln mithilfe einer der folgenden Methoden:
- Erstellen Sie einen Schlüssel in einem Hardwaresicherheitsmodul (Hardware Security Module, HSM) im Key Vault-Dienst.
- Erstellen Sie einen Schlüssel in der Software im Key Vault-Dienst.
- Importieren Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul (HSM) in HSMs im Key Vault-Dienst.
- Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.
- Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer in Hardwaresicherheitsmodule (HSMs) im Schlüsseltresordienst.
Für jeden dieser Vorgänge können Sie Wichtige Attribute bereitstellen oder Standardeinstellungen akzeptieren.
Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel im Schlüsseltresor hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben. Sie können auf die vorherigen Werte zugreifen, indem Sie den versionsspezifischen URI für diese Version des Schlüssels verwenden. Informationen zu Schlüsselversionen und der URI-Struktur finden Sie unter [Informationen](http://go.microsoft.com/fwlink/?linkid=518560) zu Schlüsseln und Geheimnissen in der Rest-API-Dokumentation zum Schlüsseltresor.
Hinweis: Wenn Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul importieren möchten, müssen Sie zuerst ein BYOK-Paket (eine Datei mit einer Byok-Dateinamenerweiterung) mithilfe des Azure Key Vault BYOK-Toolsets generieren. Weitere Informationen finden Sie unter Generieren und Übertragen HSM-Protected [Schlüssel für azure key vault](http://go.microsoft.com/fwlink/?LinkId=522252).
Als bewährte Methode sollten Sie Ihren Schlüssel nach dem Erstellen oder Aktualisieren mithilfe des cmdlets Backup-AzKeyVaultKey sichern. Es gibt keine Rückgängig-Funktionalität. Wenn Sie also versehentlich Ihren Schlüssel löschen oder löschen und dann Ihre Meinung ändern, kann der Schlüssel nur wiederhergestellt werden, wenn Sie über eine Sicherung verfügen, die Sie wiederherstellen können.

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

Mit diesem Befehl wird im Schlüsseltresor Contoso ein softwaregeschützter Schlüssel namens ITSoftware erstellt.

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

Mit diesem Befehl wird im Schlüsseltresor Contoso ein HSM-geschützter Schlüssel erstellt.

### Beispiel 3: Erstellen eines Schlüssels mit nicht standardmäßigen Werten
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

Der erste Befehl speichert die Werte zum Entschlüsseln und Überprüfen in der $KeyOperations Variablen.
Der zweite Befehl erstellt ein **DateTime-Objekt,** das in UTC definiert ist, indem das **Get-Date-Cmdlet** verwendet wird.
Dieses Objekt gibt eine Zeit von zwei Jahren in der Zukunft an. Der Befehl speichert dieses Datum in der $Expires Variablen. Weitere Informationen finden Sie unter `Get-Help Get-Date` .
Der dritte Befehl erstellt ein **DateTime-Objekt** mithilfe des **Get-Date-Cmdlets.** Dieses Objekt gibt die aktuelle UTC-Zeit an. Der Befehl speichert dieses Datum in der $NotBefore Variablen.
Mit dem letzten Befehl wird ein Schlüssel namens ITHsmNonDefault erstellt, bei dem es sich um einen HSM-geschützten Schlüssel handelt. Der Befehl gibt Werte für zulässige Schlüsselvorgänge an, die $KeyOperations. Der Befehl gibt Zeiten für die Parameter *Expires* und *NotBefore* an, die in den vorherigen Befehlen erstellt wurden, sowie Tags für hohen Schweregrad und IT. Der neue Schlüssel ist deaktiviert. Sie können dies mithilfe des **Cmdlets Set-AzKeyVaultKey** aktivieren.

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

Mit diesem Befehl wird der Schlüssel mit dem Namen ITByok von dem Speicherort importiert, den der *Parameter KeyFilePath* angibt. Der importierte Schlüssel ist ein HSM-geschützter Schlüssel.
Um einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul zu importieren, müssen Sie zuerst ein BYOK-Paket (eine Datei mit einer Byok-Dateinamenerweiterung) mithilfe des Azure Key Vault BYOK-Toolsets generieren.
Weitere Informationen finden Sie unter Generieren und Übertragen HSM-Protected [Schlüssel für azure key vault](http://go.microsoft.com/fwlink/?LinkId=522252).

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

Der erste Befehl wandelt eine Zeichenfolge mithilfe des **Cmdlets ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen. Weitere Informationen finden Sie unter `Get-Help
ConvertTo-SecureString` .
Mit dem zweiten Befehl wird ein Softwarekennwort im Contoso-Schlüsseltresor erstellt. Der Befehl gibt den Speicherort für den Schlüssel und das Kennwort an, die in der $Password.

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

Der erste Befehl wandelt eine Zeichenfolge mithilfe des **Cmdlets ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen.
Mit dem zweiten Befehl wird ein **DateTime-Objekt** mithilfe des **Get-Date-Cmdlets** erstellt und dieses Objekt dann in der $Expires gespeichert.
Mit dem dritten Befehl wird die $tags erstellt, um Tags für hohen Schweregrad und IT zu setzen.
Der letzte Befehl importiert einen Schlüssel als HSM-Schlüssel aus dem angegebenen Speicherort. Der Befehl gibt die In-$Expires- und Kennwortzeit an, die in $Password gespeichert sind, und wendet die tags an, die in $tags.

### Beispiel 7: Generieren eines Key Exchange Key (KEK) für das Feature "Bring your own key" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Generiert einen Schlüssel (als Key Exchange Key (KEK) bezeichnet). Der KEK muss ein RSA-HSM-Schlüssel sein, der nur über den Importschlüsselvorgang verfügt. Nur Key Vault Premium SKU unterstützt RSA-HSM-Schlüssel.
Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys

## PARAMETER

### -CurveName
Gibt den Kurvennamen der elliptischen Kurvenkryptografie an. Dieser Wert ist gültig, wenn KeyType EC ist.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
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

### -Ziel
Gibt an, ob der Schlüssel als softwaregeschützter Schlüssel oder als HSM-geschützter Schlüssel im Schlüsseltresordienst hinzugefügt werden soll.
Gültige Werte sind: HSM und Software.
Hinweis: Wenn Sie HSM als Ziel verwenden möchten, müssen Sie über einen Schlüsseltresor verfügen, der HSMs unterstützt. Weitere Informationen zu den Dienstebenen und -funktionen für Azure Key Vault finden Sie auf der [Azure Key Vault Pricing-Website.](http://go.microsoft.com/fwlink/?linkid=512521)
Dieser Parameter ist erforderlich, wenn Sie einen neuen Schlüssel erstellen. Wenn Sie einen Schlüssel mithilfe des *Parameters KeyFilePath importieren,* ist dieser Parameter optional:
- Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel mit der Dateinamenerweiterung BYOK importiert, importiert es diesen Schlüssel als HSM-geschützten Schlüssel. Das Cmdlet kann diesen Schlüssel nicht als softwaregeschützten Schlüssel importieren.
- Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel importiert, der eine .pfx-Dateinamenerweiterung enthält, importiert es den Schlüssel als softwaregeschützten Schlüssel.

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
Gibt an, dass der hinzugefügte Schlüssel auf den anfangs deaktivierten Zustand festgelegt ist. Bei jedem Versuch, den Schlüssel zu verwenden, ist ein Fehler zu begehen. Verwenden Sie diesen Parameter, wenn Sie Schlüssel vorab laden, die Sie später aktivieren möchten.

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

### -Läuft ab
Gibt die Ablaufzeit als **DateTime-Objekt** für den Schlüssel an, den dieses Cmdlet hinzufügt. Für diesen Parameter wird koordinierte Universalzeit (UTC) verwendet. Verwenden Sie zum Abrufen eines **DateTime-Objekts** **das Get-Date-Cmdlet.** Weitere Informationen finden Sie unter `Get-Help Get-Date` . Wenn Sie diesen Parameter nicht angeben, läuft der Schlüssel nicht ab.

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

### -HsmName
HSM-Name. Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmObject
HSM-Objekt.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -HsmResourceId
Ressourcen-ID des HSM.

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Gibt ein Kennwort für die importierte Datei als **SecureString-Objekt** an. Verwenden Sie zum Abrufen eines **SecureString-Objekts** **das Cmdlet ConvertTo-SecureString.** Weitere Informationen finden Sie unter `Get-Help ConvertTo-SecureString` . Sie müssen dieses Kennwort angeben, um eine Datei mit der Dateierweiterung PFX zu importieren.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Gibt den Pfad einer lokalen Datei an, die wichtige Materialien enthält, die von diesem Cmdlet importiert werden.
Die gültigen Dateinamenerweiterungen sind BYOK und PFX.
- Wenn es sich bei der Datei um eine BYOK-Datei handelt, wird der Schlüssel nach dem Import automatisch durch HSMs geschützt, und Sie können diese Standardeinstellung nicht außer Kraft setzen.
- Wenn es sich bei der Datei um eine PFX-Datei handelt, wird der Schlüssel nach dem Import automatisch durch Software geschützt. Um diesen Standardwert außer Kraft zu setzen, legen Sie den *Parameter Ziel* auf HSM fest, damit der Schlüssel HSM-geschützt ist.
Wenn Sie diesen Parameter angeben, ist *der Parameter Ziel* optional.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Gibt ein Array von Vorgängen an, die mithilfe des Schlüssels ausgeführt werden können, den dieses Cmdlet hinzufügt.
Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.
Die zulässigen Werte für diesen Parameter sind eine durch Kommas getrennte Liste von Schlüsselvorgängen, die durch die [JSON Web Key (JWK)-Spezifikation definiert werden:](http://go.microsoft.com/fwlink/?LinkID=613300)
- Verschlüsseln
- Entschlüsseln
- wrapKey
- unwrapKey
- Signieren
- Überprüfen
- Import (nur für KEK siehe Beispiel 7)

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

### -KeyType
Gibt den Schlüsseltyp dieses Schlüssels an. Beim Importieren von BYOK-Schlüsseln wird standardmäßig "RSA" verwendet.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Schlüssels an, der dem Schlüsseltresor hinzugefügt werden soll. Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung. Der Name muss eine Zeichenfolge von 1 bis 63 Zeichen sein, die nur 0-9, a-z, A-Z und - (das Strichsymbol) enthält.

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
Gibt die Uhrzeit als **DateTime-Objekt** an, vor der der Schlüssel nicht verwendet werden kann. Dieser Parameter verwendet UTC. Verwenden Sie zum Abrufen eines **DateTime-Objekts** **das Get-Date-Cmdlet.** Wenn Sie diesen Parameter nicht angeben, kann der Schlüssel sofort verwendet werden.

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
Tresorressourcen-ID.

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
RSA-Schlüsselgröße in Bits. Wenn nicht angegeben, stellt der Dienst eine sichere Standardeinstellung zur Verfügung.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
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
Gibt den Namen des Schlüsseltresor an, dem dieses Cmdlet den Schlüssel hinzufügt. Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und ihrer aktuellen Umgebung.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## NOTIZEN

## VERWANDTE LINKS

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
