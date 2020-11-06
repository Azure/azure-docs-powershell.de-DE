---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7034e17e119acb1077cf17dca85ded8a40cb2e2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497645"
---
# <span data-ttu-id="56b05-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="56b05-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="56b05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56b05-102">SYNOPSIS</span></span>
<span data-ttu-id="56b05-103">Ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="56b05-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56b05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56b05-104">SYNTAX</span></span>

### <span data-ttu-id="56b05-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="56b05-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56b05-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="56b05-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b05-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56b05-107">DESCRIPTION</span></span>
<span data-ttu-id="56b05-108">Das Cmdlet " **Get-AzureRmDataFactoryLinkedService** " Ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="56b05-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="56b05-109">Wenn Sie den Namen eines verknüpften Diensts angeben, ruft dieses Cmdlet Informationen zu diesem verknüpften Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="56b05-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="56b05-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen verknüpften Diensten in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="56b05-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="56b05-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56b05-111">EXAMPLES</span></span>

### <span data-ttu-id="56b05-112">Beispiel 1: Abrufen von Informationen zu allen verknüpften Diensten</span><span class="sxs-lookup"><span data-stu-id="56b05-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="56b05-113">Dieser Befehl ruft Informationen zu allen verknüpften Diensten in der Data Factory mit dem Namen WikiADF ab und übergibt dann die verknüpften Dienste mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b05-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="56b05-114">Dieses Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="56b05-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="56b05-115">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="56b05-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="56b05-116">Beispiel 2: Abrufen von Informationen zu einem bestimmten verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="56b05-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="56b05-117">Dieser Befehl ruft Informationen zum verknüpften Dienst mit dem Namen HDILinkedService in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="56b05-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="56b05-118">Beispiel 3: Abrufen von Informationen zu einem bestimmten verknüpften Dienst durch Angabe des DataFactory-Parameters</span><span class="sxs-lookup"><span data-stu-id="56b05-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="56b05-119">Der erste Befehl verwendet das Get-AzureRmDataFactory-Cmdlet, um die Data Factory mit dem Namen ContosoFactory abzurufen, und speichert Sie dann in der $datafactory-Variablen.</span><span class="sxs-lookup"><span data-stu-id="56b05-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="56b05-120">Der zweite Befehl ruft Informationen zum verknüpften Dienst für die in $DataFactory gespeicherte Daten Factory ab und übergibt diese Informationen dann mithilfe des Pipelineoperators an das Format-Table-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b05-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="56b05-121">**Format-Table** formatiert die Ausgabe als DataSet mit den angegebenen Eigenschaften als DataSet-Spalten.</span><span class="sxs-lookup"><span data-stu-id="56b05-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="56b05-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="56b05-122">PARAMETERS</span></span>

### <span data-ttu-id="56b05-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="56b05-123">-DataFactory</span></span>
<span data-ttu-id="56b05-124">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="56b05-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="56b05-125">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="56b05-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b05-126">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="56b05-126">-DataFactoryName</span></span>
<span data-ttu-id="56b05-127">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="56b05-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="56b05-128">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="56b05-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="56b05-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b05-129">-DefaultProfile</span></span>
<span data-ttu-id="56b05-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="56b05-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56b05-131">-Name</span><span class="sxs-lookup"><span data-stu-id="56b05-131">-Name</span></span>
<span data-ttu-id="56b05-132">Gibt den Namen des verknüpften Diensts an, für den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="56b05-132">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b05-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b05-133">-ResourceGroupName</span></span>
<span data-ttu-id="56b05-134">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="56b05-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="56b05-135">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="56b05-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="56b05-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b05-136">CommonParameters</span></span>
<span data-ttu-id="56b05-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b05-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b05-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b05-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b05-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56b05-139">INPUTS</span></span>

### <span data-ttu-id="56b05-140">Keine</span><span class="sxs-lookup"><span data-stu-id="56b05-140">None</span></span>
<span data-ttu-id="56b05-141">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="56b05-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56b05-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56b05-142">OUTPUTS</span></span>

### <span data-ttu-id="56b05-143">System. Collections. Generic. List ' 1 [[Microsoft. WindowsAzure. Commands. Utilities. PSLinkedService, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. Commands. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="56b05-143">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="56b05-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="56b05-144">NOTES</span></span>
* <span data-ttu-id="56b05-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="56b05-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="56b05-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56b05-146">RELATED LINKS</span></span>

[<span data-ttu-id="56b05-147">Neu – AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="56b05-147">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="56b05-148">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="56b05-148">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


