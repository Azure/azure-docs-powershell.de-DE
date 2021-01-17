---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470583"
---
# <span data-ttu-id="fb88d-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="fb88d-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="fb88d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb88d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb88d-103">Ruft Informationen zu verknüpften Diensten in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="fb88d-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="fb88d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb88d-104">SYNTAX</span></span>

### <span data-ttu-id="fb88d-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb88d-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb88d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fb88d-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb88d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb88d-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb88d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb88d-108">DESCRIPTION</span></span>
<span data-ttu-id="fb88d-109">Das Get-AzDataFactoryV2LinkedService Cmdlet ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="fb88d-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="fb88d-110">Wenn Sie den Namen eines verknüpften Diensts angeben, ruft dieses Cmdlet Informationen zu diesem verknüpften Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="fb88d-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="fb88d-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen verknüpften Diensten in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="fb88d-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="fb88d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fb88d-112">EXAMPLES</span></span>

### <span data-ttu-id="fb88d-113">Beispiel 1: Informationen zu allen verknüpften Diensten</span><span class="sxs-lookup"><span data-stu-id="fb88d-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

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

<span data-ttu-id="fb88d-114">Dieser Befehl ruft Informationen zu allen verknüpften Diensten in der Daten factory namens WikiADF ab und übergibt dann die verknüpften Dienste mithilfe des Pipelineoperators an das cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="fb88d-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fb88d-115">Auf Windows PowerShell cmdlet werden die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="fb88d-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="fb88d-116">Weitere Informationen erhalten Sie, wenn Sie Get-Help "Format-Liste" eingeben.</span><span class="sxs-lookup"><span data-stu-id="fb88d-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="fb88d-117">Sie können eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="fb88d-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="fb88d-118">Beispiel 2: Informationen zu einem bestimmten verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="fb88d-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="fb88d-119">Dieser Befehl ruft Informationen über den verknüpften Dienst "LinkedServiceCuratedWikiData" in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="fb88d-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="fb88d-120">Beispiel 3: Erhalten von Informationen zu einem bestimmten verknüpften Dienst durch Angeben des Parameters "DataFactory"</span><span class="sxs-lookup"><span data-stu-id="fb88d-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="fb88d-121">Der erste Befehl verwendet das Get-AzDataFactoryV2-Cmdlet, um die Datenfactory namens "ContosoFactory" zu erhalten, und speichert sie dann in der $DataFactory Variable.</span><span class="sxs-lookup"><span data-stu-id="fb88d-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="fb88d-122">Der zweite Befehl ruft Informationen über den verknüpften Dienst für die in $DataFactory gespeicherte Daten factory ab und übergibt diese Informationen dann mithilfe des Pipelineoperators an das cmdlet Format-Table.</span><span class="sxs-lookup"><span data-stu-id="fb88d-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fb88d-123">Das Format-Table formatiert die Ausgabe als Dataset mit den angegebenen Eigenschaften als Datasetspalten.</span><span class="sxs-lookup"><span data-stu-id="fb88d-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="fb88d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb88d-124">PARAMETERS</span></span>

### <span data-ttu-id="fb88d-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb88d-125">-DataFactory</span></span>
<span data-ttu-id="fb88d-126">Gibt ein "PSDataFactory"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fb88d-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="fb88d-127">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="fb88d-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb88d-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fb88d-128">-DataFactoryName</span></span>
<span data-ttu-id="fb88d-129">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="fb88d-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fb88d-130">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="fb88d-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb88d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb88d-131">-DefaultProfile</span></span>
<span data-ttu-id="fb88d-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb88d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb88d-133">-Name</span><span class="sxs-lookup"><span data-stu-id="fb88d-133">-Name</span></span>
<span data-ttu-id="fb88d-134">Gibt den Namen des verknüpften Diensts an, über den Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fb88d-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb88d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb88d-135">-ResourceGroupName</span></span>
<span data-ttu-id="fb88d-136">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fb88d-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fb88d-137">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fb88d-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb88d-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb88d-138">-ResourceId</span></span>
<span data-ttu-id="fb88d-139">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fb88d-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fb88d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb88d-140">CommonParameters</span></span>
<span data-ttu-id="fb88d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb88d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb88d-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb88d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb88d-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fb88d-143">INPUTS</span></span>

### <span data-ttu-id="fb88d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fb88d-144">System.String</span></span>

### <span data-ttu-id="fb88d-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fb88d-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="fb88d-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fb88d-146">OUTPUTS</span></span>

### <span data-ttu-id="fb88d-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="fb88d-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="fb88d-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fb88d-148">NOTES</span></span>
<span data-ttu-id="fb88d-149">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="fb88d-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fb88d-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fb88d-150">RELATED LINKS</span></span>

[<span data-ttu-id="fb88d-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="fb88d-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="fb88d-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="fb88d-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
