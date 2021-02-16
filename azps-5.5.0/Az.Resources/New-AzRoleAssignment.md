---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150892"
---
# <span data-ttu-id="56869-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="56869-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="56869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56869-102">SYNOPSIS</span></span>
<span data-ttu-id="56869-103">Weist dem angegebenen Prinzipal im angegebenen Bereich die angegebene RbAC-Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="56869-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="56869-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56869-104">SYNTAX</span></span>

### <span data-ttu-id="56869-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="56869-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56869-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="56869-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56869-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56869-116">DESCRIPTION</span></span>
<span data-ttu-id="56869-117">Verwenden Sie den befehl New-AzRoleAssignment, um den Zugriff zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="56869-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="56869-118">Access wird gewährt, indem ihnen im richtigen Bereich die entsprechende RbAC-Rolle zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="56869-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="56869-119">Wenn Sie zugriff auf das gesamte Abonnement gewähren möchten, weisen Sie dem Abonnementbereich eine Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="56869-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="56869-120">Wenn Sie einer bestimmten Ressourcengruppe innerhalb eines Abonnements Zugriff gewähren möchten, weisen Sie dem Bereich der Ressourcengruppe eine Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="56869-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="56869-121">Der Betreff der Zuordnung muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56869-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="56869-122">Verwenden Sie zum Angeben eines Benutzers die Parameter "SignInName" oder "Azure AD ObjectId".</span><span class="sxs-lookup"><span data-stu-id="56869-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="56869-123">Verwenden Sie den Azure AD ObjectId-Parameter, um eine Sicherheitsgruppe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="56869-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="56869-124">Verwenden Sie zum Angeben einer Azure AD-Anwendung die Parameter ApplicationId oder ObjectId.</span><span class="sxs-lookup"><span data-stu-id="56869-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="56869-125">Die zugewiesene Rolle muss mit dem Parameter "RoleDefinitionName" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56869-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="56869-126">Der Bereich, für den der Zugriff gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56869-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="56869-127">Standardmäßig wird das ausgewählte Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="56869-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="56869-128">Der Bereich der Zuordnung kann mithilfe einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56869-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="56869-129">Bereich – Dies ist der vollqualifizierte Bereich, der mit "/subscriptions/b" \<subscriptionId\> beginnt.</span><span class="sxs-lookup"><span data-stu-id="56869-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="56869-130">ResourceGroupName – zum Gewähren des Zugriffs auf die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56869-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="56869-131">c.</span><span class="sxs-lookup"><span data-stu-id="56869-131">c.</span></span>
<span data-ttu-id="56869-132">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – zum Angeben einer bestimmten Ressource innerhalb einer Ressourcengruppe, der Zugriff gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56869-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="56869-133">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56869-133">EXAMPLES</span></span>

### <span data-ttu-id="56869-134">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="56869-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="56869-135">Gewähren des Zugriffs auf die Rolle "Leser" für einen Benutzer in einem Ressourcengruppenbereich, bei dem die Rollenzuweisung für die Delegierung verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="56869-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="56869-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="56869-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="56869-137">Gewähren des Zugriffs auf eine Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="56869-137">Grant access to a security group</span></span>

### <span data-ttu-id="56869-138">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="56869-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="56869-139">Gewähren des Zugriffs auf eine Ressource (Website)</span><span class="sxs-lookup"><span data-stu-id="56869-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="56869-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="56869-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="56869-141">Gewähren des Zugriffs auf eine Gruppe in einer geschachtelten Ressource (Subnetz)</span><span class="sxs-lookup"><span data-stu-id="56869-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="56869-142">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="56869-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="56869-143">Gewähren des Lesezugriffs auf einen Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="56869-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="56869-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56869-144">PARAMETERS</span></span>

### <span data-ttu-id="56869-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="56869-145">-AllowDelegation</span></span>
<span data-ttu-id="56869-146">Das Delegierungsflag beim Erstellen einer Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="56869-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="56869-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="56869-147">-ApplicationId</span></span>
<span data-ttu-id="56869-148">Die Anwendungs-ID von "ServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="56869-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="56869-149">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="56869-149">-Condition</span></span>
<span data-ttu-id="56869-150">Bedingung, die auf die RoleAssignment angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="56869-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56869-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="56869-151">-ConditionVersion</span></span>
<span data-ttu-id="56869-152">Version der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="56869-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56869-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56869-153">-DefaultProfile</span></span>
<span data-ttu-id="56869-154">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="56869-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56869-155">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56869-155">-Description</span></span>
<span data-ttu-id="56869-156">Kurze Beschreibung der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="56869-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56869-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="56869-157">-InputFile</span></span>
<span data-ttu-id="56869-158">Path to role assignment json</span><span class="sxs-lookup"><span data-stu-id="56869-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56869-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="56869-159">-ObjectId</span></span>
<span data-ttu-id="56869-160">Azure AD ObjectID des Benutzers, der Gruppe oder des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="56869-160">Azure AD Objectid of the user, group or service principal.</span></span>

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

