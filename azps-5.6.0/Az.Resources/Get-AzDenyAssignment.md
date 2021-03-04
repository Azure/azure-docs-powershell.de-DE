---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: d54d6ff9ed26b76d3c36ab47cf04024dcdf11281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920939"
---
# <span data-ttu-id="05e5e-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="05e5e-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="05e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="05e5e-103">Listet Azure RBAC Zuordnungen im angegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="05e5e-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="05e5e-104">Standardmäßig werden alle verweigerten Zuordnungen im ausgewählten Azure-Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="05e5e-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="05e5e-105">Verwenden Sie entsprechende Parameter zum Auflisten von Zuordnungen, die einem bestimmten Benutzer verweigert werden, oder zum Auflisten von Verweigerte Zuordnungen für eine bestimmte Ressourcengruppe oder Ressource.</span><span class="sxs-lookup"><span data-stu-id="05e5e-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="05e5e-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05e5e-106">SYNTAX</span></span>

### <span data-ttu-id="05e5e-107">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="05e5e-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e5e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e5e-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e5e-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e5e-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e5e-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e5e-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e5e-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05e5e-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05e5e-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05e5e-125">DESCRIPTION</span></span>
<span data-ttu-id="05e5e-126">Verwenden Sie den befehl Get-AzDenyAssignment, um alle verweigerten Zuordnungen auflisten, die für einen Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="05e5e-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="05e5e-127">Ohne Parameter gibt dieser Befehl alle verweigerten Zuordnungen zurück, die unter dem Abonnement vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="05e5e-128">Diese Liste kann mithilfe von Filterparametern für Denk- und Zuordnungsname und -bereich gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="05e5e-129">Verwenden Sie zum Angeben eines Benutzers die Parameter SignInName oder Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="05e5e-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="05e5e-130">Verwenden Sie den Azure AD ObjectId-Parameter, um eine Sicherheitsgruppe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="05e5e-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="05e5e-131">Und zum Angeben einer Azure AD-Anwendung verwenden Sie die Parameter ServicePrincipalName oder ObjectId.</span><span class="sxs-lookup"><span data-stu-id="05e5e-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="05e5e-132">Der Bereich, in dem der Zugriff verweigert wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="05e5e-133">Es ist standardmäßig für das ausgewählte Abonnement festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05e5e-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="05e5e-134">Der Umfang der Verweigernzuordnung kann mit einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="05e5e-135">Bereich – Dies ist der vollqualifizierte Bereich, der mit /subscriptions/ \<subscriptionId\> beginnt.</span><span class="sxs-lookup"><span data-stu-id="05e5e-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="05e5e-136">Dadurch werden zuordnungs verweigernde Zuordnungen gefiltert, die in diesem bestimmten Bereich wirksam sind, d. h. alle Zuordnungen in diesem Bereich und höher zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="05e5e-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="05e5e-137">b.</span><span class="sxs-lookup"><span data-stu-id="05e5e-137">b.</span></span>
<span data-ttu-id="05e5e-138">ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05e5e-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="05e5e-139">Dadurch werden Zuordnungen gefiltert, die in der angegebenen Ressourcengruppe wirksam sind, d. h. alle Zuordnungen in diesem Bereich und höher zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="05e5e-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="05e5e-140">c.</span><span class="sxs-lookup"><span data-stu-id="05e5e-140">c.</span></span>
<span data-ttu-id="05e5e-141">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource – Gibt eine bestimmte Ressource im Abonnement an und filtert Zuordnungen, die in diesem Ressourcenbereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="05e5e-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="05e5e-142">Um zu ermitteln, welcher Zugriff für einen bestimmten Benutzer im Abonnement verweigert wird, verwenden Sie den Schalter ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="05e5e-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="05e5e-143">Dadurch werden alle Dementenzuweisungen aufgeführt, die dem Benutzer und den Gruppen zugewiesen wurden, deren Mitglied der Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="05e5e-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="05e5e-144">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05e5e-144">EXAMPLES</span></span>

### <span data-ttu-id="05e5e-145">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05e5e-145">Example 1</span></span>

<span data-ttu-id="05e5e-146">Alle verweigerten Aufgaben im Abonnement auflisten</span><span class="sxs-lookup"><span data-stu-id="05e5e-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="05e5e-147">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="05e5e-147">Example 2</span></span>

<span data-ttu-id="05e5e-148">Ruft alle dem Benutzer beim Scope testRG und höher vorgenommenen john.doe@contoso.com Dementzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="05e5e-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="05e5e-149">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="05e5e-149">Example 3</span></span>

<span data-ttu-id="05e5e-150">Ruft alle Verweigertzuordnungen des angegebenen Dienstprinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="05e5e-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="05e5e-151">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="05e5e-151">Example 4</span></span>

<span data-ttu-id="05e5e-152">Ruft Aufgaben im Websitebereich "website1" ab.</span><span class="sxs-lookup"><span data-stu-id="05e5e-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="05e5e-153">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="05e5e-153">PARAMETERS</span></span>

