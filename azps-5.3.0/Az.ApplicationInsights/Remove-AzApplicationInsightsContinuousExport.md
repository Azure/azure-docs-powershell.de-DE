---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381294"
---
# <span data-ttu-id="54f19-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="54f19-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="54f19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f19-102">SYNOPSIS</span></span>
<span data-ttu-id="54f19-103">Entfernen einer fortlaufenden Exportkonfiguration in einer Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="54f19-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="54f19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54f19-104">SYNTAX</span></span>

### <span data-ttu-id="54f19-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54f19-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54f19-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f19-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54f19-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f19-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54f19-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54f19-108">DESCRIPTION</span></span>
<span data-ttu-id="54f19-109">Entfernen einer fortlaufenden Exportkonfiguration in einer Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="54f19-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="54f19-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54f19-110">EXAMPLES</span></span>

### <span data-ttu-id="54f19-111">Beispiel 1 Entfernen einer fortlaufenden Exportkonfiguration in einer Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="54f19-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="54f19-112">Entfernen von Anwendungserkenntnissen zur fortlaufenden Exportkonfiguration mit der Export-ID "uGOoki0jQsyEs3IdQ83Q4QsNr4=" für die Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="54f19-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="54f19-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54f19-113">PARAMETERS</span></span>

### <span data-ttu-id="54f19-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="54f19-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="54f19-115">Anwendungserkenntnisse-Komponentenobjekt.</span><span class="sxs-lookup"><span data-stu-id="54f19-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="54f19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f19-116">-DefaultProfile</span></span>
<span data-ttu-id="54f19-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54f19-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f19-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="54f19-118">-ExportId</span></span>
<span data-ttu-id="54f19-119">Application Insights Continuous Export ID.</span><span class="sxs-lookup"><span data-stu-id="54f19-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="54f19-120">-Name</span><span class="sxs-lookup"><span data-stu-id="54f19-120">-Name</span></span>
<span data-ttu-id="54f19-121">Name der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="54f19-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="54f19-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54f19-122">-PassThru</span></span>
<span data-ttu-id="54f19-123">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="54f19-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="54f19-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="54f19-124">This parameter is optional.</span></span> <span data-ttu-id="54f19-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="54f19-125">Default value is false.</span></span>

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

### <span data-ttu-id="54f19-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f19-126">-ResourceGroupName</span></span>
<span data-ttu-id="54f19-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="54f19-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="54f19-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54f19-128">-ResourceId</span></span>
<span data-ttu-id="54f19-129">Ressourcen-ID der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="54f19-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="54f19-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54f19-130">-Confirm</span></span>
<span data-ttu-id="54f19-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54f19-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f19-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="54f19-132">-WhatIf</span></span>
<span data-ttu-id="54f19-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54f19-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54f19-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54f19-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f19-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f19-135">CommonParameters</span></span>
<span data-ttu-id="54f19-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f19-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f19-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f19-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f19-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54f19-138">INPUTS</span></span>

### <span data-ttu-id="54f19-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="54f19-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="54f19-140">System.String</span><span class="sxs-lookup"><span data-stu-id="54f19-140">System.String</span></span>

## <span data-ttu-id="54f19-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54f19-141">OUTPUTS</span></span>

### <span data-ttu-id="54f19-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54f19-142">System.Boolean</span></span>

## <span data-ttu-id="54f19-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54f19-143">NOTES</span></span>

## <span data-ttu-id="54f19-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54f19-144">RELATED LINKS</span></span>
