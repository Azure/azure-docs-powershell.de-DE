---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146081"
---
# <span data-ttu-id="f3ab3-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="f3ab3-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="f3ab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ab3-103">Listet Azure RBAC zuordnungen im angegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="f3ab3-104">Standardmäßig werden alle verweigerten Zuweisungen im ausgewählten Azure-Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="f3ab3-105">Verwenden Sie entsprechende Parameter, um Zuweisungen an einen bestimmten Benutzer zu verweigern, oder um Verweigern von Zuordnungen für eine bestimmte Ressourcengruppe oder Ressource auflisten.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="f3ab3-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3ab3-106">SYNTAX</span></span>

### <span data-ttu-id="f3ab3-107">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3ab3-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ab3-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ab3-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ab3-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3ab3-125">DESCRIPTION</span></span>
<span data-ttu-id="f3ab3-126">Verwenden Sie Get-AzDenyAssignment Befehl "Verweigern", um alle Verweigernzuweisungen auflisten, die für einen Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="f3ab3-127">Ohne Parameter gibt dieser Befehl alle verweigerten Zuweisungen zurück, die im Abonnement vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="f3ab3-128">Diese Liste kann mithilfe von Filterparametern für den Prinzipal, den Namen und den Bereich der Zuordnung verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="f3ab3-129">Verwenden Sie zum Angeben eines Benutzers die Parameter "SignInName" oder "Azure AD ObjectId".</span><span class="sxs-lookup"><span data-stu-id="f3ab3-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="f3ab3-130">Verwenden Sie den Azure AD ObjectId-Parameter, um eine Sicherheitsgruppe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="f3ab3-131">Um eine Azure -AD-Anwendung anzugeben, verwenden Sie die Parameter "ServicePrincipalName" oder "ObjectId".</span><span class="sxs-lookup"><span data-stu-id="f3ab3-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="f3ab3-132">Der Bereich, in dem der Zugriff verweigert wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="f3ab3-133">Standardmäßig wird das ausgewählte Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="f3ab3-134">Der Bereich der Verweigernzuweisung kann mithilfe einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="f3ab3-135">Bereich – Dies ist der vollqualifizierte Bereich, der mit "/subscriptions/" \<subscriptionId\> beginnt.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="f3ab3-136">Dadurch werden Zuordnungen gefiltert, die in diesem bestimmten Bereich wirksam sind, d. h. alle Zuordnungen in diesem Bereich und darüber verweigern.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="f3ab3-137">b.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-137">b.</span></span>
<span data-ttu-id="f3ab3-138">ResourceGroupName – Name einer beliebigen Ressourcengruppe im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="f3ab3-139">Dadurch werden Zuordnungen gefiltert, die in der angegebenen Ressourcengruppe wirksam sind, d. h. alle Zuordnungen in diesem Bereich und darüber verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="f3ab3-140">c.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-140">c.</span></span>
<span data-ttu-id="f3ab3-141">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – Identifiziert eine bestimmte Ressource unter dem Abonnement und filtert Zuordnungen, die in diesem Ressourcenbereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="f3ab3-142">Um festzustellen, welcher Zugriff für einen bestimmten Benutzer im Abonnement verweigert wird, verwenden Sie den Schalter "ExpandPrincipalGroups".</span><span class="sxs-lookup"><span data-stu-id="f3ab3-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="f3ab3-143">Dadurch werden alle dem Benutzer zugewiesenen Verweigernzuweisungen sowie die Gruppen aufgeführt, in denen der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="f3ab3-144">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3ab3-144">EXAMPLES</span></span>

### <span data-ttu-id="f3ab3-145">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3ab3-145">Example 1</span></span>

<span data-ttu-id="f3ab3-146">Alle verweigerten Aufgaben im Abonnement auflisten</span><span class="sxs-lookup"><span data-stu-id="f3ab3-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="f3ab3-147">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f3ab3-147">Example 2</span></span>

<span data-ttu-id="f3ab3-148">Ruft alle dem Benutzer beim BereichstestRG und höher vorgenommenen john.doe@contoso.com Verweigernzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="f3ab3-149">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f3ab3-149">Example 3</span></span>

<span data-ttu-id="f3ab3-150">Ruft alle Verweigernzuweisungen des angegebenen Dienstprinzipal ab.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="f3ab3-151">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f3ab3-151">Example 4</span></span>

<span data-ttu-id="f3ab3-152">Ruft Zuordnungen verweigert im Websitebereich "site1" ab.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

## <span data-ttu-id="f3ab3-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ab3-153">PARAMETERS</span></span>

