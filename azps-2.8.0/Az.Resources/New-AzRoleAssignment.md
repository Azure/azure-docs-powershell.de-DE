---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: d1fe464078c41d07f0d40024c06c4d5f88358470
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823444"
---
# <span data-ttu-id="8e3b5-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8e3b5-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="8e3b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3b5-103">Weist die angegebene RBAC-Rolle dem angegebenen Prinzipal im angegebenen Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="8e3b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e3b5-104">SYNTAX</span></span>

### <span data-ttu-id="8e3b5-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e3b5-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3b5-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3b5-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e3b5-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e3b5-115">DESCRIPTION</span></span>
<span data-ttu-id="8e3b5-116">Verwenden Sie den Befehl New-AzRoleAssignment, um Access zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-116">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="8e3b5-117">Der Zugriff wird durch Zuweisen der entsprechenden RBAC-Rolle im richtigen Bereich gewährt.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-117">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="8e3b5-118">Um dem gesamten Abonnement Zugriff zu gewähren, weisen Sie eine Rolle im Abonnement Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-118">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="8e3b5-119">Wenn Sie den Zugriff auf eine bestimmte Ressourcengruppe innerhalb eines Abonnements gewähren möchten, weisen Sie eine Rolle im Bereich der Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-119">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="8e3b5-120">Der Betreff der Aufgabe muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-120">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="8e3b5-121">Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-121">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="8e3b5-122">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-122">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="8e3b5-123">Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie ApplicationId-oder ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-123">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="8e3b5-124">Die zugewiesene Rolle muss mithilfe des RoleDefinitionName-Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-124">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="8e3b5-125">Der Bereich, in dem Access gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-125">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="8e3b5-126">Sie ist standardmäßig auf das ausgewählte Abonnement eingestellt.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-126">It defaults to the selected subscription.</span></span> <span data-ttu-id="8e3b5-127">Der Bereich der Zuordnung kann mit einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-127">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="8e3b5-128">Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \< \> -Abonnement-Nr. b.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-128">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="8e3b5-129">ResourceGroupName – zum Gewähren des Zugriffs auf die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-129">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="8e3b5-130">c.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-130">c.</span></span>
<span data-ttu-id="8e3b5-131">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – um eine bestimmte Ressource innerhalb einer Ressourcengruppe anzugeben, auf die Sie Zugriff gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-131">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="8e3b5-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e3b5-132">EXAMPLES</span></span>

### <span data-ttu-id="8e3b5-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e3b5-133">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="8e3b5-134">Gewähren des Lese Rollenzugriffs für einen Benutzer in einem Ressourcengruppen Bereich, wobei die Rollenzuweisung für die Delegierung verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="8e3b5-134">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="8e3b5-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e3b5-135">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="8e3b5-136">Gewähren des Zugriffs auf eine Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="8e3b5-136">Grant access to a security group</span></span>

### <span data-ttu-id="8e3b5-137">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8e3b5-137">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="8e3b5-138">Gewähren des Zugriffs auf einen Benutzer auf einer Ressource (Website)</span><span class="sxs-lookup"><span data-stu-id="8e3b5-138">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="8e3b5-139">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="8e3b5-139">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="8e3b5-140">Gewähren des Zugriffs auf eine Gruppe in einer geschachtelten Ressource (Subnetz)</span><span class="sxs-lookup"><span data-stu-id="8e3b5-140">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="8e3b5-141">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="8e3b5-141">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="8e3b5-142">Gewähren des Lesezugriffs auf einen Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="8e3b5-142">Grant reader access to a service principal</span></span>

## <span data-ttu-id="8e3b5-143">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e3b5-143">PARAMETERS</span></span>

