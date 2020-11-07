---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 2b5f01047bf0b86fc885a01f0c58a9ab094f7698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665391"
---
# <span data-ttu-id="7a219-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7a219-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="7a219-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a219-102">SYNOPSIS</span></span>
<span data-ttu-id="7a219-103">Startet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="7a219-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a219-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a219-104">SYNTAX</span></span>

### <span data-ttu-id="7a219-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a219-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7a219-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a219-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7a219-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7a219-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="7a219-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a219-108">DESCRIPTION</span></span>
<span data-ttu-id="7a219-109">Das Cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** startet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="7a219-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="7a219-110">Die Ressource wird bereitgestellt, und nach dem Vorgang wird der Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="7a219-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="7a219-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a219-111">EXAMPLES</span></span>

### <span data-ttu-id="7a219-112">Beispiel 1: Starten einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="7a219-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="7a219-113">Mit diesem Cmdlet wird eine verwaltete dedizierte Integrationslaufzeit mit dem Namen "Test-dediziert-IR" gestartet.</span><span class="sxs-lookup"><span data-stu-id="7a219-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="7a219-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a219-114">PARAMETERS</span></span>

### <span data-ttu-id="7a219-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a219-115">-Confirm</span></span>
<span data-ttu-id="7a219-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a219-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a219-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7a219-117">-DataFactoryName</span></span>
<span data-ttu-id="7a219-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="7a219-118">The data factory name.</span></span>

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

### <span data-ttu-id="7a219-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7a219-119">-Force</span></span>
<span data-ttu-id="7a219-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="7a219-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a219-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a219-121">-InputObject</span></span>
<span data-ttu-id="7a219-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="7a219-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="7a219-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7a219-123">-Name</span></span>
<span data-ttu-id="7a219-124">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="7a219-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="7a219-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a219-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a219-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a219-126">The resource group name.</span></span>

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

### <span data-ttu-id="7a219-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7a219-127">-ResourceId</span></span>
<span data-ttu-id="7a219-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7a219-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7a219-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a219-129">-WhatIf</span></span>
<span data-ttu-id="7a219-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a219-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="7a219-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a219-131">INPUTS</span></span>

### <span data-ttu-id="7a219-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7a219-132">System.String</span></span>
<span data-ttu-id="7a219-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7a219-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7a219-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a219-134">OUTPUTS</span></span>

### <span data-ttu-id="7a219-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="7a219-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="7a219-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a219-136">NOTES</span></span>

## <span data-ttu-id="7a219-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a219-137">RELATED LINKS</span></span>
[<span data-ttu-id="7a219-138">Stopp-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7a219-138">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