### <span data-ttu-id="f3ab3-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ab3-154">-DefaultProfile</span></span>
<span data-ttu-id="f3ab3-155">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f3ab3-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3ab3-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f3ab3-156">-DenyAssignmentName</span></span>
<span data-ttu-id="f3ab3-157">Der Name der Zuweisung "Verweigern".</span><span class="sxs-lookup"><span data-stu-id="f3ab3-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ab3-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="f3ab3-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="f3ab3-159">Wenn angegeben, werden Verweigernzuweisungen zurückgegeben, die dem Benutzer direkt zugewiesen wurden, sowie den Gruppen, deren Mitglied der Benutzer ist (transitiv).</span><span class="sxs-lookup"><span data-stu-id="f3ab3-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="f3ab3-160">Wird nur für einen Benutzerprinzipal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="f3ab3-161">-ID</span><span class="sxs-lookup"><span data-stu-id="f3ab3-161">-Id</span></span>
<span data-ttu-id="f3ab3-162">Aufgaben-ID verweigern.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ab3-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f3ab3-163">-ObjectId</span></span>
<span data-ttu-id="f3ab3-164">Die Azure AD ObjectId des Benutzers, der Gruppe oder des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="f3ab3-165">Filtert alle Verweigernzuordnungen, die für den angegebenen Prinzipal vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ab3-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="f3ab3-166">-ParentResource</span></span>
<span data-ttu-id="f3ab3-167">Die übergeordnete Ressource in der Hierarchie der Ressource, die mit dem Parameter "ResourceName" angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="f3ab3-168">Muss in Verbindung mit den Parametern "ResourceGroupName", "ResourceType" und "ResourceName" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="f3ab3-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ab3-169">-ResourceGroupName</span></span>
<span data-ttu-id="f3ab3-170">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-170">The resource group name.</span></span>
<span data-ttu-id="f3ab3-171">Listen verweigern Zuordnungen, die für die angegebene Ressourcengruppe wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="f3ab3-172">Bei Verwendung in Verbindung mit den Parametern "ResourceName", "ResourceType" und "ParentResource" verweigert die Befehlsliste Zuordnungen, die für Ressourcen innerhalb der Ressourcengruppe wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="f3ab3-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f3ab3-173">-ResourceName</span></span>
<span data-ttu-id="f3ab3-174">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-174">The resource name.</span></span>
<span data-ttu-id="f3ab3-175">Beispielsweise "storageaccountprod".</span><span class="sxs-lookup"><span data-stu-id="f3ab3-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="f3ab3-176">Muss in Verbindung mit ResourceGroupName-, ResourceType- und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="f3ab3-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f3ab3-177">-ResourceType</span></span>
<span data-ttu-id="f3ab3-178">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-178">The resource type.</span></span>
<span data-ttu-id="f3ab3-179">Für z. B. Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="f3ab3-180">Muss in Verbindung mit den Parametern "ResourceGroupName", "ResourceName" und (optional) "ParentResource" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="f3ab3-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="f3ab3-181">-Scope</span></span>
<span data-ttu-id="f3ab3-182">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="f3ab3-183">Im Format des relativen URI.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-183">In the format of relative URI.</span></span>
<span data-ttu-id="f3ab3-184">Für z. B. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="f3ab3-185">Sie muss mit "/subscriptions/{id}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="f3ab3-186">Der Befehl filtert alle verweigerten Zuordnungen, die in diesem Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="f3ab3-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f3ab3-187">-ServicePrincipalName</span></span>
<span data-ttu-id="f3ab3-188">Der "ServicePrincipalName" des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="f3ab3-189">Filtert alle verweigerten Zuordnungen, die für die angegebene Azure AD-Anwendung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="f3ab3-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f3ab3-190">-SignInName</span></span>
<span data-ttu-id="f3ab3-191">Die E-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="f3ab3-192">Filtert alle Dementenzuweisungen, die für den angegebenen Benutzer vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="f3ab3-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ab3-193">CommonParameters</span></span>
<span data-ttu-id="f3ab3-194">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ab3-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ab3-195">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3ab3-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ab3-196">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ab3-196">INPUTS</span></span>

### <span data-ttu-id="f3ab3-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f3ab3-197">System.Guid</span></span>

### <span data-ttu-id="f3ab3-198">System.String</span><span class="sxs-lookup"><span data-stu-id="f3ab3-198">System.String</span></span>

## <span data-ttu-id="f3ab3-199">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ab3-199">OUTPUTS</span></span>

### <span data-ttu-id="f3ab3-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="f3ab3-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="f3ab3-201">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f3ab3-201">NOTES</span></span>
<span data-ttu-id="f3ab3-202">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="f3ab3-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f3ab3-203">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f3ab3-203">RELATED LINKS</span></span>
