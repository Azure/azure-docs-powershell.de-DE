---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175949"
---
# <span data-ttu-id="58755-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="58755-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="58755-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58755-102">SYNOPSIS</span></span>
<span data-ttu-id="58755-103">Bricht eine Synapse Analytics Spark Job ab.</span><span class="sxs-lookup"><span data-stu-id="58755-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="58755-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58755-104">SYNTAX</span></span>

### <span data-ttu-id="58755-105">StopSparkJobByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="58755-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58755-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58755-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58755-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58755-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58755-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58755-108">DESCRIPTION</span></span>
<span data-ttu-id="58755-109">Das Cmdlet " **Stop-AzSynapseSparkJob** " bricht einen Spark-Job für Synapse Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="58755-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="58755-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58755-110">EXAMPLES</span></span>

### <span data-ttu-id="58755-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58755-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="58755-112">Mit diesem Befehl wird eine Synapse Analytics Spark-Aufgabe abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="58755-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="58755-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="58755-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="58755-114">Dieser Befehl bricht eine Synapse Analytics Spark Job durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="58755-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="58755-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="58755-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="58755-116">Dieser Befehl bricht eine Synapse Analytics Spark Job durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="58755-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="58755-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="58755-117">PARAMETERS</span></span>

### <span data-ttu-id="58755-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58755-118">-DefaultProfile</span></span>
<span data-ttu-id="58755-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58755-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58755-120">-Force</span><span class="sxs-lookup"><span data-stu-id="58755-120">-Force</span></span>
<span data-ttu-id="58755-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="58755-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="58755-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="58755-122">-LivyId</span></span>
<span data-ttu-id="58755-123">Kennung des Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="58755-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="58755-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58755-124">-PassThru</span></span>
<span data-ttu-id="58755-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="58755-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="58755-126">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="58755-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="58755-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="58755-127">-SparkJobObject</span></span>
<span data-ttu-id="58755-128">Spark Job Input-Objekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="58755-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="58755-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="58755-129">-SparkPoolName</span></span>
<span data-ttu-id="58755-130">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="58755-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="58755-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="58755-131">-SparkPoolObject</span></span>
<span data-ttu-id="58755-132">Spark Pool-Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="58755-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="58755-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58755-133">-WorkspaceName</span></span>
<span data-ttu-id="58755-134">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="58755-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="58755-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58755-135">-Confirm</span></span>
<span data-ttu-id="58755-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58755-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58755-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58755-137">-WhatIf</span></span>
<span data-ttu-id="58755-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58755-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58755-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58755-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58755-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58755-140">CommonParameters</span></span>
<span data-ttu-id="58755-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58755-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58755-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58755-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58755-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58755-143">INPUTS</span></span>

### <span data-ttu-id="58755-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="58755-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="58755-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="58755-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="58755-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58755-146">OUTPUTS</span></span>

### <span data-ttu-id="58755-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58755-147">System.Boolean</span></span>

## <span data-ttu-id="58755-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="58755-148">NOTES</span></span>

## <span data-ttu-id="58755-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58755-149">RELATED LINKS</span></span>
