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
# <span data-ttu-id="51ffe-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51ffe-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="51ffe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="51ffe-103">Listet die Azure -RBAC-Rollenzuweisungen im angegebenen Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="51ffe-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="51ffe-104">Standardmäßig werden alle Rollenzuweisungen im ausgewählten Azure-Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51ffe-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="51ffe-105">Verwenden Sie entsprechende Parameter zum Auflisten von Zuordnungen zu einem bestimmten Benutzer oder zum Auflisten von Zuordnungen für eine bestimmte Ressourcengruppe oder Ressource.</span><span class="sxs-lookup"><span data-stu-id="51ffe-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="51ffe-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51ffe-106">SYNTAX</span></span>

### <span data-ttu-id="51ffe-107">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="51ffe-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ffe-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="51ffe-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ffe-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51ffe-124">DESCRIPTION</span></span>
<span data-ttu-id="51ffe-125">Verwenden Sie Get-AzRoleAssignment Befehl "Rollen", um alle Rollenzuweisungen auflisten, die für einen Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="51ffe-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="51ffe-126">Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die im Abonnement vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="51ffe-127">Diese Liste kann mithilfe von Filterparametern für Prinzipal, Rolle und Bereich gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="51ffe-128">Der Betreff der Zuordnung muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="51ffe-129">Verwenden Sie zum Angeben eines Benutzers die Parameter "SignInName" oder "Azure AD ObjectId".</span><span class="sxs-lookup"><span data-stu-id="51ffe-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="51ffe-130">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD ObjectId-Parameter.</span><span class="sxs-lookup"><span data-stu-id="51ffe-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="51ffe-131">Um eine Azure -AD-Anwendung anzugeben, verwenden Sie die Parameter "ServicePrincipalName" oder "ObjectId".</span><span class="sxs-lookup"><span data-stu-id="51ffe-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="51ffe-132">Die zugewiesene Rolle muss mit dem Parameter "RoleDefinitionName" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="51ffe-133">Der Bereich, für den der Zugriff gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="51ffe-134">Standardmäßig wird das ausgewählte Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="51ffe-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="51ffe-135">Der Bereich der Zuordnung kann mithilfe einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="51ffe-136">Bereich – Dies ist der vollqualifizierte Bereich, der mit "/subscriptions/" \<subscriptionId\> beginnt.</span><span class="sxs-lookup"><span data-stu-id="51ffe-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="51ffe-137">Dadurch werden Zuordnungen gefiltert, die für diesen bestimmten Bereich wirksam sind, d. h. alle Zuordnungen in diesem Bereich und darüber.</span><span class="sxs-lookup"><span data-stu-id="51ffe-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="51ffe-138">b.</span><span class="sxs-lookup"><span data-stu-id="51ffe-138">b.</span></span>
<span data-ttu-id="51ffe-139">ResourceGroupName – Name einer beliebigen Ressourcengruppe im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51ffe-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="51ffe-140">Dadurch werden Zuordnungen gefiltert, die in der angegebenen Ressourcengruppe c wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="51ffe-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="51ffe-141">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – Identifiziert eine bestimmte Ressource unter dem Abonnement und filtert Zuordnungen, die in diesem Ressourcenbereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="51ffe-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="51ffe-142">Um festzustellen, welchen Zugriff ein bestimmter Benutzer im Abonnement hat, verwenden Sie den Schalter "ExpandPrincipalGroups".</span><span class="sxs-lookup"><span data-stu-id="51ffe-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="51ffe-143">Dadurch werden alle dem Benutzer zugewiesenen Rollen sowie die Gruppen aufgeführt, denen der Benutzer mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="51ffe-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="51ffe-144">Verwenden Sie den Schalter "IncludeClassicAdministrators", um auch die Abonnementadministratoren und -mitadministratoren anzeigen.</span><span class="sxs-lookup"><span data-stu-id="51ffe-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="51ffe-145">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51ffe-145">EXAMPLES</span></span>

### <span data-ttu-id="51ffe-146">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51ffe-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="51ffe-147">Auflisten aller Rollenzuweisungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="51ffe-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="51ffe-148">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="51ffe-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="51ffe-149">Ruft alle Rollenzuweisungen, die für den Benutzer vorgenommen wurden, und die Gruppen, deren Mitglied er ist, im john.doe@contoso.com TestRG-Bereich oder höher ab.</span><span class="sxs-lookup"><span data-stu-id="51ffe-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="51ffe-150">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="51ffe-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="51ffe-151">Ruft alle Rollenzuweisungen des angegebenen Dienstprinzipal ab.</span><span class="sxs-lookup"><span data-stu-id="51ffe-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="51ffe-152">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="51ffe-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="51ffe-153">Ruft Rollenzuweisungen im Websitebereich "website1" ab.</span><span class="sxs-lookup"><span data-stu-id="51ffe-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="51ffe-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51ffe-154">PARAMETERS</span></span>

