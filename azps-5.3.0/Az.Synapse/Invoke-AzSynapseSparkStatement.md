---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383660"
---
# <span data-ttu-id="f8b5e-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="f8b5e-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="f8b5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b5e-103">Ruft eine Synapse Analytics Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f8b5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8b5e-104">SYNTAX</span></span>

### <span data-ttu-id="f8b5e-105">RunSparkStatementByCodePathParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8b5e-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b5e-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b5e-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b5e-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b5e-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8b5e-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b5e-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8b5e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8b5e-109">DESCRIPTION</span></span>
<span data-ttu-id="f8b5e-110">Das **Cmdlet "Invoke-AzSynapseSparkStatement"** ruft eine Synapse Analytics Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f8b5e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8b5e-111">EXAMPLES</span></span>

### <span data-ttu-id="f8b5e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8b5e-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="f8b5e-113">Mit diesen Befehlen wird eine Sparksitzung gestartet und dann über die Pipeline eine Inline -Spark-Anweisung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="f8b5e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f8b5e-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="f8b5e-115">Diese Befehle starten eine Spark-Sitzung und rufen dann eine Inline-Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="f8b5e-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f8b5e-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="f8b5e-117">Mit diesen Befehlen wird eine Sparksitzung gestartet und dann die Sparkanweisungen in einer Datei aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="f8b5e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8b5e-118">PARAMETERS</span></span>

### <span data-ttu-id="f8b5e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8b5e-119">-AsJob</span></span>
<span data-ttu-id="f8b5e-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f8b5e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8b5e-121">-Code</span><span class="sxs-lookup"><span data-stu-id="f8b5e-121">-Code</span></span>
<span data-ttu-id="f8b5e-122">Der Ausführungscode.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-122">The execution code.</span></span>

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

### <span data-ttu-id="f8b5e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b5e-123">-DefaultProfile</span></span>
<span data-ttu-id="f8b5e-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b5e-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f8b5e-125">-FilePath</span></span>
<span data-ttu-id="f8b5e-126">Gibt einen lokalen Dateipfad an, der den Ausführungscode enthält.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="f8b5e-127">-Language</span><span class="sxs-lookup"><span data-stu-id="f8b5e-127">-Language</span></span>
<span data-ttu-id="f8b5e-128">Die Sprache des Ausführungscodes.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="f8b5e-129">-Response</span><span class="sxs-lookup"><span data-stu-id="f8b5e-129">-Response</span></span>
<span data-ttu-id="f8b5e-130">Gibt an, dass eine vollständige Antwort zurückgeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="f8b5e-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="f8b5e-131">-SessionId</span></span>
<span data-ttu-id="f8b5e-132">Id der Sparksitzung.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="f8b5e-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="f8b5e-133">-SessionObject</span></span>
<span data-ttu-id="f8b5e-134">Spark session input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f8b5e-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f8b5e-135">-SparkPoolName</span></span>
<span data-ttu-id="f8b5e-136">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f8b5e-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8b5e-137">-WorkspaceName</span></span>
<span data-ttu-id="f8b5e-138">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f8b5e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8b5e-139">-Confirm</span></span>
<span data-ttu-id="f8b5e-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b5e-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f8b5e-141">-WhatIf</span></span>
<span data-ttu-id="f8b5e-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8b5e-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b5e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b5e-144">CommonParameters</span></span>
<span data-ttu-id="f8b5e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b5e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b5e-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b5e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b5e-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8b5e-147">INPUTS</span></span>

### <span data-ttu-id="f8b5e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f8b5e-148">System.String</span></span>

### <span data-ttu-id="f8b5e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f8b5e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="f8b5e-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8b5e-150">OUTPUTS</span></span>

### <span data-ttu-id="f8b5e-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="f8b5e-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="f8b5e-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f8b5e-152">NOTES</span></span>

## <span data-ttu-id="f8b5e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f8b5e-153">RELATED LINKS</span></span>
