---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 7ffbad2d915691d5a50aa198f5c3756031fc2e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843315"
---
# <span data-ttu-id="ef734-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ef734-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="ef734-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef734-102">SYNOPSIS</span></span>
<span data-ttu-id="ef734-103">Weist die angegebene RBAC-Rolle dem angegebenen Prinzipal im angegebenen Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="ef734-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="ef734-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef734-104">SYNTAX</span></span>

### <span data-ttu-id="ef734-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef734-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-114">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef734-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef734-115">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef734-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef734-116">DESCRIPTION</span></span>
<span data-ttu-id="ef734-117">Verwenden Sie den Befehl New-AzRoleAssignment, um Access zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="ef734-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="ef734-118">Der Zugriff wird durch Zuweisen der entsprechenden RBAC-Rolle im richtigen Bereich gewährt.</span><span class="sxs-lookup"><span data-stu-id="ef734-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="ef734-119">Um dem gesamten Abonnement Zugriff zu gewähren, weisen Sie eine Rolle im Abonnement Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="ef734-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="ef734-120">Wenn Sie den Zugriff auf eine bestimmte Ressourcengruppe innerhalb eines Abonnements gewähren möchten, weisen Sie eine Rolle im Bereich der Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="ef734-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="ef734-121">Der Betreff der Aufgabe muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef734-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="ef734-122">Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef734-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="ef734-123">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef734-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="ef734-124">Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie ApplicationId-oder ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef734-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="ef734-125">Die zugewiesene Rolle muss mithilfe des RoleDefinitionName-Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef734-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="ef734-126">Der Bereich, in dem Access gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef734-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="ef734-127">Sie ist standardmäßig auf das ausgewählte Abonnement eingestellt.</span><span class="sxs-lookup"><span data-stu-id="ef734-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="ef734-128">Der Bereich der Zuordnung kann mit einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef734-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="ef734-129">Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \< \> -Abonnement-Nr. b.</span><span class="sxs-lookup"><span data-stu-id="ef734-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="ef734-130">ResourceGroupName – zum Gewähren des Zugriffs auf die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef734-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="ef734-131">c.</span><span class="sxs-lookup"><span data-stu-id="ef734-131">c.</span></span>
<span data-ttu-id="ef734-132">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – um eine bestimmte Ressource innerhalb einer Ressourcengruppe anzugeben, auf die Sie Zugriff gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="ef734-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="ef734-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef734-133">EXAMPLES</span></span>

### <span data-ttu-id="ef734-134">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef734-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="ef734-135">Gewähren des Lese Rollenzugriffs für einen Benutzer in einem Ressourcengruppen Bereich, wobei die Rollenzuweisung für die Delegierung verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="ef734-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="ef734-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ef734-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="ef734-137">Gewähren des Zugriffs auf eine Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="ef734-137">Grant access to a security group</span></span>

### <span data-ttu-id="ef734-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ef734-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="ef734-139">Gewähren des Zugriffs auf einen Benutzer auf einer Ressource (Website)</span><span class="sxs-lookup"><span data-stu-id="ef734-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="ef734-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ef734-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="ef734-141">Gewähren des Zugriffs auf eine Gruppe in einer geschachtelten Ressource (Subnetz)</span><span class="sxs-lookup"><span data-stu-id="ef734-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="ef734-142">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ef734-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="ef734-143">Gewähren des Lesezugriffs auf einen Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="ef734-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="ef734-144">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef734-144">PARAMETERS</span></span>

