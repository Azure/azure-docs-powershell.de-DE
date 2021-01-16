---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297340"
---
# <span data-ttu-id="ea4d3-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ea4d3-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="ea4d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4d3-103">Ruft eine Synapse Analytics-Rollenzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="ea4d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea4d3-104">SYNTAX</span></span>

### <span data-ttu-id="ea4d3-105">GetByWorkspaceNameAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea4d3-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4d3-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4d3-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea4d3-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea4d3-115">DESCRIPTION</span></span>
<span data-ttu-id="ea4d3-116">Das **Cmdlet "Get-AzSynapseRoleAssignment"** ruft eine Azure Synapse Analytics-Rollenzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="ea4d3-117">Wenn Sie keine Rollendefinition oder keinen Benutzerprinzipalnamen angeben, ruft dieses Cmdlet alle Rollenzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="ea4d3-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea4d3-118">EXAMPLES</span></span>

### <span data-ttu-id="ea4d3-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea4d3-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ea4d3-120">Dieser Befehl ruft alle Rollenzuweisungen in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="ea4d3-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ea4d3-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="ea4d3-122">Dieser Befehl ruft alle Rollenzuweisungen im Arbeitsbereich "ContosoWorkspace" mit dem Rollennamen "ContosoRole" ab.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="ea4d3-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ea4d3-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="ea4d3-124">Dieser Befehl ruft eine Rollenzuweisung im Arbeitsbereich "ContosoWorkspace" mit dem Rollennamen "ContosoRole" und dem Benutzerprinzipalnamen "ContosoName" ab.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="ea4d3-125">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ea4d3-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="ea4d3-126">Dieser Befehl ruft alle Rollenzuweisungen in einem Arbeitsbereich über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="ea4d3-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea4d3-127">PARAMETERS</span></span>

### <span data-ttu-id="ea4d3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4d3-128">-DefaultProfile</span></span>
<span data-ttu-id="ea4d3-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea4d3-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ea4d3-130">-ObjectId</span></span>
<span data-ttu-id="ea4d3-131">Die Azure AD ObjectId des Benutzers, der Gruppe oder des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="ea4d3-132">-RoleAssignmentId</span></span>
<span data-ttu-id="ea4d3-133">Die ID der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ea4d3-134">-RoleDefinitionId</span></span>
<span data-ttu-id="ea4d3-135">ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ea4d3-136">-RoleDefinitionName</span></span>
<span data-ttu-id="ea4d3-137">Name der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea4d3-138">-ServicePrincipalName</span></span>
<span data-ttu-id="ea4d3-139">Der "ServicePrincipalName" des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="ea4d3-140">-SignInName</span></span>
<span data-ttu-id="ea4d3-141">Die E-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ea4d3-142">-WorkspaceName</span></span>
<span data-ttu-id="ea4d3-143">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ea4d3-144">-WorkspaceObject</span></span>
<span data-ttu-id="ea4d3-145">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4d3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4d3-146">CommonParameters</span></span>
<span data-ttu-id="ea4d3-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4d3-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea4d3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4d3-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea4d3-149">INPUTS</span></span>

### <span data-ttu-id="ea4d3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea4d3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ea4d3-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea4d3-151">OUTPUTS</span></span>

### <span data-ttu-id="ea4d3-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="ea4d3-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="ea4d3-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea4d3-153">NOTES</span></span>

## <span data-ttu-id="ea4d3-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea4d3-154">RELATED LINKS</span></span>
