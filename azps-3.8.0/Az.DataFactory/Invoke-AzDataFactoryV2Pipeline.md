---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 87d4cfadd183a6aa2652b86336b4dc8d089936fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847240"
---
# <span data-ttu-id="e91bb-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e91bb-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e91bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e91bb-102">SYNOPSIS</span></span>
  <span data-ttu-id="e91bb-103">Ruft eine Pipeline auf, um einen Testlauf zu starten.</span><span class="sxs-lookup"><span data-stu-id="e91bb-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="e91bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e91bb-104">SYNTAX</span></span>

### <span data-ttu-id="e91bb-105">ByFactoryNameByParameterFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="e91bb-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91bb-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="e91bb-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91bb-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e91bb-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91bb-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e91bb-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e91bb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e91bb-109">DESCRIPTION</span></span>
<span data-ttu-id="e91bb-110">Der Befehl **Invoke-AzDataFactoryV2Pipeline** startet eine Ausführung für die angegebene Pipeline und gibt eine ID für diesen Testlauf zurück.</span><span class="sxs-lookup"><span data-stu-id="e91bb-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="e91bb-111">Diese GUID kann an **Get-AzDataFactoryV2PipelineRun** oder **Get-AzDataFactoryV2ActivityRun** übergeben werden, um weitere Details zu diesem Testlauf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e91bb-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="e91bb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e91bb-112">EXAMPLES</span></span>

### <span data-ttu-id="e91bb-113">Beispiel 1: Aufrufen einer Pipeline zum Starten einer Ausführung</span><span class="sxs-lookup"><span data-stu-id="e91bb-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="e91bb-114">Mit diesem Befehl wird eine Run für "DPWikisample"-Pipeline in der Factory "WikiADF" gestartet.</span><span class="sxs-lookup"><span data-stu-id="e91bb-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="e91bb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e91bb-115">PARAMETERS</span></span>

### <span data-ttu-id="e91bb-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e91bb-116">-DataFactoryName</span></span>
<span data-ttu-id="e91bb-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="e91bb-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91bb-118">-DefaultProfile</span></span>
<span data-ttu-id="e91bb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e91bb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e91bb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e91bb-120">-InputObject</span></span>
<span data-ttu-id="e91bb-121">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e91bb-121">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e91bb-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e91bb-122">-Parameter</span></span>
<span data-ttu-id="e91bb-123">Parameter für Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="e91bb-123">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91bb-124">-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="e91bb-124">-ParameterFile</span></span>
<span data-ttu-id="e91bb-125">Der Name der Datei mit Parametern für die Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="e91bb-125">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91bb-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="e91bb-126">-PipelineName</span></span>
<span data-ttu-id="e91bb-127">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e91bb-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91bb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e91bb-128">-ResourceGroupName</span></span>
<span data-ttu-id="e91bb-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e91bb-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91bb-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e91bb-130">-Confirm</span></span>
<span data-ttu-id="e91bb-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e91bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e91bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e91bb-132">-WhatIf</span></span>
<span data-ttu-id="e91bb-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e91bb-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e91bb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91bb-134">CommonParameters</span></span>
<span data-ttu-id="e91bb-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91bb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91bb-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e91bb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91bb-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e91bb-137">INPUTS</span></span>

### <span data-ttu-id="e91bb-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e91bb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="e91bb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e91bb-139">System.String</span></span>

### <span data-ttu-id="e91bb-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e91bb-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e91bb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e91bb-141">OUTPUTS</span></span>

### <span data-ttu-id="e91bb-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e91bb-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e91bb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="e91bb-143">NOTES</span></span>

## <span data-ttu-id="e91bb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e91bb-144">RELATED LINKS</span></span>

[<span data-ttu-id="e91bb-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e91bb-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="e91bb-146">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e91bb-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

