---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297310"
---
# <span data-ttu-id="4d5dc-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4d5dc-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="4d5dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d5dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4d5dc-103">Bricht einen Synapse Analytics Spark-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4d5dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d5dc-104">SYNTAX</span></span>

### <span data-ttu-id="4d5dc-105">StopSparkJobByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d5dc-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d5dc-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d5dc-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d5dc-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d5dc-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d5dc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d5dc-108">DESCRIPTION</span></span>
<span data-ttu-id="4d5dc-109">Das **Cmdlet "Stop-AzSynapseSparkJob"** bricht einen Synapse Analytics Spark-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4d5dc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d5dc-110">EXAMPLES</span></span>

### <span data-ttu-id="4d5dc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d5dc-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="4d5dc-112">Dieser Befehl bricht einen Synapse Analytics Spark-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="4d5dc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4d5dc-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="4d5dc-114">Mit diesem Befehl wird ein Synapse Analytics Spark-Auftrag über die Pipeline abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="4d5dc-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4d5dc-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="4d5dc-116">Mit diesem Befehl wird ein Synapse Analytics Spark-Auftrag über die Pipeline abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="4d5dc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d5dc-117">PARAMETERS</span></span>

### <span data-ttu-id="4d5dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d5dc-118">-DefaultProfile</span></span>
<span data-ttu-id="4d5dc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d5dc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4d5dc-120">-Force</span></span>
<span data-ttu-id="4d5dc-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4d5dc-122">-YYId</span><span class="sxs-lookup"><span data-stu-id="4d5dc-122">-LivyId</span></span>
<span data-ttu-id="4d5dc-123">Id des Sparkauftrags.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5dc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d5dc-124">-PassThru</span></span>
<span data-ttu-id="4d5dc-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4d5dc-126">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4d5dc-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="4d5dc-127">-SparkJobObject</span></span>
<span data-ttu-id="4d5dc-128">Sparkauftragseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d5dc-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4d5dc-129">-SparkPoolName</span></span>
<span data-ttu-id="4d5dc-130">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5dc-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="4d5dc-131">-SparkPoolObject</span></span>
<span data-ttu-id="4d5dc-132">Sparkpooleingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d5dc-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d5dc-133">-WorkspaceName</span></span>
<span data-ttu-id="4d5dc-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5dc-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d5dc-135">-Confirm</span></span>
<span data-ttu-id="4d5dc-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d5dc-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4d5dc-137">-WhatIf</span></span>
<span data-ttu-id="4d5dc-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d5dc-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d5dc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d5dc-140">CommonParameters</span></span>
<span data-ttu-id="4d5dc-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d5dc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d5dc-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d5dc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d5dc-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d5dc-143">INPUTS</span></span>

### <span data-ttu-id="4d5dc-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4d5dc-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="4d5dc-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4d5dc-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="4d5dc-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d5dc-146">OUTPUTS</span></span>

### <span data-ttu-id="4d5dc-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d5dc-147">System.Boolean</span></span>

## <span data-ttu-id="4d5dc-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d5dc-148">NOTES</span></span>

## <span data-ttu-id="4d5dc-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d5dc-149">RELATED LINKS</span></span>
