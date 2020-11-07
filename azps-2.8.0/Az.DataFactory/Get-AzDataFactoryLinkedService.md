---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: a54cdb0a30d0249ccb8fd177646e218e0fe604c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651780"
---
# <span data-ttu-id="ff4ba-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ff4ba-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="ff4ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4ba-103">Ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="ff4ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff4ba-104">SYNTAX</span></span>

### <span data-ttu-id="ff4ba-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff4ba-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff4ba-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ff4ba-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff4ba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff4ba-107">DESCRIPTION</span></span>
<span data-ttu-id="ff4ba-108">Das Cmdlet " **Get-AzDataFactoryLinkedService** " Ruft Informationen zu verknüpften Diensten in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="ff4ba-109">Wenn Sie den Namen eines verknüpften Diensts angeben, ruft dieses Cmdlet Informationen zu diesem verknüpften Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="ff4ba-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen verknüpften Diensten in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="ff4ba-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff4ba-111">EXAMPLES</span></span>

### <span data-ttu-id="ff4ba-112">Beispiel 1: Abrufen von Informationen zu allen verknüpften Diensten</span><span class="sxs-lookup"><span data-stu-id="ff4ba-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="ff4ba-113">Dieser Befehl ruft Informationen zu allen verknüpften Diensten in der Data Factory mit dem Namen WikiADF ab und übergibt dann die verknüpften Dienste mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff4ba-114">Dieses Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="ff4ba-115">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="ff4ba-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="ff4ba-116">Beispiel 2: Abrufen von Informationen zu einem bestimmten verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="ff4ba-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="ff4ba-117">Dieser Befehl ruft Informationen zum verknüpften Dienst mit dem Namen HDILinkedService in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="ff4ba-118">Beispiel 3: Abrufen von Informationen zu einem bestimmten verknüpften Dienst durch Angabe des DataFactory-Parameters</span><span class="sxs-lookup"><span data-stu-id="ff4ba-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="ff4ba-119">Der erste Befehl verwendet das Get-AzDataFactory-Cmdlet, um die Data Factory mit dem Namen ContosoFactory abzurufen, und speichert Sie dann in der $datafactory-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="ff4ba-120">Der zweite Befehl ruft Informationen zum verknüpften Dienst für die in $DataFactory gespeicherte Daten Factory ab und übergibt diese Informationen dann mithilfe des Pipelineoperators an das Format-Table-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff4ba-121">**Format-Table** formatiert die Ausgabe als DataSet mit den angegebenen Eigenschaften als DataSet-Spalten.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="ff4ba-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff4ba-122">PARAMETERS</span></span>

### <span data-ttu-id="ff4ba-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff4ba-123">-DataFactory</span></span>
<span data-ttu-id="ff4ba-124">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ff4ba-125">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ba-126">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ff4ba-126">-DataFactoryName</span></span>
<span data-ttu-id="ff4ba-127">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ff4ba-128">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff4ba-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4ba-129">-DefaultProfile</span></span>
<span data-ttu-id="ff4ba-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ff4ba-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff4ba-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ff4ba-131">-Name</span></span>
<span data-ttu-id="ff4ba-132">Gibt den Namen des verknüpften Diensts an, für den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-132">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ba-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4ba-133">-ResourceGroupName</span></span>
<span data-ttu-id="ff4ba-134">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ff4ba-135">Dieses Cmdlet ruft verknüpfte Dienste ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff4ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4ba-136">CommonParameters</span></span>
<span data-ttu-id="ff4ba-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4ba-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4ba-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4ba-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff4ba-139">INPUTS</span></span>

### <span data-ttu-id="ff4ba-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff4ba-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ff4ba-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ff4ba-141">System.String</span></span>

## <span data-ttu-id="ff4ba-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff4ba-142">OUTPUTS</span></span>

### <span data-ttu-id="ff4ba-143">Microsoft. Azure. Commands. datafactoring. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ff4ba-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="ff4ba-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff4ba-144">NOTES</span></span>
* <span data-ttu-id="ff4ba-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="ff4ba-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff4ba-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff4ba-146">RELATED LINKS</span></span>

[<span data-ttu-id="ff4ba-147">Neu – AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ff4ba-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="ff4ba-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ff4ba-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


