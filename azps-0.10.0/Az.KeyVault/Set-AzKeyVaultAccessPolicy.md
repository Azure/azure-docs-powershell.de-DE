---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a774c438f9be25dc55f48c5121031956374a2cb7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007575"
---
# Set-AzKeyVaultAccessPolicy

## Synopsis
Gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um Vorgänge mit einem schlüsseltresor durchzuführen.

## Syntax

### ByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectId
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ForVault
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzKeyVaultAccessPolicy** " gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um die angegebenen Vorgänge mit einem schlüsseltresor durchzuführen. Die Berechtigungen, die andere Benutzer, Anwendungen oder Sicherheitsgruppen im schlüsseltresor haben, werden nicht geändert.

Wenn Sie Berechtigungen für eine Sicherheitsgruppe festlegen, betrifft dieser Vorgang nur Benutzer in dieser Sicherheitsgruppe.

Die folgenden Verzeichnisse müssen alle das gleiche Azure-Verzeichnis aufweisen:
- Das Standardverzeichnis des Azure-Abonnements, in dem sich der Schlüsselspeicher befindet.
- Das Azure-Verzeichnis, in dem sich der Benutzer oder die Anwendungsgruppe befindet, dem Sie Berechtigungen erteilen.

Beispiele für Szenarien, in denen diese Bedingungen nicht erfüllt sind und dieses Cmdlet nicht funktioniert, sind:

- Autorisieren eines Benutzers aus einer anderen Organisation zum Verwalten Ihres Schlüsseldepots
Jede Organisation verfügt über ein eigenes Verzeichnis.
- Ihr Azure-Konto verfügt über mehrere Verzeichnisse.
Wenn Sie eine Anwendung in einem anderen Verzeichnis als dem Standardverzeichnis registrieren, können Sie diese Anwendung nicht autorisieren, um Ihren schlüsseltresor zu verwenden.
Die Anwendung muss sich im Standardverzeichnis befinden.

Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, um eine bessere Leistung zu erzielen.

## Beispiele

### Beispiel 1: Erteilen von Berechtigungen für einen Benutzer für einen schlüsseltresor und Ändern der Berechtigungen
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

Der erste Befehl gewährt einem Benutzer in Azure Active Directory Berechtigungen, PattiFuller@contoso.com um Vorgänge für Schlüssel und Geheimnisse mit einem schlüsseltresor mit dem Namen Contoso03Vault durchzuführen.

Mit dem zweiten Befehl werden die Berechtigungen geändert, die PattiFuller@contoso.com im ersten Befehl gewährt wurden, sodass Sie nun zusätzlich zu den Einstellungen und Löschungen auch Geheimnisse erhalten. Die Berechtigungen für Schlüsselvorgänge bleiben nach diesem Befehl unverändert. Der *passthru* -Parameter führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.

Der endgültige Befehl ändert weiterhin die vorhandenen Berechtigungen für PattiFuller@contoso.com , um alle Berechtigungen für wichtige Vorgänge zu entfernen. Die Berechtigungen für geheime Vorgänge bleiben nach diesem Befehl unverändert. Der *passthru* -Parameter führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.

### Beispiel 2: Erteilen von Berechtigungen für einen Anwendungsdienst Prinzipal zum Lesen und Schreiben von Geheimnissen
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

Dieser Befehl gewährt Berechtigungen für eine Anwendung für einen schlüsseltresor mit dem Namen Contoso03Vault.

Der *servicePrincipalName* -Parameter gibt die Anwendung an. Die Anwendung muss in Ihrem Azure Active Directory registriert sein. Der Wert des *servicePrincipalName* -Parameters muss entweder der Dienstprinzipalname der Anwendung oder die GUID der Anwendungs-ID sein.

In diesem Beispiel wird der Dienstprinzipalname angegeben `http://payroll.contoso.com` , und der Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.

### Beispiel 3: Erteilen von Berechtigungen für eine Anwendung unter Verwendung der Objekt-ID
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

Dieser Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.

In diesem Beispiel wird die Anwendung mit der Objekt-ID des Dienst Prinzipals der Anwendung angegeben.

### Beispiel 4: Erteilen von Berechtigungen für einen Benutzerprinzipalnamen
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

Dieser Befehl gewährt Get-, List-und festgelegte Berechtigungen für den angegebenen Benutzerprinzipalnamen für den Zugriff auf Geheimnisse.

### Beispiel 5: Aktivieren von "Secrets" aus einem Vault Vault-Tresor durch den Microsoft. Compute-Ressourcenanbieter
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

Dieser Befehl gewährt die Berechtigungen für Geheimnisse, die vom Contoso03Vault-schlüsseltresor vom Microsoft. Compute-Ressourcenanbieter abgerufen werden.

