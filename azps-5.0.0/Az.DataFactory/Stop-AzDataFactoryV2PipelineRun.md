---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298191"
---
# <span data-ttu-id="ec18e-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ec18e-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="ec18e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec18e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec18e-103">Beendet eine Pipeline, die in einer Data Factory ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec18e-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="ec18e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec18e-104">SYNTAX</span></span>

### <span data-ttu-id="ec18e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec18e-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec18e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec18e-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec18e-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ec18e-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec18e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec18e-108">DESCRIPTION</span></span>
<span data-ttu-id="ec18e-109">Das Cmdlet **Stop-AzDataFactoryV2PipelineRun** beendet eine Pipeline, die in einer mit der Pipeline Lauf-ID angegebenen Data Factory ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec18e-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="ec18e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec18e-110">EXAMPLES</span></span>

### <span data-ttu-id="ec18e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec18e-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="ec18e-112">Dieser Befehl beendet die Pipelineausführung mit ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd im Factory-WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ec18e-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="ec18e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec18e-113">PARAMETERS</span></span>

### <span data-ttu-id="ec18e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ec18e-114">-DataFactory</span></span>
<span data-ttu-id="ec18e-115">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ec18e-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec18e-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ec18e-116">-DataFactoryName</span></span>
<span data-ttu-id="ec18e-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="ec18e-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec18e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec18e-118">-DefaultProfile</span></span>
<span data-ttu-id="ec18e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec18e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec18e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ec18e-120">-InputObject</span></span>
<span data-ttu-id="ec18e-121">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ec18e-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec18e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec18e-122">-PassThru</span></span>
<span data-ttu-id="ec18e-123">Wenn angegeben, schreibt das Cmdlet true, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec18e-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="ec18e-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="ec18e-124">-PipelineRunId</span></span>
<span data-ttu-id="ec18e-125">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ec18e-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec18e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec18e-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec18e-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec18e-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec18e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec18e-128">-Confirm</span></span>
<span data-ttu-id="ec18e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec18e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec18e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec18e-130">-WhatIf</span></span>
<span data-ttu-id="ec18e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec18e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec18e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec18e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec18e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec18e-133">CommonParameters</span></span>
<span data-ttu-id="ec18e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec18e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec18e-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec18e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec18e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec18e-136">INPUTS</span></span>

### <span data-ttu-id="ec18e-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="ec18e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="ec18e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ec18e-138">System.String</span></span>

### <span data-ttu-id="ec18e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ec18e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ec18e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec18e-140">OUTPUTS</span></span>

### <span data-ttu-id="ec18e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec18e-141">System.Boolean</span></span>

## <span data-ttu-id="ec18e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec18e-142">NOTES</span></span>

## <span data-ttu-id="ec18e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec18e-143">RELATED LINKS</span></span>
