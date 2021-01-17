---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383437"
---
# <span data-ttu-id="3f5a8-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3f5a8-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="3f5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5a8-103">Löscht eine Synapse Analytics-Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="3f5a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f5a8-104">SYNTAX</span></span>

### <span data-ttu-id="3f5a8-105">RemoveByWorkspaceNameAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f5a8-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f5a8-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f5a8-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f5a8-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f5a8-115">DESCRIPTION</span></span>
<span data-ttu-id="3f5a8-116">Das **Cmdlet "Remove-AzSynapseRoleAssignment"** löscht eine Azure Synapse Analytics-Rollenzuweisung endgültig.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="3f5a8-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f5a8-117">EXAMPLES</span></span>

### <span data-ttu-id="3f5a8-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f5a8-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="3f5a8-119">Mit diesem Befehl wird eine Azure Synapse Analytics-Rollenzuweisung mit einer Rollenzuweisungs-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="3f5a8-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3f5a8-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="3f5a8-121">Mit diesem Befehl wird eine Azure Synapse Analytics-Rollenzuweisung mit einem Rollennamen und einem Benutzerprinzipalnamen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="3f5a8-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3f5a8-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="3f5a8-123">Mit diesem Befehl wird eine Azure Synapse Analytics-Rollenzuweisung mit einer Rollenzuweisungs-ID über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="3f5a8-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f5a8-124">PARAMETERS</span></span>

### <span data-ttu-id="3f5a8-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f5a8-125">-AsJob</span></span>
<span data-ttu-id="3f5a8-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3f5a8-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f5a8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5a8-127">-DefaultProfile</span></span>
<span data-ttu-id="3f5a8-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f5a8-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3f5a8-129">-ObjectId</span></span>
<span data-ttu-id="3f5a8-130">Die Azure AD ObjectId des Benutzers, der Gruppe oder des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="3f5a8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f5a8-131">-PassThru</span></span>
<span data-ttu-id="3f5a8-132">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3f5a8-133">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3f5a8-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="3f5a8-134">-RoleAssignmentId</span></span>
<span data-ttu-id="3f5a8-135">Die ID der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="3f5a8-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3f5a8-136">-RoleDefinitionId</span></span>
<span data-ttu-id="3f5a8-137">ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3f5a8-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3f5a8-138">-RoleDefinitionName</span></span>
<span data-ttu-id="3f5a8-139">Name der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3f5a8-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3f5a8-140">-ServicePrincipalName</span></span>
<span data-ttu-id="3f5a8-141">Der "ServicePrincipalName" des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="3f5a8-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3f5a8-142">-SignInName</span></span>
<span data-ttu-id="3f5a8-143">Die E-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="3f5a8-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f5a8-144">-WorkspaceName</span></span>
<span data-ttu-id="3f5a8-145">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3f5a8-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f5a8-146">-WorkspaceObject</span></span>
<span data-ttu-id="3f5a8-147">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3f5a8-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f5a8-148">-Confirm</span></span>
<span data-ttu-id="3f5a8-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f5a8-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3f5a8-150">-WhatIf</span></span>
<span data-ttu-id="3f5a8-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f5a8-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f5a8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5a8-153">CommonParameters</span></span>
<span data-ttu-id="3f5a8-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f5a8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5a8-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f5a8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5a8-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f5a8-156">INPUTS</span></span>

### <span data-ttu-id="3f5a8-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f5a8-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3f5a8-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f5a8-158">OUTPUTS</span></span>

### <span data-ttu-id="3f5a8-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f5a8-159">System.Boolean</span></span>

## <span data-ttu-id="3f5a8-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f5a8-160">NOTES</span></span>

## <span data-ttu-id="3f5a8-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f5a8-161">RELATED LINKS</span></span>
