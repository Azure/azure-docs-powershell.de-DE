---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167178"
---
# <span data-ttu-id="de803-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="de803-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="de803-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de803-102">SYNOPSIS</span></span>
<span data-ttu-id="de803-103">Bricht eine Synapse Analytics Spark Job ab.</span><span class="sxs-lookup"><span data-stu-id="de803-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="de803-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de803-104">SYNTAX</span></span>

### <span data-ttu-id="de803-105">StopSparkJobByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="de803-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de803-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de803-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de803-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de803-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de803-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de803-108">DESCRIPTION</span></span>
<span data-ttu-id="de803-109">Das Cmdlet " **Stop-AzSynapseSparkJob** " bricht einen Spark-Job für Synapse Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="de803-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="de803-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de803-110">EXAMPLES</span></span>

### <span data-ttu-id="de803-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de803-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="de803-112">Mit diesem Befehl wird eine Synapse Analytics Spark-Aufgabe abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="de803-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="de803-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="de803-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="de803-114">Dieser Befehl bricht eine Synapse Analytics Spark Job durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="de803-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="de803-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="de803-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="de803-116">Dieser Befehl bricht eine Synapse Analytics Spark Job durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="de803-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="de803-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="de803-117">PARAMETERS</span></span>

### <span data-ttu-id="de803-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de803-118">-DefaultProfile</span></span>
<span data-ttu-id="de803-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de803-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de803-120">-Force</span><span class="sxs-lookup"><span data-stu-id="de803-120">-Force</span></span>
<span data-ttu-id="de803-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="de803-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="de803-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="de803-122">-LivyId</span></span>
<span data-ttu-id="de803-123">Kennung des Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="de803-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="de803-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de803-124">-PassThru</span></span>
<span data-ttu-id="de803-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="de803-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="de803-126">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="de803-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="de803-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="de803-127">-SparkJobObject</span></span>
<span data-ttu-id="de803-128">Spark Job Input-Objekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="de803-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="de803-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="de803-129">-SparkPoolName</span></span>
<span data-ttu-id="de803-130">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="de803-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="de803-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="de803-131">-SparkPoolObject</span></span>
<span data-ttu-id="de803-132">Spark Pool-Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="de803-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="de803-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="de803-133">-WorkspaceName</span></span>
<span data-ttu-id="de803-134">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="de803-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="de803-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de803-135">-Confirm</span></span>
<span data-ttu-id="de803-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de803-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de803-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de803-137">-WhatIf</span></span>
<span data-ttu-id="de803-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de803-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de803-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de803-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de803-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de803-140">CommonParameters</span></span>
<span data-ttu-id="de803-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de803-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de803-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de803-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de803-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de803-143">INPUTS</span></span>

### <span data-ttu-id="de803-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="de803-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="de803-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="de803-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="de803-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de803-146">OUTPUTS</span></span>

### <span data-ttu-id="de803-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de803-147">System.Boolean</span></span>

## <span data-ttu-id="de803-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="de803-148">NOTES</span></span>

## <span data-ttu-id="de803-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de803-149">RELATED LINKS</span></span>
