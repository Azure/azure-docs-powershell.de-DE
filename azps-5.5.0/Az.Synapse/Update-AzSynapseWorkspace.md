---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165561"
---
# <span data-ttu-id="34dec-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34dec-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="34dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34dec-102">SYNOPSIS</span></span>
<span data-ttu-id="34dec-103">Aktualisiert einen Synapse Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="34dec-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="34dec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34dec-104">SYNTAX</span></span>

### <span data-ttu-id="34dec-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="34dec-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34dec-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34dec-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34dec-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34dec-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34dec-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34dec-108">DESCRIPTION</span></span>
<span data-ttu-id="34dec-109">Das **Cmdlet "Update-AzSynapseWorkspace"** aktualisiert einen Azure Synapse Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="34dec-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="34dec-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34dec-110">EXAMPLES</span></span>

### <span data-ttu-id="34dec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34dec-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="34dec-112">Mit diesen Befehlen werden Tags für den spezifikationsierten Azure Synapse Analytics-Arbeitsbereich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="34dec-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="34dec-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="34dec-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="34dec-114">Mit diesen Befehlen werden Tags für den spezifikationsierten Azure Synapse Analytics-Arbeitsbereich über die Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="34dec-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="34dec-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="34dec-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="34dec-116">Mit diesen Befehlen werden Tags für den spezifikationsierten Azure Synapse Analytics-Arbeitsbereich über die Pipeline mit Ressourcen-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="34dec-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="34dec-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34dec-117">PARAMETERS</span></span>

### <span data-ttu-id="34dec-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34dec-118">-AsJob</span></span>
<span data-ttu-id="34dec-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="34dec-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34dec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34dec-120">-DefaultProfile</span></span>
<span data-ttu-id="34dec-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34dec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34dec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34dec-122">-InputObject</span></span>
<span data-ttu-id="34dec-123">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="34dec-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34dec-124">-Name</span><span class="sxs-lookup"><span data-stu-id="34dec-124">-Name</span></span>
<span data-ttu-id="34dec-125">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="34dec-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34dec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34dec-126">-ResourceGroupName</span></span>
<span data-ttu-id="34dec-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="34dec-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34dec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34dec-128">-ResourceId</span></span>
<span data-ttu-id="34dec-129">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="34dec-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34dec-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="34dec-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="34dec-131">Das neue SQL Administratorkennwort für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="34dec-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34dec-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="34dec-132">-Tag</span></span>
<span data-ttu-id="34dec-133">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="34dec-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34dec-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34dec-134">-Confirm</span></span>
<span data-ttu-id="34dec-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34dec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34dec-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="34dec-136">-WhatIf</span></span>
<span data-ttu-id="34dec-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34dec-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34dec-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34dec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34dec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34dec-139">CommonParameters</span></span>
<span data-ttu-id="34dec-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34dec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34dec-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34dec-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34dec-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34dec-142">INPUTS</span></span>

### <span data-ttu-id="34dec-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34dec-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="34dec-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34dec-144">OUTPUTS</span></span>

### <span data-ttu-id="34dec-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34dec-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="34dec-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="34dec-146">NOTES</span></span>

## <span data-ttu-id="34dec-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="34dec-147">RELATED LINKS</span></span>
