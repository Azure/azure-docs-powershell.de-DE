---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472680"
---
# <span data-ttu-id="2a5bb-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2a5bb-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="2a5bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5bb-103">Ruft Schlüssel für eine selbst gehostete Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="2a5bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a5bb-104">SYNTAX</span></span>

### <span data-ttu-id="2a5bb-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a5bb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a5bb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a5bb-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a5bb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2a5bb-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a5bb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a5bb-108">DESCRIPTION</span></span>
<span data-ttu-id="2a5bb-109">Hier erhalten Sie Schlüssel für eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="2a5bb-110">Die Schlüssel werden zum Registrieren eines Integrationslaufzeitknotens verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="2a5bb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a5bb-111">EXAMPLES</span></span>

### <span data-ttu-id="2a5bb-112">Beispiel 1: Erhalten von Integrations-Runtime-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="2a5bb-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="2a5bb-113">Das Cmdlet ruft Schlüssel für eine Integrationslaufzeit mit dem Namen "test-selfhost-ir" ab.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2a5bb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a5bb-114">PARAMETERS</span></span>

### <span data-ttu-id="2a5bb-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2a5bb-115">-DataFactoryName</span></span>
<span data-ttu-id="2a5bb-116">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-116">The data factory name.</span></span>

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

### <span data-ttu-id="2a5bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5bb-117">-DefaultProfile</span></span>
<span data-ttu-id="2a5bb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a5bb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a5bb-119">-InputObject</span></span>
<span data-ttu-id="2a5bb-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="2a5bb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2a5bb-121">-Name</span></span>
<span data-ttu-id="2a5bb-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="2a5bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a5bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a5bb-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-124">The resource group name.</span></span>

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

### <span data-ttu-id="2a5bb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a5bb-125">-ResourceId</span></span>
<span data-ttu-id="2a5bb-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2a5bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5bb-127">CommonParameters</span></span>
<span data-ttu-id="2a5bb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a5bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5bb-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a5bb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5bb-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a5bb-130">INPUTS</span></span>

### <span data-ttu-id="2a5bb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2a5bb-131">System.String</span></span>

### <span data-ttu-id="2a5bb-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2a5bb-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2a5bb-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a5bb-133">OUTPUTS</span></span>

### <span data-ttu-id="2a5bb-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="2a5bb-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="2a5bb-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a5bb-135">NOTES</span></span>

## <span data-ttu-id="2a5bb-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a5bb-136">RELATED LINKS</span></span>

[<span data-ttu-id="2a5bb-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2a5bb-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
