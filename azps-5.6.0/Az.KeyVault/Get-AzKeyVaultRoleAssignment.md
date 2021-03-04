---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 7de4753d47ff2a285da6a9d3d60e0f95fcbf6e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944134"
---
# <span data-ttu-id="54c4c-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="54c4c-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="54c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="54c4c-103">Erhalten oder Auflisten von Rollenzuweisungen eines verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="54c4c-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="54c4c-104">Verwenden Sie entsprechende Parameter, um Zuordnungen zu einem bestimmten Benutzer oder einer Rollendefinition auflisten.</span><span class="sxs-lookup"><span data-stu-id="54c4c-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="54c4c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54c4c-105">SYNTAX</span></span>

### <span data-ttu-id="54c4c-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="54c4c-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c4c-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="54c4c-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c4c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54c4c-108">DESCRIPTION</span></span>
<span data-ttu-id="54c4c-109">Verwenden Sie `Get-AzKeyVaultRoleAssignment` den Befehl, um alle Rollenzuweisungen auflisten, die für einen Bereich wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="54c4c-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="54c4c-110">Ohne Parameter gibt dieser Befehl alle Rollenzuweisungen zurück, die unter dem verwalteten HSM vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="54c4c-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="54c4c-111">Diese Liste kann mithilfe von Filterparametern für Prinzipal, Rolle und Umfang gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="54c4c-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="54c4c-112">Der Betreff der Zuordnung muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54c4c-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="54c4c-113">Verwenden Sie zum Angeben eines Benutzers die Parameter SignInName oder Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="54c4c-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="54c4c-114">Verwenden Sie den Azure AD ObjectId-Parameter, um eine Sicherheitsgruppe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="54c4c-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="54c4c-115">Und zum Angeben einer Azure AD-Anwendung verwenden Sie die Parameter ApplicationId oder ObjectId.</span><span class="sxs-lookup"><span data-stu-id="54c4c-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="54c4c-116">Die zugewiesene Rolle muss mit dem Parameter RoleDefinitionName oder RoleDefinitionId angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54c4c-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="54c4c-117">Der Bereich, in dem der Zugriff gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54c4c-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="54c4c-118">Sie ist standardmäßig auf "/" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54c4c-118">It defaults to "/".</span></span>

## <span data-ttu-id="54c4c-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54c4c-119">EXAMPLES</span></span>

### <span data-ttu-id="54c4c-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54c4c-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="54c4c-121">In diesem Beispiel werden alle Rollenzuweisungen von "myHsm" für den ganzen Bereich aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="54c4c-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="54c4c-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="54c4c-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="54c4c-123">In diesem Beispiel werden alle Rollenzuweisungen von "myHsm" im Bereich "/keys" aufgeführt und das Ergebnis nach Dem Anmeldenamen des Benutzers filtern.</span><span class="sxs-lookup"><span data-stu-id="54c4c-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="54c4c-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54c4c-124">PARAMETERS</span></span>

### <span data-ttu-id="54c4c-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54c4c-125">-ApplicationId</span></span>
<span data-ttu-id="54c4c-126">Die App SPN.</span><span class="sxs-lookup"><span data-stu-id="54c4c-126">The app SPN.</span></span>

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

### <span data-ttu-id="54c4c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c4c-127">-DefaultProfile</span></span>
<span data-ttu-id="54c4c-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54c4c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c4c-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="54c4c-129">-HsmName</span></span>
<span data-ttu-id="54c4c-130">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="54c4c-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="54c4c-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="54c4c-131">-ObjectId</span></span>
<span data-ttu-id="54c4c-132">Die Benutzer- oder Gruppenobjekt-ID.</span><span class="sxs-lookup"><span data-stu-id="54c4c-132">The user or group object id.</span></span>

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

### <span data-ttu-id="54c4c-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="54c4c-133">-RoleAssignmentName</span></span>
<span data-ttu-id="54c4c-134">Name der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="54c4c-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="54c4c-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="54c4c-135">-RoleDefinitionId</span></span>
<span data-ttu-id="54c4c-136">Rollen-ID, der der Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="54c4c-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="54c4c-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="54c4c-137">-RoleDefinitionName</span></span>
<span data-ttu-id="54c4c-138">Name der Rolle "RBAC", mit der der Prinzipal zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="54c4c-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="54c4c-139">-Scope</span><span class="sxs-lookup"><span data-stu-id="54c4c-139">-Scope</span></span>
<span data-ttu-id="54c4c-140">Bereich, für den die Rollenzuweisung oder -definition gilt, z. B. "/" oder "/keys" oder "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="54c4c-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="54c4c-141">"/" wird verwendet, wenn sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="54c4c-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="54c4c-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="54c4c-142">-SignInName</span></span>
<span data-ttu-id="54c4c-143">Der Benutzer SignInName.</span><span class="sxs-lookup"><span data-stu-id="54c4c-143">The user SignInName.</span></span>

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

### <span data-ttu-id="54c4c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c4c-144">CommonParameters</span></span>
<span data-ttu-id="54c4c-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c4c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c4c-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54c4c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c4c-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54c4c-147">INPUTS</span></span>

### <span data-ttu-id="54c4c-148">Keine</span><span class="sxs-lookup"><span data-stu-id="54c4c-148">None</span></span>

## <span data-ttu-id="54c4c-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54c4c-149">OUTPUTS</span></span>

### <span data-ttu-id="54c4c-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="54c4c-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="54c4c-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54c4c-151">NOTES</span></span>

## <span data-ttu-id="54c4c-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54c4c-152">RELATED LINKS</span></span>
