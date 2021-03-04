---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 62894b5d879febdeeb7c14360c16c66fb8a28ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934595"
---
# <span data-ttu-id="e752c-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="e752c-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="e752c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e752c-102">SYNOPSIS</span></span>
<span data-ttu-id="e752c-103">Ruft eine Synapse Analytics Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="e752c-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="e752c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e752c-104">SYNTAX</span></span>

### <span data-ttu-id="e752c-105">RunSparkStatementByCodePathParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e752c-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e752c-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e752c-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e752c-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e752c-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e752c-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e752c-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e752c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e752c-109">DESCRIPTION</span></span>
<span data-ttu-id="e752c-110">Das **Cmdlet Invoke-AzSynapseSparkStatement** ruft eine Synapse Analytics Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="e752c-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="e752c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e752c-111">EXAMPLES</span></span>

### <span data-ttu-id="e752c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e752c-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="e752c-113">Diese Befehle starten eine Spark-Sitzung und rufen dann über die Pipeline eine Inline-Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="e752c-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="e752c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e752c-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="e752c-115">Diese Befehle starten eine Spark-Sitzung und rufen dann eine Inline-Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="e752c-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="e752c-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e752c-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="e752c-117">Diese Befehle starten eine Spark-Sitzung und rufen dann Spark-Anweisungen in einer Datei auf.</span><span class="sxs-lookup"><span data-stu-id="e752c-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="e752c-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e752c-118">PARAMETERS</span></span>

### <span data-ttu-id="e752c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e752c-119">-AsJob</span></span>
<span data-ttu-id="e752c-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e752c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e752c-121">-Code</span><span class="sxs-lookup"><span data-stu-id="e752c-121">-Code</span></span>
<span data-ttu-id="e752c-122">Der Ausführungscode.</span><span class="sxs-lookup"><span data-stu-id="e752c-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e752c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e752c-123">-DefaultProfile</span></span>
<span data-ttu-id="e752c-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e752c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e752c-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e752c-125">-FilePath</span></span>
<span data-ttu-id="e752c-126">Gibt einen lokalen Dateipfad an, der den Ausführungscode enthält.</span><span class="sxs-lookup"><span data-stu-id="e752c-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e752c-127">-Sprache</span><span class="sxs-lookup"><span data-stu-id="e752c-127">-Language</span></span>
<span data-ttu-id="e752c-128">Sprache des Ausführungscodes.</span><span class="sxs-lookup"><span data-stu-id="e752c-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e752c-129">-Antwort</span><span class="sxs-lookup"><span data-stu-id="e752c-129">-Response</span></span>
<span data-ttu-id="e752c-130">Gibt an, dass die vollständige Antwort zurückgeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e752c-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="e752c-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="e752c-131">-SessionId</span></span>
<span data-ttu-id="e752c-132">Bezeichner der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e752c-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e752c-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="e752c-133">-SessionObject</span></span>
<span data-ttu-id="e752c-134">Spark-Sitzungseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e752c-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e752c-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e752c-135">-SparkPoolName</span></span>
<span data-ttu-id="e752c-136">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="e752c-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e752c-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e752c-137">-WorkspaceName</span></span>
<span data-ttu-id="e752c-138">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e752c-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e752c-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e752c-139">-Confirm</span></span>
<span data-ttu-id="e752c-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e752c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e752c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e752c-141">-WhatIf</span></span>
<span data-ttu-id="e752c-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e752c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e752c-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e752c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e752c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e752c-144">CommonParameters</span></span>
<span data-ttu-id="e752c-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e752c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e752c-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e752c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e752c-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e752c-147">INPUTS</span></span>

### <span data-ttu-id="e752c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e752c-148">System.String</span></span>

### <span data-ttu-id="e752c-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="e752c-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="e752c-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e752c-150">OUTPUTS</span></span>

### <span data-ttu-id="e752c-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="e752c-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="e752c-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e752c-152">NOTES</span></span>

## <span data-ttu-id="e752c-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e752c-153">RELATED LINKS</span></span>
