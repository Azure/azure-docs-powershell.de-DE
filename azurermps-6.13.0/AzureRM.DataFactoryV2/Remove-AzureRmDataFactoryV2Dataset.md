---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 86330711dc9b35c85d87543d2b2ee55e9b1d4a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476137"
---
# <span data-ttu-id="3d3d9-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3d3d9-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="3d3d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3d9-103">Entfernt ein DataSet aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d3d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d3d9-104">SYNTAX</span></span>

### <span data-ttu-id="3d3d9-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d3d9-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d3d9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d3d9-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d3d9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d3d9-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d3d9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d3d9-108">DESCRIPTION</span></span>
<span data-ttu-id="3d3d9-109">Das Remove-AzureRmDataFactoryV2Dataset-Cmdlet entfernt ein DataSet aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="3d3d9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d3d9-110">EXAMPLES</span></span>

### <span data-ttu-id="3d3d9-111">Beispiel 1: Entfernen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="3d3d9-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="3d3d9-112">Dieser Befehl entfernt das DataSet mit dem Namen DAWikiAggregatedData aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="3d3d9-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="3d3d9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d3d9-114">PARAMETERS</span></span>

### <span data-ttu-id="3d3d9-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3d3d9-115">-DataFactoryName</span></span>
<span data-ttu-id="3d3d9-116">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3d3d9-117">Dieses Cmdlet entfernt ein DataSet aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d3d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3d9-118">-DefaultProfile</span></span>
<span data-ttu-id="3d3d9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d3d9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3d3d9-120">-Force</span></span>
<span data-ttu-id="3d3d9-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3d3d9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d3d9-122">-InputObject</span></span>
<span data-ttu-id="3d3d9-123">Gibt ein zu entfernendes DataSet-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3d9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d3d9-124">-Name</span></span>
<span data-ttu-id="3d3d9-125">Gibt den Namen des zu entfernenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d3d9-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3d3d9-128">Mit diesem Cmdlet wird ein DataSet aus der Gruppe entfernt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d3d9-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3d3d9-129">-ResourceId</span></span>
<span data-ttu-id="3d3d9-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3d3d9-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d3d9-131">-Confirm</span></span>
<span data-ttu-id="3d3d9-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d3d9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d3d9-133">-WhatIf</span></span>
<span data-ttu-id="3d3d9-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3d3d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3d9-135">CommonParameters</span></span>
<span data-ttu-id="3d3d9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d3d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3d9-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3d9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3d9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d3d9-138">INPUTS</span></span>

### <span data-ttu-id="3d3d9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3d3d9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="3d3d9-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3d3d9-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3d3d9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3d3d9-141">System.String</span></span>

## <span data-ttu-id="3d3d9-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d3d9-142">OUTPUTS</span></span>

### <span data-ttu-id="3d3d9-143">System. void</span><span class="sxs-lookup"><span data-stu-id="3d3d9-143">System.Void</span></span>

## <span data-ttu-id="3d3d9-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d3d9-144">NOTES</span></span>
<span data-ttu-id="3d3d9-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="3d3d9-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3d3d9-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d3d9-146">RELATED LINKS</span></span>

[<span data-ttu-id="3d3d9-147">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3d3d9-147">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="3d3d9-148">Satz-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3d3d9-148">Set-AzureRmDataFactoryV2Dataset</span></span>]()
