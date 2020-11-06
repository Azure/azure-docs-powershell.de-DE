---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8068a560954d94a134205d5e67eab19e641bed74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499626"
---
# <span data-ttu-id="2ea7e-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2ea7e-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="2ea7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ea7e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea7e-103">Ruft Informationen zu verknüpften Diensten in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ea7e-104">SYNTAX</span></span>

### <span data-ttu-id="2ea7e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ea7e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ea7e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2ea7e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ea7e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ea7e-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ea7e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ea7e-108">DESCRIPTION</span></span>
<span data-ttu-id="2ea7e-109">Das Get-AzureRmDataFactoryV2LinkedService-Cmdlet ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-109">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="2ea7e-110">Wenn Sie den Namen eines verknüpften Diensts angeben, ruft dieses Cmdlet Informationen zu diesem verknüpften Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="2ea7e-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen verknüpften Diensten in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="2ea7e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ea7e-112">EXAMPLES</span></span>

### <span data-ttu-id="2ea7e-113">Beispiel 1: Abrufen von Informationen zu allen verknüpften Diensten</span><span class="sxs-lookup"><span data-stu-id="2ea7e-113">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="2ea7e-114">Dieser Befehl ruft Informationen zu allen verknüpften Diensten in der Data Factory mit dem Namen WikiADF ab und übergibt dann die verknüpften Dienste mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ea7e-115">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="2ea7e-116">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="2ea7e-117">Sie können eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="2ea7e-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="2ea7e-118">Beispiel 2: Abrufen von Informationen zu einem bestimmten verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="2ea7e-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="2ea7e-119">Dieser Befehl ruft Informationen zum verknüpften Dienst mit dem Namen LinkedServiceCuratedWikiData in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="2ea7e-120">Beispiel 3: Abrufen von Informationen zu einem bestimmten verknüpften Dienst durch Angabe des DataFactory-Parameters</span><span class="sxs-lookup"><span data-stu-id="2ea7e-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="2ea7e-121">Der erste Befehl verwendet das Get-AzureRmDataFactoryV2-Cmdlet, um die Data Factory mit dem Namen ContosoFactory abzurufen, und speichert Sie dann in der $datafactory-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-121">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="2ea7e-122">Der zweite Befehl ruft Informationen zum verknüpften Dienst für die in $DataFactory gespeicherte Daten Factory ab und übergibt diese Informationen dann mithilfe des Pipelineoperators an das Format-Table-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ea7e-123">Das Format-Table-Cmdlet formatiert die Ausgabe als DataSet mit den angegebenen Eigenschaften als DataSet-Spalten.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="2ea7e-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ea7e-124">PARAMETERS</span></span>

### <span data-ttu-id="2ea7e-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea7e-125">-DataFactory</span></span>
<span data-ttu-id="2ea7e-126">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="2ea7e-127">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ea7e-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2ea7e-128">-DataFactoryName</span></span>
<span data-ttu-id="2ea7e-129">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2ea7e-130">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ea7e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea7e-131">-DefaultProfile</span></span>
<span data-ttu-id="2ea7e-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea7e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="2ea7e-133">-Name</span></span>
<span data-ttu-id="2ea7e-134">Gibt den Namen des verknüpften Diensts an, für den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="2ea7e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea7e-135">-ResourceGroupName</span></span>
<span data-ttu-id="2ea7e-136">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2ea7e-137">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ea7e-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2ea7e-138">-ResourceId</span></span>
<span data-ttu-id="2ea7e-139">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2ea7e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea7e-140">CommonParameters</span></span>
<span data-ttu-id="2ea7e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea7e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea7e-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea7e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea7e-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ea7e-143">INPUTS</span></span>

### <span data-ttu-id="2ea7e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea7e-144">System.String</span></span>

### <span data-ttu-id="2ea7e-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2ea7e-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="2ea7e-146">Parameter: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ea7e-146">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="2ea7e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ea7e-147">OUTPUTS</span></span>

### <span data-ttu-id="2ea7e-148">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="2ea7e-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="2ea7e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ea7e-149">NOTES</span></span>
<span data-ttu-id="2ea7e-150">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="2ea7e-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2ea7e-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ea7e-151">RELATED LINKS</span></span>

[<span data-ttu-id="2ea7e-152">Satz-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2ea7e-152">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="2ea7e-153">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2ea7e-153">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
