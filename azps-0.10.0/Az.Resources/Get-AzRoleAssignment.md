---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 01714a43f086f675af0bfd493b6cf204390c861e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843400"
---
# <span data-ttu-id="3d9c8-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3d9c8-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="3d9c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d9c8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9c8-103">Listet Azure-RBAC-Rollenzuweisungen im angegebenen Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="3d9c8-104">Standardmäßig werden alle Rollenzuweisungen im ausgewählten Azure-Abonnement aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="3d9c8-105">Verwenden Sie die entsprechenden Parameter, um Aufgaben für einen bestimmten Benutzer aufzulisten oder um Aufgaben für eine bestimmte Ressourcengruppe oder Ressource aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="3d9c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d9c8-106">SYNTAX</span></span>

### <span data-ttu-id="3d9c8-107">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d9c8-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9c8-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d9c8-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d9c8-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d9c8-124">DESCRIPTION</span></span>
<span data-ttu-id="3d9c8-125">Verwenden Sie den Befehl Get-AzRoleAssignment, um alle Rollenzuweisungen aufzulisten, die für einen Bereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="3d9c8-126">Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die unter dem Abonnement vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="3d9c8-127">Diese Liste kann mithilfe von Filterparametern für Principal, Role und Scope gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="3d9c8-128">Der Betreff der Aufgabe muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="3d9c8-129">Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="3d9c8-130">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="3d9c8-131">Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie servicePrincipalName-oder ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="3d9c8-132">Die zugewiesene Rolle muss mithilfe des RoleDefinitionName-Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="3d9c8-133">Der Bereich, in dem Access gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="3d9c8-134">Sie ist standardmäßig auf das ausgewählte Abonnement eingestellt.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="3d9c8-135">Der Bereich der Zuordnung kann mit einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="3d9c8-136">Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \< \> -Abonnement-Nr.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="3d9c8-137">Dadurch werden Aufgaben gefiltert, die in diesem bestimmten Bereich gültig sind, also alle Aufgaben in diesem Bereich und darüber.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="3d9c8-138">b.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-138">b.</span></span>
<span data-ttu-id="3d9c8-139">ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="3d9c8-140">Damit werden die Aufgaben, die bei der angegebenen Ressourcengruppe c wirksam sind, gefiltert.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="3d9c8-141">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource-kennzeichnet eine bestimmte Ressource unter dem Abonnement und filtert Aufgaben, die in diesem Ressourcenbereich effektiv sind.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="3d9c8-142">Verwenden Sie den ExpandPrincipalGroups-Schalter, um zu ermitteln, welchen Zugriff ein bestimmter Benutzer im Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="3d9c8-143">Dadurch werden alle dem Benutzer zugewiesenen Rollen sowie die Gruppen aufgelistet, in denen der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="3d9c8-144">Verwenden Sie den IncludeClassicAdministrators-Schalter, um auch die Abonnement Administratoren und Co-Administratoren anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="3d9c8-145">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d9c8-145">EXAMPLES</span></span>

### <span data-ttu-id="3d9c8-146">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d9c8-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="3d9c8-147">Auflisten aller Rollenzuweisungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d9c8-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="3d9c8-148">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3d9c8-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="3d9c8-149">Ruft alle Rollenzuweisungen an john.doe@contoso.com den Benutzer und die Gruppen ab, deren Mitglied er ist, im testRG-Bereich oder höher.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="3d9c8-150">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3d9c8-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="3d9c8-151">Ruft alle Rollenzuweisungen des angegebenen Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="3d9c8-152">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="3d9c8-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="3d9c8-153">Ruft Rollenzuweisungen auf dem Website Bereich "site1" ab.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="3d9c8-154">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d9c8-154">PARAMETERS</span></span>

