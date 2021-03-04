---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 405754afec3ff62eb59d385646df43f699557d18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942867"
---
# <span data-ttu-id="83fa3-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="83fa3-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="83fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="83fa3-103">Beendet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="83fa3-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="83fa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83fa3-104">SYNTAX</span></span>

### <span data-ttu-id="83fa3-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="83fa3-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83fa3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83fa3-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83fa3-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="83fa3-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83fa3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83fa3-108">DESCRIPTION</span></span>
<span data-ttu-id="83fa3-109">Das **Cmdlet Stop-AzDataFactoryV2IntegrationRuntime** beendet eine verwaltete dedizierte Integrations-Runtime im Zustand "Started", die vom cmdlet Start-AzDataFactoryV2IntegrationRuntime wurde.</span><span class="sxs-lookup"><span data-stu-id="83fa3-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="83fa3-110">Die Ressourcen werden freigegeben, und der Zustand wird an "Beendet" überträgt.</span><span class="sxs-lookup"><span data-stu-id="83fa3-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="83fa3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83fa3-111">EXAMPLES</span></span>

### <span data-ttu-id="83fa3-112">Beispiel 1: Beenden einer verwalteten Integrationslaufzeit im Status "Gestartet".</span><span class="sxs-lookup"><span data-stu-id="83fa3-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="83fa3-113">Die verwaltete Integrations-Runtime "test-reserlved-ir" befindet sich im Status "Gestartet".</span><span class="sxs-lookup"><span data-stu-id="83fa3-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="83fa3-114">Nachdem sie Stop-AzDataFactoryV2IntegrationRuntime cmdlet ausgeführt haben, werden die Ressourcen freigegeben und der Zustand an "Beendet" überträgt.</span><span class="sxs-lookup"><span data-stu-id="83fa3-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="83fa3-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="83fa3-115">PARAMETERS</span></span>

### <span data-ttu-id="83fa3-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="83fa3-116">-DataFactoryName</span></span>
<span data-ttu-id="83fa3-117">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="83fa3-117">The data factory name.</span></span>

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

### <span data-ttu-id="83fa3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fa3-118">-DefaultProfile</span></span>
<span data-ttu-id="83fa3-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83fa3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83fa3-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="83fa3-120">-Force</span></span>
<span data-ttu-id="83fa3-121">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="83fa3-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="83fa3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83fa3-122">-InputObject</span></span>
<span data-ttu-id="83fa3-123">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="83fa3-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="83fa3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="83fa3-124">-Name</span></span>
<span data-ttu-id="83fa3-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="83fa3-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="83fa3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83fa3-126">-ResourceGroupName</span></span>
<span data-ttu-id="83fa3-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="83fa3-127">The resource group name.</span></span>

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

### <span data-ttu-id="83fa3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83fa3-128">-ResourceId</span></span>
<span data-ttu-id="83fa3-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="83fa3-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="83fa3-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83fa3-130">-Confirm</span></span>
<span data-ttu-id="83fa3-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83fa3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83fa3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83fa3-132">-WhatIf</span></span>
<span data-ttu-id="83fa3-133">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83fa3-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="83fa3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fa3-134">CommonParameters</span></span>
<span data-ttu-id="83fa3-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83fa3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fa3-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fa3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fa3-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83fa3-137">INPUTS</span></span>

### <span data-ttu-id="83fa3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="83fa3-138">System.String</span></span>

### <span data-ttu-id="83fa3-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="83fa3-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="83fa3-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83fa3-140">OUTPUTS</span></span>

### <span data-ttu-id="83fa3-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="83fa3-141">System.Void</span></span>

## <span data-ttu-id="83fa3-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="83fa3-142">NOTES</span></span>
<span data-ttu-id="83fa3-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="83fa3-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="83fa3-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="83fa3-144">RELATED LINKS</span></span>

[<span data-ttu-id="83fa3-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="83fa3-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
