---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007671"
---
# <span data-ttu-id="4f904-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="4f904-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="4f904-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f904-102">SYNOPSIS</span></span>
<span data-ttu-id="4f904-103">Bricht eine Synapse Analytics Spark-Anweisung ab.</span><span class="sxs-lookup"><span data-stu-id="4f904-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="4f904-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f904-104">SYNTAX</span></span>

### <span data-ttu-id="4f904-105">StopSparkStatementByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f904-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f904-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f904-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f904-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f904-107">DESCRIPTION</span></span>
<span data-ttu-id="4f904-108">Das Cmdlet " **Stop-AzSynapseSparkStatement** " bricht eine Synapse Analytics Spark-Anweisung ab.</span><span class="sxs-lookup"><span data-stu-id="4f904-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="4f904-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f904-109">EXAMPLES</span></span>

### <span data-ttu-id="4f904-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f904-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="4f904-111">Mit diesem Befehl wird die Spark-Anweisung mit der angegebenen Livius-ID abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4f904-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="4f904-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4f904-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="4f904-113">Dieser Befehl bricht die Spark-Anweisung mit der angegebenen Livius-ID bis zur Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="4f904-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="4f904-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f904-114">PARAMETERS</span></span>

### <span data-ttu-id="4f904-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f904-115">-DefaultProfile</span></span>
<span data-ttu-id="4f904-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f904-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f904-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4f904-117">-Force</span></span>
<span data-ttu-id="4f904-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="4f904-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4f904-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="4f904-119">-LivyId</span></span>
<span data-ttu-id="4f904-120">Bezeichner der Spark-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="4f904-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="4f904-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f904-121">-PassThru</span></span>
<span data-ttu-id="4f904-122">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4f904-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4f904-123">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4f904-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4f904-124">-SessionID</span><span class="sxs-lookup"><span data-stu-id="4f904-124">-SessionId</span></span>
<span data-ttu-id="4f904-125">Kennung der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4f904-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="4f904-126">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="4f904-126">-SessionObject</span></span>
<span data-ttu-id="4f904-127">Spark Session-Eingabeobjekt, in der Regel durch die Pipeline geleitet.</span><span class="sxs-lookup"><span data-stu-id="4f904-127">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4f904-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4f904-128">-SparkPoolName</span></span>
<span data-ttu-id="4f904-129">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="4f904-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="4f904-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4f904-130">-WorkspaceName</span></span>
<span data-ttu-id="4f904-131">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="4f904-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4f904-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f904-132">-Confirm</span></span>
<span data-ttu-id="4f904-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f904-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f904-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f904-134">-WhatIf</span></span>
<span data-ttu-id="4f904-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f904-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f904-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f904-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f904-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f904-137">CommonParameters</span></span>
<span data-ttu-id="4f904-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f904-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f904-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f904-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f904-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f904-140">INPUTS</span></span>

### <span data-ttu-id="4f904-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="4f904-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="4f904-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f904-142">OUTPUTS</span></span>

### <span data-ttu-id="4f904-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f904-143">System.Boolean</span></span>

## <span data-ttu-id="4f904-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f904-144">NOTES</span></span>

## <span data-ttu-id="4f904-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f904-145">RELATED LINKS</span></span>
