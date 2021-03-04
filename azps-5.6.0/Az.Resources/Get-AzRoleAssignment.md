---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: dd59b49ad4002d38cd9a49506cb1723b5ac1e426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942224"
---
# <span data-ttu-id="210b5-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="210b5-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="210b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="210b5-102">SYNOPSIS</span></span>
<span data-ttu-id="210b5-103">Listet Azure RBAC-Rollenzuweisungen im angegebenen Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="210b5-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="210b5-104">Standardmäßig werden alle Rollenzuweisungen im ausgewählten Azure-Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="210b5-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="210b5-105">Verwenden Sie entsprechende Parameter zum Auflisten von Zuordnungen zu einem bestimmten Benutzer oder zum Auflisten von Zuordnungen zu einer bestimmten Ressourcengruppe oder Ressource.</span><span class="sxs-lookup"><span data-stu-id="210b5-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="210b5-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="210b5-106">SYNTAX</span></span>

### <span data-ttu-id="210b5-107">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="210b5-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210b5-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="210b5-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="210b5-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="210b5-124">DESCRIPTION</span></span>
<span data-ttu-id="210b5-125">Verwenden Sie den Get-AzRoleAssignment, um alle Rollenzuweisungen auflisten, die für einen Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="210b5-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="210b5-126">Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die unter dem Abonnement vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="210b5-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="210b5-127">Diese Liste kann mithilfe von Filterparametern für Prinzipal, Rolle und Umfang gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="210b5-128">Der Betreff der Zuordnung muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="210b5-129">Verwenden Sie zum Angeben eines Benutzers die Parameter SignInName oder Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="210b5-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="210b5-130">Verwenden Sie den Azure AD ObjectId-Parameter, um eine Sicherheitsgruppe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="210b5-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="210b5-131">Und zum Angeben einer Azure AD-Anwendung verwenden Sie die Parameter ServicePrincipalName oder ObjectId.</span><span class="sxs-lookup"><span data-stu-id="210b5-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="210b5-132">Die zugewiesene Rolle muss mit dem Parameter RoleDefinitionName angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="210b5-133">Der Bereich, in dem der Zugriff gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="210b5-134">Es ist standardmäßig für das ausgewählte Abonnement festgelegt.</span><span class="sxs-lookup"><span data-stu-id="210b5-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="210b5-135">Der Umfang der Zuordnung kann mithilfe einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="210b5-136">Bereich – Dies ist der vollqualifizierte Bereich, der mit /subscriptions/ \<subscriptionId\> beginnt.</span><span class="sxs-lookup"><span data-stu-id="210b5-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="210b5-137">Dadurch werden Zuordnungen gefiltert, die in diesem bestimmten Bereich wirksam sind, d. h. alle Zuordnungen in diesem Bereich und darüber.</span><span class="sxs-lookup"><span data-stu-id="210b5-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="210b5-138">b.</span><span class="sxs-lookup"><span data-stu-id="210b5-138">b.</span></span>
<span data-ttu-id="210b5-139">ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="210b5-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="210b5-140">Dadurch werden Zuordnungen gefiltert, die in der angegebenen Ressourcengruppe c wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="210b5-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="210b5-141">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – Gibt eine bestimmte Ressource unter dem Abonnement an und filtert Zuordnungen, die in diesem Ressourcenbereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="210b5-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="210b5-142">Um zu bestimmen, über welchen Zugriff ein bestimmter Benutzer im Abonnement verfügt, verwenden Sie den Schalter ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="210b5-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="210b5-143">Dadurch werden alle Rollen aufgeführt, die dem Benutzer und den Gruppen zugewiesen sind, deren Mitglied der Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="210b5-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="210b5-144">Verwenden Sie den Schalter IncludeClassicAdministrators, um auch die Abonnementadministratoren und Mitadministratoren anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="210b5-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="210b5-145">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="210b5-145">EXAMPLES</span></span>

### <span data-ttu-id="210b5-146">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="210b5-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="210b5-147">Auflisten aller Rollenzuweisungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="210b5-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="210b5-148">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="210b5-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="210b5-149">Ruft alle Rollenzuweisungen ab, die dem Benutzer und den Gruppen, deren Mitglied er ist, im john.doe@contoso.com TestRG-Bereich oder höher vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="210b5-150">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="210b5-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="210b5-151">Ruft alle Rollenzuweisungen des angegebenen Dienstprinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="210b5-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="210b5-152">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="210b5-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="210b5-153">Ruft Rollenzuweisungen im Websitebereich "website1" ab.</span><span class="sxs-lookup"><span data-stu-id="210b5-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="210b5-154">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="210b5-154">PARAMETERS</span></span>

