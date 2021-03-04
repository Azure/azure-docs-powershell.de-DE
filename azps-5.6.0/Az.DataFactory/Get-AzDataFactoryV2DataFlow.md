---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 4838ba48d12fa3a4b1fd7d129e63e0a643357a78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930259"
---
# <span data-ttu-id="8923d-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="8923d-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="8923d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8923d-102">SYNOPSIS</span></span>
<span data-ttu-id="8923d-103">Ruft Informationen zu Datenflüssen in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="8923d-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="8923d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8923d-104">SYNTAX</span></span>

### <span data-ttu-id="8923d-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8923d-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8923d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8923d-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8923d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8923d-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8923d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8923d-108">DESCRIPTION</span></span>
<span data-ttu-id="8923d-109">Das Get-AzDataFactoryV2DataFlow-Cmdlet ruft Informationen zu Datenflüssen in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="8923d-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="8923d-110">Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.</span><span class="sxs-lookup"><span data-stu-id="8923d-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="8923d-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenflüssen in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="8923d-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="8923d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8923d-112">EXAMPLES</span></span>
### <span data-ttu-id="8923d-113">Beispiel 1: Informationen zu allen Datenflüssen</span><span class="sxs-lookup"><span data-stu-id="8923d-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="8923d-114">Dieser Befehl ruft Informationen zu allen Datenflüssen in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="8923d-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8923d-115">Beispiel 2: Informationen zu einem bestimmten Datenfluss</span><span class="sxs-lookup"><span data-stu-id="8923d-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="8923d-116">Dieser Befehl ruft Informationen zum Datenfluss namens "Dataflow1" in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="8923d-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="8923d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8923d-117">PARAMETERS</span></span>

### <span data-ttu-id="8923d-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8923d-118">-DataFactory</span></span>
<span data-ttu-id="8923d-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8923d-119">The data factory object.</span></span>

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

### <span data-ttu-id="8923d-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8923d-120">-DataFactoryName</span></span>
<span data-ttu-id="8923d-121">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="8923d-121">The data factory name.</span></span>

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

### <span data-ttu-id="8923d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8923d-122">-DefaultProfile</span></span>
<span data-ttu-id="8923d-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8923d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8923d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8923d-124">-Name</span></span>
<span data-ttu-id="8923d-125">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="8923d-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8923d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8923d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8923d-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8923d-127">The resource group name.</span></span>

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

### <span data-ttu-id="8923d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8923d-128">-ResourceId</span></span>
<span data-ttu-id="8923d-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8923d-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8923d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8923d-130">CommonParameters</span></span>
<span data-ttu-id="8923d-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8923d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8923d-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8923d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8923d-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8923d-133">INPUTS</span></span>

### <span data-ttu-id="8923d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8923d-134">System.String</span></span>

### <span data-ttu-id="8923d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8923d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8923d-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8923d-136">OUTPUTS</span></span>

### <span data-ttu-id="8923d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="8923d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="8923d-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8923d-138">NOTES</span></span>
<span data-ttu-id="8923d-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="8923d-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8923d-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8923d-140">RELATED LINKS</span></span>

[<span data-ttu-id="8923d-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8923d-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="8923d-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8923d-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)