### <span data-ttu-id="51ffe-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ffe-155">-DefaultProfile</span></span>
<span data-ttu-id="51ffe-156">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="51ffe-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51ffe-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="51ffe-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="51ffe-158">Gibt bei Angabe die Rollen zurück, die dem Benutzer direkt zugewiesen wurden, sowie den Gruppen, deren Mitglied der Benutzer ist (transitiv).</span><span class="sxs-lookup"><span data-stu-id="51ffe-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="51ffe-159">Wird nur für einen Benutzerprinzipal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51ffe-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="51ffe-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="51ffe-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="51ffe-161">Falls angegeben, werden auch klassische Abonnementadministratoren (Co-Administratoren, Dienstadministratoren usw.) Rollenzuweisungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51ffe-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="51ffe-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="51ffe-162">-ObjectId</span></span>
<span data-ttu-id="51ffe-163">Die Azure AD ObjectId des Benutzers, der Gruppe oder des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="51ffe-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="51ffe-164">Filtert alle Zuordnungen, die für den angegebenen Prinzipal vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="51ffe-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="51ffe-165">-ParentResource</span></span>
<span data-ttu-id="51ffe-166">Die übergeordnete Ressource in der Hierarchie der Ressource, die mit dem Parameter "ResourceName" angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="51ffe-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="51ffe-167">Muss in Verbindung mit den Parametern "ResourceGroupName", "ResourceType" und "ResourceName" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="51ffe-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51ffe-168">-ResourceGroupName</span></span>
<span data-ttu-id="51ffe-169">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="51ffe-169">The resource group name.</span></span>
<span data-ttu-id="51ffe-170">Listet Rollenzuweisungen auf, die für die angegebene Ressourcengruppe wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="51ffe-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="51ffe-171">Bei Verwendung in Verbindung mit den Parametern "ResourceName", "ResourceType" und "ParentResource" werden im Befehl Zuordnungen aufgeführt, die für Ressourcen innerhalb der Ressourcengruppe effektiv sind.</span><span class="sxs-lookup"><span data-stu-id="51ffe-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="51ffe-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="51ffe-172">-ResourceName</span></span>
<span data-ttu-id="51ffe-173">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="51ffe-173">The resource name.</span></span>
<span data-ttu-id="51ffe-174">Beispielsweise "storageaccountprod".</span><span class="sxs-lookup"><span data-stu-id="51ffe-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="51ffe-175">Muss in Verbindung mit ResourceGroupName-, ResourceType- und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="51ffe-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="51ffe-176">-ResourceType</span></span>
<span data-ttu-id="51ffe-177">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="51ffe-177">The resource type.</span></span>
<span data-ttu-id="51ffe-178">Für z. B. Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="51ffe-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="51ffe-179">Muss in Verbindung mit den Parametern "ResourceGroupName", "ResourceName" und (optional) "ParentResource" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="51ffe-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="51ffe-180">-RoleDefinitionId</span></span>
<span data-ttu-id="51ffe-181">ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="51ffe-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="51ffe-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="51ffe-182">-RoleDefinitionName</span></span>
<span data-ttu-id="51ffe-183">Rolle, die dem Prinzipal zugewiesen ist, z. B. Leser, Mitwirkender, Virtueller Netzwerkadministrator usw.</span><span class="sxs-lookup"><span data-stu-id="51ffe-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="51ffe-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="51ffe-184">-Scope</span></span>
<span data-ttu-id="51ffe-185">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="51ffe-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="51ffe-186">Im Format des relativen URI.</span><span class="sxs-lookup"><span data-stu-id="51ffe-186">In the format of relative URI.</span></span>
<span data-ttu-id="51ffe-187">Für z. B. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="51ffe-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="51ffe-188">Sie muss mit "/subscriptions/{id}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="51ffe-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="51ffe-189">Der Befehl filtert alle Zuordnungen, die in diesem Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="51ffe-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="51ffe-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="51ffe-190">-ServicePrincipalName</span></span>
<span data-ttu-id="51ffe-191">Der "ServicePrincipalName" des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="51ffe-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="51ffe-192">Filtert alle Zuordnungen, die an der angegebenen Azure AD-Anwendung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="51ffe-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="51ffe-193">-SignInName</span></span>
<span data-ttu-id="51ffe-194">Die E-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="51ffe-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="51ffe-195">Filtert alle Zuordnungen, die für den angegebenen Benutzer vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="51ffe-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ffe-196">CommonParameters</span></span>
<span data-ttu-id="51ffe-197">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51ffe-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ffe-198">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51ffe-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ffe-199">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51ffe-199">INPUTS</span></span>

### <span data-ttu-id="51ffe-200">System.String</span><span class="sxs-lookup"><span data-stu-id="51ffe-200">System.String</span></span>

### <span data-ttu-id="51ffe-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="51ffe-201">System.Guid</span></span>

## <span data-ttu-id="51ffe-202">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51ffe-202">OUTPUTS</span></span>

### <span data-ttu-id="51ffe-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51ffe-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="51ffe-204">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="51ffe-204">NOTES</span></span>
<span data-ttu-id="51ffe-205">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="51ffe-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="51ffe-206">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="51ffe-206">RELATED LINKS</span></span>

[<span data-ttu-id="51ffe-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51ffe-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="51ffe-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51ffe-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="51ffe-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="51ffe-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

