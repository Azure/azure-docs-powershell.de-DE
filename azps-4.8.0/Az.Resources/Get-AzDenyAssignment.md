---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165688"
---
# <span data-ttu-id="eaccd-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="eaccd-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="eaccd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eaccd-102">SYNOPSIS</span></span>
<span data-ttu-id="eaccd-103">Listet Azure-RBAC-Deny-Zuweisungen im angegebenen Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="eaccd-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="eaccd-104">Standardmäßig werden alle Verweigerungs Aufgaben im ausgewählten Azure-Abonnement aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eaccd-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="eaccd-105">Verwenden Sie die entsprechenden Parameter zum Auflisten von Verweigerungs Zuweisungen für einen bestimmten Benutzer oder zum Auflisten von Verweigerungs Aufgaben für eine bestimmte Ressourcengruppe oder Ressource.</span><span class="sxs-lookup"><span data-stu-id="eaccd-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="eaccd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaccd-106">SYNTAX</span></span>

### <span data-ttu-id="eaccd-107">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eaccd-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaccd-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaccd-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaccd-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaccd-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaccd-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaccd-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaccd-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaccd-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eaccd-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eaccd-125">DESCRIPTION</span></span>
<span data-ttu-id="eaccd-126">Verwenden Sie den Befehl Get-AzDenyAssignment, um alle Verweigerungs Aufgaben aufzulisten, die für einen Bereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="eaccd-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="eaccd-127">Ohne Parameter gibt dieser Befehl alle Verweigerungs Aufgaben zurück, die unter dem Abonnement vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="eaccd-128">Diese Liste kann mithilfe von Filterparametern für Principal, Zuweisungsname und Bereich verweigern gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="eaccd-129">Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="eaccd-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="eaccd-130">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="eaccd-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="eaccd-131">Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie servicePrincipalName-oder ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="eaccd-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="eaccd-132">Der Bereich, in dem der Zugriff verweigert wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="eaccd-133">Sie ist standardmäßig auf das ausgewählte Abonnement eingestellt.</span><span class="sxs-lookup"><span data-stu-id="eaccd-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="eaccd-134">Der Bereich der Verweigerungs Zuweisung kann mithilfe einer der folgenden Parameterkombinationen a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="eaccd-135">Scope – Dies ist der vollqualifizierte Bereich, beginnend mit/Subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="eaccd-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="eaccd-136">Dadurch werden die Aufgaben, die in diesem bestimmten Bereich gültig sind, d.h. alle Aufgaben, die in diesem Bereich und oberhalb verweigert werden, abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="eaccd-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="eaccd-137">b.</span><span class="sxs-lookup"><span data-stu-id="eaccd-137">b.</span></span>
<span data-ttu-id="eaccd-138">ResourceGroupName – Name einer beliebigen Ressourcengruppe unter dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eaccd-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="eaccd-139">Dadurch werden die Aufgaben, die bei der angegebenen Ressourcengruppe gültig sind, d.h. alle Aufgaben, die in diesem Bereich und oben abgelehnt werden, gefiltert.</span><span class="sxs-lookup"><span data-stu-id="eaccd-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="eaccd-140">c.</span><span class="sxs-lookup"><span data-stu-id="eaccd-140">c.</span></span>
<span data-ttu-id="eaccd-141">ResourceName, ResourceType, ResourceGroupName und (optional) ParentResource-kennzeichnet eine bestimmte Ressource unter dem Abonnement und filtert Aufgaben, die für diesen Ressourcenbereich effektiv sind.</span><span class="sxs-lookup"><span data-stu-id="eaccd-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="eaccd-142">Verwenden Sie den ExpandPrincipalGroups-Schalter, um festzustellen, welcher Zugriff für einen bestimmten Benutzer im Abonnement verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="eaccd-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="eaccd-143">Dadurch werden alle dem Benutzer zugewiesenen Deny-Zuweisungen sowie die Gruppen aufgeführt, in denen der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="eaccd-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="eaccd-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaccd-144">EXAMPLES</span></span>

### <span data-ttu-id="eaccd-145">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eaccd-145">Example 1</span></span>

<span data-ttu-id="eaccd-146">Auflisten aller Verweigerungs Aufgaben im Abonnement</span><span class="sxs-lookup"><span data-stu-id="eaccd-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="eaccd-147">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eaccd-147">Example 2</span></span>

<span data-ttu-id="eaccd-148">Ruft alle Deny-Aufgaben ab, john.doe@contoso.com die an den Benutzer im Bereich testRG und höher vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="eaccd-149">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="eaccd-149">Example 3</span></span>

<span data-ttu-id="eaccd-150">Ruft alle Deny-Zuweisungen des angegebenen Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="eaccd-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="eaccd-151">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="eaccd-151">Example 4</span></span>

<span data-ttu-id="eaccd-152">Ruft Aufgaben im Bereich "site1" auf.</span><span class="sxs-lookup"><span data-stu-id="eaccd-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="eaccd-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaccd-153">PARAMETERS</span></span>

