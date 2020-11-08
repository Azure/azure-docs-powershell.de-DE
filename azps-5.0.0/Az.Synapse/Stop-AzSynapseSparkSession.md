---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175948"
---
# <span data-ttu-id="f1cf1-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f1cf1-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="f1cf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cf1-103">Stoppt eine Synapse Analytics Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="f1cf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1cf1-104">SYNTAX</span></span>

### <span data-ttu-id="f1cf1-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1cf1-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1cf1-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1cf1-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1cf1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1cf1-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1cf1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1cf1-108">DESCRIPTION</span></span>
<span data-ttu-id="f1cf1-109">Das Cmdlet **Stop-AzSynapseSparkSession** beendet eine Synapse Analytics Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="f1cf1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1cf1-110">EXAMPLES</span></span>

### <span data-ttu-id="f1cf1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1cf1-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="f1cf1-112">Dieser Befehl beendet eine Synapse Analytics Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="f1cf1-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f1cf1-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="f1cf1-114">Dieser Befehl beendet eine Synapse Analytics Spark-Sitzung durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="f1cf1-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f1cf1-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="f1cf1-116">Dieser Befehl beendet eine Synapse Analytics Spark-Sitzung durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="f1cf1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1cf1-117">PARAMETERS</span></span>

### <span data-ttu-id="f1cf1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1cf1-118">-AsJob</span></span>
<span data-ttu-id="f1cf1-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1cf1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1cf1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cf1-120">-DefaultProfile</span></span>
<span data-ttu-id="f1cf1-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1cf1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1cf1-122">-InputObject</span></span>
<span data-ttu-id="f1cf1-123">Spark Session-Eingabeobjekt, in der Regel durch die Pipeline geleitet.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1cf1-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="f1cf1-124">-LivyId</span></span>
<span data-ttu-id="f1cf1-125">Kennung der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="f1cf1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1cf1-126">-PassThru</span></span>
<span data-ttu-id="f1cf1-127">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f1cf1-128">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f1cf1-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f1cf1-129">-SparkPoolName</span></span>
<span data-ttu-id="f1cf1-130">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f1cf1-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="f1cf1-131">-SparkPoolObject</span></span>
<span data-ttu-id="f1cf1-132">Spark Pool-Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1cf1-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1cf1-133">-WorkspaceName</span></span>
<span data-ttu-id="f1cf1-134">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="f1cf1-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f1cf1-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1cf1-135">-Confirm</span></span>
<span data-ttu-id="f1cf1-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1cf1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1cf1-137">-WhatIf</span></span>
<span data-ttu-id="f1cf1-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1cf1-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1cf1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cf1-140">CommonParameters</span></span>
<span data-ttu-id="f1cf1-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cf1-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1cf1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cf1-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1cf1-143">INPUTS</span></span>

### <span data-ttu-id="f1cf1-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f1cf1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="f1cf1-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f1cf1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="f1cf1-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1cf1-146">OUTPUTS</span></span>

### <span data-ttu-id="f1cf1-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1cf1-147">System.Boolean</span></span>

## <span data-ttu-id="f1cf1-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1cf1-148">NOTES</span></span>

## <span data-ttu-id="f1cf1-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1cf1-149">RELATED LINKS</span></span>
