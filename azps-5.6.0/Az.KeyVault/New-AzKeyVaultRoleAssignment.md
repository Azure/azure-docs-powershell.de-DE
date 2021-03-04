---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ae55bf782f627c17cd73cbb075fd9f0d36ae6081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944063"
---
# <span data-ttu-id="953c3-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="953c3-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="953c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="953c3-102">SYNOPSIS</span></span>
<span data-ttu-id="953c3-103">Weist dem angegebenen Prinzipal im angegebenen Bereich die angegebene RBAC-Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="953c3-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="953c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="953c3-104">SYNTAX</span></span>

### <span data-ttu-id="953c3-105">DefinitionNameSignInName (Standard)</span><span class="sxs-lookup"><span data-stu-id="953c3-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953c3-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="953c3-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953c3-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="953c3-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953c3-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="953c3-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953c3-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="953c3-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953c3-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="953c3-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="953c3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="953c3-111">DESCRIPTION</span></span>
<span data-ttu-id="953c3-112">Verwenden Sie den `New-AzKeyVaultRoleAssignment` Befehl, um Zugriff zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="953c3-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="953c3-113">Access wird gewährt, indem ihnen die entsprechende RBAC-Rolle im richtigen Bereich zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="953c3-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="953c3-114">Der Betreff der Zuordnung muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="953c3-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="953c3-115">Verwenden Sie zum Angeben eines Benutzers die Parameter SignInName oder Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="953c3-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="953c3-116">Verwenden Sie den Azure AD ObjectId-Parameter, um eine Sicherheitsgruppe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="953c3-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="953c3-117">Und zum Angeben einer Azure AD-Anwendung verwenden Sie die Parameter ApplicationId oder ObjectId.</span><span class="sxs-lookup"><span data-stu-id="953c3-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="953c3-118">Die zugewiesene Rolle muss mit dem Parameter RoleDefinitionName pr RoleDefinitionId angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="953c3-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="953c3-119">Der Bereich, in dem der Zugriff gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="953c3-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="953c3-120">Es ist standardmäßig für das ausgewählte Abonnement festgelegt.</span><span class="sxs-lookup"><span data-stu-id="953c3-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="953c3-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="953c3-121">EXAMPLES</span></span>

### <span data-ttu-id="953c3-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="953c3-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="953c3-123">In diesem Beispiel wird dem Benutzer im obersten Bereich die Rolle "Verwalteter HSM-Richtlinienadministrator" user1@microsoft.com zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="953c3-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="953c3-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="953c3-124">PARAMETERS</span></span>

### <span data-ttu-id="953c3-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="953c3-125">-ApplicationId</span></span>
<span data-ttu-id="953c3-126">Die App SPN.</span><span class="sxs-lookup"><span data-stu-id="953c3-126">The app SPN.</span></span>

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

### <span data-ttu-id="953c3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953c3-127">-DefaultProfile</span></span>
<span data-ttu-id="953c3-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="953c3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="953c3-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="953c3-129">-HsmName</span></span>
<span data-ttu-id="953c3-130">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="953c3-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="953c3-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="953c3-131">-ObjectId</span></span>
<span data-ttu-id="953c3-132">Die Benutzer- oder Gruppenobjekt-ID.</span><span class="sxs-lookup"><span data-stu-id="953c3-132">The user or group object id.</span></span>

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

### <span data-ttu-id="953c3-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="953c3-133">-RoleDefinitionId</span></span>
<span data-ttu-id="953c3-134">Rollen-ID, der der Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="953c3-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="953c3-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="953c3-135">-RoleDefinitionName</span></span>
<span data-ttu-id="953c3-136">Name der Rolle "RBAC", mit der der Prinzipal zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="953c3-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="953c3-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="953c3-137">-Scope</span></span>
<span data-ttu-id="953c3-138">Bereich, für den die Rollenzuweisung oder -definition gilt, z. B. "/" oder "/keys" oder "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="953c3-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="953c3-139">"/" wird verwendet, wenn sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="953c3-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="953c3-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="953c3-140">-SignInName</span></span>
<span data-ttu-id="953c3-141">Der Benutzer SignInName.</span><span class="sxs-lookup"><span data-stu-id="953c3-141">The user SignInName.</span></span>

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

### <span data-ttu-id="953c3-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="953c3-142">-Confirm</span></span>
<span data-ttu-id="953c3-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="953c3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="953c3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953c3-144">-WhatIf</span></span>
<span data-ttu-id="953c3-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="953c3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="953c3-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="953c3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="953c3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953c3-147">CommonParameters</span></span>
<span data-ttu-id="953c3-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953c3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953c3-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="953c3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953c3-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="953c3-150">INPUTS</span></span>

### <span data-ttu-id="953c3-151">Keine</span><span class="sxs-lookup"><span data-stu-id="953c3-151">None</span></span>

## <span data-ttu-id="953c3-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="953c3-152">OUTPUTS</span></span>

### <span data-ttu-id="953c3-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="953c3-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="953c3-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="953c3-154">NOTES</span></span>

## <span data-ttu-id="953c3-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="953c3-155">RELATED LINKS</span></span>