### <span data-ttu-id="eaccd-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaccd-154">-DefaultProfile</span></span>
<span data-ttu-id="eaccd-155">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eaccd-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaccd-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="eaccd-156">-DenyAssignmentName</span></span>
<span data-ttu-id="eaccd-157">Der Name der Verweigerungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="eaccd-157">Name of the deny assignment.</span></span>

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

### <span data-ttu-id="eaccd-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="eaccd-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="eaccd-159">Gibt, falls angegeben, die Deny-Zuweisungen zurück, die dem Benutzer und den Gruppen, denen der Benutzer angehört (transitiv), direkt zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="eaccd-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="eaccd-160">Wird nur für einen Benutzerprinzipal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eaccd-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="eaccd-161">-ID</span><span class="sxs-lookup"><span data-stu-id="eaccd-161">-Id</span></span>
<span data-ttu-id="eaccd-162">Zuordnungs-ID ablehnen</span><span class="sxs-lookup"><span data-stu-id="eaccd-162">Deny assignment id.</span></span>

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

### <span data-ttu-id="eaccd-163">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="eaccd-163">-ObjectId</span></span>
<span data-ttu-id="eaccd-164">Die Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="eaccd-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="eaccd-165">Filtert alle Verweigerungs Aufgaben, die am angegebenen Prinzipal vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-165">Filters all deny assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="eaccd-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="eaccd-166">-ParentResource</span></span>
<span data-ttu-id="eaccd-167">Die übergeordnete Ressource in der Hierarchie der Ressource, die mithilfe des resourceName-Parameters angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="eaccd-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="eaccd-168">Muss in Verbindung mit den Parametern "ResourceGroupName", "Ressourcenparameter" und "resourceName" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="eaccd-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaccd-169">-ResourceGroupName</span></span>
<span data-ttu-id="eaccd-170">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eaccd-170">The resource group name.</span></span>
<span data-ttu-id="eaccd-171">Listet Aufgaben ab, die für die angegebene Ressourcengruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="eaccd-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="eaccd-172">Bei Verwendung in Verbindung mit resourceName-, ResourceType-und ParentResource-Parametern listet der Befehl Aufgaben auf, die bei Ressourcen innerhalb der Ressourcengruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="eaccd-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="eaccd-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="eaccd-173">-ResourceName</span></span>
<span data-ttu-id="eaccd-174">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="eaccd-174">The resource name.</span></span>
<span data-ttu-id="eaccd-175">Für z.b. storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="eaccd-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="eaccd-176">Muss in Verbindung mit ResourceGroupName-, Parameter-und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="eaccd-177">-</span><span class="sxs-lookup"><span data-stu-id="eaccd-177">-ResourceType</span></span>
<span data-ttu-id="eaccd-178">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="eaccd-178">The resource type.</span></span>
<span data-ttu-id="eaccd-179">Für z.b. Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="eaccd-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="eaccd-180">Muss in Verbindung mit ResourceGroupName-, resourceName-und (optional) ParentResource-Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="eaccd-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="eaccd-181">-Scope</span></span>
<span data-ttu-id="eaccd-182">Der Bereich der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="eaccd-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="eaccd-183">Im Format des relativen URIs.</span><span class="sxs-lookup"><span data-stu-id="eaccd-183">In the format of relative URI.</span></span>
<span data-ttu-id="eaccd-184">Für z.b./Subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="eaccd-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="eaccd-185">Sie muss mit "/Subscriptions/{ID}" beginnen.</span><span class="sxs-lookup"><span data-stu-id="eaccd-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="eaccd-186">Der Befehl filtert alle Verweigerungs Aufgaben, die in diesem Bereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="eaccd-186">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="eaccd-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="eaccd-187">-ServicePrincipalName</span></span>
<span data-ttu-id="eaccd-188">Die servicePrincipalName des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="eaccd-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="eaccd-189">Filtert alle Deny-Zuweisungen, die an der angegebenen Azure AD-Anwendung vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="eaccd-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="eaccd-190">-SignInName</span></span>
<span data-ttu-id="eaccd-191">Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="eaccd-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="eaccd-192">Filtert alle Deny-Zuweisungen, die an den angegebenen Benutzer vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="eaccd-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="eaccd-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaccd-193">CommonParameters</span></span>
<span data-ttu-id="eaccd-194">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaccd-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaccd-195">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaccd-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaccd-196">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eaccd-196">INPUTS</span></span>

### <span data-ttu-id="eaccd-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="eaccd-197">System.Guid</span></span>

### <span data-ttu-id="eaccd-198">System. String</span><span class="sxs-lookup"><span data-stu-id="eaccd-198">System.String</span></span>

## <span data-ttu-id="eaccd-199">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eaccd-199">OUTPUTS</span></span>

### <span data-ttu-id="eaccd-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="eaccd-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="eaccd-201">Notizen</span><span class="sxs-lookup"><span data-stu-id="eaccd-201">NOTES</span></span>
<span data-ttu-id="eaccd-202">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="eaccd-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="eaccd-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eaccd-203">RELATED LINKS</span></span>
