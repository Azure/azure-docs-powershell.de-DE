---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166137"
---
# Get-AzRoleAssignment

## Synopsis
Listet Azure-RBAC-Rollenzuweisungen im angegebenen Bereich auf.
Standardmäßig werden alle Rollenzuweisungen im ausgewählten Azure-Abonnement aufgelistet.
Verwenden Sie die entsprechenden Parameter, um Aufgaben für einen bestimmten Benutzer aufzulisten oder um Aufgaben für eine bestimmte Ressourcengruppe oder Ressource aufzulisten.

## Syntax

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

## Beschreibung
Verwenden Sie den Befehl Get-AzRoleAssignment, um alle Rollenzuweisungen aufzulisten, die für einen Bereich gültig sind.
Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die unter dem Abonnement vorgenommen wurden.
Diese Liste kann mithilfe von Filterparametern für Principal, Role und Scope gefiltert werden.
Der Betreff der Aufgabe muss angegeben werden.
Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.
Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.
Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie servicePrincipalName-oder ObjectID-Parameter.
Die zugewiesene Rolle muss mithilfe des RoleDefinitionName-Parameters angegeben werden.
Der Bereich, in dem Access gewährt wird, kann angegeben werden.
Sie ist standardmäßig auf das ausgewählte Abonnement eingestellt. Der Bereich der Zuordnung kann mit einer der folgenden Parameterkombinationen a angegeben werden.
Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \<subscriptionId\> .
Dadurch werden Aufgaben gefiltert, die in diesem bestimmten Bereich gültig sind, also alle Aufgaben in diesem Bereich und darüber.
b.
ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.
Damit werden die Aufgaben, die bei der angegebenen Ressourcengruppe c wirksam sind, gefiltert.
ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource-kennzeichnet eine bestimmte Ressource unter dem Abonnement und filtert Aufgaben, die in diesem Ressourcenbereich effektiv sind.
Verwenden Sie den ExpandPrincipalGroups-Schalter, um zu ermitteln, welchen Zugriff ein bestimmter Benutzer im Abonnement hat.
Dadurch werden alle dem Benutzer zugewiesenen Rollen sowie die Gruppen aufgelistet, in denen der Benutzer Mitglied ist.
Verwenden Sie den IncludeClassicAdministrators-Schalter, um auch die Abonnement Administratoren und Co-Administratoren anzuzeigen.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzRoleAssignment
```

Auflisten aller Rollenzuweisungen im Abonnement

### Beispiel 2
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

Ruft alle Rollenzuweisungen an john.doe@contoso.com den Benutzer und die Gruppen ab, deren Mitglied er ist, im testRG-Bereich oder höher.

### Beispiel 3
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

Ruft alle Rollenzuweisungen des angegebenen Dienst Prinzipals ab.

### Beispiel 4
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

Ruft Rollenzuweisungen auf dem Website Bereich "site1" ab.

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

### -ExpandPrincipalGroups
Gibt, falls angegeben, Rollen zurück, die dem Benutzer und den Gruppen, denen der Benutzer angehört (transitiv), direkt zugewiesen sind.
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
Wenn angegeben, werden auch Abonnement klassische Administratoren (gemeinsame Administratoren, Dienstadministratoren usw.) aufgelistet.

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

### -ObjectID
Die Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.
Filtert alle Aufgaben, die am angegebenen Prinzipal vorgenommen wurden.

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
Die übergeordnete Ressource in der Hierarchie der Ressource, die mithilfe des resourceName-Parameters angegeben wurde.
Muss in Verbindung mit den Parametern "ResourceGroupName", "Ressourcenparameter" und "resourceName" verwendet werden.

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
Listet Rollenzuweisungen auf, die bei der angegebenen Ressourcengruppe gültig sind.
Bei Verwendung in Verbindung mit resourceName-, ResourceType-und ParentResource-Parametern listet der Befehl Zuordnungen auf, die bei Ressourcen innerhalb der Ressourcengruppe gültig sind.

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
Für z.b. storageaccountprod.
Muss in Verbindung mit ResourceGroupName-, Parameter-und (optional) ParentResource-Parametern verwendet werden.

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

### -
Der Ressourcentyp.
Für z.b. Microsoft. Network/virtualNetworks.
Muss in Verbindung mit ResourceGroupName-, resourceName-und (optional) ParentResource-Parametern verwendet werden.

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
Die ID der Rolle, die dem Prinzipal zugewiesen ist.

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
Rolle, die dem Prinzipal zugewiesen ist, also Leser, Mitwirkender, virtueller Netzwerk Administrator usw.

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
Im Format des relativen URIs.
Für z.b./Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.
Sie muss mit "/Subscriptions/{ID}" beginnen.
Der Befehl filtert alle Aufgaben, die in diesem Bereich gültig sind.

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
Die servicePrincipalName des Dienst Prinzipals.
Filtert alle Aufgaben, die an der angegebenen Azure AD-Anwendung vorgenommen wurden.

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
Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.
Filtert alle Aufgaben, die an den angegebenen Benutzer vorgenommen wurden.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. GUID

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links

[Neu – AzRoleAssignment](./New-AzRoleAssignment.md)

[Remove-AzRoleAssignment](./Remove-AzRoleAssignment.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

