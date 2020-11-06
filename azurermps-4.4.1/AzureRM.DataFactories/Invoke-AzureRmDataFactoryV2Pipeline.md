---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: a7486c3fc50e5c6517022190e05d099329fc6001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497109"
---
# <span data-ttu-id="689c9-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="689c9-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="689c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="689c9-102">SYNOPSIS</span></span>
  <span data-ttu-id="689c9-103">Ruft eine Pipeline auf, um einen Testlauf zu starten.</span><span class="sxs-lookup"><span data-stu-id="689c9-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="689c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="689c9-104">SYNTAX</span></span>

### <span data-ttu-id="689c9-105">ByFactoryNameByParameterFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="689c9-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="689c9-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="689c9-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="689c9-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="689c9-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="689c9-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="689c9-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="689c9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="689c9-109">DESCRIPTION</span></span>
<span data-ttu-id="689c9-110">Der Befehl **Invoke-AzureRmDataFactoryV2Pipeline** startet eine Ausführung für die angegebene Pipeline und gibt eine ID für diesen Testlauf zurück.</span><span class="sxs-lookup"><span data-stu-id="689c9-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="689c9-111">Diese GUID kann an **Get-AzureRmDataFactoryV2PipelineRun** oder **Get-AzureRmDataFactoryV2ActivityRun** übergeben werden, um weitere Details zu diesem Testlauf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="689c9-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="689c9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="689c9-112">EXAMPLES</span></span>

### <span data-ttu-id="689c9-113">Beispiel 1: Aufrufen einer Pipeline zum Starten einer Ausführung</span><span class="sxs-lookup"><span data-stu-id="689c9-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="689c9-114">Mit diesem Befehl wird eine Run für "DPWikisample"-Pipeline in der Factory "WikiADF" gestartet.</span><span class="sxs-lookup"><span data-stu-id="689c9-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="689c9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="689c9-115">PARAMETERS</span></span>

### <span data-ttu-id="689c9-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="689c9-116">-Confirm</span></span>
<span data-ttu-id="689c9-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="689c9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="689c9-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="689c9-118">-DataFactoryName</span></span>
<span data-ttu-id="689c9-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="689c9-119">The data factory name.</span></span>

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

### <span data-ttu-id="689c9-120">-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="689c9-120">-ParameterFile</span></span>
<span data-ttu-id="689c9-121">Der Name der Datei mit Parametern für die Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="689c9-121">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="689c9-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="689c9-122">-Parameter</span></span>
<span data-ttu-id="689c9-123">Parameter für Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="689c9-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="689c9-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="689c9-124">-InputObject</span></span>
<span data-ttu-id="689c9-125">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="689c9-125">The data factory object.</span></span>

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

### <span data-ttu-id="689c9-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="689c9-126">-PipelineName</span></span>
<span data-ttu-id="689c9-127">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="689c9-127">The pipeline name.</span></span>

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

### <span data-ttu-id="689c9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689c9-128">-ResourceGroupName</span></span>
<span data-ttu-id="689c9-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="689c9-129">The resource group name.</span></span>

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

### <span data-ttu-id="689c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="689c9-130">-WhatIf</span></span>
<span data-ttu-id="689c9-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="689c9-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="689c9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689c9-132">-DefaultProfile</span></span>
<span data-ttu-id="689c9-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="689c9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689c9-134">CommonParameters</span></span>
<span data-ttu-id="689c9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="689c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689c9-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="689c9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689c9-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="689c9-137">INPUTS</span></span>

### <span data-ttu-id="689c9-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="689c9-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="689c9-139">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="689c9-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="689c9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="689c9-140">OUTPUTS</span></span>

### <span data-ttu-id="689c9-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="689c9-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="689c9-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="689c9-142">NOTES</span></span>

## <span data-ttu-id="689c9-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="689c9-143">RELATED LINKS</span></span>

[<span data-ttu-id="689c9-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="689c9-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="689c9-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="689c9-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

