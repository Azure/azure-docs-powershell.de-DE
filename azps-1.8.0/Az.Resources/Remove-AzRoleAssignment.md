---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: 907d3046a2534b64380299d1f3ff8d65509e534d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659536"
---
# <span data-ttu-id="db1b4-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db1b4-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="db1b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="db1b4-103">Entfernt eine Rollenzuweisung an den angegebenen Prinzipal, der einer bestimmten Rolle in einem bestimmten Bereich zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="db1b4-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="db1b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db1b4-104">SYNTAX</span></span>

### <span data-ttu-id="db1b4-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="db1b4-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1b4-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1b4-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db1b4-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db1b4-117">DESCRIPTION</span></span>
<span data-ttu-id="db1b4-118">Verwenden Sie die Remove-AzRoleAssignment Unifiedgroup, um den Zugriff auf alle Prinzipale im angegebenen Bereich und der angegebenen Rolle zu widerrufen.</span><span class="sxs-lookup"><span data-stu-id="db1b4-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="db1b4-119">Das Objekt der Aufgabe, also der Prinzipal, muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db1b4-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="db1b4-120">Der Prinzipal kann ein Benutzer sein (verwenden Sie SignInName-oder ObjectID-Parameter, um einen Benutzer zu identifizieren), Sicherheitsgruppe (verwenden Sie ObjectID-Parameter, um eine Gruppe zu identifizieren) oder Dienstprinzipal (verwenden Sie servicePrincipalName-oder ObjectID-Parameter, um einen ServicePrincipal zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="db1b4-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="db1b4-121">Die Rolle, der der Prinzipal zugewiesen ist, muss mithilfe des RoleDefinitionName-Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db1b4-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="db1b4-122">Der Umfang der Zuordnung kann angegeben werden und wenn nicht angegeben, wird standardmäßig der Abonnement Bereich verwendet, d. h., es wird versucht, eine Zuordnung zum angegebenen Prinzipal und zur Rolle im Abonnement Bereich zu löschen.</span><span class="sxs-lookup"><span data-stu-id="db1b4-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="db1b4-123">Der Bereich der Zuordnung kann mit einem der folgenden Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db1b4-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="db1b4-124">eine.</span><span class="sxs-lookup"><span data-stu-id="db1b4-124">a.</span></span>
<span data-ttu-id="db1b4-125">Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \< \> -Abonnement-Nr. b.</span><span class="sxs-lookup"><span data-stu-id="db1b4-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="db1b4-126">ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db1b4-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="db1b4-127">c.</span><span class="sxs-lookup"><span data-stu-id="db1b4-127">c.</span></span>
<span data-ttu-id="db1b4-128">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource-kennzeichnet eine bestimmte Ressource unter dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db1b4-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="db1b4-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db1b4-129">EXAMPLES</span></span>

### <span data-ttu-id="db1b4-130">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db1b4-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="db1b4-131">Entfernt eine Rollenzuweisung für die Person, die john.doe@contoso.com der Leserrolle im RG1-Bereich "ResourceGroup" zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="db1b4-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="db1b4-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="db1b4-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="db1b4-133">Entfernt die Rollenzuweisung zu dem von der ObjectID identifizierten und der Reader-Rolle zugewiesenen Gruppen Prinzipal.</span><span class="sxs-lookup"><span data-stu-id="db1b4-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="db1b4-134">Standardmäßig wird das aktuelle Abonnement als Bereich verwendet, um die Aufgabe zu finden, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="db1b4-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="db1b4-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="db1b4-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="db1b4-136">Entfernt das erste Rollen Zuordnungsobjekt, das aus dem Get-AzRoleAssignment Unifiedgroup abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="db1b4-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="db1b4-137">Parameter</span><span class="sxs-lookup"><span data-stu-id="db1b4-137">PARAMETERS</span></span>

