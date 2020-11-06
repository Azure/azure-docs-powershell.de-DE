---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8ee5ba855e1c9f9815e9dbcb844ebb23d7118d3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479326"
---
# <span data-ttu-id="a24a4-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a24a4-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="a24a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a24a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a24a4-103">Ruft Informationen zu verknüpften Diensten in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="a24a4-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a24a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a24a4-104">SYNTAX</span></span>

### <span data-ttu-id="a24a4-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a24a4-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a24a4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a24a4-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a24a4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a24a4-107">DESCRIPTION</span></span>
<span data-ttu-id="a24a4-108">Das Get-AzureRmDataFactoryV2LinkedService-Cmdlet ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="a24a4-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="a24a4-109">Wenn Sie den Namen eines verknüpften Diensts angeben, ruft dieses Cmdlet Informationen zu diesem verknüpften Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="a24a4-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="a24a4-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen verknüpften Diensten in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="a24a4-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="a24a4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a24a4-111">EXAMPLES</span></span>

### <span data-ttu-id="a24a4-112">Beispiel 1: Abrufen von Informationen zu allen verknüpften Diensten</span><span class="sxs-lookup"><span data-stu-id="a24a4-112">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="a24a4-113">Dieser Befehl ruft Informationen zu allen verknüpften Diensten in der Data Factory mit dem Namen WikiADF ab und übergibt dann die verknüpften Dienste mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a24a4-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a24a4-114">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="a24a4-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="a24a4-115">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="a24a4-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="a24a4-116">Sie können eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="a24a4-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="a24a4-117">Beispiel 2: Abrufen von Informationen zu einem bestimmten verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="a24a4-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="a24a4-118">Dieser Befehl ruft Informationen zum verknüpften Dienst mit dem Namen LinkedServiceCuratedWikiData in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="a24a4-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="a24a4-119">Beispiel 3: Abrufen von Informationen zu einem bestimmten verknüpften Dienst durch Angabe des DataFactory-Parameters</span><span class="sxs-lookup"><span data-stu-id="a24a4-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="a24a4-120">Der erste Befehl verwendet das Get-AzureRmDataFactoryV2-Cmdlet, um die Data Factory mit dem Namen ContosoFactory abzurufen, und speichert Sie dann in der $datafactory-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a24a4-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="a24a4-121">Der zweite Befehl ruft Informationen zum verknüpften Dienst für die in $DataFactory gespeicherte Daten Factory ab und übergibt diese Informationen dann mithilfe des Pipelineoperators an das Format-Table-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a24a4-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a24a4-122">Das Format-Table-Cmdlet formatiert die Ausgabe als DataSet mit den angegebenen Eigenschaften als DataSet-Spalten.</span><span class="sxs-lookup"><span data-stu-id="a24a4-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="a24a4-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="a24a4-123">PARAMETERS</span></span>

### <span data-ttu-id="a24a4-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a24a4-124">-DataFactory</span></span>
<span data-ttu-id="a24a4-125">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a24a4-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="a24a4-126">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a24a4-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24a4-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a24a4-127">-DataFactoryName</span></span>
<span data-ttu-id="a24a4-128">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="a24a4-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a24a4-129">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a24a4-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24a4-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a24a4-130">-Name</span></span>
<span data-ttu-id="a24a4-131">Gibt den Namen des verknüpften Diensts an, für den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a24a4-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24a4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24a4-132">-ResourceGroupName</span></span>
<span data-ttu-id="a24a4-133">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a24a4-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a24a4-134">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a24a4-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24a4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24a4-135">-DefaultProfile</span></span>
<span data-ttu-id="a24a4-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a24a4-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24a4-137">CommonParameters</span></span>
<span data-ttu-id="a24a4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24a4-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24a4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24a4-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a24a4-140">INPUTS</span></span>

### <span data-ttu-id="a24a4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a24a4-141">System.String</span></span>
<span data-ttu-id="a24a4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a24a4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a24a4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a24a4-143">OUTPUTS</span></span>

### <span data-ttu-id="a24a4-144">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a24a4-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a24a4-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a24a4-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="a24a4-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a24a4-146">NOTES</span></span>
<span data-ttu-id="a24a4-147">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="a24a4-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a24a4-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a24a4-148">RELATED LINKS</span></span>

[<span data-ttu-id="a24a4-149">Satz-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a24a4-149">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="a24a4-150">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a24a4-150">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
