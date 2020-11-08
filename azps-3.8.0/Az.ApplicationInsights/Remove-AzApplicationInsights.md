---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: d9aa737a34e106fc8514c0e9bbbcfb70b73f015a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004349"
---
# <span data-ttu-id="a8e2e-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a8e2e-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="a8e2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e2e-103">Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a8e2e-103">Remove an application insights resource</span></span>

## <span data-ttu-id="a8e2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8e2e-104">SYNTAX</span></span>

### <span data-ttu-id="a8e2e-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8e2e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8e2e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8e2e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8e2e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8e2e-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8e2e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8e2e-108">DESCRIPTION</span></span>
<span data-ttu-id="a8e2e-109">Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a8e2e-109">Remove an application insights resource</span></span>

## <span data-ttu-id="a8e2e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8e2e-110">EXAMPLES</span></span>

### <span data-ttu-id="a8e2e-111">Beispiel 1 Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a8e2e-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="a8e2e-112">Entfernen einer Application Insights-Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="a8e2e-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a8e2e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8e2e-113">PARAMETERS</span></span>

### <span data-ttu-id="a8e2e-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a8e2e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a8e2e-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="a8e2e-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e2e-116">-DefaultProfile</span></span>
<span data-ttu-id="a8e2e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8e2e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a8e2e-118">-Name</span></span>
<span data-ttu-id="a8e2e-119">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="a8e2e-119">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e2e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8e2e-120">-PassThru</span></span>
<span data-ttu-id="a8e2e-121">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a8e2e-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-122">This parameter is optional.</span></span> <span data-ttu-id="a8e2e-123">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="a8e2e-123">Default value is false.</span></span>

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

### <span data-ttu-id="a8e2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8e2e-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e2e-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a8e2e-126">-ResourceId</span></span>
<span data-ttu-id="a8e2e-127">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e2e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8e2e-128">-Confirm</span></span>
<span data-ttu-id="a8e2e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8e2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e2e-130">-WhatIf</span></span>
<span data-ttu-id="a8e2e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8e2e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8e2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e2e-133">CommonParameters</span></span>
<span data-ttu-id="a8e2e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8e2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e2e-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8e2e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e2e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8e2e-136">INPUTS</span></span>

### <span data-ttu-id="a8e2e-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a8e2e-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a8e2e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8e2e-138">System.String</span></span>

## <span data-ttu-id="a8e2e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8e2e-139">OUTPUTS</span></span>

### <span data-ttu-id="a8e2e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8e2e-140">System.Boolean</span></span>

## <span data-ttu-id="a8e2e-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8e2e-141">NOTES</span></span>

## <span data-ttu-id="a8e2e-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8e2e-142">RELATED LINKS</span></span>
