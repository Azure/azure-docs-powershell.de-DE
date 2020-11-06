---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://go.microsoft.com/fwlink/?LinkId=690163
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 9ebf606a41a3a972b2d636846fbdc7834388ef29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504101"
---
# Set-AzureRmKeyVaultAccessPolicy

## Synopsis
Gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um Vorgänge mit einem schlüsseltresor durchzuführen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByServicePrincipalName
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByUserPrincipalName
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectId
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByEmailAddress
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ForVault
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmKeyVaultAccessPolicy** " gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um die angegebenen Vorgänge mit einem schlüsseltresor durchzuführen.
Die Berechtigungen, die andere Benutzer, Anwendungen oder Sicherheitsgruppen im schlüsseltresor haben, werden nicht geändert.

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

### Beispiel 1: Erteilen von Berechtigungen für einen Benutzer für einen Key Vault-schlüsseltresor und Ändern des permissionskey-Tresors
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets 'set,delete'
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

Der erste Befehl gewährt einem Benutzer in Azure Active Directory Berechtigungen, PattiFuller@contoso.com um Vorgänge für Schlüssel und Geheimnisse mit einem schlüsseltresor mit dem Namen Contoso03Vault durchzuführen.

Mit dem zweiten Befehl werden die Berechtigungen geändert, die PattiFuller@contoso.com im ersten Befehl gewährt wurden, sodass Sie nun zusätzlich zu den Einstellungen und Löschungen auch Geheimnisse erhalten.
Die Berechtigungen für Schlüsselvorgänge bleiben nach diesem Befehl unverändert.
Der *passthru* -Parameter führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.

Der endgültige Befehl ändert weiterhin die vorhandenen Berechtigungen für PattiFuller@contoso.com , um alle Berechtigungen für wichtige Vorgänge zu entfernen.
Die Berechtigungen für geheime Vorgänge bleiben nach diesem Befehl unverändert.
Der *passthru* -Parameter führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.

### Beispiel 2: Erteilen von Berechtigungen für einen Anwendungsdienst Prinzipal zum Lesen und Schreiben von Geheimnissen
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

Dieser Befehl gewährt Berechtigungen für eine Anwendung für einen schlüsseltresor mit dem Namen Contoso03Vault.
Der *servicePrincipalName* -Parameter gibt die Anwendung an.
Die Anwendung muss in Ihrem Azure Active Directory registriert sein.
Der Wert des *servicePrincipalName* -Parameters muss entweder der Dienstprinzipalname der Anwendung oder die GUID der Anwendungs-ID sein.
In diesem Beispiel wird der Dienstprinzipalname angegeben http://payroll.contoso.com , und der Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.

### Beispiel 3: Erteilen von Berechtigungen für eine Anwendung unter Verwendung der Objekt-ID
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

Dieser Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.
In diesem Beispiel wird die Anwendung mit der Objekt-ID des Dienst Prinzipals der Anwendung angegeben.

### Beispiel 4: Erteilen von Berechtigungen für einen Benutzerprinzipalnamen
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

Dieser Befehl gewährt Get-, List-und festgelegte Berechtigungen für den angegebenen Benutzerprinzipalnamen für den Zugriff auf Geheimnisse.

### Beispiel 5: Aktivieren von Geheimnissen aus einem schlüsseltresor durch den Microsoft. Compute Resource providerkey Vault
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

Dieser Befehl gewährt die Berechtigungen für Geheimnisse, die vom Contoso03Vault-schlüsseltresor vom Microsoft. Compute-Ressourcenanbieter abgerufen werden.

### Beispiel 6: Erteilen von Berechtigungen für eine Sicherheitsgruppe
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

Der erste Befehl verwendet das Get-AzureRmADGroup-Cmdlet, um alle Active Directory-Gruppen abzurufen.
In der Ausgabe werden drei zurückgegebene Gruppen mit dem Namen " **group1** ", " **group2** " und " **Gruppe3** " angezeigt.
Mehrere Gruppen können denselben Namen haben, aber immer eine eindeutige ObjectID aufweisen.
Wenn mehr als eine Gruppe mit demselben Namen zurückgegeben wird, verwenden Sie die ObjectID in der Ausgabe, um die gewünschte Gruppe zu identifizieren.

Anschließend verwenden Sie die Ausgabe dieses Befehls mit Set-AzureRmKeyVaultAccessPolicy, um group2-Berechtigungen für Ihren schlüsseltresor mit dem Namen **myownvault** zu erteilen.
In diesem Beispiel werden die Gruppen mit dem Namen "group2" Inline in der gleichen Befehlszeile aufgelistet.
In der zurückgegebenen Liste können mehrere Gruppen mit dem Namen "group2" vorhanden sein.
In diesem Beispiel wird das erste Element mit dem Index \[ 0 \] in der zurückgegebenen Liste markiert.

### Beispiel 7: Gewähren des Azure Information Protection-Zugriffs auf den vom Kunden verwalteten Mandanten Schlüssel (BYOK)
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,encrypt,unwrapkey,wrapkey,verify,sign,get
```

Mit diesem Befehl wird der Azure-Informationsschutz autorisiert, einen vom Kunden verwalteten Schlüssel (das Szenario "eigene Schlüssel" oder "BYOK") als Azure Information Protection-Mandanten Schlüssel zu verwenden.
Wenn Sie diesen Befehl ausführen, geben Sie Ihren eigenen Tresor Namen an, aber Sie müssen den *servicePrincipalName* -Parameter mit der GUID **00000012-0000-0000-C000-000000000000** angeben und alle Berechtigungen im Beispiel angeben.

## Parameter

### -ApplicationId
Für die spätere Verwendung.

```yaml
Type: System.Nullable`1[System.Guid]
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Email-Email
Gibt die e-Mail-Adresse des Benutzers an, dem Sie Berechtigungen erteilen möchten.
Diese e-Mail-Adresse muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist, und eindeutig sein.

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Die zulässigen Werte für diesen Parameter lauten wie folgt:

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
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PermissionsToKeys
Gibt ein Array von Schlüssel Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

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
Type: System.String[]
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
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Erhalten
- Liste
- Einrichten
- Löschen
- Backup
- Wiederherstellungs
- Wiederherstellen
- Purge

```yaml
Type: System.String[]
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
Gibt die Berechtigungen für verwalteten Speicherkonto und SAS-Definitions Vorgang an, die einem Benutzer oder Dienstprinzipal gewährt werden.

```yaml
Type: System.String[]
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
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Gibt den Dienstprinzipalnamen der Anwendung an, der Berechtigungen erteilt werden sollen.
Geben Sie die Anwendungs-ID (auch Client-ID genannt) an, die für die Anwendung im AzureActive-Verzeichnis registriert wurde.
Die Anwendung mit dem Dienstprinzipalnamen, den dieser Parameter angibt, muss im Azure-Verzeichnis registriert sein, in dem sich das aktuelle Abonnement befindet.

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### String, Guid, String [], Switch

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSVault

## Notizen

## Verwandte Links

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[Remove-AzureRmKeyVaultAccessPolicy](./Remove-AzureRmKeyVaultAccessPolicy.md)

