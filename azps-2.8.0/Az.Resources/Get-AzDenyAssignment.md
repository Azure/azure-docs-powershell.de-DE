---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 745df057c7c111bdca7cc30ac0864e15905ffd6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823531"
---
# <span data-ttu-id="8b838-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8b838-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="8b838-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b838-102">SYNOPSIS</span></span>
<span data-ttu-id="8b838-103">Listet Azure-RBAC-Deny-Zuweisungen im angegebenen Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="8b838-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="8b838-104">Standardmäßig werden alle Verweigerungs Aufgaben im ausgewählten Azure-Abonnement aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8b838-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="8b838-105">Verwenden Sie die entsprechenden Parameter zum Auflisten von Verweigerungs Zuweisungen für einen bestimmten Benutzer oder zum Auflisten von Verweigerungs Aufgaben für eine bestimmte Ressourcengruppe oder Ressource.</span><span class="sxs-lookup"><span data-stu-id="8b838-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="8b838-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b838-106">SYNTAX</span></span>

### <span data-ttu-id="8b838-107">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b838-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-108">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-108">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-109">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-109">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment -DenyAssignmentName <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-110">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-110">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-111">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-111">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-112">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-112">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-113">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-113">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-114">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-114">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-115">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-115">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-116">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-116">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-117">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-117">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-118">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-118">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-119">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-119">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-120">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-120">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-121">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-121">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-122">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-122">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-123">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-123">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b838-124">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b838-124">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b838-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b838-125">DESCRIPTION</span></span>
<span data-ttu-id="8b838-126">Verwenden Sie den Befehl Get-AzDenyAssignment, um alle Verweigerungs Aufgaben aufzulisten, die für einen Bereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8b838-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="8b838-127">Ohne Parameter gibt dieser Befehl alle Verweigerungs Aufgaben zurück, die unter dem Abonnement vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8b838-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="8b838-128">Diese Liste kann mithilfe von Filterparametern für Principal, Zuweisungsname und Bereich verweigern gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="8b838-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="8b838-129">Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b838-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="8b838-130">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b838-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="8b838-131">Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie servicePrincipalName-oder ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b838-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="8b838-132">Der Bereich, in dem der Zugriff verweigert wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b838-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="8b838-133">Sie ist standardmäßig auf das ausgewählte Abonnement eingestellt.</span><span class="sxs-lookup"><span data-stu-id="8b838-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="8b838-134">Der Bereich der Verweigerungs Zuweisung kann mithilfe einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b838-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="8b838-135">Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \< \> -Abonnement-Nr.</span><span class="sxs-lookup"><span data-stu-id="8b838-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="8b838-136">Dadurch werden die Aufgaben, die in diesem bestimmten Bereich gültig sind, d.h. alle Aufgaben, die in diesem Bereich und oberhalb verweigert werden, abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="8b838-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8b838-137">b.</span><span class="sxs-lookup"><span data-stu-id="8b838-137">b.</span></span>
<span data-ttu-id="8b838-138">ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b838-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="8b838-139">Dadurch werden die Aufgaben, die bei der angegebenen Ressourcengruppe gültig sind, d.h. alle Aufgaben, die in diesem Bereich und oben abgelehnt werden, gefiltert.</span><span class="sxs-lookup"><span data-stu-id="8b838-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8b838-140">c.</span><span class="sxs-lookup"><span data-stu-id="8b838-140">c.</span></span>
<span data-ttu-id="8b838-141">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource-kennzeichnet eine bestimmte Ressource unter dem Abonnement und filtert Aufgaben, die für diesen Ressourcenbereich effektiv sind.</span><span class="sxs-lookup"><span data-stu-id="8b838-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="8b838-142">Verwenden Sie den ExpandPrincipalGroups-Schalter, um festzustellen, welcher Zugriff für einen bestimmten Benutzer im Abonnement verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="8b838-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="8b838-143">Dadurch werden alle dem Benutzer zugewiesenen Deny-Zuweisungen sowie die Gruppen aufgeführt, in denen der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="8b838-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="8b838-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b838-144">EXAMPLES</span></span>

### <span data-ttu-id="8b838-145">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b838-145">Example 1</span></span>

<span data-ttu-id="8b838-146">Auflisten aller Verweigerungs Aufgaben im Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b838-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="8b838-147">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8b838-147">Example 2</span></span>

<span data-ttu-id="8b838-148">Ruft alle Deny-Aufgaben ab, john.doe@contoso.com die an den Benutzer im Bereich testRG und höher vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8b838-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="8b838-149">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8b838-149">Example 3</span></span>

