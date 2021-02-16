---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153465"
---
# <span data-ttu-id="e5e4d-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e5e4d-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e5e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e4d-103">Startet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="e5e4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5e4d-104">SYNTAX</span></span>

### <span data-ttu-id="e5e4d-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5e4d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e4d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e4d-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e4d-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e5e4d-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e4d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5e4d-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e4d-109">Das **Cmdlet "Start-AzDataFactoryV2IntegrationRuntime"** startet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="e5e4d-110">Die Ressource wird bereitgestellt, und nach dem Vorgang ist der Zustand "Started".</span><span class="sxs-lookup"><span data-stu-id="e5e4d-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="e5e4d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5e4d-111">EXAMPLES</span></span>

### <span data-ttu-id="e5e4d-112">Beispiel 1: Starten einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="e5e4d-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

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
    PublicIPs                    : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="e5e4d-113">Dieses Cmdlet startet eine verwaltete dedizierte Integrationslaufzeit mit dem Namen "test-dedicated-ir".</span><span class="sxs-lookup"><span data-stu-id="e5e4d-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="e5e4d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5e4d-114">PARAMETERS</span></span>

### <span data-ttu-id="e5e4d-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e5e4d-115">-DataFactoryName</span></span>
<span data-ttu-id="e5e4d-116">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-116">The data factory name.</span></span>

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

### <span data-ttu-id="e5e4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e4d-117">-DefaultProfile</span></span>
<span data-ttu-id="e5e4d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5e4d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e5e4d-119">-Force</span></span>
<span data-ttu-id="e5e4d-120">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e4d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e4d-121">-InputObject</span></span>
<span data-ttu-id="e5e4d-122">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="e5e4d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e5e4d-123">-Name</span></span>
<span data-ttu-id="e5e4d-124">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="e5e4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5e4d-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-126">The resource group name.</span></span>

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

### <span data-ttu-id="e5e4d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e4d-127">-ResourceId</span></span>
<span data-ttu-id="e5e4d-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e5e4d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5e4d-129">-Confirm</span></span>
<span data-ttu-id="e5e4d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e4d-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e5e4d-131">-WhatIf</span></span>
<span data-ttu-id="e5e4d-132">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e4d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e4d-133">CommonParameters</span></span>
<span data-ttu-id="e5e4d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e4d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e4d-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e4d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e4d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5e4d-136">INPUTS</span></span>

### <span data-ttu-id="e5e4d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e5e4d-137">System.String</span></span>

### <span data-ttu-id="e5e4d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e5e4d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e5e4d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5e4d-139">OUTPUTS</span></span>

### <span data-ttu-id="e5e4d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="e5e4d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="e5e4d-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e5e4d-141">NOTES</span></span>

## <span data-ttu-id="e5e4d-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e5e4d-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5e4d-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e5e4d-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
