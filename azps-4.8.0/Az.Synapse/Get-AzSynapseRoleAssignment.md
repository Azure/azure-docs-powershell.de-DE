---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007687"
---
# <span data-ttu-id="0bf97-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0bf97-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="0bf97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0bf97-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf97-103">Ruft eine Synapse-Analyse Rollenzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="0bf97-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="0bf97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bf97-104">SYNTAX</span></span>

### <span data-ttu-id="0bf97-105">GetByWorkspaceNameAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0bf97-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf97-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf97-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf97-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bf97-115">DESCRIPTION</span></span>
<span data-ttu-id="0bf97-116">Das Cmdlet " **Get-AzSynapseRoleAssignment** " erhält eine Azure Synapse-Analyse Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="0bf97-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="0bf97-117">Wenn Sie keine Rollendefinition oder einen Benutzerprinzipalnamen angeben, ruft dieses Cmdlet alle Rollenzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="0bf97-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="0bf97-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0bf97-118">EXAMPLES</span></span>

### <span data-ttu-id="0bf97-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bf97-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0bf97-120">Dieser Befehl ruft alle Rollenzuweisungen unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="0bf97-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="0bf97-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0bf97-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="0bf97-122">Dieser Befehl ruft alle Rollenzuweisungen unter Workspace ContosoWorkspace mit dem Rollennamen ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="0bf97-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="0bf97-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0bf97-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="0bf97-124">Dieser Befehl ruft eine Rollenzuweisung unter Workspace ContosoWorkspace mit dem Rollennamen ContosoRole und dem Benutzerprinzipalnamen contosoname ab.</span><span class="sxs-lookup"><span data-stu-id="0bf97-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="0bf97-125">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="0bf97-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="0bf97-126">Dieser Befehl ruft alle Rollenzuweisungen unter einem Arbeitsbereich durch Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="0bf97-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="0bf97-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bf97-127">PARAMETERS</span></span>

### <span data-ttu-id="0bf97-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf97-128">-DefaultProfile</span></span>
<span data-ttu-id="0bf97-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0bf97-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bf97-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="0bf97-130">-ObjectId</span></span>
<span data-ttu-id="0bf97-131">Die Azure AD-ObjectID des Benutzers, der Gruppe oder des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="0bf97-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="0bf97-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="0bf97-132">-RoleAssignmentId</span></span>
<span data-ttu-id="0bf97-133">Die ID der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="0bf97-133">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="0bf97-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0bf97-134">-RoleDefinitionId</span></span>
<span data-ttu-id="0bf97-135">Die ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0bf97-135">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="0bf97-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0bf97-136">-RoleDefinitionName</span></span>
<span data-ttu-id="0bf97-137">Der Name der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0bf97-137">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="0bf97-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0bf97-138">-ServicePrincipalName</span></span>
<span data-ttu-id="0bf97-139">Die servicePrincipalName des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="0bf97-139">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="0bf97-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0bf97-140">-SignInName</span></span>
<span data-ttu-id="0bf97-141">Die e-Mail-Adresse oder der Benutzerprinzipalname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="0bf97-141">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="0bf97-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0bf97-142">-WorkspaceName</span></span>
<span data-ttu-id="0bf97-143">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0bf97-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0bf97-144">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="0bf97-144">-WorkspaceObject</span></span>
<span data-ttu-id="0bf97-145">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="0bf97-145">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0bf97-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf97-146">CommonParameters</span></span>
<span data-ttu-id="0bf97-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf97-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf97-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bf97-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf97-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0bf97-149">INPUTS</span></span>

### <span data-ttu-id="0bf97-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0bf97-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0bf97-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0bf97-151">OUTPUTS</span></span>

### <span data-ttu-id="0bf97-152">Microsoft. Azure. Commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="0bf97-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="0bf97-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="0bf97-153">NOTES</span></span>

## <span data-ttu-id="0bf97-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0bf97-154">RELATED LINKS</span></span>
