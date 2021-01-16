---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384150"
---
# <span data-ttu-id="a9201-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="a9201-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="a9201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9201-102">SYNOPSIS</span></span>
<span data-ttu-id="a9201-103">Deaktiviert die erweiterte Datensicherheit in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a9201-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="a9201-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9201-104">SYNTAX</span></span>

### <span data-ttu-id="a9201-105">DisableByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9201-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9201-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9201-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9201-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9201-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9201-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9201-108">DESCRIPTION</span></span>
<span data-ttu-id="a9201-109">Das **Cmdlet "Disable-AzSynapseSqlAdvancedDataSecurity"** deaktiviert Die erweiterte Datensicherheit in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a9201-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="a9201-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9201-110">EXAMPLES</span></span>

### <span data-ttu-id="a9201-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9201-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a9201-112">Mit diesem Befehl wird Advanced Data Security im Arbeitsbereich "ContosoWorkspace" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a9201-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a9201-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9201-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="a9201-114">Mit diesem Befehl wird Advanced Data Security im Arbeitsbereich mit dem Namen "ContosoWorkspace" über die Pipeline deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a9201-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a9201-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9201-115">PARAMETERS</span></span>

### <span data-ttu-id="a9201-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9201-116">-AsJob</span></span>
<span data-ttu-id="a9201-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a9201-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9201-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9201-118">-DefaultProfile</span></span>
<span data-ttu-id="a9201-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9201-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9201-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9201-120">-InputObject</span></span>
<span data-ttu-id="a9201-121">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9201-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9201-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9201-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9201-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a9201-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9201-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9201-124">-ResourceId</span></span>
<span data-ttu-id="a9201-125">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a9201-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9201-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9201-126">-WorkspaceName</span></span>
<span data-ttu-id="a9201-127">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a9201-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9201-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9201-128">-Confirm</span></span>
<span data-ttu-id="a9201-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9201-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9201-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a9201-130">-WhatIf</span></span>
<span data-ttu-id="a9201-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9201-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9201-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9201-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9201-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9201-133">CommonParameters</span></span>
<span data-ttu-id="a9201-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9201-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9201-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9201-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9201-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9201-136">INPUTS</span></span>

### <span data-ttu-id="a9201-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a9201-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a9201-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9201-138">OUTPUTS</span></span>

### <span data-ttu-id="a9201-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="a9201-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="a9201-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9201-140">NOTES</span></span>

## <span data-ttu-id="a9201-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9201-141">RELATED LINKS</span></span>
