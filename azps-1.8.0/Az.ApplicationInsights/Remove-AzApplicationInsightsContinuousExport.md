---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 0265a273cb575d2cc3a165afae8f7a2090499cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661861"
---
# <span data-ttu-id="a222e-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a222e-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a222e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a222e-102">SYNOPSIS</span></span>
<span data-ttu-id="a222e-103">Entfernen einer cotinuous-Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a222e-103">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="a222e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a222e-104">SYNTAX</span></span>

### <span data-ttu-id="a222e-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a222e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a222e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a222e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a222e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a222e-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a222e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a222e-108">DESCRIPTION</span></span>
<span data-ttu-id="a222e-109">Entfernen einer cotinuous-Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a222e-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="a222e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a222e-110">EXAMPLES</span></span>

### <span data-ttu-id="a222e-111">Beispiel 1 Entfernen einer cotinuous-Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a222e-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="a222e-112">Entfernen der fortlaufenden Exportkonfiguration von Application Insights mit der Export-ID "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" für die Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="a222e-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a222e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a222e-113">PARAMETERS</span></span>

### <span data-ttu-id="a222e-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a222e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a222e-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="a222e-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="a222e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a222e-116">-DefaultProfile</span></span>
<span data-ttu-id="a222e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a222e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a222e-118">-Export-Nr</span><span class="sxs-lookup"><span data-stu-id="a222e-118">-ExportId</span></span>
<span data-ttu-id="a222e-119">Application Insights-fortlaufende Export-ID.</span><span class="sxs-lookup"><span data-stu-id="a222e-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a222e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a222e-120">-Name</span></span>
<span data-ttu-id="a222e-121">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="a222e-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="a222e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a222e-122">-PassThru</span></span>
<span data-ttu-id="a222e-123">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a222e-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a222e-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a222e-124">This parameter is optional.</span></span> <span data-ttu-id="a222e-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="a222e-125">Default value is false.</span></span>

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

### <span data-ttu-id="a222e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a222e-126">-ResourceGroupName</span></span>
<span data-ttu-id="a222e-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a222e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="a222e-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a222e-128">-ResourceId</span></span>
<span data-ttu-id="a222e-129">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a222e-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="a222e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a222e-130">-Confirm</span></span>
<span data-ttu-id="a222e-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a222e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a222e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a222e-132">-WhatIf</span></span>
<span data-ttu-id="a222e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a222e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a222e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a222e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a222e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a222e-135">CommonParameters</span></span>
<span data-ttu-id="a222e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a222e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a222e-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a222e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a222e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a222e-138">INPUTS</span></span>

### <span data-ttu-id="a222e-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a222e-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a222e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a222e-140">System.String</span></span>

## <span data-ttu-id="a222e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a222e-141">OUTPUTS</span></span>

### <span data-ttu-id="a222e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a222e-142">System.Boolean</span></span>

## <span data-ttu-id="a222e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a222e-143">NOTES</span></span>

## <span data-ttu-id="a222e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a222e-144">RELATED LINKS</span></span>
