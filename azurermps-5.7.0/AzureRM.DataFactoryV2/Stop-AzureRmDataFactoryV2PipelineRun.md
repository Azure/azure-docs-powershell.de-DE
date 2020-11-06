---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 7ddbc2809c58172eea2cd98ce048e0e49fbb14f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483050"
---
# <span data-ttu-id="7e4cb-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="7e4cb-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="7e4cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e4cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4cb-103">Beendet eine pieline, die in einer Data Factory ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e4cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e4cb-104">SYNTAX</span></span>

### <span data-ttu-id="7e4cb-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e4cb-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e4cb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7e4cb-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e4cb-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7e4cb-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4cb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e4cb-108">DESCRIPTION</span></span>
<span data-ttu-id="7e4cb-109">Das Cmdlet **Stop-AzureRmDataFactoryV2PipelineRun** beendet eine Pipeline, die in einer mit der pieline-Lauf Kennung angegebenen Daten Factory ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="7e4cb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e4cb-110">EXAMPLES</span></span>

### <span data-ttu-id="7e4cb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e4cb-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="7e4cb-112">Dieser Befehl beendet die Pipelineausführung mit ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd im Factory-WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="7e4cb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e4cb-113">PARAMETERS</span></span>

### <span data-ttu-id="7e4cb-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e4cb-114">-DataFactory</span></span>
<span data-ttu-id="7e4cb-115">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-115">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7e4cb-116">-DataFactoryName</span></span>
<span data-ttu-id="7e4cb-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4cb-118">-DefaultProfile</span></span>
<span data-ttu-id="7e4cb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7e4cb-120">-InputObject</span></span>
<span data-ttu-id="7e4cb-121">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-121">The Run ID of the pipeline.</span></span>

```yaml
Type: PSPipelineRun
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e4cb-122">-PassThru</span></span>
<span data-ttu-id="7e4cb-123">Wenn angegeben, schreibt das Cmdlet true, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-123">If specified the cmdlet write true in case operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="7e4cb-124">-PipelineRunId</span></span>
<span data-ttu-id="7e4cb-125">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e4cb-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e4cb-128">-Confirm</span></span>
<span data-ttu-id="7e4cb-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4cb-130">-WhatIf</span></span>
<span data-ttu-id="7e4cb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e4cb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4cb-133">CommonParameters</span></span>
<span data-ttu-id="7e4cb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e4cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4cb-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e4cb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4cb-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e4cb-136">INPUTS</span></span>

### <span data-ttu-id="7e4cb-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="7e4cb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="7e4cb-138">System. String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7e4cb-138">System.String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7e4cb-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e4cb-139">OUTPUTS</span></span>

### <span data-ttu-id="7e4cb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e4cb-140">System.Boolean</span></span>

## <span data-ttu-id="7e4cb-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e4cb-141">NOTES</span></span>

## <span data-ttu-id="7e4cb-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e4cb-142">RELATED LINKS</span></span>

