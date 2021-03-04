---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 12810756f1ebe3e3bf345519d981b660f4c61aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930240"
---
# <span data-ttu-id="9ad9b-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="9ad9b-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="9ad9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ad9b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad9b-103">Ruft Metrikdaten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="9ad9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ad9b-104">SYNTAX</span></span>

### <span data-ttu-id="9ad9b-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ad9b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ad9b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad9b-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad9b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9ad9b-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad9b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ad9b-108">DESCRIPTION</span></span>
<span data-ttu-id="9ad9b-109">Das Get-AzDataFactoryV2IntegrationRuntimeMetric-Cmdlet ruft Metrikdaten zur Integrationslaufzeit in einer Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="9ad9b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ad9b-110">EXAMPLES</span></span>

### <span data-ttu-id="9ad9b-111">Beispiel 1: Get integration runtime metric</span><span class="sxs-lookup"><span data-stu-id="9ad9b-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="9ad9b-112">Dieser Befehl zeigt metrikierte Daten zur Integrations-Runtime mit dem Namen "test-selfhost-ir" im Abonnement für die Ressourcengruppe mit dem Namen "rg-test-dfv2" und die Daten factory mit dem Namen "test-df-eu2" an.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="9ad9b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ad9b-113">PARAMETERS</span></span>

### <span data-ttu-id="9ad9b-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9ad9b-114">-DataFactoryName</span></span>
<span data-ttu-id="9ad9b-115">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-115">The data factory name.</span></span>

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

### <span data-ttu-id="9ad9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad9b-116">-DefaultProfile</span></span>
<span data-ttu-id="9ad9b-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ad9b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ad9b-118">-InputObject</span></span>
<span data-ttu-id="9ad9b-119">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="9ad9b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9ad9b-120">-Name</span></span>
<span data-ttu-id="9ad9b-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="9ad9b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad9b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ad9b-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-123">The resource group name.</span></span>

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

### <span data-ttu-id="9ad9b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad9b-124">-ResourceId</span></span>
<span data-ttu-id="9ad9b-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9ad9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad9b-126">CommonParameters</span></span>
<span data-ttu-id="9ad9b-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad9b-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad9b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad9b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ad9b-129">INPUTS</span></span>

### <span data-ttu-id="9ad9b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9ad9b-130">System.String</span></span>

### <span data-ttu-id="9ad9b-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9ad9b-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9ad9b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ad9b-132">OUTPUTS</span></span>

### <span data-ttu-id="9ad9b-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="9ad9b-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="9ad9b-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ad9b-134">NOTES</span></span>

## <span data-ttu-id="9ad9b-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ad9b-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ad9b-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9ad9b-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

