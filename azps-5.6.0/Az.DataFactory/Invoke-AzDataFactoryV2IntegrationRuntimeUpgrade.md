---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: 941e820bb1c274a74cc52042b80cdf1b259a34b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930163"
---
# <span data-ttu-id="c0555-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="c0555-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="c0555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0555-102">SYNOPSIS</span></span>
<span data-ttu-id="c0555-103">Aktualisiert die selbst gehostete Integrations-Runtime.</span><span class="sxs-lookup"><span data-stu-id="c0555-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="c0555-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0555-104">SYNTAX</span></span>

### <span data-ttu-id="c0555-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0555-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0555-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0555-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0555-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c0555-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0555-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0555-108">DESCRIPTION</span></span>
<span data-ttu-id="c0555-109">Das **Cmdlet Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** aktualisiert die selbst gehostete Integrationslaufzeit, wenn die neue Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c0555-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="c0555-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0555-110">EXAMPLES</span></span>

### <span data-ttu-id="c0555-111">Beispiel 1: Upgrades einer selbst gehosteten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="c0555-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="c0555-112">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "test-selfhost-ir" in der Daten factory "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="c0555-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="c0555-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c0555-113">PARAMETERS</span></span>

### <span data-ttu-id="c0555-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c0555-114">-DataFactoryName</span></span>
<span data-ttu-id="c0555-115">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="c0555-115">The data factory name.</span></span>

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

### <span data-ttu-id="c0555-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0555-116">-DefaultProfile</span></span>
<span data-ttu-id="c0555-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0555-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0555-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0555-118">-InputObject</span></span>
<span data-ttu-id="c0555-119">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0555-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="c0555-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c0555-120">-Name</span></span>
<span data-ttu-id="c0555-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="c0555-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="c0555-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0555-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0555-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c0555-123">The resource group name.</span></span>

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

### <span data-ttu-id="c0555-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0555-124">-ResourceId</span></span>
<span data-ttu-id="c0555-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c0555-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c0555-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0555-126">-Confirm</span></span>
<span data-ttu-id="c0555-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0555-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0555-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0555-128">-WhatIf</span></span>
<span data-ttu-id="c0555-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0555-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0555-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0555-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0555-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0555-131">CommonParameters</span></span>
<span data-ttu-id="c0555-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0555-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0555-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0555-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0555-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0555-134">INPUTS</span></span>

### <span data-ttu-id="c0555-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c0555-135">System.String</span></span>

### <span data-ttu-id="c0555-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c0555-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c0555-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0555-137">OUTPUTS</span></span>

### <span data-ttu-id="c0555-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="c0555-138">System.Void</span></span>

## <span data-ttu-id="c0555-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c0555-139">NOTES</span></span>
<span data-ttu-id="c0555-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="c0555-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c0555-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c0555-141">RELATED LINKS</span></span>

<span data-ttu-id="c0555-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="c0555-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

