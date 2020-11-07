---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 9f5bac03f9c1d59e2d2fc271f462e1e08ca6349b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662226"
---
# <span data-ttu-id="cb12c-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb12c-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="cb12c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb12c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb12c-103">Entfernt eine Pipeline aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cb12c-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb12c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb12c-104">SYNTAX</span></span>

### <span data-ttu-id="cb12c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb12c-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb12c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb12c-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb12c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb12c-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb12c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb12c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb12c-109">Das Remove-AzureRmDataFactoryV2Pipeline-Cmdlet entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cb12c-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="cb12c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb12c-110">EXAMPLES</span></span>

### <span data-ttu-id="cb12c-111">Beispiel 1: Entfernen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb12c-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="cb12c-112">Dieses Cmdlet entfernt die Pipeline mit dem Namen DPWikisample aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cb12c-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="cb12c-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="cb12c-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="cb12c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb12c-114">PARAMETERS</span></span>

### <span data-ttu-id="cb12c-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cb12c-115">-DataFactoryName</span></span>
<span data-ttu-id="cb12c-116">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="cb12c-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cb12c-117">Dieses Cmdlet entfernt eine Pipeline aus der Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cb12c-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb12c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb12c-118">-DefaultProfile</span></span>
<span data-ttu-id="cb12c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb12c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb12c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cb12c-120">-Force</span></span>
<span data-ttu-id="cb12c-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="cb12c-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cb12c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cb12c-122">-InputObject</span></span>
<span data-ttu-id="cb12c-123">Gibt ein Pipeline Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cb12c-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="cb12c-124">Dieses Cmdlet entfernt die von diesem Parameter festgelegte Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb12c-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb12c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cb12c-125">-Name</span></span>
<span data-ttu-id="cb12c-126">Gibt den Namen der zu entfernenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="cb12c-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb12c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb12c-127">-ResourceGroupName</span></span>
<span data-ttu-id="cb12c-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cb12c-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cb12c-129">Dieses Cmdlet entfernt eine Pipeline aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cb12c-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb12c-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cb12c-130">-ResourceId</span></span>
<span data-ttu-id="cb12c-131">Die Azure-Ressourcen-ID der zu entfernenden Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb12c-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb12c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb12c-132">-Confirm</span></span>
<span data-ttu-id="cb12c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb12c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb12c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb12c-134">-WhatIf</span></span>
<span data-ttu-id="cb12c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb12c-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cb12c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb12c-136">CommonParameters</span></span>
<span data-ttu-id="cb12c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb12c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb12c-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb12c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb12c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb12c-139">INPUTS</span></span>

### <span data-ttu-id="cb12c-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="cb12c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="cb12c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cb12c-141">System.String</span></span>

## <span data-ttu-id="cb12c-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb12c-142">OUTPUTS</span></span>

### <span data-ttu-id="cb12c-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="cb12c-143">System.Object</span></span>

## <span data-ttu-id="cb12c-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb12c-144">NOTES</span></span>
<span data-ttu-id="cb12c-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="cb12c-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cb12c-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb12c-146">RELATED LINKS</span></span>

[<span data-ttu-id="cb12c-147">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb12c-147">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="cb12c-148">Satz-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb12c-148">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="cb12c-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb12c-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