### <span data-ttu-id="56869-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="56869-161">-ParentResource</span></span>
<span data-ttu-id="56869-162">Die übergeordnete Ressource in der Hierarchie (der Ressource, die mit dem Parameter "ResourceName" angegeben wurde).</span><span class="sxs-lookup"><span data-stu-id="56869-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="56869-163">Sollte nur in Verbindung mit den Parametern "ResourceGroupName", "ResourceType" und "ResourceName" verwendet werden, um einen hierarchischen Bereich in Form eines relativen URI zu erstellen, der eine Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56869-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="56869-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56869-164">-ResourceGroupName</span></span>
<span data-ttu-id="56869-165">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56869-165">The resource group name.</span></span>
<span data-ttu-id="56869-166">Erstellt eine Zuordnung, die für die angegebene Ressourcengruppe wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="56869-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="56869-167">Bei Verwendung in Verbindung mit resourceName-, ResourceType- und (optional)ParentResource-Parametern erstellt der Befehl einen hierarchischen Bereich in Form eines relativen URI, der eine Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56869-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="56869-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="56869-168">-ResourceName</span></span>
<span data-ttu-id="56869-169">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="56869-169">The resource name.</span></span>
<span data-ttu-id="56869-170">Beispielsweise "storageaccountprod".</span><span class="sxs-lookup"><span data-stu-id="56869-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="56869-171">Sollte nur in Verbindung mit ResourceGroupName-, ResourceType- und (optional) ParentResource-Parametern verwendet werden, um einen hierarchischen Bereich in Form eines relativen URI zu erstellen, der eine Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56869-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="56869-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="56869-172">-ResourceType</span></span>
<span data-ttu-id="56869-173">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="56869-173">The resource type.</span></span>
<span data-ttu-id="56869-174">Für z. B. Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="56869-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="56869-175">Sollte nur in Verbindung mit den Parametern "ResourceGroupName", "ResourceName" und (optional) "ParentResource" verwendet werden, um einen hierarchischen Bereich in Form eines relativen URI zu erstellen, der eine Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56869-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="56869-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="56869-176">-RoleDefinitionId</span></span>
<span data-ttu-id="56869-177">Id der RBAC-Rolle, die dem Prinzipal zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="56869-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="56869-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="56869-178">-RoleDefinitionName</span></span>
<span data-ttu-id="56869-179">Name der RBAC-Rolle, die dem Prinzipal zugewiesen werden muss, z. B. Leser, Mitwirkender, Virtueller Netzwerkadministrator usw.</span><span class="sxs-lookup"><span data-stu-id="56869-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="56869-180">-Scope</span><span class="sxs-lookup"><span data-stu-id="56869-180">-Scope</span></span>
<span data-ttu-id="56869-181">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="56869-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="56869-182">Im Format des relativen URI.</span><span class="sxs-lookup"><span data-stu-id="56869-182">In the format of relative URI.</span></span>
<span data-ttu-id="56869-183">Für z. B. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="56869-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="56869-184">Wenn nichts angegeben ist, wird die Rollenzuweisung auf Abonnementebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="56869-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="56869-185">Falls angegeben, sollte es mit "/subscriptions/{id}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="56869-185">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="56869-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="56869-186">-SignInName</span></span>
<span data-ttu-id="56869-187">Die E-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="56869-187">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="56869-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56869-188">CommonParameters</span></span>
<span data-ttu-id="56869-189">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56869-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56869-190">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56869-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56869-191">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56869-191">INPUTS</span></span>

### <span data-ttu-id="56869-192">System.String</span><span class="sxs-lookup"><span data-stu-id="56869-192">System.String</span></span>

### <span data-ttu-id="56869-193">System.Guid</span><span class="sxs-lookup"><span data-stu-id="56869-193">System.Guid</span></span>

## <span data-ttu-id="56869-194">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56869-194">OUTPUTS</span></span>

### <span data-ttu-id="56869-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="56869-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="56869-196">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56869-196">NOTES</span></span>
<span data-ttu-id="56869-197">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="56869-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="56869-198">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56869-198">RELATED LINKS</span></span>

[<span data-ttu-id="56869-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="56869-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="56869-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="56869-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="56869-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="56869-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
