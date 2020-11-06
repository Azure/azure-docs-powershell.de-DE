---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: 7466ad5617fb78d48deb92ac2d623fc05ad90634
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505094"
---
# <span data-ttu-id="b85c2-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b85c2-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="b85c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b85c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b85c2-103">Ruft Informationen zu verknüpften Diensten in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b85c2-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b85c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b85c2-104">SYNTAX</span></span>

### <span data-ttu-id="b85c2-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b85c2-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="b85c2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b85c2-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
```
## <span data-ttu-id="b85c2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b85c2-107">DESCRIPTION</span></span>
<span data-ttu-id="b85c2-108">Das Get-AzureRmDataFactoryV2LinkedService-Cmdlet ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b85c2-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="b85c2-109">Wenn Sie den Namen eines verknüpften Diensts angeben, ruft dieses Cmdlet Informationen zu diesem verknüpften Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="b85c2-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="b85c2-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen verknüpften Diensten in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b85c2-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="b85c2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b85c2-111">EXAMPLES</span></span>

### <span data-ttu-id="b85c2-112">Beispiel 1: Abrufen von Informationen zu allen verknüpften Diensten</span><span class="sxs-lookup"><span data-stu-id="b85c2-112">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="b85c2-113">Dieser Befehl ruft Informationen zu allen verknüpften Diensten in der Data Factory mit dem Namen WikiADF ab und übergibt dann die verknüpften Dienste mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b85c2-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b85c2-114">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="b85c2-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="b85c2-115">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="b85c2-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="b85c2-116">Sie können eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="b85c2-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="b85c2-117">Beispiel 2: Abrufen von Informationen zu einem bestimmten verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="b85c2-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="b85c2-118">Dieser Befehl ruft Informationen zum verknüpften Dienst mit dem Namen LinkedServiceCuratedWikiData in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="b85c2-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b85c2-119">Beispiel 3: Abrufen von Informationen zu einem bestimmten verknüpften Dienst durch Angabe des DataFactory-Parameters</span><span class="sxs-lookup"><span data-stu-id="b85c2-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="b85c2-120">Der erste Befehl verwendet das Get-AzureRmDataFactoryV2-Cmdlet, um die Data Factory mit dem Namen ContosoFactory abzurufen, und speichert Sie dann in der $datafactory-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b85c2-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="b85c2-121">Der zweite Befehl ruft Informationen zum verknüpften Dienst für die in $DataFactory gespeicherte Daten Factory ab und übergibt diese Informationen dann mithilfe des Pipelineoperators an das Format-Table-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b85c2-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b85c2-122">Das Format-Table-Cmdlet formatiert die Ausgabe als DataSet mit den angegebenen Eigenschaften als DataSet-Spalten.</span><span class="sxs-lookup"><span data-stu-id="b85c2-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="b85c2-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="b85c2-123">PARAMETERS</span></span>

### <span data-ttu-id="b85c2-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b85c2-124">-DataFactory</span></span>
<span data-ttu-id="b85c2-125">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b85c2-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="b85c2-126">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b85c2-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b85c2-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b85c2-127">-DataFactoryName</span></span>
<span data-ttu-id="b85c2-128">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="b85c2-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b85c2-129">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b85c2-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b85c2-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b85c2-130">-Name</span></span>
<span data-ttu-id="b85c2-131">Gibt den Namen des verknüpften Diensts an, für den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b85c2-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85c2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85c2-132">-ResourceGroupName</span></span>
<span data-ttu-id="b85c2-133">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b85c2-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b85c2-134">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b85c2-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="b85c2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b85c2-135">INPUTS</span></span>

### <span data-ttu-id="b85c2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b85c2-136">System.String</span></span>
<span data-ttu-id="b85c2-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b85c2-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="b85c2-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b85c2-138">OUTPUTS</span></span>

### <span data-ttu-id="b85c2-139">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b85c2-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b85c2-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b85c2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="b85c2-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b85c2-141">NOTES</span></span>
<span data-ttu-id="b85c2-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="b85c2-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b85c2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b85c2-143">RELATED LINKS</span></span>
[<span data-ttu-id="b85c2-144">Satz-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b85c2-144">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="b85c2-145">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b85c2-145">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
