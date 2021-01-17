---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ee90ab1b4ba22f1a5c40427f7fc435c75cef992d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458327"
---
# <span data-ttu-id="f7d2e-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f7d2e-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="f7d2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d2e-103">Weist dem angegebenen Prinzipal im angegebenen Bereich die angegebene RbAC-Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="f7d2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7d2e-104">SYNTAX</span></span>

### <span data-ttu-id="f7d2e-105">DefinitionNameSignInName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7d2e-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d2e-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="f7d2e-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d2e-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="f7d2e-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d2e-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="f7d2e-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d2e-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="f7d2e-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d2e-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="f7d2e-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d2e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7d2e-111">DESCRIPTION</span></span>
<span data-ttu-id="f7d2e-112">Verwenden Sie den `New-AzKeyVaultRoleAssignment` Befehl, um den Zugriff zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="f7d2e-113">Access wird gewährt, indem ihnen im richtigen Bereich die entsprechende RbAC-Rolle zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="f7d2e-114">Der Betreff der Zuordnung muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="f7d2e-115">Verwenden Sie zum Angeben eines Benutzers die Parameter "SignInName" oder "Azure AD ObjectId".</span><span class="sxs-lookup"><span data-stu-id="f7d2e-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="f7d2e-116">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD ObjectId-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="f7d2e-117">Verwenden Sie zum Angeben einer Azure AD-Anwendung die Parameter ApplicationId oder ObjectId.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="f7d2e-118">Die zugewiesene Rolle muss mit dem Parameter "RoleDefinitionName pr RoleDefinitionId" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="f7d2e-119">Der Bereich, für den der Zugriff gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="f7d2e-120">Standardmäßig wird das ausgewählte Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="f7d2e-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7d2e-121">EXAMPLES</span></span>

### <span data-ttu-id="f7d2e-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7d2e-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="f7d2e-123">In diesem Beispiel wird dem Benutzer "" im oberen Bereich die Rolle "Verwalteter user1@microsoft.com HSM-Richtlinienadministrator" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="f7d2e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7d2e-124">PARAMETERS</span></span>

### <span data-ttu-id="f7d2e-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f7d2e-125">-ApplicationId</span></span>
<span data-ttu-id="f7d2e-126">Der App-SPN.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-126">The app SPN.</span></span>

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

### <span data-ttu-id="f7d2e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d2e-127">-DefaultProfile</span></span>
<span data-ttu-id="f7d2e-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d2e-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f7d2e-129">-HsmName</span></span>
<span data-ttu-id="f7d2e-130">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="f7d2e-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7d2e-131">-ObjectId</span></span>
<span data-ttu-id="f7d2e-132">Die Id des Benutzer- oder Gruppenobjekts.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-132">The user or group object id.</span></span>

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

### <span data-ttu-id="f7d2e-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f7d2e-133">-RoleDefinitionId</span></span>
<span data-ttu-id="f7d2e-134">Rollen-ID, der der Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="f7d2e-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f7d2e-135">-RoleDefinitionName</span></span>
<span data-ttu-id="f7d2e-136">Name der RBAC-Rolle, der der Prinzipal zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="f7d2e-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="f7d2e-137">-Scope</span></span>
<span data-ttu-id="f7d2e-138">Bereich, für den die Rollenzuweisung oder -definition gilt, z. B. '/' oder '/keys' oder '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="f7d2e-139">Bei Ausgelassen wird "/" verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="f7d2e-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f7d2e-140">-SignInName</span></span>
<span data-ttu-id="f7d2e-141">Der Benutzer SignInName.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-141">The user SignInName.</span></span>

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

### <span data-ttu-id="f7d2e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7d2e-142">-Confirm</span></span>
<span data-ttu-id="f7d2e-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d2e-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f7d2e-144">-WhatIf</span></span>
<span data-ttu-id="f7d2e-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d2e-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d2e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d2e-147">CommonParameters</span></span>
<span data-ttu-id="f7d2e-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d2e-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7d2e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d2e-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7d2e-150">INPUTS</span></span>

### <span data-ttu-id="f7d2e-151">Keine</span><span class="sxs-lookup"><span data-stu-id="f7d2e-151">None</span></span>

## <span data-ttu-id="f7d2e-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7d2e-152">OUTPUTS</span></span>

### <span data-ttu-id="f7d2e-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f7d2e-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="f7d2e-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7d2e-154">NOTES</span></span>

## <span data-ttu-id="f7d2e-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7d2e-155">RELATED LINKS</span></span>
