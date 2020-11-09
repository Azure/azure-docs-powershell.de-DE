---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298192"
---
# <span data-ttu-id="3764c-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3764c-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3764c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3764c-102">SYNOPSIS</span></span>
<span data-ttu-id="3764c-103">Beendet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3764c-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="3764c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3764c-104">SYNTAX</span></span>

### <span data-ttu-id="3764c-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3764c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3764c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3764c-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3764c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3764c-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3764c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3764c-108">DESCRIPTION</span></span>
<span data-ttu-id="3764c-109">Das Cmdlet **Stop-AzDataFactoryV2IntegrationRuntime** beendet eine verwaltete dedizierte Integrationslaufzeit im Zustand "Started", die vom Cmdlet Start-AzDataFactoryV2IntegrationRuntime gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="3764c-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="3764c-110">Die Ressourcen werden freigegeben, und der Status wird an "gestoppt" übertragen.</span><span class="sxs-lookup"><span data-stu-id="3764c-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="3764c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3764c-111">EXAMPLES</span></span>

### <span data-ttu-id="3764c-112">Beispiel 1: Beenden einer verwalteten Integrationslaufzeit, die sich im Zustand "gestartet" befindet.</span><span class="sxs-lookup"><span data-stu-id="3764c-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="3764c-113">Die verwaltete Integrationslaufzeit "Test-reserlved-IR" befindet sich im Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="3764c-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="3764c-114">Nach dem Ausführen Stop-AzDataFactoryV2IntegrationRuntime-Cmdlets werden die Ressourcen freigegeben, und der Zustand wird an "stopped" übertragen.</span><span class="sxs-lookup"><span data-stu-id="3764c-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="3764c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3764c-115">PARAMETERS</span></span>

### <span data-ttu-id="3764c-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3764c-116">-DataFactoryName</span></span>
<span data-ttu-id="3764c-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="3764c-117">The data factory name.</span></span>

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

### <span data-ttu-id="3764c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3764c-118">-DefaultProfile</span></span>
<span data-ttu-id="3764c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3764c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3764c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3764c-120">-Force</span></span>
<span data-ttu-id="3764c-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="3764c-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3764c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3764c-122">-InputObject</span></span>
<span data-ttu-id="3764c-123">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="3764c-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="3764c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3764c-124">-Name</span></span>
<span data-ttu-id="3764c-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3764c-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="3764c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3764c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3764c-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3764c-127">The resource group name.</span></span>

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

### <span data-ttu-id="3764c-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3764c-128">-ResourceId</span></span>
<span data-ttu-id="3764c-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3764c-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3764c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3764c-130">-Confirm</span></span>
<span data-ttu-id="3764c-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3764c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3764c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3764c-132">-WhatIf</span></span>
<span data-ttu-id="3764c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3764c-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3764c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3764c-134">CommonParameters</span></span>
<span data-ttu-id="3764c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3764c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3764c-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3764c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3764c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3764c-137">INPUTS</span></span>

### <span data-ttu-id="3764c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3764c-138">System.String</span></span>

### <span data-ttu-id="3764c-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3764c-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3764c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3764c-140">OUTPUTS</span></span>

### <span data-ttu-id="3764c-141">System. void</span><span class="sxs-lookup"><span data-stu-id="3764c-141">System.Void</span></span>

## <span data-ttu-id="3764c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3764c-142">NOTES</span></span>
<span data-ttu-id="3764c-143">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="3764c-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="3764c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3764c-144">RELATED LINKS</span></span>

[<span data-ttu-id="3764c-145">Anfang-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3764c-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
