---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 8583a078e12be5da3a6bcbbe16bc3349f51b9bdb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296889"
---
# Add-AzKeyVaultKey

## Synopsis
Erstellt einen Schlüssel in einem schlüsseltresor oder importiert einen Schlüssel in einen schlüsseltresor.

## Syntax

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

## Beschreibung
Das Cmdlet **Add-AzKeyVaultKey** erstellt einen Schlüssel in einem schlüsseltresor im Azure Key Vault oder importiert einen Schlüssel in einen schlüsseltresor.
Verwenden Sie dieses Cmdlet, um Schlüssel mithilfe einer der folgenden Methoden hinzuzufügen:
- Erstellen Sie einen Schlüssel in einem Hardwaresicherheitsmodul (HSM) im Key Vault-Dienst.
- Erstellen Sie einen Schlüssel in Software im Key Vault-Dienst.
- Importieren Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul (HSM) zu HSMs im Key Vault-Dienst.
- Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.
- Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer in die Hardwaresicherheitsmodule (HSMs) des Key Vault-Diensts.
Für alle diese Vorgänge können Sie wichtige Attribute bereitstellen oder Standardeinstellungen akzeptieren.
Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel in Ihrem schlüsseltresor hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben. Sie können mithilfe des versionsspezifischen URIs für diese Version des Schlüssels auf die vorherigen Werte zugreifen. Informationen zu Schlüssel Versionen und der URI-Struktur finden Sie unter [Informationen zu Schlüsseln und Geheimnissen](http://go.microsoft.com/fwlink/?linkid=518560) in der Key Vault-Ruhe API-Dokumentation.
Hinweis: Wenn Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul importieren möchten, müssen Sie zunächst ein BYOK-Paket (eine Datei mit der Dateinamenerweiterung. BYOK) mithilfe des Azure Key Vault-BYOK-Toolsets erstellen. Weitere Informationen finden Sie unter [so wird es gemacht: generieren und übertragen von HSM-Protected Schlüsseln für Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).
Als bewährte Methode können Sie mithilfe des Backup-AzKeyVaultKey-Cmdlets Ihren Schlüssel nach dem Erstellen oder aktualisieren sichern. Es gibt keine Funktion zur Undelete-Funktion, wenn Sie Ihren Schlüssel versehentlich löschen oder löschen und dann Ihre Vorstellung ändern, ist der Schlüssel nicht wiederherstellbar, es sei denn, Sie haben eine Sicherungskopie davon, die Sie wiederherstellen können.

## Beispiele

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

Dieser Befehl erstellt einen Software geschützten Schlüssel mit dem Namen ITSoftware im schlüsseltresor mit dem Namen contoso.

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

Mit diesem Befehl wird im schlüsseltresor mit dem Namen Contoso ein HSM-geschützter Schlüssel erstellt.

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

Der erste Befehl speichert die Werte, die entschlüsselt und in der $KeyOperations Variablen überprüft werden.
Mit dem zweiten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt, das in UTC definiert ist.
Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an. Der Befehl speichert dieses Datum in der $Expires Variablen. Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .
Der dritte Befehl erstellt mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt. Dieses Objekt gibt die aktuelle UTC-Zeit an. Der Befehl speichert dieses Datum in der $NotBefore Variablen.
Der endgültige Befehl erstellt einen Schlüssel mit dem Namen ITHsmNonDefault, bei dem es sich um einen HSM-geschützten Schlüssel handelt. Der Befehl gibt Werte für zulässige Schlüsselvorgänge an, die $KeyOperations gespeichert sind. Der Befehl gibt die Zeiten für die in den vorherigen Befehlen erstellten Ablauf-und *NotBefore* -Parameter sowie die Tags für den höchsten Schweregrad und das *Datum* an. Der neue Schlüssel ist deaktiviert. Sie können es mithilfe des Cmdlets " **festlegen-AzKeyVaultKey** " aktivieren.

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

Dieser Befehl importiert den Schlüssel mit dem Namen ITByok von dem Speicherort, der vom *keyFilePath* -Parameter angegeben wird. Der importierte Schlüssel ist ein HSM-geschützter Schlüssel.
Wenn Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul importieren möchten, müssen Sie zunächst ein BYOK-Paket (eine Datei mit der Dateinamenerweiterung. BYOK) mithilfe des Azure Key Vault-BYOK-Toolsets erstellen.
Weitere Informationen finden Sie unter [so wird es gemacht: generieren und übertragen von HSM-Protected Schlüsseln für Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).

### Beispiel 5: Importieren eines Software geschützten Schlüssels
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

Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen. Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .
Der zweite Befehl erstellt ein Software Kennwort im Contoso-Schlüsselspeicher. Der Befehl gibt den Speicherort für den Schlüssel und das Kennwort an, das in $Password gespeichert ist.

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

Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen.
Der zweite Befehl erstellt mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt und speichert dieses Objekt dann in der $Expires-Variablen.
Mit dem dritten Befehl wird die $Tags-Variable erstellt, um Tags für einen höheren Schweregrad und die Variable festzulegen.
Der endgültige Befehl importiert einen Schlüssel als HSM-Schlüssel vom angegebenen Speicherort. Der Befehl gibt die Ablaufzeit an, die in $Expires und dem in $Password gespeicherten Kennwort gespeichert ist, und wendet die in $Tags gespeicherten Tags an.

### Beispiel 7: Generieren eines Schlüsselaustausch Schlüssels (KEK) für das Feature "eigene Schlüssel bringen" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Generiert einen Schlüssel (wird als Schlüsselaustauschschlüssel (KEK) bezeichnet). Bei der KEK muss es sich um einen RSA-HSM-Schlüssel mit nur dem Import Schlüssel Vorgang handeln. Nur Key Vault Premium-SKU unterstützt RSA-HSM-Schlüssel.
Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt an, ob der Schlüssel als Software geschützter Schlüssel oder als HSM-geschützter Schlüssel im Key Vault-Dienst hinzugefügt werden soll.
Gültige Werte sind: HSM und Software.
Hinweis: Wenn Sie HSM als Ziel verwenden möchten, müssen Sie über einen schlüsseltresor verfügen, der HSMs unterstützt. Weitere Informationen zu den Dienstebenen und Funktionen für Azure Key Vault finden Sie auf der [Azure Key Vault-Preis Website](http://go.microsoft.com/fwlink/?linkid=512521).
Dieser Parameter ist erforderlich, wenn Sie einen neuen Schlüssel erstellen. Wenn Sie einen Schlüssel mithilfe des *keyFilePath* -Parameters importieren, ist dieser Parameter optional:
- Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel importiert, der über die Dateinamenerweiterung Byok verfügt, wird dieser Schlüssel als HSM-geschützter Schlüssel importiert. Das Cmdlet kann diesen Schlüssel nicht als Software geschützten Schlüssel importieren.
- Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel importiert, der über die Dateinamenerweiterung PFX verfügt, wird der Schlüssel als Software geschützter Schlüssel importiert.

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

### -Deaktivieren Sie
Gibt an, dass der hinzuzufügende Schlüssel auf den Anfangszustand disabled festgesetzt ist. Jeder Versuch, den Schlüssel zu verwenden, schlägt fehl. Verwenden Sie diesen Parameter, wenn Sie Schlüssel Vorabladen, die Sie später aktivieren möchten.

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
Gibt die Ablaufzeit als **DateTime** -Objekt für den Schlüssel an, den dieses Cmdlet hinzufügt. Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC). Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen. Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` . Wenn Sie diesen Parameter nicht angeben, läuft der Schlüssel nicht ab.

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

### -Inputobject
Vault-Objekt

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
Gibt ein Kennwort für die importierte Datei als **SecureString** -Objekt an. Verwenden Sie zum Abrufen eines **SecureString** -Objekts das Cmdlet **ConvertTo-SecureString** . Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` . Sie müssen dieses Kennwort angeben, um eine Datei mit der Dateinamenerweiterung PFX zu importieren.

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
Gibt den Pfad einer lokalen Datei an, die das Schlüsselmaterial enthält, das von diesem Cmdlet importiert wird.
Die gültigen Dateinamenerweiterungen sind Byok und PFX.
- Wenn es sich bei der Datei um eine Byok-Datei handelt, wird der Schlüssel nach dem Import automatisch durch HSMs geschützt, und Sie können diesen Standardwert nicht außer Kraft setzen.
- Wenn es sich bei der Datei um eine PFX-Datei handelt, wird der Schlüssel nach dem Import automatisch durch Software geschützt. Um diesen Standardwert zu überschreiben, setzen Sie den *Ziel* Parameter auf HSM, damit der Schlüssel HSM-geschützt ist.
Wenn Sie diesen Parameter angeben, ist der *Ziel* Parameter optional.

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
Gibt ein Array von Vorgängen an, die mit dem vom Cmdlet hinzugefügten Schlüssel ausgeführt werden können.
Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.
Bei den akzeptablen Werten für diesen Parameter handelt es sich um eine durch trennzeichengetrennte Liste der wichtigsten Vorgänge, wie Sie in der [JSON Web Key (JWK)-Spezifikation](http://go.microsoft.com/fwlink/?LinkID=613300)definiert ist:
- Verschlüsseln
- Entschlüsseln
- wrapKey
- unwrapKey
- melden sich
- prüfen
- Importieren (nur für KEK, siehe Beispiel 7)

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
Gibt den Namen des Schlüssels an, der dem schlüsseltresor hinzugefügt werden soll. Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung. Der Name muss eine Zeichenfolge von 1 bis 63 Zeichen lang sein, die nur 0-9, a-z, a-z und-(das Strichsymbol) enthält.

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
Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann. Dieser Parameter verwendet UTC. Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen. Wenn Sie diesen Parameter nicht angeben, kann der Schlüssel sofort verwendet werden.

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

### -Resourcen-Nr
Vault-Ressourcen-ID.

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
RSA-Schlüsselgröße in Bits. Wenn keine Angabe erfolgt, stellt der Dienst einen sicheren Standard bereit.

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
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}

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

### -Vaultname
Gibt den Namen des Schlüsselspeichers an, dem dieses Cmdlet den Schlüssel hinzufügt. Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVault

### System. String

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey

## Notizen

## Verwandte Links

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Satz-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
