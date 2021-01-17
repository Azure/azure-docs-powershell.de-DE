---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383408"
---
# <span data-ttu-id="d747f-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d747f-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="d747f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d747f-102">SYNOPSIS</span></span>
<span data-ttu-id="d747f-103">Entfernt einen Azure AD-Administrator für Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="d747f-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="d747f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d747f-104">SYNTAX</span></span>

### <span data-ttu-id="d747f-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d747f-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d747f-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d747f-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d747f-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d747f-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d747f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d747f-108">DESCRIPTION</span></span>
<span data-ttu-id="d747f-109">Das **Cmdlet "Remove-AzSynapseSqlActiveDirectoryAdministrator"** entfernt einen Azure Active Directory (Azure AD)-Administrator für Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="d747f-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="d747f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d747f-110">EXAMPLES</span></span>

### <span data-ttu-id="d747f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d747f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d747f-112">Mit diesem Befehl wird der Azure AD-Administrator für den Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="d747f-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d747f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d747f-113">PARAMETERS</span></span>

### <span data-ttu-id="d747f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d747f-114">-AsJob</span></span>
<span data-ttu-id="d747f-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d747f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d747f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d747f-116">-DefaultProfile</span></span>
<span data-ttu-id="d747f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d747f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d747f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d747f-118">-Force</span></span>
<span data-ttu-id="d747f-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="d747f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d747f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d747f-120">-InputObject</span></span>
<span data-ttu-id="d747f-121">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d747f-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d747f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d747f-122">-PassThru</span></span>
<span data-ttu-id="d747f-123">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d747f-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d747f-124">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="d747f-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d747f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d747f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d747f-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d747f-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d747f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d747f-127">-ResourceId</span></span>
<span data-ttu-id="d747f-128">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d747f-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d747f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d747f-129">-WorkspaceName</span></span>
<span data-ttu-id="d747f-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d747f-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d747f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d747f-131">-Confirm</span></span>
<span data-ttu-id="d747f-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d747f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d747f-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d747f-133">-WhatIf</span></span>
<span data-ttu-id="d747f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d747f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d747f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d747f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d747f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d747f-136">CommonParameters</span></span>
<span data-ttu-id="d747f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d747f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d747f-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d747f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d747f-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d747f-139">INPUTS</span></span>

### <span data-ttu-id="d747f-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d747f-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d747f-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d747f-141">OUTPUTS</span></span>

### <span data-ttu-id="d747f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d747f-142">System.Boolean</span></span>

## <span data-ttu-id="d747f-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d747f-143">NOTES</span></span>

## <span data-ttu-id="d747f-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d747f-144">RELATED LINKS</span></span>
