---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842091"
---
# Set-AzKeyVaultSecretAttribute

## Synopsis
Aktualisiert Attribute eines Geheimnisses in einem schlüsseltresor.

## Syntax

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzKeyVaultSecretAttribute** " aktualisiert bearbeitbare Attribute eines geheimen Schlüssels in einem schlüsseltresor.

## Beispiele

### Beispiel 1: Ändern der Attribute eines geheimen Schlüssels
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

Die ersten vier Befehle definieren Attribute für das Ablaufdatum, das NotBefore-Datum, die Tags und den Kontexttyp und speichern die Attribute in Variablen.

Der endgültige Befehl ändert die Attribute für den geheimen Namen HR im schlüsseltresor mit dem Namen ContosoVault unter Verwendung der gespeicherten Variablen.

### Beispiel 2: Löschen der Kategorien und des Inhaltstyps für einen geheimen Schlüssel
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Mit diesem Befehl werden die Tags und der Inhaltstyp für die angegebene Version des geheimen namens HR im schlüsseltresor mit dem Namen "Contoso" gelöscht.

### Beispiel 3: Deaktivieren Sie die aktuelle Version von Secrets, deren Name mit ihr beginnt
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

Der erste Befehl speichert den Zeichenfolgenwert Contoso in der $Vault Variablen.

Der zweite Befehl speichert den Zeichenfolgenwert in der $prefix Variablen.

Der dritte Befehl verwendet das Get-AzKeyVaultSecret-Cmdlet, um die Geheimnisse im angegebenen schlüsseltresor abzurufen, und übergibt diese Geheimnisse dann an das Cmdlet **Where-Object** . Das Cmdlet **Where-Object** filtert die Geheimnisse für Namen, die mit den Zeichen beginnen. Der Befehl Pipes die Geheimnisse, die dem Filter entsprechen, mit dem Set-AzKeyVaultSecretAttribute-Cmdlet ab, wodurch Sie deaktiviert werden.

### Beispiel 4: Einrichten des ContentType für alle Versionen eines geheimen Schlüssels
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

Die ersten drei Befehle definieren Zeichenfolgenvariablen, die für die Parameter *vaultname* , *Name* und *ContentType* verwendet werden. Der vierte Befehl verwendet das Get-AzKeyVaultKey-Cmdlet, um die angegebenen Schlüssel abzurufen, und leitet die Schlüssel an das Set-AzKeyVaultSecretAttribute-Cmdlet weiter, um den Inhaltstyp auf XML festzulegen.

## Parameter

### -ContentType
Gibt den Inhaltstyp eines Geheimnisses an. Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am Inhaltstyp des aktuellen Schlüssels. Wenn Sie den vorhandenen Inhaltstyp entfernen möchten, geben Sie eine leere Zeichenfolge an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Gibt an, ob ein Schlüssel aktiviert werden soll. Geben Sie $false an, um einen Schlüssel zu deaktivieren, oder $true, um einen geheimen Schlüssel zu aktivieren. Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am aktivierten oder deaktivierten Zustand des aktuellen Schlüssels.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Läuft ab
Gibt das Datum und die Uhrzeit an, zu dem ein geheimer abläuft.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen eines Geheimnisses an. Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Gibt die koordinierte Weltzeit (Coordinated Universal Time, UTC) an, vor der der Schlüssel nicht verwendet werden kann.
Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am NotBefore-Attribut des aktuellen Geheimnisses.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen des zu ändernden Schlüsseldepots an.
Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuell ausgewählten Umgebung.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Version eines geheimen Schlüssels an.
Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. Secret
Gibt das Microsoft. Azure. Commands. keyvault. Models. Secret-Objekt zurück, wenn passthru angegeben ist. Andernfalls wird Nothing zurückgegeben.

## Notizen

## Verwandte Links

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)
