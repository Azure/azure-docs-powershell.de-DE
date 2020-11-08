---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007681"
---
# <span data-ttu-id="4ad54-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="4ad54-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="4ad54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ad54-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad54-103">Ruft eine Synapse Analytics Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="4ad54-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="4ad54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ad54-104">SYNTAX</span></span>

### <span data-ttu-id="4ad54-105">RunSparkStatementByCodePathParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ad54-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ad54-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ad54-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ad54-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ad54-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ad54-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ad54-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ad54-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ad54-109">DESCRIPTION</span></span>
<span data-ttu-id="4ad54-110">Das Cmdlet **Invoke-AzSynapseSparkStatement** Ruft eine Synapse Analytics Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="4ad54-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="4ad54-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ad54-111">EXAMPLES</span></span>

### <span data-ttu-id="4ad54-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ad54-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="4ad54-113">Diese Befehle starten eine Funken Sitzung und rufen dann eine Inline Spark-Anweisung über Pipeline auf.</span><span class="sxs-lookup"><span data-stu-id="4ad54-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="4ad54-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ad54-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="4ad54-115">Diese Befehle starten eine Funken Sitzung und rufen dann eine Inline Spark-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="4ad54-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="4ad54-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4ad54-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="4ad54-117">Diese Befehle starten eine Funken Sitzung und rufen dann Spark-Anweisungen in einer Datei auf.</span><span class="sxs-lookup"><span data-stu-id="4ad54-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="4ad54-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ad54-118">PARAMETERS</span></span>

### <span data-ttu-id="4ad54-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ad54-119">-AsJob</span></span>
<span data-ttu-id="4ad54-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4ad54-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ad54-121">-Code</span><span class="sxs-lookup"><span data-stu-id="4ad54-121">-Code</span></span>
<span data-ttu-id="4ad54-122">Der Ausführungscode.</span><span class="sxs-lookup"><span data-stu-id="4ad54-122">The execution code.</span></span>

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

### <span data-ttu-id="4ad54-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad54-123">-DefaultProfile</span></span>
<span data-ttu-id="4ad54-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ad54-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad54-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="4ad54-125">-FilePath</span></span>
<span data-ttu-id="4ad54-126">Gibt einen lokalen Dateipfad an, der den Ausführungscode enthält.</span><span class="sxs-lookup"><span data-stu-id="4ad54-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="4ad54-127">– Sprache</span><span class="sxs-lookup"><span data-stu-id="4ad54-127">-Language</span></span>
<span data-ttu-id="4ad54-128">Die Sprache des Ausführungscodes.</span><span class="sxs-lookup"><span data-stu-id="4ad54-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="4ad54-129">-Response</span><span class="sxs-lookup"><span data-stu-id="4ad54-129">-Response</span></span>
<span data-ttu-id="4ad54-130">Gibt an, dass die vollständige Antwort zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ad54-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="4ad54-131">-SessionID</span><span class="sxs-lookup"><span data-stu-id="4ad54-131">-SessionId</span></span>
<span data-ttu-id="4ad54-132">Kennung der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4ad54-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="4ad54-133">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="4ad54-133">-SessionObject</span></span>
<span data-ttu-id="4ad54-134">Spark Session-Eingabeobjekt, in der Regel durch die Pipeline geleitet.</span><span class="sxs-lookup"><span data-stu-id="4ad54-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4ad54-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4ad54-135">-SparkPoolName</span></span>
<span data-ttu-id="4ad54-136">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="4ad54-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="4ad54-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ad54-137">-WorkspaceName</span></span>
<span data-ttu-id="4ad54-138">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="4ad54-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4ad54-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ad54-139">-Confirm</span></span>
<span data-ttu-id="4ad54-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ad54-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad54-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad54-141">-WhatIf</span></span>
<span data-ttu-id="4ad54-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ad54-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ad54-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ad54-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad54-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad54-144">CommonParameters</span></span>
<span data-ttu-id="4ad54-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad54-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad54-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ad54-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad54-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ad54-147">INPUTS</span></span>

### <span data-ttu-id="4ad54-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4ad54-148">System.String</span></span>

### <span data-ttu-id="4ad54-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="4ad54-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="4ad54-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ad54-150">OUTPUTS</span></span>

### <span data-ttu-id="4ad54-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="4ad54-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="4ad54-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ad54-152">NOTES</span></span>

## <span data-ttu-id="4ad54-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ad54-153">RELATED LINKS</span></span>