### <span data-ttu-id="ef734-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="ef734-145">-AllowDelegation</span></span>
<span data-ttu-id="ef734-146">Das Flag "Delegierung" beim Erstellen einer Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="ef734-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef734-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ef734-147">-ApplicationId</span></span>
<span data-ttu-id="ef734-148">Die Anwendungs-ID des ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef734-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef734-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef734-149">-DefaultProfile</span></span>
<span data-ttu-id="ef734-150">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ef734-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef734-151">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ef734-151">-ObjectId</span></span>
<span data-ttu-id="ef734-152">Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="ef734-152">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef734-153">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="ef734-153">-ParentResource</span></span>
<span data-ttu-id="ef734-154">Die übergeordnete Ressource in der Hierarchie (der mit dem Parameter resourceName angegebenen Ressource).</span><span class="sxs-lookup"><span data-stu-id="ef734-154">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="ef734-155">Sollte nur in Verbindung mit ResourceGroupName-, ResourceType-und resourceName-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ef734-155">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ef734-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef734-156">-ResourceGroupName</span></span>
<span data-ttu-id="ef734-157">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef734-157">The resource group name.</span></span>
<span data-ttu-id="ef734-158">Erstellt eine Aufgabe, die bei der angegebenen Ressourcengruppe gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ef734-158">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="ef734-159">Bei Verwendung in Verbindung mit resourceName-, ResourceType-und (optional) ParentResource-Parametern erstellt der Befehl einen hierarchischen Bereich in Form eines relativen URIs, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ef734-159">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef734-160">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ef734-160">-ResourceName</span></span>
<span data-ttu-id="ef734-161">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ef734-161">The resource name.</span></span>
<span data-ttu-id="ef734-162">Für z.b. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="ef734-162">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="ef734-163">Sollte nur in Verbindung mit ResourceGroupName-, ResourceType-und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ef734-163">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ef734-164">-</span><span class="sxs-lookup"><span data-stu-id="ef734-164">-ResourceType</span></span>
<span data-ttu-id="ef734-165">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ef734-165">The resource type.</span></span>
<span data-ttu-id="ef734-166">Für z.b. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="ef734-166">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="ef734-167">Sollte nur in Verbindung mit ResourceGroupName, resourceName und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ef734-167">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ef734-168">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ef734-168">-RoleDefinitionId</span></span>
<span data-ttu-id="ef734-169">Die ID der RBAC-Rolle, die dem Prinzipal zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef734-169">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="ef734-170">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ef734-170">-RoleDefinitionName</span></span>
<span data-ttu-id="ef734-171">Der Name der RBAC-Rolle, die dem Prinzipal zugewiesen werden muss, also Leser, Mitwirkender, virtueller Netzwerk Administrator usw.</span><span class="sxs-lookup"><span data-stu-id="ef734-171">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef734-172">-Scope</span><span class="sxs-lookup"><span data-stu-id="ef734-172">-Scope</span></span>
<span data-ttu-id="ef734-173">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="ef734-173">The Scope of the role assignment.</span></span>
<span data-ttu-id="ef734-174">Im Format des relativen URIs.</span><span class="sxs-lookup"><span data-stu-id="ef734-174">In the format of relative URI.</span></span>
<span data-ttu-id="ef734-175">Für z.b. "/Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="ef734-175">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="ef734-176">Wenn nicht angegeben, wird die Rollenzuweisung auf Abonnementebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef734-176">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="ef734-177">Wenn angegeben, sollte Sie mit "/Subscriptions/{ID}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="ef734-177">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef734-178">-SignInName</span><span class="sxs-lookup"><span data-stu-id="ef734-178">-SignInName</span></span>
<span data-ttu-id="ef734-179">Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ef734-179">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef734-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef734-180">CommonParameters</span></span>
<span data-ttu-id="ef734-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef734-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef734-182">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef734-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef734-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef734-183">INPUTS</span></span>

### <span data-ttu-id="ef734-184">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ef734-184">System.Guid</span></span>

### <span data-ttu-id="ef734-185">System. String</span><span class="sxs-lookup"><span data-stu-id="ef734-185">System.String</span></span>

## <span data-ttu-id="ef734-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef734-186">OUTPUTS</span></span>

### <span data-ttu-id="ef734-187">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ef734-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="ef734-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef734-188">NOTES</span></span>
<span data-ttu-id="ef734-189">Schlüsselwörter: Azure, AZ, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ef734-189">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ef734-190">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef734-190">RELATED LINKS</span></span>

[<span data-ttu-id="ef734-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ef734-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="ef734-192">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ef734-192">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="ef734-193">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ef734-193">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
