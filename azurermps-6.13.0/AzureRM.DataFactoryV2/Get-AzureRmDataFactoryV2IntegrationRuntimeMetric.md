---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 07c5b03b3d5717115238e3cd66b9f80925b51537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499630"
---
# <span data-ttu-id="910be-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="910be-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="910be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="910be-102">SYNOPSIS</span></span>
<span data-ttu-id="910be-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="910be-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="910be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="910be-104">SYNTAX</span></span>

### <span data-ttu-id="910be-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="910be-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="910be-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="910be-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="910be-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="910be-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="910be-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="910be-108">DESCRIPTION</span></span>
<span data-ttu-id="910be-109">Das Get-AzureRmDataFactoryV2IntegrationRuntimeMetric-Cmdlet ruft metrische Daten zur Integrationslaufzeit in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="910be-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="910be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="910be-110">EXAMPLES</span></span>

### <span data-ttu-id="910be-111">Beispiel 1: Abrufen der Integrationslauf Zeit Metrik</span><span class="sxs-lookup"><span data-stu-id="910be-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="910be-112">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="910be-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="910be-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="910be-113">PARAMETERS</span></span>

### <span data-ttu-id="910be-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="910be-114">-DataFactoryName</span></span>
<span data-ttu-id="910be-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="910be-115">The data factory name.</span></span>

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

### <span data-ttu-id="910be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910be-116">-DefaultProfile</span></span>
<span data-ttu-id="910be-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="910be-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="910be-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="910be-118">-InputObject</span></span>
<span data-ttu-id="910be-119">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="910be-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="910be-120">-Name</span><span class="sxs-lookup"><span data-stu-id="910be-120">-Name</span></span>
<span data-ttu-id="910be-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="910be-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="910be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="910be-122">-ResourceGroupName</span></span>
<span data-ttu-id="910be-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="910be-123">The resource group name.</span></span>

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

### <span data-ttu-id="910be-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="910be-124">-ResourceId</span></span>
<span data-ttu-id="910be-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="910be-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="910be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910be-126">CommonParameters</span></span>
<span data-ttu-id="910be-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="910be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910be-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="910be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910be-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="910be-129">INPUTS</span></span>

### <span data-ttu-id="910be-130">System. String</span><span class="sxs-lookup"><span data-stu-id="910be-130">System.String</span></span>

### <span data-ttu-id="910be-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="910be-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="910be-132">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="910be-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="910be-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="910be-133">OUTPUTS</span></span>

### <span data-ttu-id="910be-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="910be-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="910be-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="910be-135">NOTES</span></span>

## <span data-ttu-id="910be-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="910be-136">RELATED LINKS</span></span>

[<span data-ttu-id="910be-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="910be-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