<span data-ttu-id="8b838-150">Ruft alle Deny-Zuweisungen des angegebenen Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="8b838-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="8b838-151">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="8b838-151">Example 4</span></span>

<span data-ttu-id="8b838-152">Ruft Aufgaben im Bereich "site1" auf.</span><span class="sxs-lookup"><span data-stu-id="8b838-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="8b838-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b838-153">PARAMETERS</span></span>

### <span data-ttu-id="8b838-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b838-154">-DefaultProfile</span></span>
<span data-ttu-id="8b838-155">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b838-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b838-156">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="8b838-156">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="8b838-157">Gibt, falls angegeben, die Deny-Zuweisungen zurück, die dem Benutzer und den Gruppen, denen der Benutzer angehört (transitiv), direkt zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="8b838-157">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="8b838-158">Wird nur für einen Benutzerprinzipal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b838-158">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="8b838-159">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8b838-159">-ObjectId</span></span>
<span data-ttu-id="8b838-160">Die Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="8b838-160">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="8b838-161">Filtert alle Verweigerungs Aufgaben, die am angegebenen Prinzipal vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8b838-161">Filters all deny assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="8b838-162">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="8b838-162">-ParentResource</span></span>
<span data-ttu-id="8b838-163">Die übergeordnete Ressource in der Hierarchie der Ressource, die mithilfe des resourceName-Parameters angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8b838-163">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="8b838-164">Muss in Verbindung mit den Parametern "ResourceGroupName", "Ressourcenparameter" und "resourceName" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b838-164">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="8b838-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b838-165">-ResourceGroupName</span></span>
<span data-ttu-id="8b838-166">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8b838-166">The resource group name.</span></span>
<span data-ttu-id="8b838-167">Listet Aufgaben ab, die für die angegebene Ressourcengruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8b838-167">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="8b838-168">Bei Verwendung in Verbindung mit resourceName-, ResourceType-und ParentResource-Parametern listet der Befehl Aufgaben auf, die bei Ressourcen innerhalb der Ressourcengruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8b838-168">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="8b838-169">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8b838-169">-ResourceName</span></span>
<span data-ttu-id="8b838-170">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8b838-170">The resource name.</span></span>
<span data-ttu-id="8b838-171">Für z.b. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="8b838-171">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="8b838-172">Muss in Verbindung mit ResourceGroupName-, Parameter-und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b838-172">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="8b838-173">-</span><span class="sxs-lookup"><span data-stu-id="8b838-173">-ResourceType</span></span>
<span data-ttu-id="8b838-174">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="8b838-174">The resource type.</span></span>
<span data-ttu-id="8b838-175">Für z.b. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="8b838-175">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="8b838-176">Muss in Verbindung mit ResourceGroupName-, resourceName-und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b838-176">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="8b838-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="8b838-177">-Scope</span></span>
<span data-ttu-id="8b838-178">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="8b838-178">The Scope of the role assignment.</span></span>
<span data-ttu-id="8b838-179">Im Format des relativen URIs.</span><span class="sxs-lookup"><span data-stu-id="8b838-179">In the format of relative URI.</span></span>
<span data-ttu-id="8b838-180">Für z.b./Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="8b838-180">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="8b838-181">Sie muss mit "/Subscriptions/{ID}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="8b838-181">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="8b838-182">Der Befehl filtert alle Verweigerungs Aufgaben, die in diesem Bereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8b838-182">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="8b838-183">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8b838-183">-ServicePrincipalName</span></span>
<span data-ttu-id="8b838-184">Die servicePrincipalName des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="8b838-184">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="8b838-185">Filtert alle Deny-Zuweisungen, die an der angegebenen Azure AD-Anwendung vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8b838-185">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="8b838-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="8b838-186">-SignInName</span></span>
<span data-ttu-id="8b838-187">Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8b838-187">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="8b838-188">Filtert alle Deny-Zuweisungen, die an den angegebenen Benutzer vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8b838-188">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="8b838-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b838-189">CommonParameters</span></span>
<span data-ttu-id="8b838-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b838-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b838-191">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b838-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b838-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b838-192">INPUTS</span></span>

### <span data-ttu-id="8b838-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8b838-193">System.Guid</span></span>

### <span data-ttu-id="8b838-194">System. String</span><span class="sxs-lookup"><span data-stu-id="8b838-194">System.String</span></span>

## <span data-ttu-id="8b838-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b838-195">OUTPUTS</span></span>

### <span data-ttu-id="8b838-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8b838-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="8b838-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b838-197">NOTES</span></span>
<span data-ttu-id="8b838-198">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="8b838-198">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>