### <span data-ttu-id="05e5e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e5e-154">-DefaultProfile</span></span>
<span data-ttu-id="05e5e-155">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="05e5e-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05e5e-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="05e5e-156">-DenyAssignmentName</span></span>
<span data-ttu-id="05e5e-157">Name der Verweigerten Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="05e5e-157">Name of the deny assignment.</span></span>

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

### <span data-ttu-id="05e5e-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="05e5e-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="05e5e-159">Wenn angegeben, werden dem Benutzer und den Gruppen, deren Mitglied der Benutzer ist ( transitiv) direkt zugewiesene Verweigerte Zuordnungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="05e5e-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="05e5e-160">Wird nur für einen Benutzerprinzipal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05e5e-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="05e5e-161">-ID</span><span class="sxs-lookup"><span data-stu-id="05e5e-161">-Id</span></span>
<span data-ttu-id="05e5e-162">Verweigern Sie die Zuordnungs-ID.</span><span class="sxs-lookup"><span data-stu-id="05e5e-162">Deny assignment id.</span></span>

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

### <span data-ttu-id="05e5e-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="05e5e-163">-ObjectId</span></span>
<span data-ttu-id="05e5e-164">Die Azure AD-ObjectId des Benutzers, der Gruppe oder des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="05e5e-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="05e5e-165">Filtert alle Dementenzuordnungen, die dem angegebenen Prinzipal vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-165">Filters all deny assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="05e5e-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="05e5e-166">-ParentResource</span></span>
<span data-ttu-id="05e5e-167">Die übergeordnete Ressource in der Hierarchie der Ressource, die mit dem Parameter "ResourceName" angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="05e5e-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="05e5e-168">Muss in Verbindung mit den Parametern ResourceGroupName, ResourceType und ResourceName verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="05e5e-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e5e-169">-ResourceGroupName</span></span>
<span data-ttu-id="05e5e-170">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05e5e-170">The resource group name.</span></span>
<span data-ttu-id="05e5e-171">Listen verweigern Zuordnungen, die in der angegebenen Ressourcengruppe wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="05e5e-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="05e5e-172">Bei Verwendung in Verbindung mit den Parametern "ResourceName", "ResourceType" und "ParentResource" werden in der Befehlsliste Zuordnungen verweigert, die für Ressourcen innerhalb der Ressourcengruppe wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="05e5e-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="05e5e-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="05e5e-173">-ResourceName</span></span>
<span data-ttu-id="05e5e-174">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="05e5e-174">The resource name.</span></span>
<span data-ttu-id="05e5e-175">Für z. B. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="05e5e-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="05e5e-176">Muss in Verbindung mit den Parametern ResourceGroupName, ResourceType und (optional) ParentResource verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="05e5e-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="05e5e-177">-ResourceType</span></span>
<span data-ttu-id="05e5e-178">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="05e5e-178">The resource type.</span></span>
<span data-ttu-id="05e5e-179">Für z. B. Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="05e5e-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="05e5e-180">Muss in Verbindung mit den Parametern ResourceGroupName, ResourceName und (optional) ParentResource verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="05e5e-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="05e5e-181">-Scope</span></span>
<span data-ttu-id="05e5e-182">Der Umfang der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="05e5e-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="05e5e-183">Im Format des relativen URI.</span><span class="sxs-lookup"><span data-stu-id="05e5e-183">In the format of relative URI.</span></span>
<span data-ttu-id="05e5e-184">Für z. B. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="05e5e-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="05e5e-185">Sie muss mit "/subscriptions/{id}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="05e5e-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="05e5e-186">Der Befehl filtert alle Zuordnungen, die in diesem Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="05e5e-186">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="05e5e-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="05e5e-187">-ServicePrincipalName</span></span>
<span data-ttu-id="05e5e-188">Der ServicePrincipalName des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="05e5e-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="05e5e-189">Filtert alle verweigerten Zuordnungen, die an die angegebene Azure AD-Anwendung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="05e5e-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="05e5e-190">-SignInName</span></span>
<span data-ttu-id="05e5e-191">Die E-Mail-Adresse oder der Benutzername des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="05e5e-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="05e5e-192">Filtert alle Dementenzuweisungen, die dem angegebenen Benutzer vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="05e5e-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="05e5e-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e5e-193">CommonParameters</span></span>
<span data-ttu-id="05e5e-194">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e5e-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e5e-195">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05e5e-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e5e-196">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05e5e-196">INPUTS</span></span>

### <span data-ttu-id="05e5e-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="05e5e-197">System.Guid</span></span>

### <span data-ttu-id="05e5e-198">System.String</span><span class="sxs-lookup"><span data-stu-id="05e5e-198">System.String</span></span>

## <span data-ttu-id="05e5e-199">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05e5e-199">OUTPUTS</span></span>

### <span data-ttu-id="05e5e-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="05e5e-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="05e5e-201">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="05e5e-201">NOTES</span></span>
<span data-ttu-id="05e5e-202">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="05e5e-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="05e5e-203">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="05e5e-203">RELATED LINKS</span></span>
