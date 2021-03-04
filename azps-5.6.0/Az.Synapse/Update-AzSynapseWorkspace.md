---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 60631b8d4c42ac314268453c5dedf16893281861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941360"
---
# <span data-ttu-id="84480-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="84480-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="84480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84480-102">SYNOPSIS</span></span>
<span data-ttu-id="84480-103">Aktualisiert einen Synapse Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="84480-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="84480-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84480-104">SYNTAX</span></span>

### <span data-ttu-id="84480-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="84480-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84480-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84480-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84480-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84480-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84480-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84480-108">DESCRIPTION</span></span>
<span data-ttu-id="84480-109">Das **Cmdlet Update-AzSynapseWorkspace** aktualisiert einen Azure Synapse Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="84480-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="84480-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84480-110">EXAMPLES</span></span>

### <span data-ttu-id="84480-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84480-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="84480-112">Mit diesen Befehlen werden Tags für den spekulierten Azure Synapse Analytics-Arbeitsbereich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="84480-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="84480-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="84480-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="84480-114">Mit diesen Befehlen werden Tags für den spekulierten Azure Synapse Analytics-Arbeitsbereich über die Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="84480-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="84480-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="84480-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="84480-116">Mit diesen Befehlen werden Tags für den spekulierten Azure Synapse Analytics-Arbeitsbereich über eine Pipeline mit Ressourcen-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="84480-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="84480-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="84480-117">PARAMETERS</span></span>

### <span data-ttu-id="84480-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84480-118">-AsJob</span></span>
<span data-ttu-id="84480-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="84480-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84480-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84480-120">-DefaultProfile</span></span>
<span data-ttu-id="84480-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84480-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84480-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84480-122">-InputObject</span></span>
<span data-ttu-id="84480-123">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="84480-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="84480-124">-Name</span><span class="sxs-lookup"><span data-stu-id="84480-124">-Name</span></span>
<span data-ttu-id="84480-125">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="84480-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="84480-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84480-126">-ResourceGroupName</span></span>
<span data-ttu-id="84480-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84480-127">Resource group name.</span></span>

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

### <span data-ttu-id="84480-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84480-128">-ResourceId</span></span>
<span data-ttu-id="84480-129">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="84480-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="84480-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="84480-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="84480-131">Das neue SQL Administratorkennwort für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="84480-131">The new SQL administrator password for the workspace.</span></span>

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

### <span data-ttu-id="84480-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="84480-132">-Tag</span></span>
<span data-ttu-id="84480-133">Eine Zeichenfolge, ein Zeichenfolgenwörterbuch mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="84480-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="84480-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84480-134">-Confirm</span></span>
<span data-ttu-id="84480-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84480-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84480-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84480-136">-WhatIf</span></span>
<span data-ttu-id="84480-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84480-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84480-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84480-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84480-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84480-139">CommonParameters</span></span>
<span data-ttu-id="84480-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84480-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84480-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84480-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84480-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84480-142">INPUTS</span></span>

### <span data-ttu-id="84480-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="84480-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="84480-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84480-144">OUTPUTS</span></span>

### <span data-ttu-id="84480-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="84480-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="84480-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="84480-146">NOTES</span></span>

## <span data-ttu-id="84480-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="84480-147">RELATED LINKS</span></span>
