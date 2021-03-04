---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: a14079c92a59864b98dd086d8e65a340e2a277d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939139"
---
# <span data-ttu-id="d773f-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="d773f-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="d773f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d773f-102">SYNOPSIS</span></span>
<span data-ttu-id="d773f-103">Bricht eine Synapse Analytics Spark-Anweisung ab.</span><span class="sxs-lookup"><span data-stu-id="d773f-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="d773f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d773f-104">SYNTAX</span></span>

### <span data-ttu-id="d773f-105">StopSparkStatementByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d773f-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d773f-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d773f-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d773f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d773f-107">DESCRIPTION</span></span>
<span data-ttu-id="d773f-108">Das **Cmdlet Stop-AzSynapseSparkStatement** sagt eine Synapse Analytics Spark-Anweisung ab.</span><span class="sxs-lookup"><span data-stu-id="d773f-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="d773f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d773f-109">EXAMPLES</span></span>

### <span data-ttu-id="d773f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d773f-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="d773f-111">Mit diesem Befehl wird die Spark-Anweisung mit der angegebenen Lebenswert-ID abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d773f-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="d773f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d773f-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="d773f-113">Mit diesem Befehl wird die Spark-Anweisung mit der angegebenen Lebenswert-ID über die Pipeline abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d773f-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="d773f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d773f-114">PARAMETERS</span></span>

### <span data-ttu-id="d773f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d773f-115">-DefaultProfile</span></span>
<span data-ttu-id="d773f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d773f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d773f-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d773f-117">-Force</span></span>
<span data-ttu-id="d773f-118">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="d773f-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d773f-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="d773f-119">-LivyId</span></span>
<span data-ttu-id="d773f-120">Bezeichner der Spark-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="d773f-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d773f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d773f-121">-PassThru</span></span>
<span data-ttu-id="d773f-122">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d773f-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d773f-123">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="d773f-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d773f-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="d773f-124">-SessionId</span></span>
<span data-ttu-id="d773f-125">Bezeichner der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d773f-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d773f-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="d773f-126">-SessionObject</span></span>
<span data-ttu-id="d773f-127">Spark-Sitzungseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d773f-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d773f-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="d773f-128">-SparkPoolName</span></span>
<span data-ttu-id="d773f-129">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="d773f-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d773f-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d773f-130">-WorkspaceName</span></span>
<span data-ttu-id="d773f-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d773f-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d773f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d773f-132">-Confirm</span></span>
<span data-ttu-id="d773f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d773f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d773f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d773f-134">-WhatIf</span></span>
<span data-ttu-id="d773f-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d773f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d773f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d773f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d773f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d773f-137">CommonParameters</span></span>
<span data-ttu-id="d773f-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d773f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d773f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d773f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d773f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d773f-140">INPUTS</span></span>

### <span data-ttu-id="d773f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="d773f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="d773f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d773f-142">OUTPUTS</span></span>

### <span data-ttu-id="d773f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d773f-143">System.Boolean</span></span>

## <span data-ttu-id="d773f-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d773f-144">NOTES</span></span>

## <span data-ttu-id="d773f-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d773f-145">RELATED LINKS</span></span>
