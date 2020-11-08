---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 3b02bf3471546c9b6bc68d0ded109133341d20bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175509"
---
# <span data-ttu-id="6316a-101">New-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6316a-101">New-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="6316a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6316a-102">SYNOPSIS</span></span>
<span data-ttu-id="6316a-103">Weist die angegebene RBAC-Rolle dem angegebenen Prinzipal im angegebenen Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="6316a-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="6316a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6316a-104">SYNTAX</span></span>

### <span data-ttu-id="6316a-105">DefinitionNameSignInName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6316a-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6316a-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="6316a-106">DefinitionNameApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6316a-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="6316a-107">DefinitionNameObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6316a-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="6316a-108">DefinitionIdApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6316a-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="6316a-109">DefinitionIdObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6316a-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="6316a-110">DefinitionIdSignInName</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6316a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6316a-111">DESCRIPTION</span></span>
<span data-ttu-id="6316a-112">Verwenden Sie den `New-AzManagedHsmRoleAssignment` Befehl zum Gewähren des Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="6316a-112">Use the `New-AzManagedHsmRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="6316a-113">Der Zugriff wird durch Zuweisen der entsprechenden RBAC-Rolle im richtigen Bereich gewährt.</span><span class="sxs-lookup"><span data-stu-id="6316a-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="6316a-114">Der Betreff der Aufgabe muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6316a-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="6316a-115">Verwenden Sie zum Angeben eines Benutzers SignInName-oder Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6316a-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="6316a-116">Verwenden Sie zum Angeben einer Sicherheitsgruppe den Azure AD-ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6316a-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="6316a-117">Wenn Sie eine Azure AD-Anwendung angeben möchten, verwenden Sie ApplicationId-oder ObjectID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6316a-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="6316a-118">Die zugewiesene Rolle muss mit dem RoleDefinitionName PR RoleDefinitionId-Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6316a-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="6316a-119">Der Bereich, in dem Access gewährt wird, kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6316a-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="6316a-120">Sie ist standardmäßig auf das ausgewählte Abonnement eingestellt.</span><span class="sxs-lookup"><span data-stu-id="6316a-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="6316a-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6316a-121">EXAMPLES</span></span>

### <span data-ttu-id="6316a-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6316a-122">Example 1</span></span>
```powershell
PS C:\> New-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="6316a-123">In diesem Beispiel wird der Rolle "Managed HSM Policy Administrator" dem Benutzer " user1@microsoft.com " im oberen Bereich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6316a-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="6316a-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="6316a-124">PARAMETERS</span></span>

### <span data-ttu-id="6316a-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6316a-125">-ApplicationId</span></span>
<span data-ttu-id="6316a-126">Der APP-SPN.</span><span class="sxs-lookup"><span data-stu-id="6316a-126">The app SPN.</span></span>

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

### <span data-ttu-id="6316a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6316a-127">-DefaultProfile</span></span>
<span data-ttu-id="6316a-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6316a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6316a-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6316a-129">-HsmName</span></span>
<span data-ttu-id="6316a-130">Der Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="6316a-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="6316a-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="6316a-131">-ObjectId</span></span>
<span data-ttu-id="6316a-132">Die Objekt-ID des Benutzers oder der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6316a-132">The user or group object id.</span></span>

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

### <span data-ttu-id="6316a-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6316a-133">-RoleDefinitionId</span></span>
<span data-ttu-id="6316a-134">Die Rollen-ID, der der Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6316a-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="6316a-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6316a-135">-RoleDefinitionName</span></span>
<span data-ttu-id="6316a-136">Der Name der RBAC-Rolle, der der Prinzipal zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6316a-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="6316a-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="6316a-137">-Scope</span></span>
<span data-ttu-id="6316a-138">Der Bereich, für den die Rollenzuweisung oder-Definition gilt, beispielsweise "/" oder "/Keys" oder "/Keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="6316a-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="6316a-139">"/" wird verwendet, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="6316a-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="6316a-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6316a-140">-SignInName</span></span>
<span data-ttu-id="6316a-141">Der Benutzer SignInName.</span><span class="sxs-lookup"><span data-stu-id="6316a-141">The user SignInName.</span></span>

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

### <span data-ttu-id="6316a-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6316a-142">-Confirm</span></span>
<span data-ttu-id="6316a-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6316a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6316a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6316a-144">-WhatIf</span></span>
<span data-ttu-id="6316a-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6316a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6316a-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6316a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6316a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6316a-147">CommonParameters</span></span>
<span data-ttu-id="6316a-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6316a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6316a-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6316a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6316a-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6316a-150">INPUTS</span></span>

### <span data-ttu-id="6316a-151">Keine</span><span class="sxs-lookup"><span data-stu-id="6316a-151">None</span></span>

## <span data-ttu-id="6316a-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6316a-152">OUTPUTS</span></span>

### <span data-ttu-id="6316a-153">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6316a-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="6316a-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="6316a-154">NOTES</span></span>

## <span data-ttu-id="6316a-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6316a-155">RELATED LINKS</span></span>
