---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 00d9682eb6562cfbfb9d06a4c8a6bac3b149cea1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929467"
---
# <span data-ttu-id="5471c-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="5471c-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="5471c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5471c-102">SYNOPSIS</span></span>
<span data-ttu-id="5471c-103">Entfernt die Überwachungseinstellungen eines Azure Synapse Analytics-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="5471c-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="5471c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5471c-104">SYNTAX</span></span>

### <span data-ttu-id="5471c-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5471c-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5471c-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5471c-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5471c-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5471c-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5471c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5471c-108">DESCRIPTION</span></span>
<span data-ttu-id="5471c-109">Das **Cmdlet Reset-AzSynapseSqlAuditSetting** entfernt die Überwachungseinstellungen eines Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="5471c-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="5471c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5471c-110">EXAMPLES</span></span>

### <span data-ttu-id="5471c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5471c-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5471c-112">Mit diesem Befehl werden die Überwachungseinstellungen eines Azure Synapse Analytics-Arbeitsbereichs namens ContosoWorkspace entfernt.</span><span class="sxs-lookup"><span data-stu-id="5471c-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="5471c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5471c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="5471c-114">Mit diesem Befehl werden die Überwachungseinstellungen eines Azure Synapse Analytics-Arbeitsbereichs namens ContosoWorkspace über die Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="5471c-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5471c-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5471c-115">PARAMETERS</span></span>

### <span data-ttu-id="5471c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5471c-116">-AsJob</span></span>
<span data-ttu-id="5471c-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5471c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5471c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5471c-118">-DefaultProfile</span></span>
<span data-ttu-id="5471c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5471c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5471c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5471c-120">-InputObject</span></span>
<span data-ttu-id="5471c-121">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5471c-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5471c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5471c-122">-PassThru</span></span>
<span data-ttu-id="5471c-123">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5471c-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5471c-124">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5471c-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5471c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5471c-125">-ResourceGroupName</span></span>
<span data-ttu-id="5471c-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5471c-126">Resource group name.</span></span>

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

### <span data-ttu-id="5471c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5471c-127">-ResourceId</span></span>
<span data-ttu-id="5471c-128">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="5471c-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="5471c-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5471c-129">-WorkspaceName</span></span>
<span data-ttu-id="5471c-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="5471c-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5471c-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5471c-131">-Confirm</span></span>
<span data-ttu-id="5471c-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5471c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5471c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5471c-133">-WhatIf</span></span>
<span data-ttu-id="5471c-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5471c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5471c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5471c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5471c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5471c-136">CommonParameters</span></span>
<span data-ttu-id="5471c-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5471c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5471c-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5471c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5471c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5471c-139">INPUTS</span></span>

### <span data-ttu-id="5471c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5471c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5471c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5471c-141">OUTPUTS</span></span>

### <span data-ttu-id="5471c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5471c-142">System.Boolean</span></span>

## <span data-ttu-id="5471c-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5471c-143">NOTES</span></span>

## <span data-ttu-id="5471c-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5471c-144">RELATED LINKS</span></span>
