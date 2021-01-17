---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470585"
---
# <span data-ttu-id="45186-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="45186-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="45186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45186-102">SYNOPSIS</span></span>
<span data-ttu-id="45186-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="45186-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="45186-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45186-104">SYNTAX</span></span>

### <span data-ttu-id="45186-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="45186-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45186-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="45186-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45186-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="45186-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45186-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45186-108">DESCRIPTION</span></span>
<span data-ttu-id="45186-109">Das Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet ruft metrische Daten zur Integrationslaufzeit in einer Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="45186-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="45186-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45186-110">EXAMPLES</span></span>

### <span data-ttu-id="45186-111">Beispiel 1: Get integration runtime metric</span><span class="sxs-lookup"><span data-stu-id="45186-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="45186-112">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "test-selfhost-ir" im Abonnement für die Ressourcengruppe mit dem Namen "rg-test-dfv2" und der Daten factory mit dem Namen "test-df-eu2" an.</span><span class="sxs-lookup"><span data-stu-id="45186-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="45186-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45186-113">PARAMETERS</span></span>

### <span data-ttu-id="45186-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="45186-114">-DataFactoryName</span></span>
<span data-ttu-id="45186-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="45186-115">The data factory name.</span></span>

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

### <span data-ttu-id="45186-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45186-116">-DefaultProfile</span></span>
<span data-ttu-id="45186-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45186-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45186-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45186-118">-InputObject</span></span>
<span data-ttu-id="45186-119">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="45186-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="45186-120">-Name</span><span class="sxs-lookup"><span data-stu-id="45186-120">-Name</span></span>
<span data-ttu-id="45186-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="45186-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="45186-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45186-122">-ResourceGroupName</span></span>
<span data-ttu-id="45186-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="45186-123">The resource group name.</span></span>

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

### <span data-ttu-id="45186-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45186-124">-ResourceId</span></span>
<span data-ttu-id="45186-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="45186-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="45186-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45186-126">CommonParameters</span></span>
<span data-ttu-id="45186-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45186-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45186-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45186-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45186-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45186-129">INPUTS</span></span>

### <span data-ttu-id="45186-130">System.String</span><span class="sxs-lookup"><span data-stu-id="45186-130">System.String</span></span>

### <span data-ttu-id="45186-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="45186-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="45186-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45186-132">OUTPUTS</span></span>

### <span data-ttu-id="45186-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="45186-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="45186-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45186-134">NOTES</span></span>

## <span data-ttu-id="45186-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45186-135">RELATED LINKS</span></span>

[<span data-ttu-id="45186-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="45186-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