### Beispiel 6: Erteilen von Berechtigungen für eine Sicherheitsgruppe
```
PS C:\>Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

Der erste Befehl verwendet das Get-AzADGroup-Cmdlet, um alle Active Directory-Gruppen abzurufen. In der Ausgabe werden drei zurückgegebene Gruppen mit dem Namen " **group1** ", " **group2** " und " **Gruppe3** " angezeigt. Mehrere Gruppen können denselben Namen haben, aber immer eine eindeutige ObjectID aufweisen. Wenn mehr als eine Gruppe mit demselben Namen zurückgegeben wird, verwenden Sie die ObjectID in der Ausgabe, um die gewünschte Gruppe zu identifizieren.

Anschließend verwenden Sie die Ausgabe dieses Befehls mit Set-AzKeyVaultAccessPolicy, um group2-Berechtigungen für Ihren schlüsseltresor mit dem Namen **myownvault** zu erteilen. In diesem Beispiel werden die Gruppen mit dem Namen "group2" Inline in der gleichen Befehlszeile aufgelistet.

In der zurückgegebenen Liste können mehrere Gruppen mit dem Namen "group2" vorhanden sein.
In diesem Beispiel wird das erste Element mit dem Index \[ 0 \] in der zurückgegebenen Liste markiert.

### Beispiel 7: Gewähren des Azure Information Protection-Zugriffs auf den vom Kunden verwalteten Mandanten Schlüssel (BYOK)
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

Mit diesem Befehl wird der Azure-Informationsschutz autorisiert, einen vom Kunden verwalteten Schlüssel (das Szenario "eigene Schlüssel" oder "BYOK") als Azure Information Protection-Mandanten Schlüssel zu verwenden.

Wenn Sie diesen Befehl ausführen, geben Sie Ihren eigenen schlüsseltresor Namen an, aber Sie müssen den *servicePrincipalName* -Parameter mit der GUID **00000012-0000-0000-C000-000000000000** angeben und die Berechtigungen im Beispiel angeben.

## Parameter

### -ApplicationId
Für die spätere Verwendung.

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BypassObjectIdValidation
Ermöglicht es Ihnen, eine Objekt-ID anzugeben, ohne zu überprüfen, ob das Objekt in Azure Active Directory vorhanden ist.

Verwenden Sie diesen Parameter nur, wenn Sie einer Objekt-ID, die sich auf eine delegierte Sicherheitsgruppe aus einem anderen Azure-Mandanten bezieht, Zugriff auf Ihren schlüsseltresor gewähren möchten.

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
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

### -Email-Email
Gibt die e-Mail-Adresse des Benutzers an, dem Sie Berechtigungen erteilen möchten.

Diese e-Mail-Adresse muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist, und eindeutig sein.

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDeployment
Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Gibt die Objekt-ID des Benutzers oder Dienst Prinzipals in Azure Active Directory an, für den Berechtigungen erteilt werden sollen.

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases:

Required: True
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

### -PermissionsToCertificates
Gibt ein Array von Zertifikat Berechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.

Die zulässigen Werte für diesen Parameter:

- Erhalten
- Liste
- Löschen
- Erstellen
- Importieren
- Aktualisieren
- Managecontacts
- Getissuer
- Listissuers
- Setissuer
- Deleteissuers
- Manageissuers

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PermissionsToKeys
Gibt ein Array von Schlüssel Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.

Die zulässigen Werte für diesen Parameter:

- Entschlüsseln
- Verschlüsseln
- UnwrapKey
- WrapKey
- Prüfen
- Melden sich
- Erhalten
- Liste
- Aktualisieren
- Erstellen
- Importieren
- Löschen
- Backup
- Wiederherstellungs
- Wiederherstellen
- Purge

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PermissionsToSecrets
Gibt ein Array von geheimen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.

Die zulässigen Werte für diesen Parameter:

- Erhalten
- Liste
- Einrichten
- Löschen
- Backup
- Wiederherstellungs
- Wiederherstellen
- Purge

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PermissionsToStorage
Gibt die Berechtigungen des verwalteten speicherkontos und des SAS-Definitionsvorgangs an, die einem Benutzer oder Dienstprinzipal gewährt werden.

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Gibt den Dienstprinzipalnamen der Anwendung an, der Berechtigungen erteilt werden sollen.

Geben Sie die Anwendungs-ID (auch Client-ID genannt) an, die für die Anwendung im AzureActive-Verzeichnis registriert wurde. Die Anwendung mit dem Dienstprinzipalnamen, den dieser Parameter angibt, muss im Azure-Verzeichnis registriert sein, in dem sich das aktuelle Abonnement befindet.

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Gibt den Benutzerprinzipalnamen des Benutzers an, dem Sie Berechtigungen erteilen möchten.

Dieser Benutzerprinzipalname muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen eines Schlüsseldepots an.

Mit diesem Cmdlet wird die Zugriffsrichtlinie für den schlüsseltresor geändert, den dieser Parameter angibt.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### String, Guid, String [], Switch

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSVault

## Notizen

## Verwandte Links

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVaultAccessPolicy](./Remove-AzKeyVaultAccessPolicy.md)

