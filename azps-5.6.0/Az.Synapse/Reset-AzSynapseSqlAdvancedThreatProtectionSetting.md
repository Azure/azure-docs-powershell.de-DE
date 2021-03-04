---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9b4e55f701b956fc653cf08cddb87997a998315e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936571"
---
# <span data-ttu-id="9e945-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9e945-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9e945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e945-102">SYNOPSIS</span></span>
<span data-ttu-id="9e945-103">Entfernt die erweiterten Einstellungen für den Bedrohungsschutz aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="9e945-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="9e945-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e945-104">SYNTAX</span></span>

### <span data-ttu-id="9e945-105">ClearByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e945-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e945-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e945-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e945-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e945-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e945-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e945-108">DESCRIPTION</span></span>
<span data-ttu-id="9e945-109">Das **Cmdlet Reset-AzSynapseSqlAdvancedThreatProtectionSetting** entfernt die erweiterten Bedrohungsschutzeinstellungen aus einem Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="9e945-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="9e945-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e945-110">EXAMPLES</span></span>

### <span data-ttu-id="9e945-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e945-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9e945-112">Mit diesem Befehl werden die erweiterten Bedrohungsschutzeinstellungen aus einem Arbeitsbereich namens ContosoWorkspace entfernt.</span><span class="sxs-lookup"><span data-stu-id="9e945-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9e945-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e945-113">PARAMETERS</span></span>

### <span data-ttu-id="9e945-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e945-114">-AsJob</span></span>
<span data-ttu-id="9e945-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9e945-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e945-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e945-116">-DefaultProfile</span></span>
<span data-ttu-id="9e945-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e945-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e945-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e945-118">-InputObject</span></span>
<span data-ttu-id="9e945-119">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e945-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e945-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e945-120">-PassThru</span></span>
<span data-ttu-id="9e945-121">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9e945-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9e945-122">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9e945-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9e945-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e945-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e945-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9e945-124">Resource group name.</span></span>

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

### <span data-ttu-id="9e945-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e945-125">-ResourceId</span></span>
<span data-ttu-id="9e945-126">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="9e945-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e945-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e945-127">-WorkspaceName</span></span>
<span data-ttu-id="9e945-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="9e945-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e945-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e945-129">-Confirm</span></span>
<span data-ttu-id="9e945-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e945-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e945-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e945-131">-WhatIf</span></span>
<span data-ttu-id="9e945-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e945-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e945-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e945-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e945-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e945-134">CommonParameters</span></span>
<span data-ttu-id="9e945-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e945-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e945-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e945-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e945-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e945-137">INPUTS</span></span>

### <span data-ttu-id="9e945-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e945-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9e945-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e945-139">OUTPUTS</span></span>

### <span data-ttu-id="9e945-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e945-140">System.Boolean</span></span>

## <span data-ttu-id="9e945-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e945-141">NOTES</span></span>

## <span data-ttu-id="9e945-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e945-142">RELATED LINKS</span></span>
