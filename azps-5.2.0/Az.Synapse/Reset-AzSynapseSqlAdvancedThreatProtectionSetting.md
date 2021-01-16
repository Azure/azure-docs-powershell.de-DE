---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295097"
---
# <span data-ttu-id="f360d-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f360d-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f360d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f360d-102">SYNOPSIS</span></span>
<span data-ttu-id="f360d-103">Entfernt die erweiterten Threat Protection-Einstellungen aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="f360d-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="f360d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f360d-104">SYNTAX</span></span>

### <span data-ttu-id="f360d-105">ClearByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f360d-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f360d-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f360d-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f360d-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f360d-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f360d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f360d-108">DESCRIPTION</span></span>
<span data-ttu-id="f360d-109">Das **Cmdlet "Reset-AzSynapseSqlAdvancedThreatProtectionSetting"** entfernt die erweiterten Threat Protection-Einstellungen aus einem Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="f360d-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="f360d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f360d-110">EXAMPLES</span></span>

### <span data-ttu-id="f360d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f360d-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f360d-112">Mit diesem Befehl werden die erweiterten Threat Protection-Einstellungen aus einem Arbeitsbereich namens "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f360d-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f360d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f360d-113">PARAMETERS</span></span>

### <span data-ttu-id="f360d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f360d-114">-AsJob</span></span>
<span data-ttu-id="f360d-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f360d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f360d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f360d-116">-DefaultProfile</span></span>
<span data-ttu-id="f360d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f360d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f360d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f360d-118">-InputObject</span></span>
<span data-ttu-id="f360d-119">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f360d-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f360d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f360d-120">-PassThru</span></span>
<span data-ttu-id="f360d-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f360d-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f360d-122">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="f360d-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f360d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f360d-123">-ResourceGroupName</span></span>
<span data-ttu-id="f360d-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f360d-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f360d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f360d-125">-ResourceId</span></span>
<span data-ttu-id="f360d-126">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f360d-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f360d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f360d-127">-WorkspaceName</span></span>
<span data-ttu-id="f360d-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f360d-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f360d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f360d-129">-Confirm</span></span>
<span data-ttu-id="f360d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f360d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f360d-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f360d-131">-WhatIf</span></span>
<span data-ttu-id="f360d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f360d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f360d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f360d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f360d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f360d-134">CommonParameters</span></span>
<span data-ttu-id="f360d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f360d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f360d-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f360d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f360d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f360d-137">INPUTS</span></span>

### <span data-ttu-id="f360d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f360d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f360d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f360d-139">OUTPUTS</span></span>

### <span data-ttu-id="f360d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f360d-140">System.Boolean</span></span>

## <span data-ttu-id="f360d-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f360d-141">NOTES</span></span>

## <span data-ttu-id="f360d-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f360d-142">RELATED LINKS</span></span>
