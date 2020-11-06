---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505098"
---
# <span data-ttu-id="0c6c5-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0c6c5-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="0c6c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6c5-103">Ruft Schlüssel für eine selbst gehostete Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c6c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c6c5-104">SYNTAX</span></span>

### <span data-ttu-id="0c6c5-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c6c5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="0c6c5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c6c5-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="0c6c5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0c6c5-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="0c6c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c6c5-108">DESCRIPTION</span></span>
<span data-ttu-id="0c6c5-109">Abrufen von Schlüsseln für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="0c6c5-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="0c6c5-110">Die Schlüssel werden zum Registrieren eines Integrationslauf Zeit Knotens verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="0c6c5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c6c5-111">EXAMPLES</span></span>

### <span data-ttu-id="0c6c5-112">Beispiel 1: Abrufen von Integrationslauf Zeit Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="0c6c5-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="0c6c5-113">Das Cmdlet ruft Schlüssel für eine Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" ab.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0c6c5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c6c5-114">PARAMETERS</span></span>

### <span data-ttu-id="0c6c5-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0c6c5-115">-DataFactoryName</span></span>
<span data-ttu-id="0c6c5-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-116">The data factory name.</span></span>

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

### <span data-ttu-id="0c6c5-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0c6c5-117">-InputObject</span></span>
<span data-ttu-id="0c6c5-118">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="0c6c5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0c6c5-119">-Name</span></span>
<span data-ttu-id="0c6c5-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="0c6c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c6c5-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-122">The resource group name.</span></span>

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

### <span data-ttu-id="0c6c5-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0c6c5-123">-ResourceId</span></span>
<span data-ttu-id="0c6c5-124">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0c6c5-124">The Azure resource ID.</span></span>

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

## <span data-ttu-id="0c6c5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c6c5-125">INPUTS</span></span>

### <span data-ttu-id="0c6c5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0c6c5-126">System.String</span></span>
<span data-ttu-id="0c6c5-127">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0c6c5-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="0c6c5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c6c5-128">OUTPUTS</span></span>

### <span data-ttu-id="0c6c5-129">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="0c6c5-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="0c6c5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c6c5-130">NOTES</span></span>

## <span data-ttu-id="0c6c5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c6c5-131">RELATED LINKS</span></span>
[<span data-ttu-id="0c6c5-132">Neu – AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0c6c5-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
