---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: a3ee8cdaabfc328574497f27a9b35c93992cb03b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496617"
---
# <span data-ttu-id="43b57-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="43b57-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="43b57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43b57-102">SYNOPSIS</span></span>
<span data-ttu-id="43b57-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="43b57-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b57-104">SYNTAX</span></span>

### <span data-ttu-id="43b57-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="43b57-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43b57-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="43b57-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43b57-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="43b57-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43b57-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43b57-108">DESCRIPTION</span></span>
<span data-ttu-id="43b57-109">Das Get-AzureRmDataFactoryV2IntegrationRuntimeMetric-Cmdlet ruft metrische Daten zur Integrationslaufzeit in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="43b57-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="43b57-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43b57-110">EXAMPLES</span></span>

### <span data-ttu-id="43b57-111">Beispiel 1: Abrufen der Integrationslauf Zeit Metrik</span><span class="sxs-lookup"><span data-stu-id="43b57-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="43b57-112">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2" an.</span><span class="sxs-lookup"><span data-stu-id="43b57-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="43b57-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b57-113">PARAMETERS</span></span>

### <span data-ttu-id="43b57-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="43b57-114">-DataFactoryName</span></span>
<span data-ttu-id="43b57-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="43b57-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b57-116">-DefaultProfile</span></span>
<span data-ttu-id="43b57-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43b57-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b57-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43b57-118">-InputObject</span></span>
<span data-ttu-id="43b57-119">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="43b57-119">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43b57-120">-Name</span><span class="sxs-lookup"><span data-stu-id="43b57-120">-Name</span></span>
<span data-ttu-id="43b57-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="43b57-121">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b57-122">-ResourceGroupName</span></span>
<span data-ttu-id="43b57-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43b57-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b57-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="43b57-124">-ResourceId</span></span>
<span data-ttu-id="43b57-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="43b57-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b57-126">CommonParameters</span></span>
<span data-ttu-id="43b57-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b57-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b57-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b57-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43b57-129">INPUTS</span></span>

### <span data-ttu-id="43b57-130">System. String</span><span class="sxs-lookup"><span data-stu-id="43b57-130">System.String</span></span>
<span data-ttu-id="43b57-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43b57-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="43b57-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43b57-132">OUTPUTS</span></span>

### <span data-ttu-id="43b57-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="43b57-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="43b57-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="43b57-134">NOTES</span></span>

## <span data-ttu-id="43b57-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43b57-135">RELATED LINKS</span></span>

[<span data-ttu-id="43b57-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43b57-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

