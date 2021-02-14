---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149961"
---
# <span data-ttu-id="67b5d-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="67b5d-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="67b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="67b5d-103">Löscht eine Synapse Analytics-Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="67b5d-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="67b5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67b5d-104">SYNTAX</span></span>

### <span data-ttu-id="67b5d-105">RemoveByWorkspaceNameAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="67b5d-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b5d-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b5d-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b5d-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b5d-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b5d-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b5d-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67b5d-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67b5d-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67b5d-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b5d-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b5d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67b5d-115">DESCRIPTION</span></span>
<span data-ttu-id="67b5d-116">Das **Cmdlet "Remove-AzSynapseRoleAssignment"** löscht eine Azure Synapse Analytics-Rollenzuweisung endgültig.</span><span class="sxs-lookup"><span data-stu-id="67b5d-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="67b5d-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67b5d-117">EXAMPLES</span></span>

### <span data-ttu-id="67b5d-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67b5d-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="67b5d-119">Mit diesem Befehl wird eine Azure Synapse Analytics-Rollenzuweisung mit einer Rollenzuweisungs-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="67b5d-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="67b5d-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="67b5d-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="67b5d-121">Mit diesem Befehl wird eine Azure Synapse Analytics-Rollenzuweisung mit einem Rollennamen und einem Benutzerprinzipalnamen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="67b5d-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="67b5d-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="67b5d-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="67b5d-123">Mit diesem Befehl wird eine Azure Synapse Analytics-Rollenzuweisung mit einer Rollenzuweisungs-ID über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="67b5d-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="67b5d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67b5d-124">PARAMETERS</span></span>

### <span data-ttu-id="67b5d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67b5d-125">-AsJob</span></span>
<span data-ttu-id="67b5d-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="67b5d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67b5d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b5d-127">-DefaultProfile</span></span>
<span data-ttu-id="67b5d-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67b5d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67b5d-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="67b5d-129">-ObjectId</span></span>
<span data-ttu-id="67b5d-130">Die Azure AD ObjectId des Benutzers, der Gruppe oder des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="67b5d-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67b5d-131">-PassThru</span></span>
<span data-ttu-id="67b5d-132">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="67b5d-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="67b5d-133">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="67b5d-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="67b5d-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="67b5d-134">-RoleAssignmentId</span></span>
<span data-ttu-id="67b5d-135">Die ID der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="67b5d-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="67b5d-136">-RoleDefinitionId</span></span>
<span data-ttu-id="67b5d-137">ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="67b5d-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="67b5d-138">-RoleDefinitionName</span></span>
<span data-ttu-id="67b5d-139">Name der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="67b5d-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="67b5d-140">-ServicePrincipalName</span></span>
<span data-ttu-id="67b5d-141">Der "ServicePrincipalName" des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="67b5d-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="67b5d-142">-SignInName</span></span>
<span data-ttu-id="67b5d-143">Die E-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="67b5d-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67b5d-144">-WorkspaceName</span></span>
<span data-ttu-id="67b5d-145">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="67b5d-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="67b5d-146">-WorkspaceObject</span></span>
<span data-ttu-id="67b5d-147">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="67b5d-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67b5d-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67b5d-148">-Confirm</span></span>
<span data-ttu-id="67b5d-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67b5d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b5d-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="67b5d-150">-WhatIf</span></span>
<span data-ttu-id="67b5d-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67b5d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67b5d-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67b5d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67b5d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b5d-153">CommonParameters</span></span>
<span data-ttu-id="67b5d-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b5d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b5d-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67b5d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b5d-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67b5d-156">INPUTS</span></span>

### <span data-ttu-id="67b5d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="67b5d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="67b5d-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67b5d-158">OUTPUTS</span></span>

### <span data-ttu-id="67b5d-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67b5d-159">System.Boolean</span></span>

## <span data-ttu-id="67b5d-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="67b5d-160">NOTES</span></span>

## <span data-ttu-id="67b5d-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="67b5d-161">RELATED LINKS</span></span>