### <span data-ttu-id="3d9c8-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9c8-155">-DefaultProfile</span></span>
<span data-ttu-id="3d9c8-156">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d9c8-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9c8-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="3d9c8-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="3d9c8-158">Gibt, falls angegeben, Rollen zurück, die dem Benutzer und den Gruppen, denen der Benutzer angehört (transitiv), direkt zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="3d9c8-159">Wird nur für einen Benutzerprinzipal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="3d9c8-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="3d9c8-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="3d9c8-161">Wenn angegeben, werden auch Abonnement klassische Administratoren (gemeinsame Administratoren, Dienstadministratoren usw.) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="3d9c8-162">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="3d9c8-162">-ObjectId</span></span>
<span data-ttu-id="3d9c8-163">Die Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="3d9c8-164">Filtert alle Aufgaben, die am angegebenen Prinzipal vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9c8-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="3d9c8-165">-ParentResource</span></span>
<span data-ttu-id="3d9c8-166">Die übergeordnete Ressource in der Hierarchie der Ressource, die mithilfe des resourceName-Parameters angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="3d9c8-167">Muss in Verbindung mit den Parametern "ResourceGroupName", "Ressourcenparameter" und "resourceName" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="3d9c8-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9c8-168">-ResourceGroupName</span></span>
<span data-ttu-id="3d9c8-169">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-169">The resource group name.</span></span>
<span data-ttu-id="3d9c8-170">Listet Rollenzuweisungen auf, die bei der angegebenen Ressourcengruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="3d9c8-171">Bei Verwendung in Verbindung mit resourceName-, ResourceType-und ParentResource-Parametern listet der Befehl Zuordnungen auf, die bei Ressourcen innerhalb der Ressourcengruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="3d9c8-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3d9c8-172">-ResourceName</span></span>
<span data-ttu-id="3d9c8-173">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-173">The resource name.</span></span>
<span data-ttu-id="3d9c8-174">Für z.b. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="3d9c8-175">Muss in Verbindung mit ResourceGroupName-, Parameter-und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="3d9c8-176">-</span><span class="sxs-lookup"><span data-stu-id="3d9c8-176">-ResourceType</span></span>
<span data-ttu-id="3d9c8-177">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-177">The resource type.</span></span>
<span data-ttu-id="3d9c8-178">Für z.b. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="3d9c8-179">Muss in Verbindung mit ResourceGroupName-, resourceName-und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="3d9c8-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3d9c8-180">-RoleDefinitionId</span></span>
<span data-ttu-id="3d9c8-181">Die ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3d9c8-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3d9c8-182">-RoleDefinitionName</span></span>
<span data-ttu-id="3d9c8-183">Rolle, die dem Prinzipal zugewiesen ist, also Leser, Mitwirkender, virtueller Netzwerk Administrator usw.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="3d9c8-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="3d9c8-184">-Scope</span></span>
<span data-ttu-id="3d9c8-185">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="3d9c8-186">Im Format des relativen URIs.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-186">In the format of relative URI.</span></span>
<span data-ttu-id="3d9c8-187">Für z.b./Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="3d9c8-188">Sie muss mit "/Subscriptions/{ID}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="3d9c8-189">Der Befehl filtert alle Aufgaben, die in diesem Bereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="3d9c8-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d9c8-190">-ServicePrincipalName</span></span>
<span data-ttu-id="3d9c8-191">Die servicePrincipalName des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="3d9c8-192">Filtert alle Aufgaben, die an der angegebenen Azure AD-Anwendung vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="3d9c8-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3d9c8-193">-SignInName</span></span>
<span data-ttu-id="3d9c8-194">Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="3d9c8-195">Filtert alle Aufgaben, die an den angegebenen Benutzer vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="3d9c8-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9c8-196">CommonParameters</span></span>
<span data-ttu-id="3d9c8-197">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9c8-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9c8-198">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9c8-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9c8-199">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d9c8-199">INPUTS</span></span>

### <span data-ttu-id="3d9c8-200">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3d9c8-200">System.Guid</span></span>

### <span data-ttu-id="3d9c8-201">System. String</span><span class="sxs-lookup"><span data-stu-id="3d9c8-201">System.String</span></span>

## <span data-ttu-id="3d9c8-202">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d9c8-202">OUTPUTS</span></span>

### <span data-ttu-id="3d9c8-203">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3d9c8-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="3d9c8-204">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d9c8-204">NOTES</span></span>
<span data-ttu-id="3d9c8-205">Schlüsselwörter: Azure, AZ, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3d9c8-205">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3d9c8-206">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d9c8-206">RELATED LINKS</span></span>

[<span data-ttu-id="3d9c8-207">Neu – AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3d9c8-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="3d9c8-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3d9c8-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="3d9c8-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3d9c8-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

