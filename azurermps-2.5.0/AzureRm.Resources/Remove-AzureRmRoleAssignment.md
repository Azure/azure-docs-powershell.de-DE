---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
ms.openlocfilehash: adf6147db102ee834f7e12e19409a95734fae7e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850532"
---
# Remove-AzureRmRoleAssignment

## Synopsis
Entfernt eine Rollenzuweisung an den angegebenen Prinzipal, der einer bestimmten Rolle in einem bestimmten Bereich zugewiesen ist.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### EmptyParameterSet (Standard)
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithObjectIdParameterSet
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithObjectIdParameterSet
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithObjectIdParameterSet
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleIdWithScopeAndObjectIdParameterSet
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSignInNameParameterSet
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSignInNameParameterSet
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithSignInNameParameterSet
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSPNParameterSet
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSPNParameterSet
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ScopeWithSPNParameterSet
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleAssignmentParameterSet
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Verwenden Sie die Remove-AzureRmRoleAssignment Unifiedgroup, um den Zugriff auf alle Prinzipale im angegebenen Bereich und der angegebenen Rolle zu widerrufen.
Das Objekt der Aufgabe, also der Prinzipal, muss angegeben werden.
Der Prinzipal kann ein Benutzer sein (verwenden Sie SignInName-oder ObjectID-Parameter, um einen Benutzer zu identifizieren), Sicherheitsgruppe (verwenden Sie ObjectID-Parameter, um eine Gruppe zu identifizieren) oder Dienstprinzipal (verwenden Sie servicePrincipalName-oder ObjectID-Parameter, um einen ServicePrincipal zu identifizieren.
Die Rolle, der der Prinzipal zugewiesen ist, muss mithilfe des RoleDefinitionName-Parameters angegeben werden.
Der Umfang der Zuordnung kann angegeben werden und wenn nicht angegeben, wird standardmäßig der Abonnement Bereich verwendet, d. h., es wird versucht, eine Zuordnung zum angegebenen Prinzipal und zur Rolle im Abonnement Bereich zu löschen.
Der Bereich der Zuordnung kann mit einem der folgenden Parameter angegeben werden.
eine.
Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \<subscriptionId\> b.
ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.
c.
ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource-kennzeichnet eine bestimmte Ressource unter dem Abonnement.

## Beispiele

### Beispiel 1
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

Entfernt eine Rollenzuweisung für die Person, die john.doe@contoso.com der Leserrolle im RG1-Bereich "ResourceGroup" zugewiesen ist.

### Beispiel 2
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

Entfernt die Rollenzuweisung zu dem von der ObjectID identifizierten und der Reader-Rolle zugewiesenen Gruppen Prinzipal.
Standardmäßig wird das aktuelle Abonnement als Bereich verwendet, um die Aufgabe zu finden, die gelöscht werden soll.

### Beispiel 3
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

Entfernt das erste Rollen Zuordnungsobjekt, das aus dem Get-AzureRmRoleAssignment Unifiedgroup abgerufen wird.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Inputobject
Rollen Zuweisungs Objekt

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectID
Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentResource
Die übergeordnete Ressource in der Hierarchie (der mit dem Parameter resourceName angegebenen Ressource) (sofern vorhanden).
Muss in Verbindung mit ResourceGroupName-, ResourceType-und resourceName-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der die Ressource identifiziert.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Wenn angegeben, wird die gelöschte Rollenzuweisung angezeigt.

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

### -ResourceGroupName
Der Ressourcengruppenname, dem die Rolle zugewiesen ist.
Versucht, eine Aufgabe im angegebenen Ressourcengruppen Bereich zu löschen.
Bei Verwendung in Verbindung mit resourceName-, ResourceType-und (optional) ParentResource-Parametern erstellt der Befehl einen hierarchischen Bereich in Form eines relativen URIs, der eine Ressource kennzeichnet.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Der Ressourcenname.
Für z.b. storageaccountprod.
Muss in Verbindung mit ResourceGroupName-, ResourceType-und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der die Ressource identifiziert und eine Aufgabe in diesem Bereich löscht.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -
Der Ressourcentyp.
Für z.b. Microsoft. Network/virtualNetworks.
Muss in Verbindung mit ResourceGroupName, resourceName und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der die Ressource identifiziert und eine Aufgabe in diesem Ressourcenbereich löscht.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionId
Die ID der RBAC-Rolle, für die die Zuordnung gelöscht werden muss.

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionName
Der Name der RBAC-Rolle, für die die Aufgabe gelöscht werden muss, also Leser, Mitwirkender, virtueller Netzwerk Administrator usw.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
Der Bereich der Rollenzuweisung, der gelöscht werden soll.
Im Format des relativen URIs.
Für z.b. "/Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".
Wenn nicht angegeben, wird versucht, die Rolle auf Abonnementebene zu löschen.
Wenn angegeben, sollte Sie mit "/Subscriptions/{ID}" beginnen.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Die servicePrincipalName der Azure AD-Anwendung

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SignInName
Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. GUID

### System. String

### Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment
Parameter: Inputobject (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links

[Neu – AzureRmRoleAssignment](./New-AzureRmRoleAssignment.md)

[Get-AzureRmRoleAssignment](./Get-AzureRmRoleAssignment.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

