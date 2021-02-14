---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147673"
---
# <span data-ttu-id="bb8e2-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="bb8e2-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="bb8e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8e2-103">Entfernt eine Rollenzuweisung für den angegebenen Prinzipal, dem eine bestimmte Rolle in einem bestimmten Bereich zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="bb8e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb8e2-104">SYNTAX</span></span>

### <span data-ttu-id="bb8e2-105">DefinitionNameSignInName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb8e2-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8e2-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="bb8e2-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8e2-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="bb8e2-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8e2-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="bb8e2-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8e2-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="bb8e2-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8e2-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="bb8e2-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8e2-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb8e2-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb8e2-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="bb8e2-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8e2-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb8e2-113">DESCRIPTION</span></span>
<span data-ttu-id="bb8e2-114">Verwenden Sie `Remove-AzKeyVaultRoleAssignment` das Cmdlet, um den Zugriff auf einen Beliebigen Prinzipal in einem bestimmten Bereich und einer bestimmten Rolle zu widerrufen.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="bb8e2-115">Das Objekt der Zuordnung, d. h. der Prinzipal MUSS angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="bb8e2-116">Der Prinzipal kann ein Benutzer (Verwenden von SignInName- oder ObjectId-Parametern zum Identifizieren eines Benutzers), eine Sicherheitsgruppe (mit dem ObjectId-Parameter zum Identifizieren einer Gruppe) oder ein Dienstprinzipal (ApplicationId- oder ObjectId-Parameter verwenden, um einen "ServicePrincipal" zu identifizieren) sein.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="bb8e2-117">Die Rolle, der der Prinzipal zugewiesen ist, muss mit dem Parameter "RoleDefinitionName" oder "RoleDefinitionId" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="bb8e2-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb8e2-118">EXAMPLES</span></span>

### <span data-ttu-id="bb8e2-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb8e2-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="bb8e2-120">In diesem Beispiel wird die Rolle "Verwalteter HSM-Richtlinienadministrator" von user1@microsoft.com "" im Bereich "/keys" widerrufen.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="bb8e2-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bb8e2-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="bb8e2-122">In diesem Beispiel werden alle Rollen von " user1@microsoft.com in allen Gültigkeitsbereich widerrufen.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="bb8e2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb8e2-123">PARAMETERS</span></span>

### <span data-ttu-id="bb8e2-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bb8e2-124">-ApplicationId</span></span>
<span data-ttu-id="bb8e2-125">Der App-SPN.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8e2-126">-DefaultProfile</span></span>
<span data-ttu-id="bb8e2-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb8e2-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="bb8e2-128">-HsmName</span></span>
<span data-ttu-id="bb8e2-129">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb8e2-130">-InputObject</span></span>
<span data-ttu-id="bb8e2-131">Rollenzuweisungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bb8e2-132">-ObjectId</span></span>
<span data-ttu-id="bb8e2-133">Die Id des Benutzer- oder Gruppenobjekts.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb8e2-134">-PassThru</span></span>
<span data-ttu-id="bb8e2-135">Geben Sie "true" zurück, wenn das HSM wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="bb8e2-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="bb8e2-136">-RoleAssignmentName</span></span>
<span data-ttu-id="bb8e2-137">Name der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bb8e2-138">-RoleDefinitionId</span></span>
<span data-ttu-id="bb8e2-139">Rollen-ID, der der Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bb8e2-140">-RoleDefinitionName</span></span>
<span data-ttu-id="bb8e2-141">Name der RBAC-Rolle, der der Prinzipal zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="bb8e2-142">-Scope</span></span>
<span data-ttu-id="bb8e2-143">Bereich, für den die Rollenzuweisung oder -definition gilt, z. B. '/' oder '/keys' oder '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="bb8e2-144">Bei Ausgelassen wird "/" verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="bb8e2-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="bb8e2-145">-SignInName</span></span>
<span data-ttu-id="bb8e2-146">Der Benutzer SignInName.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8e2-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb8e2-147">-Confirm</span></span>
<span data-ttu-id="bb8e2-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8e2-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bb8e2-149">-WhatIf</span></span>
<span data-ttu-id="bb8e2-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb8e2-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8e2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8e2-152">CommonParameters</span></span>
<span data-ttu-id="bb8e2-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8e2-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb8e2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8e2-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb8e2-155">INPUTS</span></span>

### <span data-ttu-id="bb8e2-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="bb8e2-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="bb8e2-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb8e2-157">OUTPUTS</span></span>

### <span data-ttu-id="bb8e2-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="bb8e2-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="bb8e2-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb8e2-159">NOTES</span></span>

## <span data-ttu-id="bb8e2-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb8e2-160">RELATED LINKS</span></span>
