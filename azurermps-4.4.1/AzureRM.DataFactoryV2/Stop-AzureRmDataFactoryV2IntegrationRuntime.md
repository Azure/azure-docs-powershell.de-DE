---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 181d63a41853105b21826353fabfca83cddf1bd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505965"
---
# <span data-ttu-id="e41cd-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e41cd-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e41cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e41cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e41cd-103">Beendet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e41cd-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e41cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e41cd-104">SYNTAX</span></span>

### <span data-ttu-id="e41cd-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e41cd-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e41cd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e41cd-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e41cd-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e41cd-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="e41cd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e41cd-108">DESCRIPTION</span></span>
<span data-ttu-id="e41cd-109">Das Cmdlet **Stop-AzureRmDataFactoryV2IntegrationRuntime** beendet eine verwaltete dedizierte Integrationslaufzeit im Zustand "Started", die vom Cmdlet Start-AzureRmDataFactoryV2IntegrationRuntime gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e41cd-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="e41cd-110">Die Ressourcen werden freigegeben, und der Status wird an "gestoppt" übertragen.</span><span class="sxs-lookup"><span data-stu-id="e41cd-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="e41cd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e41cd-111">EXAMPLES</span></span>

### <span data-ttu-id="e41cd-112">Beispiel 1: Beenden einer verwalteten Integrationslaufzeit, die sich im Zustand "gestartet" befindet.</span><span class="sxs-lookup"><span data-stu-id="e41cd-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="e41cd-113">Die verwaltete Integrationslaufzeit "Test-reserlved-IR" befindet sich im Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="e41cd-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="e41cd-114">Nach dem Ausführen Stop-AzureRmDataFactoryV2IntegrationRuntime-Cmdlets werden die Ressourcen freigegeben, und der Zustand wird an "stopped" übertragen.</span><span class="sxs-lookup"><span data-stu-id="e41cd-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="e41cd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e41cd-115">PARAMETERS</span></span>

### <span data-ttu-id="e41cd-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e41cd-116">-Confirm</span></span>
<span data-ttu-id="e41cd-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e41cd-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e41cd-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e41cd-118">-DataFactoryName</span></span>
<span data-ttu-id="e41cd-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="e41cd-119">The data factory name.</span></span>

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

### <span data-ttu-id="e41cd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e41cd-120">-Force</span></span>
<span data-ttu-id="e41cd-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="e41cd-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e41cd-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e41cd-122">-InputObject</span></span>
<span data-ttu-id="e41cd-123">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="e41cd-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="e41cd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e41cd-124">-Name</span></span>
<span data-ttu-id="e41cd-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e41cd-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="e41cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e41cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="e41cd-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e41cd-127">The resource group name.</span></span>

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

### <span data-ttu-id="e41cd-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e41cd-128">-ResourceId</span></span>
<span data-ttu-id="e41cd-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e41cd-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e41cd-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e41cd-130">-Confirm</span></span>
<span data-ttu-id="e41cd-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e41cd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e41cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e41cd-132">-WhatIf</span></span>
<span data-ttu-id="e41cd-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e41cd-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e41cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e41cd-134">CommonParameters</span></span>
<span data-ttu-id="e41cd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e41cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e41cd-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e41cd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e41cd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e41cd-137">INPUTS</span></span>

### <span data-ttu-id="e41cd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e41cd-138">System.String</span></span>
<span data-ttu-id="e41cd-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e41cd-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e41cd-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e41cd-140">OUTPUTS</span></span>

### <span data-ttu-id="e41cd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e41cd-141">System.Boolean</span></span>

## <span data-ttu-id="e41cd-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e41cd-142">NOTES</span></span>
<span data-ttu-id="e41cd-143">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="e41cd-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e41cd-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e41cd-144">RELATED LINKS</span></span>
[<span data-ttu-id="e41cd-145">Anfang-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e41cd-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
