---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175494"
---
# <span data-ttu-id="642f6-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="642f6-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="642f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="642f6-102">SYNOPSIS</span></span>
<span data-ttu-id="642f6-103">Entfernt eine Rollenzuweisung an den angegebenen Prinzipal, der einer bestimmten Rolle in einem bestimmten Bereich zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="642f6-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="642f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="642f6-104">SYNTAX</span></span>

### <span data-ttu-id="642f6-105">DefinitionNameSignInName (Standard)</span><span class="sxs-lookup"><span data-stu-id="642f6-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642f6-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="642f6-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642f6-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="642f6-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642f6-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="642f6-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642f6-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="642f6-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642f6-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="642f6-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642f6-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="642f6-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642f6-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="642f6-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="642f6-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642f6-113">DESCRIPTION</span></span>
<span data-ttu-id="642f6-114">Verwenden Sie das `Remove-AzManagedHsmRoleAssignment` Cmdlet, um den Zugriff auf alle Prinzipale im angegebenen Bereich und der angegebenen Rolle zu widerrufen.</span><span class="sxs-lookup"><span data-stu-id="642f6-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="642f6-115">Das Objekt der Aufgabe, also der Prinzipal, muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="642f6-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="642f6-116">Der Prinzipal kann ein Benutzer sein (verwenden Sie SignInName-oder ObjectID-Parameter, um einen Benutzer zu identifizieren), Sicherheitsgruppe (verwenden Sie ObjectID-Parameter, um eine Gruppe zu identifizieren) oder Dienstprinzipal (verwenden Sie ApplicationId-oder ObjectID-Parameter, um einen ServicePrincipal zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="642f6-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="642f6-117">Die Rolle, der der Prinzipal zugewiesen ist, muss mithilfe des RoleDefinitionName-oder RoleDefinitionId-Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="642f6-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="642f6-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="642f6-118">EXAMPLES</span></span>

### <span data-ttu-id="642f6-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="642f6-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="642f6-120">In diesem Beispiel wird die Rolle "verwalteter HSM-Richtlinien Administrator" von " user1@microsoft.com " im Bereich "/Keys" aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="642f6-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="642f6-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="642f6-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="642f6-122">In diesem Beispiel werden alle Rollen von " user1@microsoft.com " in allen Bereichen aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="642f6-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="642f6-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="642f6-123">PARAMETERS</span></span>

### <span data-ttu-id="642f6-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="642f6-124">-ApplicationId</span></span>
<span data-ttu-id="642f6-125">Der APP-SPN.</span><span class="sxs-lookup"><span data-stu-id="642f6-125">The app SPN.</span></span>

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

### <span data-ttu-id="642f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642f6-126">-DefaultProfile</span></span>
<span data-ttu-id="642f6-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="642f6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="642f6-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="642f6-128">-HsmName</span></span>
<span data-ttu-id="642f6-129">Der Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="642f6-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="642f6-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="642f6-130">-InputObject</span></span>
<span data-ttu-id="642f6-131">Rollen Zuweisungs Objekt</span><span class="sxs-lookup"><span data-stu-id="642f6-131">Role assignment object.</span></span>

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

### <span data-ttu-id="642f6-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="642f6-132">-ObjectId</span></span>
<span data-ttu-id="642f6-133">Die Objekt-ID des Benutzers oder der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="642f6-133">The user or group object id.</span></span>

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

### <span data-ttu-id="642f6-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="642f6-134">-PassThru</span></span>
<span data-ttu-id="642f6-135">Gibt true zurück, wenn das HSM wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="642f6-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="642f6-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="642f6-136">-RoleAssignmentName</span></span>
<span data-ttu-id="642f6-137">Der Name der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="642f6-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="642f6-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="642f6-138">-RoleDefinitionId</span></span>
<span data-ttu-id="642f6-139">Die Rollen-ID, der der Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="642f6-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="642f6-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="642f6-140">-RoleDefinitionName</span></span>
<span data-ttu-id="642f6-141">Der Name der RBAC-Rolle, der der Prinzipal zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="642f6-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="642f6-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="642f6-142">-Scope</span></span>
<span data-ttu-id="642f6-143">Der Bereich, für den die Rollenzuweisung oder-Definition gilt, beispielsweise "/" oder "/Keys" oder "/Keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="642f6-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="642f6-144">"/" wird verwendet, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="642f6-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="642f6-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="642f6-145">-SignInName</span></span>
<span data-ttu-id="642f6-146">Der Benutzer SignInName.</span><span class="sxs-lookup"><span data-stu-id="642f6-146">The user SignInName.</span></span>

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

### <span data-ttu-id="642f6-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="642f6-147">-Confirm</span></span>
<span data-ttu-id="642f6-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="642f6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642f6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642f6-149">-WhatIf</span></span>
<span data-ttu-id="642f6-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="642f6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="642f6-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="642f6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642f6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642f6-152">CommonParameters</span></span>
<span data-ttu-id="642f6-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="642f6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642f6-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="642f6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642f6-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="642f6-155">INPUTS</span></span>

### <span data-ttu-id="642f6-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="642f6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="642f6-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="642f6-157">OUTPUTS</span></span>

### <span data-ttu-id="642f6-158">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="642f6-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="642f6-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="642f6-159">NOTES</span></span>

## <span data-ttu-id="642f6-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="642f6-160">RELATED LINKS</span></span>
