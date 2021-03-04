---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 7de4753d47ff2a285da6a9d3d60e0f95fcbf6e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944134"
---
# Get-AzKeyVaultRoleAssignment

## SYNOPSIS
Erhalten oder Auflisten von Rollenzuweisungen eines verwalteten HSM. Verwenden Sie entsprechende Parameter, um Zuordnungen zu einem bestimmten Benutzer oder einer Rollendefinition auflisten.

## SYNTAX

### Liste (Standard)
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Verwenden Sie `Get-AzKeyVaultRoleAssignment` den Befehl, um alle Rollenzuweisungen auflisten, die für einen Bereich wirksam sind.
Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die unter dem verwalteten HSM vorgenommen wurden.
Diese Liste kann mithilfe von Filterparametern für Prinzipal, Rolle und Umfang gefiltert werden.
Der Betreff der Zuordnung muss angegeben werden.
Verwenden Sie zum Angeben eines Benutzers die Parameter SignInName oder Azure AD ObjectId.
Verwenden Sie den Azure AD ObjectId-Parameter, um eine Sicherheitsgruppe anzugeben.
Und zum Angeben einer Azure AD-Anwendung verwenden Sie die Parameter ApplicationId oder ObjectId.
Die zugewiesene Rolle muss mit dem Parameter RoleDefinitionName oder RoleDefinitionId angegeben werden.
Der Bereich, in dem der Zugriff gewährt wird, kann angegeben werden. Sie ist standardmäßig auf "/" festgelegt.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

In diesem Beispiel werden alle Rollenzuweisungen von "myHsm" für den ganzen Bereich aufgeführt.

### Beispiel 2
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

In diesem Beispiel werden alle Rollenzuweisungen von "myHsm" im Bereich "/keys" aufgeführt und das Ergebnis nach Dem Anmeldenamen des Benutzers filtern.

## PARAMETER

### -ApplicationId
Die App SPN.

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

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

### -HsmName
Name des HSM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Die Benutzer- oder Gruppenobjekt-ID.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleAssignmentName
Name der Rollenzuweisung.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
Rollen-ID, der der Prinzipal zugewiesen ist.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionName
Name der Rolle "RBAC", mit der der Prinzipal zugewiesen werden soll.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Bereich, für den die Rollenzuweisung oder -definition gilt, z. B. "/" oder "/keys" oder "/keys/{keyName}".
"/" wird verwendet, wenn sie nicht angegeben wird.

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

### -SignInName
Der Benutzer SignInName.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment

## NOTIZEN

## VERWANDTE LINKS
