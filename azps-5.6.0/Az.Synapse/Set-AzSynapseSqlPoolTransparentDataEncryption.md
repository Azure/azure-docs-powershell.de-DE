---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cdc72a2bb0e21873bd0fa2d82123afe8ed011378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939211"
---
# <span data-ttu-id="0d370-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0d370-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="0d370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d370-102">SYNOPSIS</span></span>
<span data-ttu-id="0d370-103">Ändert die TDE-Eigenschaft für einen SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="0d370-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="0d370-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d370-104">SYNTAX</span></span>

### <span data-ttu-id="0d370-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d370-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d370-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d370-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d370-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d370-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d370-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d370-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d370-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d370-109">DESCRIPTION</span></span>
<span data-ttu-id="0d370-110">Das **Cmdlet Set-AzSynapseSqlPoolTransparentDataEncryption** ändert die Eigenschaft Transparente Datenverschlüsselung (Transparent Data Encryption, TDE) eines Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="0d370-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0d370-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d370-111">EXAMPLES</span></span>

### <span data-ttu-id="0d370-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d370-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="0d370-113">Mit diesem Befehl wird TDE für den SQL ContosoSqlPool unter dem Arbeitsbereich "ContosoWorkspace" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0d370-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="0d370-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0d370-114">PARAMETERS</span></span>

### <span data-ttu-id="0d370-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d370-115">-AsJob</span></span>
<span data-ttu-id="0d370-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0d370-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d370-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d370-117">-DefaultProfile</span></span>
<span data-ttu-id="0d370-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d370-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d370-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d370-119">-InputObject</span></span>
<span data-ttu-id="0d370-120">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d370-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d370-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0d370-121">-Name</span></span>
<span data-ttu-id="0d370-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="0d370-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d370-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d370-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d370-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0d370-124">Resource group name.</span></span>

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

### <span data-ttu-id="0d370-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d370-125">-ResourceId</span></span>
<span data-ttu-id="0d370-126">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="0d370-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="0d370-127">-State</span><span class="sxs-lookup"><span data-stu-id="0d370-127">-State</span></span>
<span data-ttu-id="0d370-128">Der Zustand der transparenten Datenverschlüsselung in Azure Synapse Analytics Sql Pool.</span><span class="sxs-lookup"><span data-stu-id="0d370-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d370-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d370-129">-WorkspaceName</span></span>
<span data-ttu-id="0d370-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="0d370-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d370-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0d370-131">-WorkspaceObject</span></span>
<span data-ttu-id="0d370-132">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d370-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d370-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d370-133">-Confirm</span></span>
<span data-ttu-id="0d370-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d370-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d370-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d370-135">-WhatIf</span></span>
<span data-ttu-id="0d370-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d370-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d370-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d370-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d370-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d370-138">CommonParameters</span></span>
<span data-ttu-id="0d370-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d370-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d370-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d370-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d370-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d370-141">INPUTS</span></span>

### <span data-ttu-id="0d370-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d370-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0d370-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0d370-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0d370-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d370-144">OUTPUTS</span></span>

### <span data-ttu-id="0d370-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0d370-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="0d370-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0d370-146">NOTES</span></span>

## <span data-ttu-id="0d370-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0d370-147">RELATED LINKS</span></span>
