---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e936d237589aec46d0f677344dfcd4274e19816d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477190"
---
# <span data-ttu-id="b078f-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b078f-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="b078f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b078f-102">SYNOPSIS</span></span>
<span data-ttu-id="b078f-103">Entfernt eine Pipeline aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b078f-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b078f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b078f-104">SYNTAX</span></span>

### <span data-ttu-id="b078f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b078f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b078f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b078f-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b078f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b078f-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b078f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b078f-108">DESCRIPTION</span></span>
<span data-ttu-id="b078f-109">Das Remove-AzureRmDataFactoryV2Pipeline-Cmdlet entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b078f-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="b078f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b078f-110">EXAMPLES</span></span>

### <span data-ttu-id="b078f-111">Beispiel 1: Entfernen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="b078f-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="b078f-112">Dieses Cmdlet entfernt die Pipeline mit dem Namen DPWikisample aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b078f-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="b078f-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="b078f-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="b078f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b078f-114">PARAMETERS</span></span>

### <span data-ttu-id="b078f-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b078f-115">-Confirm</span></span>
<span data-ttu-id="b078f-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b078f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b078f-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b078f-117">-DataFactoryName</span></span>
<span data-ttu-id="b078f-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="b078f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b078f-119">Dieses Cmdlet entfernt eine Pipeline aus der Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b078f-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b078f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b078f-120">-Force</span></span>
<span data-ttu-id="b078f-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="b078f-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b078f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b078f-122">-Name</span></span>
<span data-ttu-id="b078f-123">Gibt den Namen der zu entfernenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="b078f-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b078f-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b078f-124">-InputObject</span></span>
<span data-ttu-id="b078f-125">Gibt ein Pipeline Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b078f-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="b078f-126">Dieses Cmdlet entfernt die von diesem Parameter festgelegte Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b078f-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b078f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b078f-127">-ResourceGroupName</span></span>
<span data-ttu-id="b078f-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b078f-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b078f-129">Dieses Cmdlet entfernt eine Pipeline aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b078f-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b078f-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b078f-130">-ResourceId</span></span>
<span data-ttu-id="b078f-131">Die Azure-Ressourcen-ID der zu entfernenden Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b078f-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b078f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b078f-132">-WhatIf</span></span>
<span data-ttu-id="b078f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b078f-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b078f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b078f-134">-DefaultProfile</span></span>
<span data-ttu-id="b078f-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b078f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b078f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b078f-136">CommonParameters</span></span>
<span data-ttu-id="b078f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b078f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b078f-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b078f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b078f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b078f-139">INPUTS</span></span>

### <span data-ttu-id="b078f-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b078f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="b078f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b078f-141">System.String</span></span>

## <span data-ttu-id="b078f-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b078f-142">OUTPUTS</span></span>

### <span data-ttu-id="b078f-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="b078f-143">System.Object</span></span>

## <span data-ttu-id="b078f-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b078f-144">NOTES</span></span>
<span data-ttu-id="b078f-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="b078f-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b078f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b078f-146">RELATED LINKS</span></span>

[<span data-ttu-id="b078f-147">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b078f-147">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b078f-148">Satz-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b078f-148">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b078f-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b078f-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