### <span data-ttu-id="db1b4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1b4-138">-DefaultProfile</span></span>
<span data-ttu-id="db1b4-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="db1b4-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db1b4-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="db1b4-140">-InputObject</span></span>
<span data-ttu-id="db1b4-141">Rollen Zuweisungs Objekt</span><span class="sxs-lookup"><span data-stu-id="db1b4-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="db1b4-142">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="db1b4-142">-ObjectId</span></span>
<span data-ttu-id="db1b4-143">Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="db1b4-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1b4-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="db1b4-144">-ParentResource</span></span>
<span data-ttu-id="db1b4-145">Die übergeordnete Ressource in der Hierarchie (der mit dem Parameter resourceName angegebenen Ressource) (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="db1b4-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="db1b4-146">Muss in Verbindung mit ResourceGroupName-, ResourceType-und resourceName-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="db1b4-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="db1b4-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db1b4-147">-PassThru</span></span>
<span data-ttu-id="db1b4-148">Wenn angegeben, wird die gelöschte Rollenzuweisung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db1b4-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="db1b4-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1b4-149">-ResourceGroupName</span></span>
<span data-ttu-id="db1b4-150">Der Ressourcengruppenname, dem die Rolle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="db1b4-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="db1b4-151">Versucht, eine Aufgabe im angegebenen Ressourcengruppen Bereich zu löschen.</span><span class="sxs-lookup"><span data-stu-id="db1b4-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="db1b4-152">Bei Verwendung in Verbindung mit resourceName-, ResourceType-und (optional) ParentResource-Parametern erstellt der Befehl einen hierarchischen Bereich in Form eines relativen URIs, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="db1b4-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="db1b4-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="db1b4-153">-ResourceName</span></span>
<span data-ttu-id="db1b4-154">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="db1b4-154">The resource name.</span></span>
<span data-ttu-id="db1b4-155">Für z.b. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="db1b4-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="db1b4-156">Muss in Verbindung mit ResourceGroupName-, ResourceType-und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der die Ressource identifiziert und eine Aufgabe in diesem Bereich löscht.</span><span class="sxs-lookup"><span data-stu-id="db1b4-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="db1b4-157">-</span><span class="sxs-lookup"><span data-stu-id="db1b4-157">-ResourceType</span></span>
<span data-ttu-id="db1b4-158">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="db1b4-158">The resource type.</span></span>
<span data-ttu-id="db1b4-159">Für z.b. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="db1b4-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="db1b4-160">Muss in Verbindung mit ResourceGroupName, resourceName und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der die Ressource identifiziert und eine Aufgabe in diesem Ressourcenbereich löscht.</span><span class="sxs-lookup"><span data-stu-id="db1b4-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="db1b4-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="db1b4-161">-RoleDefinitionId</span></span>
<span data-ttu-id="db1b4-162">Die ID der RBAC-Rolle, für die die Zuordnung gelöscht werden muss.</span><span class="sxs-lookup"><span data-stu-id="db1b4-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="db1b4-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="db1b4-163">-RoleDefinitionName</span></span>
<span data-ttu-id="db1b4-164">Der Name der RBAC-Rolle, für die die Aufgabe gelöscht werden muss, also Leser, Mitwirkender, virtueller Netzwerk Administrator usw.</span><span class="sxs-lookup"><span data-stu-id="db1b4-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="db1b4-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="db1b4-165">-Scope</span></span>
<span data-ttu-id="db1b4-166">Der Bereich der Rollenzuweisung, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="db1b4-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="db1b4-167">Im Format des relativen URIs.</span><span class="sxs-lookup"><span data-stu-id="db1b4-167">In the format of relative URI.</span></span>
<span data-ttu-id="db1b4-168">Für z.b. "/Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="db1b4-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="db1b4-169">Wenn nicht angegeben, wird versucht, die Rolle auf Abonnementebene zu löschen.</span><span class="sxs-lookup"><span data-stu-id="db1b4-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="db1b4-170">Wenn angegeben, sollte Sie mit "/Subscriptions/{ID}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="db1b4-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="db1b4-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="db1b4-171">-ServicePrincipalName</span></span>
<span data-ttu-id="db1b4-172">Die servicePrincipalName der Azure AD-Anwendung</span><span class="sxs-lookup"><span data-stu-id="db1b4-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="db1b4-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="db1b4-173">-SignInName</span></span>
<span data-ttu-id="db1b4-174">Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="db1b4-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="db1b4-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="db1b4-175">-Confirm</span></span>
<span data-ttu-id="db1b4-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db1b4-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db1b4-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db1b4-177">-WhatIf</span></span>
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

### <span data-ttu-id="db1b4-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1b4-178">CommonParameters</span></span>
<span data-ttu-id="db1b4-179">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1b4-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1b4-180">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1b4-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1b4-181">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db1b4-181">INPUTS</span></span>

### <span data-ttu-id="db1b4-182">System. String</span><span class="sxs-lookup"><span data-stu-id="db1b4-182">System.String</span></span>

### <span data-ttu-id="db1b4-183">System. GUID</span><span class="sxs-lookup"><span data-stu-id="db1b4-183">System.Guid</span></span>

### <span data-ttu-id="db1b4-184">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db1b4-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="db1b4-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db1b4-185">OUTPUTS</span></span>

### <span data-ttu-id="db1b4-186">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db1b4-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="db1b4-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="db1b4-187">NOTES</span></span>
<span data-ttu-id="db1b4-188">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="db1b4-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="db1b4-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db1b4-189">RELATED LINKS</span></span>

[<span data-ttu-id="db1b4-190">Neu – AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db1b4-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="db1b4-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db1b4-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="db1b4-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="db1b4-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

