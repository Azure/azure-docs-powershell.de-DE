---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: 485558c47fa8b879999777b79341fc855085b81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929472"
---
# <span data-ttu-id="df291-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="df291-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="df291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df291-102">SYNOPSIS</span></span>
<span data-ttu-id="df291-103">Setzt das Timeout einer Synapse Analytics Spark-Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="df291-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="df291-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df291-104">SYNTAX</span></span>

### <span data-ttu-id="df291-105">ResetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="df291-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df291-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df291-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df291-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df291-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df291-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df291-108">DESCRIPTION</span></span>
<span data-ttu-id="df291-109">Das **Cmdlet Remove-AzSynapseSparkSessionTimeout** setzt das Timeout einer Synapse Analytics Spark-Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="df291-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="df291-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df291-110">EXAMPLES</span></span>

### <span data-ttu-id="df291-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df291-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="df291-112">Mit diesem Befehl wird das Timeout der Synapse Analytics Spark-Sitzung mit der angegebenen Livy-ID zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="df291-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="df291-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df291-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="df291-114">Mit diesem Befehl wird das Timeout der Synapse Analytics Spark-Sitzung mit der angegebenen Livy-ID über die Pipeline zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="df291-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="df291-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="df291-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="df291-116">Mit diesem Befehl wird das Timeout der Synapse Analytics Spark-Sitzung mit der angegebenen Livy-ID über die Pipeline zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="df291-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="df291-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="df291-117">PARAMETERS</span></span>

### <span data-ttu-id="df291-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df291-118">-AsJob</span></span>
<span data-ttu-id="df291-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="df291-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df291-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df291-120">-DefaultProfile</span></span>
<span data-ttu-id="df291-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df291-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df291-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df291-122">-InputObject</span></span>
<span data-ttu-id="df291-123">Spark-Sitzungseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="df291-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df291-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="df291-124">-LivyId</span></span>
<span data-ttu-id="df291-125">Bezeichner der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="df291-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df291-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df291-126">-PassThru</span></span>
<span data-ttu-id="df291-127">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="df291-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="df291-128">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="df291-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="df291-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="df291-129">-SparkPoolName</span></span>
<span data-ttu-id="df291-130">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="df291-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df291-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="df291-131">-SparkPoolObject</span></span>
<span data-ttu-id="df291-132">Spark pool input object, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="df291-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df291-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="df291-133">-WorkspaceName</span></span>
<span data-ttu-id="df291-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="df291-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df291-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df291-135">-Confirm</span></span>
<span data-ttu-id="df291-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df291-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df291-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df291-137">-WhatIf</span></span>
<span data-ttu-id="df291-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df291-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df291-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df291-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df291-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df291-140">CommonParameters</span></span>
<span data-ttu-id="df291-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df291-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df291-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df291-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df291-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df291-143">INPUTS</span></span>

### <span data-ttu-id="df291-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="df291-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="df291-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="df291-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="df291-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df291-146">OUTPUTS</span></span>

### <span data-ttu-id="df291-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df291-147">System.Boolean</span></span>

## <span data-ttu-id="df291-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="df291-148">NOTES</span></span>

## <span data-ttu-id="df291-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="df291-149">RELATED LINKS</span></span>
