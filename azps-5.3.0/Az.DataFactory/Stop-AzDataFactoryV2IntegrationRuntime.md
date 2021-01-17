---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472624"
---
# <span data-ttu-id="d1694-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d1694-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="d1694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1694-102">SYNOPSIS</span></span>
<span data-ttu-id="d1694-103">Beendet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="d1694-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="d1694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1694-104">SYNTAX</span></span>

### <span data-ttu-id="d1694-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1694-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1694-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1694-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1694-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d1694-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1694-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1694-108">DESCRIPTION</span></span>
<span data-ttu-id="d1694-109">Das **Cmdlet "Stop-AzDataFactoryV2IntegrationRuntime"** beendet eine verwaltete dedizierte Integrationslaufzeit im Zustand "Started", die vom cmdlet Start-AzDataFactoryV2IntegrationRuntime wurde.</span><span class="sxs-lookup"><span data-stu-id="d1694-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="d1694-110">Die Ressourcen werden freigegeben, und der Zustand wird auf "Stopped" (Beendet) umgelassen.</span><span class="sxs-lookup"><span data-stu-id="d1694-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="d1694-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d1694-111">EXAMPLES</span></span>

### <span data-ttu-id="d1694-112">Beispiel 1: Beenden einer verwalteten Integrationslaufzeit im Zustand "Gestartet".</span><span class="sxs-lookup"><span data-stu-id="d1694-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="d1694-113">Die verwaltete Integrationslaufzeit "test-reserlved-ir" befindet sich im Zustand "Started".</span><span class="sxs-lookup"><span data-stu-id="d1694-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="d1694-114">Nachdem Sie Stop-AzDataFactoryV2IntegrationRuntime cmdlet ausgeführt haben, werden die Ressourcen freigegeben, und der Zustand wird in "Stopped" (Beendet) transferiert.</span><span class="sxs-lookup"><span data-stu-id="d1694-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="d1694-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1694-115">PARAMETERS</span></span>

### <span data-ttu-id="d1694-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d1694-116">-DataFactoryName</span></span>
<span data-ttu-id="d1694-117">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="d1694-117">The data factory name.</span></span>

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

### <span data-ttu-id="d1694-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1694-118">-DefaultProfile</span></span>
<span data-ttu-id="d1694-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1694-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1694-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d1694-120">-Force</span></span>
<span data-ttu-id="d1694-121">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="d1694-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d1694-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1694-122">-InputObject</span></span>
<span data-ttu-id="d1694-123">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d1694-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="d1694-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d1694-124">-Name</span></span>
<span data-ttu-id="d1694-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="d1694-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="d1694-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1694-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1694-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1694-127">The resource group name.</span></span>

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

### <span data-ttu-id="d1694-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1694-128">-ResourceId</span></span>
<span data-ttu-id="d1694-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d1694-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d1694-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1694-130">-Confirm</span></span>
<span data-ttu-id="d1694-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1694-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1694-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d1694-132">-WhatIf</span></span>
<span data-ttu-id="d1694-133">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1694-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d1694-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1694-134">CommonParameters</span></span>
<span data-ttu-id="d1694-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1694-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1694-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1694-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1694-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d1694-137">INPUTS</span></span>

### <span data-ttu-id="d1694-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d1694-138">System.String</span></span>

### <span data-ttu-id="d1694-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d1694-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d1694-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d1694-140">OUTPUTS</span></span>

### <span data-ttu-id="d1694-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="d1694-141">System.Void</span></span>

## <span data-ttu-id="d1694-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d1694-142">NOTES</span></span>
<span data-ttu-id="d1694-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="d1694-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="d1694-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d1694-144">RELATED LINKS</span></span>

[<span data-ttu-id="d1694-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d1694-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
