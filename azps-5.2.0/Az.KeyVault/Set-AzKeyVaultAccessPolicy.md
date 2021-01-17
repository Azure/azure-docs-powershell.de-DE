---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: eeaea44ec387dc7739a97b5026054186ff817ab3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360813"
---
# Set-AzKeyVaultAccessPolicy

## SYNOPSIS
Gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um Vorgänge mit einem Schlüsseltresor durchzuführen.

## SYNTAX

### ByUserPrincipalName (Standard)
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObjectId
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
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

### InputObjectByObjectId
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectForVault
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByObjectId
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdForVault
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzKeyVaultAccessPolicy"** erteilt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um die angegebenen Vorgänge mit einem Schlüsseltresor durchzuführen. Die Berechtigungen, die andere Benutzer, Anwendungen oder Sicherheitsgruppen für den Schlüsseltresor besitzen, werden nicht geändert.
Wenn Sie Berechtigungen für eine Sicherheitsgruppe festlegen, wirkt sich dieser Vorgang nur auf Benutzer in dieser Sicherheitsgruppe aus.
Die folgenden Verzeichnisse müssen alle dasselbe Azure-Verzeichnis sein:
- Das Standardverzeichnis des Azure-Abonnements, in dem sich der Schlüsseltresor befindet.
- Das Azure-Verzeichnis, das den Benutzer oder die Anwendungsgruppe enthält, dem Sie Berechtigungen erteilen.
Beispiele für Szenarien, in denen diese Bedingungen nicht erfüllt sind und dieses Cmdlet nicht funktioniert:
- Autorisieren eines Benutzers aus einer anderen Organisation zum Verwalten Ihres Schlüsseltresor.
Jede Organisation verfügt über ein eigenes Verzeichnis.
- Ihr Azure-Konto verfügt über mehrere Verzeichnisse.
Wenn Sie eine Anwendung in einem anderen Verzeichnis als dem Standardverzeichnis registrieren, können Sie diese Anwendung nicht autorisieren, Ihren Schlüsseltresor zu verwenden.
Die Anwendung muss sich im Standardverzeichnis befinden.
Beachten Sie: Obwohl die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, sollten Sie dies zur Leistungssteigerung tun.

> [!NOTE]
> Wenn Sie zum Erteilen von Zugriffsrichtlinienberechtigungen einen Dienstprinzipal verwenden, müssen Sie den Parameter `-BypassObjectIdValidation` verwenden.

## BEISPIELE

### Beispiel 1: Erteilen von Berechtigungen für einen Schlüsseltresor und Ändern der Berechtigungen für einen Benutzer
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

Der erste Befehl erteilt einem Benutzer in Azure Active Directory Berechtigungen zum Ausführen von Vorgängen mit Schlüsseln und geheimen Daten mit einem Schlüsseltresor namens PattiFuller@contoso.com "Contoso03Vault". Der *Parameter "PassThru"* führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.
Der zweite Befehl ändert die Berechtigungen, die im ersten Befehl erteilt wurden, um jetzt zusätzlich zum Festlegen und Löschen des Befehls das Abrufen von geheimen Daten PattiFuller@contoso.com zu ermöglichen. Die Berechtigungen für Wichtige Vorgänge bleiben nach diesem Befehl unverändert.
Der letzte Befehl ändert außerdem die vorhandenen Berechtigungen zum PattiFuller@contoso.com Entfernen aller Berechtigungen für Schlüsselvorgänge. Die Berechtigungen für geheime Vorgänge bleiben nach diesem Befehl unverändert.

### Beispiel 2: Erteilen von Berechtigungen für einen Anwendungsdienstprinzipal zum Lesen und Schreiben von geheimen Daten
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

Dieser Befehl erteilt einer Anwendung Berechtigungen für einen Schlüsseltresor namens Contoso03Vault.
Der *Parameter "ServicePrincipalName"* gibt die Anwendung an. Die Anwendung muss in Azure Active Directory registriert sein. Der Wert des Parameters *"ServicePrincipalName"* muss entweder der Dienstprinzipalname der Anwendung oder die Anwendungs-ID-GUID sein.
In diesem Beispiel wird der Dienstprinzipalname angegeben, und der Befehl erteilt der Anwendung Berechtigungen `http://payroll.contoso.com` zum Lesen und Schreiben von geheimen Daten.

### Beispiel 3: Erteilen von Berechtigungen für eine Anwendung mithilfe der Objekt-ID
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

Dieser Befehl erteilt der Anwendung Berechtigungen zum Lesen und Schreiben von geheimen Daten.
In diesem Beispiel wird die Anwendung mit der Objekt-ID des Dienstprinzipal der Anwendung angegeben.

### Beispiel 4: Erteilen von Berechtigungen für einen Benutzerprinzipalnamen
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

Mit diesem Befehl werden "get", "list" und "set permissions" für den angegebenen Benutzerprinzipalnamen für den Zugriff auf geheime Daten erteilt.

### Beispiel 5: Ermöglichen, dass geheime Daten vom Microsoft.Compute-Ressourcenanbieter aus einem Schlüsseltresor abgerufen werden
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

Dieser Befehl erteilt die Berechtigungen für geheime Daten, die vom Microsoft.Compute-Ressourcenanbieter aus dem Schlüsseltresor Contoso03Vault abgerufen werden sollen.

### Beispiel 6: Erteilen von Berechtigungen für eine Sicherheitsgruppe
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