### <span data-ttu-id="8e3b5-144">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="8e3b5-144">-AllowDelegation</span></span>
<span data-ttu-id="8e3b5-145">Das Flag "Delegierung" beim Erstellen einer Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-145">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="8e3b5-146">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8e3b5-146">-ApplicationId</span></span>
<span data-ttu-id="8e3b5-147">Die Anwendungs-ID des ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8e3b5-147">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="8e3b5-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3b5-148">-DefaultProfile</span></span>
<span data-ttu-id="8e3b5-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8e3b5-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e3b5-150">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8e3b5-150">-ObjectId</span></span>
<span data-ttu-id="8e3b5-151">Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-151">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3b5-152">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="8e3b5-152">-ParentResource</span></span>
<span data-ttu-id="8e3b5-153">Die übergeordnete Ressource in der Hierarchie (der mit dem Parameter resourceName angegebenen Ressource).</span><span class="sxs-lookup"><span data-stu-id="8e3b5-153">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="8e3b5-154">Sollte nur in Verbindung mit ResourceGroupName-, ResourceType-und resourceName-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-154">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="8e3b5-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3b5-155">-ResourceGroupName</span></span>
<span data-ttu-id="8e3b5-156">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-156">The resource group name.</span></span>
<span data-ttu-id="8e3b5-157">Erstellt eine Aufgabe, die bei der angegebenen Ressourcengruppe gültig ist.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-157">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="8e3b5-158">Bei Verwendung in Verbindung mit resourceName-, ResourceType-und (optional) ParentResource-Parametern erstellt der Befehl einen hierarchischen Bereich in Form eines relativen URIs, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-158">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="8e3b5-159">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8e3b5-159">-ResourceName</span></span>
<span data-ttu-id="8e3b5-160">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-160">The resource name.</span></span>
<span data-ttu-id="8e3b5-161">Für z.b. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-161">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="8e3b5-162">Sollte nur in Verbindung mit ResourceGroupName-, ResourceType-und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-162">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="8e3b5-163">-</span><span class="sxs-lookup"><span data-stu-id="8e3b5-163">-ResourceType</span></span>
<span data-ttu-id="8e3b5-164">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-164">The resource type.</span></span>
<span data-ttu-id="8e3b5-165">Für z.b. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-165">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="8e3b5-166">Sollte nur in Verbindung mit ResourceGroupName, resourceName und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URIs zu konstruieren, der eine Ressource kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-166">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="8e3b5-167">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8e3b5-167">-RoleDefinitionId</span></span>
<span data-ttu-id="8e3b5-168">Die ID der RBAC-Rolle, die dem Prinzipal zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-168">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="8e3b5-169">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8e3b5-169">-RoleDefinitionName</span></span>
<span data-ttu-id="8e3b5-170">Der Name der RBAC-Rolle, die dem Prinzipal zugewiesen werden muss, also Leser, Mitwirkender, virtueller Netzwerk Administrator usw.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-170">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3b5-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="8e3b5-171">-Scope</span></span>
<span data-ttu-id="8e3b5-172">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-172">The Scope of the role assignment.</span></span>
<span data-ttu-id="8e3b5-173">Im Format des relativen URIs.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-173">In the format of relative URI.</span></span>
<span data-ttu-id="8e3b5-174">Für z.b. "/Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="8e3b5-174">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="8e3b5-175">Wenn nicht angegeben, wird die Rollenzuweisung auf Abonnementebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-175">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="8e3b5-176">Wenn angegeben, sollte Sie mit "/Subscriptions/{ID}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-176">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3b5-177">-SignInName</span><span class="sxs-lookup"><span data-stu-id="8e3b5-177">-SignInName</span></span>
<span data-ttu-id="8e3b5-178">Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-178">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="8e3b5-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3b5-179">CommonParameters</span></span>
<span data-ttu-id="8e3b5-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e3b5-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3b5-181">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e3b5-181">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3b5-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e3b5-182">INPUTS</span></span>

### <span data-ttu-id="8e3b5-183">System. String</span><span class="sxs-lookup"><span data-stu-id="8e3b5-183">System.String</span></span>

### <span data-ttu-id="8e3b5-184">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8e3b5-184">System.Guid</span></span>

## <span data-ttu-id="8e3b5-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e3b5-185">OUTPUTS</span></span>

### <span data-ttu-id="8e3b5-186">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8e3b5-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="8e3b5-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e3b5-187">NOTES</span></span>
<span data-ttu-id="8e3b5-188">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="8e3b5-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8e3b5-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e3b5-189">RELATED LINKS</span></span>

[<span data-ttu-id="8e3b5-190">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8e3b5-190">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="8e3b5-191">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8e3b5-191">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="8e3b5-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8e3b5-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
