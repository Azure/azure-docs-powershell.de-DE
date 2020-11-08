---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 20e80617d47cd0a1f0ffb5cdb80d836656cd9abd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175512"
---
# <span data-ttu-id="bfe79-101">Get-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="bfe79-101">Get-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="bfe79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bfe79-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe79-103">Abrufen oder Auflisten von Rollenzuweisungen für ein verwaltetes HSM</span><span class="sxs-lookup"><span data-stu-id="bfe79-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="bfe79-104">Verwenden Sie die entsprechenden Parameter, um Aufgaben für einen bestimmten Benutzer oder eine Rollendefinition aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="bfe79-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="bfe79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfe79-105">SYNTAX</span></span>

### <span data-ttu-id="bfe79-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="bfe79-106">List (Default)</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfe79-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="bfe79-107">GetByName</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfe79-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfe79-108">DESCRIPTION</span></span>
<span data-ttu-id="bfe79-109">Verwenden Sie den `Get-AzManagedHsmRoleAssignment` Befehl, um alle Rollenzuweisungen aufzulisten, die für einen Bereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="bfe79-109">Use the `Get-AzManagedHsmRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="bfe79-110">Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die unter dem verwalteten HSM vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bfe79-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="bfe79-111">Diese Liste kann mithilfe von Filterparametern für Principal, Role und Scope gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="bfe79-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="bfe79-112">Der Betreff der Aufgabe muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bfe79-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="bfe79-113">Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="bfe79-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="bfe79-114">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="bfe79-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="bfe79-115">Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie ApplicationId-oder ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="bfe79-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="bfe79-116">Die zugewiesene Rolle muss mithilfe des RoleDefinitionName-oder RoleDefinitionId-Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bfe79-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="bfe79-117">Der Bereich, in dem Access gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bfe79-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="bfe79-118">Standardmäßig wird "/" verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfe79-118">It defaults to "/".</span></span>

## <span data-ttu-id="bfe79-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfe79-119">EXAMPLES</span></span>

### <span data-ttu-id="bfe79-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bfe79-120">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="bfe79-121">In diesem Beispiel werden alle Rollenzuweisungen von "myHsm" für den gesamten Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bfe79-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="bfe79-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bfe79-122">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="bfe79-123">In diesem Beispiel werden alle Rollenzuweisungen von "myHsm" im Bereich "/Keys" aufgelistet, und das Ergebnis wird nach dem Anmeldenamen des Benutzers gefiltert.</span><span class="sxs-lookup"><span data-stu-id="bfe79-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="bfe79-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfe79-124">PARAMETERS</span></span>

### <span data-ttu-id="bfe79-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bfe79-125">-ApplicationId</span></span>
<span data-ttu-id="bfe79-126">Der APP-SPN.</span><span class="sxs-lookup"><span data-stu-id="bfe79-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe79-127">-DefaultProfile</span></span>
<span data-ttu-id="bfe79-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bfe79-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfe79-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="bfe79-129">-HsmName</span></span>
<span data-ttu-id="bfe79-130">Der Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="bfe79-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="bfe79-131">-ObjectId</span></span>
<span data-ttu-id="bfe79-132">Die Objekt-ID des Benutzers oder der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="bfe79-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="bfe79-133">-RoleAssignmentName</span></span>
<span data-ttu-id="bfe79-134">Der Name der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="bfe79-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe79-135">-RoleDefinitionId</span></span>
<span data-ttu-id="bfe79-136">Die Rollen-ID, der der Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bfe79-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bfe79-137">-RoleDefinitionName</span></span>
<span data-ttu-id="bfe79-138">Der Name der RBAC-Rolle, der der Prinzipal zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfe79-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-139">-Scope</span><span class="sxs-lookup"><span data-stu-id="bfe79-139">-Scope</span></span>
<span data-ttu-id="bfe79-140">Der Bereich, für den die Rollenzuweisung oder-Definition gilt, beispielsweise "/" oder "/Keys" oder "/Keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="bfe79-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="bfe79-141">"/" wird verwendet, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="bfe79-141">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="bfe79-142">-SignInName</span></span>
<span data-ttu-id="bfe79-143">Der Benutzer SignInName.</span><span class="sxs-lookup"><span data-stu-id="bfe79-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe79-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe79-144">CommonParameters</span></span>
<span data-ttu-id="bfe79-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe79-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe79-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfe79-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe79-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bfe79-147">INPUTS</span></span>

### <span data-ttu-id="bfe79-148">Keine</span><span class="sxs-lookup"><span data-stu-id="bfe79-148">None</span></span>

## <span data-ttu-id="bfe79-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bfe79-149">OUTPUTS</span></span>

### <span data-ttu-id="bfe79-150">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="bfe79-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="bfe79-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="bfe79-151">NOTES</span></span>

## <span data-ttu-id="bfe79-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bfe79-152">RELATED LINKS</span></span>
