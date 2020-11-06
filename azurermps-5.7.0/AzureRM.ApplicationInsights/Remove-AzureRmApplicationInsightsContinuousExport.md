---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: ccccfe4ba17fe9d5fc9f35f6604f5f7bb9263d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501561"
---
# <span data-ttu-id="7c3c0-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7c3c0-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="7c3c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c3c0-103">Entfernen einer cotinuous-Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="7c3c0-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c3c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c3c0-104">SYNTAX</span></span>

### <span data-ttu-id="7c3c0-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c3c0-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c3c0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c3c0-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c3c0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c3c0-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c3c0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c3c0-108">DESCRIPTION</span></span>
<span data-ttu-id="7c3c0-109">Entfernen einer cotinuous-Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="7c3c0-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="7c3c0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c3c0-110">EXAMPLES</span></span>

### <span data-ttu-id="7c3c0-111">Beispiel 1 Entfernen einer cotinuous-Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="7c3c0-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="7c3c0-112">Entfernen der fortlaufenden Exportkonfiguration von Application Insights mit der Export-ID "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" für die Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="7c3c0-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7c3c0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c3c0-113">PARAMETERS</span></span>

### <span data-ttu-id="7c3c0-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7c3c0-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7c3c0-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="7c3c0-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c0-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c3c0-116">-Confirm</span></span>
<span data-ttu-id="7c3c0-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c3c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c3c0-118">-DefaultProfile</span></span>
<span data-ttu-id="7c3c0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c0-120">-Export-Nr</span><span class="sxs-lookup"><span data-stu-id="7c3c0-120">-ExportId</span></span>
<span data-ttu-id="7c3c0-121">Application Insights-fortlaufende Export-ID.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-121">Application Insights Continuous Export ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7c3c0-122">-Name</span></span>
<span data-ttu-id="7c3c0-123">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="7c3c0-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c3c0-124">-PassThru</span></span>
<span data-ttu-id="7c3c0-125">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7c3c0-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-126">This parameter is optional.</span></span> <span data-ttu-id="7c3c0-127">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="7c3c0-127">Default value is false.</span></span>

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

### <span data-ttu-id="7c3c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c3c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="7c3c0-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c0-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7c3c0-130">-ResourceId</span></span>
<span data-ttu-id="7c3c0-131">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c3c0-132">-WhatIf</span></span>
<span data-ttu-id="7c3c0-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c3c0-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c3c0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c3c0-135">CommonParameters</span></span>
<span data-ttu-id="7c3c0-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c3c0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c3c0-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c3c0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c3c0-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c3c0-138">INPUTS</span></span>

### <span data-ttu-id="7c3c0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7c3c0-139">System.String</span></span>

## <span data-ttu-id="7c3c0-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c3c0-140">OUTPUTS</span></span>

### <span data-ttu-id="7c3c0-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="7c3c0-141">System.Object</span></span>

## <span data-ttu-id="7c3c0-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c3c0-142">NOTES</span></span>

## <span data-ttu-id="7c3c0-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c3c0-143">RELATED LINKS</span></span>

