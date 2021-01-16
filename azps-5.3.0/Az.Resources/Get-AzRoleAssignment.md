---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459391"
---
# Get-AzRoleAssignment

## SYNOPSIS
Listet die Azure -RBAC-Rollenzuweisungen im angegebenen Bereich auf.
Standardmäßig werden alle Rollenzuweisungen im ausgewählten Azure-Abonnement aufgeführt.
Verwenden Sie entsprechende Parameter zum Auflisten von Zuordnungen zu einem bestimmten Benutzer oder zum Auflisten von Zuordnungen für eine bestimmte Ressourcengruppe oder Ressource.

## SYNTAX

### EmptyParameterSet (Standard)
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceWithObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleIdWithScopeAndObjectIdParameterSet
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithSignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceWithSignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithSignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithSPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceWithSPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithSPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupParameterSet
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceParameterSet
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeParameterSet
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Verwenden Sie Get-AzRoleAssignment Befehl "Rollen", um alle Rollenzuweisungen auflisten, die für einen Bereich wirksam sind.
Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die im Abonnement vorgenommen wurden.
Diese Liste kann mithilfe von Filterparametern für Prinzipal, Rolle und Bereich gefiltert werden.
Der Betreff der Zuordnung muss angegeben werden.
Verwenden Sie zum Angeben eines Benutzers die Parameter "SignInName" oder "Azure AD ObjectId".
Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD ObjectId-Parameter.
Um eine Azure -AD-Anwendung anzugeben, verwenden Sie die Parameter "ServicePrincipalName" oder "ObjectId".
Die zugewiesene Rolle muss mit dem Parameter "RoleDefinitionName" angegeben werden.
Der Bereich, für den der Zugriff gewährt wird, kann angegeben werden.
Standardmäßig wird das ausgewählte Abonnement verwendet. Der Bereich der Zuordnung kann mithilfe einer der folgenden Parameterkombinationen a angegeben werden.
Bereich – Dies ist der vollqualifizierte Bereich, der mit "/subscriptions/" \<subscriptionId\> beginnt.
Dadurch werden Zuordnungen gefiltert, die für diesen bestimmten Bereich wirksam sind, d. h. alle Zuordnungen in diesem Bereich und darüber.
b.
ResourceGroupName – Name einer beliebigen Ressourcengruppe im Abonnement.
Dadurch werden Zuordnungen gefiltert, die in der angegebenen Ressourcengruppe c wirksam sind.
ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – Identifiziert eine bestimmte Ressource unter dem Abonnement und filtert Zuordnungen, die in diesem Ressourcenbereich wirksam sind.
Um festzustellen, welchen Zugriff ein bestimmter Benutzer im Abonnement hat, verwenden Sie den Schalter "ExpandPrincipalGroups".
Dadurch werden alle dem Benutzer zugewiesenen Rollen sowie die Gruppen aufgeführt, denen der Benutzer mitglied ist.
Verwenden Sie den Schalter "IncludeClassicAdministrators", um auch die Abonnementadministratoren und -mitadministratoren anzeigen.

## BEISPIELE

### Beispiel 1
```
PS C:\> Get-AzRoleAssignment
```

Auflisten aller Rollenzuweisungen im Abonnement

### Beispiel 2
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

Ruft alle Rollenzuweisungen, die für den Benutzer vorgenommen wurden, und die Gruppen, deren Mitglied er ist, im john.doe@contoso.com TestRG-Bereich oder höher ab.

### Beispiel 3
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

Ruft alle Rollenzuweisungen des angegebenen Dienstprinzipal ab.

### Beispiel 4
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

Ruft Rollenzuweisungen im Websitebereich "website1" ab.

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

### -ExpandPrincipalGroups
Gibt bei Angabe die Rollen zurück, die dem Benutzer direkt zugewiesen wurden, sowie den Gruppen, deren Mitglied der Benutzer ist (transitiv).
Wird nur für einen Benutzerprinzipal unterstützt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeClassicAdministrators
Falls angegeben, werden auch klassische Abonnementadministratoren (Co-Administratoren, Dienstadministratoren usw.) Rollenzuweisungen aufgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Die Azure AD ObjectId des Benutzers, der Gruppe oder des Dienstprinzipal.
Filtert alle Zuordnungen, die für den angegebenen Prinzipal vorgenommen werden.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentResource
Die übergeordnete Ressource in der Hierarchie der Ressource, die mit dem Parameter "ResourceName" angegeben wurde.
Muss in Verbindung mit den Parametern "ResourceGroupName", "ResourceType" und "ResourceName" verwendet werden.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.
Listet Rollenzuweisungen auf, die für die angegebene Ressourcengruppe wirksam sind.
Bei Verwendung in Verbindung mit den Parametern "ResourceName", "ResourceType" und "ParentResource" werden im Befehl Zuordnungen aufgeführt, die für Ressourcen innerhalb der Ressourcengruppe effektiv sind.

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Der Ressourcenname.
Beispielsweise "storageaccountprod".
Muss in Verbindung mit ResourceGroupName-, ResourceType- und (optional) ParentResource-Parametern verwendet werden.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Der Ressourcentyp.
Für z. B. Microsoft.Network/virtualNetworks.
Muss in Verbindung mit den Parametern "ResourceGroupName", "ResourceName" und (optional) "ParentResource" verwendet werden.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionId
ID der Rolle, die dem Prinzipal zugewiesen ist.

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
Rolle, die dem Prinzipal zugewiesen ist, z. B. Leser, Mitwirkender, Virtueller Netzwerkadministrator usw.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
Der Bereich der Rollenzuweisung.
Im Format des relativen URI.
Für z. B. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.
Sie muss mit "/subscriptions/{id}" beginnen.
Der Befehl filtert alle Zuordnungen, die in diesem Bereich wirksam sind.

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Der "ServicePrincipalName" des Dienstprinzipals.
Filtert alle Zuordnungen, die an der angegebenen Azure AD-Anwendung vorgenommen werden.

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SignInName
Die E-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.
Filtert alle Zuordnungen, die für den angegebenen Benutzer vorgenommen wurden.

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Guid

## AUSGABEN

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## HINWEISE
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS ZU VERWANDTEN THEMEN

[New-AzRoleAssignment](./New-AzRoleAssignment.md)

[Remove-AzRoleAssignment](./Remove-AzRoleAssignment.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