Im ersten Befehl wird das Get-AzADGroup cmdlet verwendet, um alle Active Directory-Gruppen zu erhalten. Aus der Ausgabe werden 3 Gruppen zurückgegeben, mit den Namen **"Gruppe1",** **"Gruppe2"** und **"Gruppe3".** Mehrere Gruppen können denselben Namen, aber immer eine eindeutige ObjectId haben. Wenn mehr als eine Gruppe mit demselben Namen zurückgegeben wird, verwenden Sie die ObjectId in der Ausgabe, um die Gruppe zu identifizieren, die Sie verwenden möchten.
Anschließend verwenden Sie die Ausgabe dieses Befehls mit Set-AzKeyVaultAccessPolicy, um Berechtigungen für Den Schlüsseltresor **"myownvault"** der Gruppe 2 zu erteilen. In diesem Beispiel werden die Gruppen mit dem Namen "group2" inline in derselben Befehlszeile aufgezählt.
Die zurückgegebene Liste enthält möglicherweise mehrere Gruppen mit dem Namen "Gruppe2".
In diesem Beispiel wird das erste Beispiel, das durch Index \[ 0 \] in der zurückgegebenen Liste angegeben ist, verwendet.

### Beispiel 7: Gewähren des Azure Information Protection-Zugriffs auf den vom Kunden verwalteten Mandantenschlüssel (BYOK)
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

Mit diesem Befehl wird Azure Information Protection autorisiert, einen vom Kunden verwalteten Schlüssel (das "Bring your own key" oder "BYOK"-Szenario) als Azure Information Protection-Mandantenschlüssel zu verwenden.
Wenn Sie diesen Befehl ausführen, geben Sie Ihren eigenen Namen für den Schlüsseltresor an, müssen jedoch den Parameter *"ServicePrincipalName"* mit der GUID **00000012-0000-0000-c000-0000000000** angeben und die Berechtigungen im Beispiel angeben.

## PARAMETERS

### -ApplicationId
Für die zukünftige Verwendung.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BypassObjectIdValidation
Ermöglicht es Ihnen, eine Objekt-ID anzugeben, ohne zu überprüfen, ob das Objekt in Azure Active Directory vorhanden ist.
Verwenden Sie diesen Parameter nur, wenn Sie Zugriff auf Ihren Schlüsseltresor auf eine Objekt-ID gewähren möchten, die sich auf eine delegierte Sicherheitsgruppe von einem anderen Azure-Mandanten bezieht.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
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

### -EmailAddress
Gibt die E-Mail-Adresse des Benutzers an, dem Berechtigungen erteilt werden.
Diese E-Mail-Adresse muss in dem Verzeichnis vorhanden sein, das mit dem aktuellen Abonnement verknüpft ist, und eindeutig sein.

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
Ermöglicht es dem Microsoft.Compute-Ressourcenanbieter, geheime Daten aus diesem Schlüsseltresor abzurufen, wenn bei der Ressourcenerstellung auf diesen Schlüsseltresor verwiesen wird, z. B. beim Erstellen eines virtuellen Computers.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Ermöglicht dem Azure-Datenträgerverschlüsselungsdienst das Erhalten von geheimen Schlüsseln und Entpackungsschlüsseln aus diesem Schlüsseltresor.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Ermöglicht Azure Resource Manager, geheime Daten aus diesem Schlüsseltresor zu erhalten, wenn in einer Vorlagenbereitstellung auf diesen Schlüsseltresor verwiesen wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Key Vault Object

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Gibt die Objekt-ID des Benutzers oder Dienstprinzipal in Azure Active Directory an, für den Berechtigungen erteilt werden.

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
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

### -PermissionsToCertificates
Gibt ein Array von Zertifikatberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden.
Die zulässigen Werte für diesen Parameter:
- Alle
- Erhalten
- Liste
- Löschen
- Erstellen
- Importieren
- Update
- Managecontacts
- Getissuers
- Listissuers
- Setissuers
- Deleteissuers
- Manageissuers
- Wiederherstellen
- Sicherung
- Wiederherstellen
- Löschen

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToKeys
Gibt ein Array mit wichtigen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden müssen.
Die zulässigen Werte für diesen Parameter:
- Alle
- Entschlüsseln
- Verschlüsseln
- UnwrapKey
- WrapKey
- Überprüfen
- Signieren
- Erhalten
- Liste
- Update
- Erstellen
- Importieren
- Löschen
- Sicherung
- Wiederherstellen
- Wiederherstellen
- Löschen

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToSecrets
Gibt ein Array mit geheimen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden.
Die zulässigen Werte für diesen Parameter:
- Alle
- Erhalten
- Liste
- Festlegen
- Löschen
- Sicherung
- Wiederherstellen
- Wiederherstellen
- Löschen

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToStorage
Gibt die Berechtigungen für verwaltete Speicherkonto- und SaS-Definitionsvorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden.
Die zulässigen Werte für diesen Parameter:
- alle
- Erhalten
- Liste
- Löschen
- festlegen
- Update
- regeneratekey
- getsas
- Listsas
- deletesas
- Setsas
- Wiederherstellen
- Sicherung
- Wiederherstellen
- Löschen

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Ressourcen-ID des Schlüsseltresor

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Gibt den Dienstprinzipalnamen der Anwendung an, der Berechtigungen erteilt werden soll.
Geben Sie die Anwendungs-ID( auch bekannt als Client-ID) an, die für die Anwendung in AzureActive Directory registriert ist. Die Anwendung mit dem von diesem Parameter angegebenen Dienstprinzipalnamen muss im Azure-Verzeichnis registriert sein, das Ihr aktuelles Abonnement enthält.

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
Gibt den Benutzerprinzipalnamen des Benutzers an, dem Berechtigungen erteilt werden.
Dieser Benutzerprinzipalname muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Gibt den Namen eines Schlüsseltresor an.
Dieses Cmdlet ändert die Zugriffsrichtlinie für den Schlüsseltresor, den dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVaultAccessPolicy](./Remove-AzKeyVaultAccessPolicy.md)