### <span data-ttu-id="210b5-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210b5-155">-DefaultProfile</span></span>
<span data-ttu-id="210b5-156">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="210b5-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="210b5-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="210b5-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="210b5-158">Wenn angegeben, werden Rollen zurückgegeben, die dem Benutzer direkt zugewiesen sind, und den Gruppen, deren Mitglied der Benutzer ist (transitiv).</span><span class="sxs-lookup"><span data-stu-id="210b5-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="210b5-159">Wird nur für einen Benutzerprinzipal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="210b5-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="210b5-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="210b5-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="210b5-161">Wenn angegeben, werden auch klassische Abonnementadministratoren (Co-Administratoren, Dienstadministratoren usw.) rollende Aufgaben aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="210b5-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="210b5-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="210b5-162">-ObjectId</span></span>
<span data-ttu-id="210b5-163">Die Azure AD-ObjectId des Benutzers, der Gruppe oder des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="210b5-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="210b5-164">Filtert alle Zuordnungen, die an den angegebenen Prinzipal vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="210b5-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="210b5-165">-ParentResource</span></span>
<span data-ttu-id="210b5-166">Die übergeordnete Ressource in der Hierarchie der Ressource, die mit dem Parameter "ResourceName" angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="210b5-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="210b5-167">Muss in Verbindung mit den Parametern ResourceGroupName, ResourceType und ResourceName verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="210b5-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="210b5-168">-ResourceGroupName</span></span>
<span data-ttu-id="210b5-169">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="210b5-169">The resource group name.</span></span>
<span data-ttu-id="210b5-170">Listet Rollenzuordnungen auf, die in der angegebenen Ressourcengruppe wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="210b5-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="210b5-171">Bei Verwendung in Verbindung mit den Parametern "ResourceName", "ResourceType" und "ParentResource" werden im Befehl Zuordnungen aufgeführt, die für Ressourcen innerhalb der Ressourcengruppe wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="210b5-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="210b5-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="210b5-172">-ResourceName</span></span>
<span data-ttu-id="210b5-173">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="210b5-173">The resource name.</span></span>
<span data-ttu-id="210b5-174">Für z. B. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="210b5-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="210b5-175">Muss in Verbindung mit den Parametern ResourceGroupName, ResourceType und (optional) ParentResource verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="210b5-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="210b5-176">-ResourceType</span></span>
<span data-ttu-id="210b5-177">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="210b5-177">The resource type.</span></span>
<span data-ttu-id="210b5-178">Für z. B. Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="210b5-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="210b5-179">Muss in Verbindung mit den Parametern ResourceGroupName, ResourceName und (optional) ParentResource verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="210b5-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="210b5-180">-RoleDefinitionId</span></span>
<span data-ttu-id="210b5-181">ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="210b5-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="210b5-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="210b5-182">-RoleDefinitionName</span></span>
<span data-ttu-id="210b5-183">Rolle, die dem Prinzipal zugewiesen ist, z. B. Reader, Mitwirkender, Virtueller Netzwerkadministrator usw.</span><span class="sxs-lookup"><span data-stu-id="210b5-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="210b5-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="210b5-184">-Scope</span></span>
<span data-ttu-id="210b5-185">Der Umfang der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="210b5-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="210b5-186">Im Format des relativen URI.</span><span class="sxs-lookup"><span data-stu-id="210b5-186">In the format of relative URI.</span></span>
<span data-ttu-id="210b5-187">Für z. B. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="210b5-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="210b5-188">Sie muss mit "/subscriptions/{id}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="210b5-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="210b5-189">Der Befehl filtert alle Zuordnungen, die in diesem Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="210b5-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="210b5-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="210b5-190">-ServicePrincipalName</span></span>
<span data-ttu-id="210b5-191">Der ServicePrincipalName des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="210b5-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="210b5-192">Filtert alle Zuordnungen, die an der angegebenen Azure AD-Anwendung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="210b5-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="210b5-193">-SignInName</span></span>
<span data-ttu-id="210b5-194">Die E-Mail-Adresse oder der Benutzername des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="210b5-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="210b5-195">Filtert alle Zuordnungen, die an den angegebenen Benutzer vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="210b5-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="210b5-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210b5-196">CommonParameters</span></span>
<span data-ttu-id="210b5-197">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="210b5-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210b5-198">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="210b5-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210b5-199">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="210b5-199">INPUTS</span></span>

### <span data-ttu-id="210b5-200">System.String</span><span class="sxs-lookup"><span data-stu-id="210b5-200">System.String</span></span>

### <span data-ttu-id="210b5-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="210b5-201">System.Guid</span></span>

## <span data-ttu-id="210b5-202">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="210b5-202">OUTPUTS</span></span>

### <span data-ttu-id="210b5-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="210b5-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="210b5-204">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="210b5-204">NOTES</span></span>
<span data-ttu-id="210b5-205">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="210b5-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="210b5-206">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="210b5-206">RELATED LINKS</span></span>

[<span data-ttu-id="210b5-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="210b5-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="210b5-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="210b5-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="210b5-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="210b5-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

