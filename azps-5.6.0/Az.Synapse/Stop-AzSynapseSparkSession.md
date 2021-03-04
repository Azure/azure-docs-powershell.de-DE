---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: 204166bc48e01ea186ca18ad5aa95b0dcf05192a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939144"
---
# <span data-ttu-id="52f84-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="52f84-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="52f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f84-102">SYNOPSIS</span></span>
<span data-ttu-id="52f84-103">Beendet eine Synapse Analytics Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="52f84-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="52f84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52f84-104">SYNTAX</span></span>

### <span data-ttu-id="52f84-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52f84-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f84-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f84-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f84-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f84-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f84-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52f84-108">DESCRIPTION</span></span>
<span data-ttu-id="52f84-109">Das **Cmdlet Stop-AzSynapseSparkSession** beendet eine Synapse Analytics Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="52f84-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="52f84-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52f84-110">EXAMPLES</span></span>

### <span data-ttu-id="52f84-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52f84-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="52f84-112">Mit diesem Befehl wird eine Synapse Analytics Spark-Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="52f84-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="52f84-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="52f84-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="52f84-114">Mit diesem Befehl wird eine Synapse Analytics Spark-Sitzung über eine Pipeline beendet.</span><span class="sxs-lookup"><span data-stu-id="52f84-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="52f84-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="52f84-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="52f84-116">Mit diesem Befehl wird eine Synapse Analytics Spark-Sitzung über eine Pipeline beendet.</span><span class="sxs-lookup"><span data-stu-id="52f84-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="52f84-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="52f84-117">PARAMETERS</span></span>

### <span data-ttu-id="52f84-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52f84-118">-AsJob</span></span>
<span data-ttu-id="52f84-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="52f84-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52f84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f84-120">-DefaultProfile</span></span>
<span data-ttu-id="52f84-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52f84-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52f84-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52f84-122">-InputObject</span></span>
<span data-ttu-id="52f84-123">Spark-Sitzungseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="52f84-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52f84-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="52f84-124">-LivyId</span></span>
<span data-ttu-id="52f84-125">Bezeichner der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="52f84-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f84-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52f84-126">-PassThru</span></span>
<span data-ttu-id="52f84-127">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="52f84-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="52f84-128">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="52f84-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="52f84-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="52f84-129">-SparkPoolName</span></span>
<span data-ttu-id="52f84-130">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="52f84-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f84-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="52f84-131">-SparkPoolObject</span></span>
<span data-ttu-id="52f84-132">Spark pool input object, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="52f84-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52f84-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52f84-133">-WorkspaceName</span></span>
<span data-ttu-id="52f84-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="52f84-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f84-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52f84-135">-Confirm</span></span>
<span data-ttu-id="52f84-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52f84-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f84-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f84-137">-WhatIf</span></span>
<span data-ttu-id="52f84-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52f84-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52f84-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52f84-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f84-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f84-140">CommonParameters</span></span>
<span data-ttu-id="52f84-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f84-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f84-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52f84-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f84-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52f84-143">INPUTS</span></span>

### <span data-ttu-id="52f84-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="52f84-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="52f84-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="52f84-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="52f84-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52f84-146">OUTPUTS</span></span>

### <span data-ttu-id="52f84-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52f84-147">System.Boolean</span></span>

## <span data-ttu-id="52f84-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="52f84-148">NOTES</span></span>

## <span data-ttu-id="52f84-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="52f84-149">RELATED LINKS</span></span>
