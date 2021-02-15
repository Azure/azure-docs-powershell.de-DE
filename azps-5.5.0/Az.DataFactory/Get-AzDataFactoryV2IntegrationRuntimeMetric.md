---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174681"
---
# <span data-ttu-id="5c284-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="5c284-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="5c284-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c284-102">SYNOPSIS</span></span>
<span data-ttu-id="5c284-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="5c284-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="5c284-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c284-104">SYNTAX</span></span>

### <span data-ttu-id="5c284-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c284-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c284-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c284-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c284-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5c284-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c284-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c284-108">DESCRIPTION</span></span>
<span data-ttu-id="5c284-109">Das Get-AzDataFactoryV2IntegrationRuntimeMetric Cmdlet ruft metrische Daten zur Integrationslaufzeit in einer Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="5c284-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="5c284-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c284-110">EXAMPLES</span></span>

### <span data-ttu-id="5c284-111">Beispiel 1: Get integration runtime metric</span><span class="sxs-lookup"><span data-stu-id="5c284-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="5c284-112">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "test-selfhost-ir" im Abonnement für die Ressourcengruppe mit dem Namen "rg-test-dfv2" und der Daten factory mit dem Namen "test-df-eu2" an.</span><span class="sxs-lookup"><span data-stu-id="5c284-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="5c284-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c284-113">PARAMETERS</span></span>

### <span data-ttu-id="5c284-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5c284-114">-DataFactoryName</span></span>
<span data-ttu-id="5c284-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="5c284-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c284-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c284-116">-DefaultProfile</span></span>
<span data-ttu-id="5c284-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c284-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c284-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c284-118">-InputObject</span></span>
<span data-ttu-id="5c284-119">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c284-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c284-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5c284-120">-Name</span></span>
<span data-ttu-id="5c284-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="5c284-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c284-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c284-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c284-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5c284-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c284-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c284-124">-ResourceId</span></span>
<span data-ttu-id="5c284-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5c284-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c284-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c284-126">CommonParameters</span></span>
<span data-ttu-id="5c284-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c284-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c284-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c284-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c284-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c284-129">INPUTS</span></span>

### <span data-ttu-id="5c284-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5c284-130">System.String</span></span>

### <span data-ttu-id="5c284-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5c284-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5c284-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c284-132">OUTPUTS</span></span>

### <span data-ttu-id="5c284-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="5c284-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="5c284-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c284-134">NOTES</span></span>

## <span data-ttu-id="5c284-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c284-135">RELATED LINKS</span></span>

[<span data-ttu-id="5c284-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5c284-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

