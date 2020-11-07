---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 5665b85a680411910513663d782791f56b7c1081
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658105"
---
# <span data-ttu-id="20e4b-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="20e4b-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="20e4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="20e4b-103">Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="20e4b-103">Remove an application insights resource</span></span>

## <span data-ttu-id="20e4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20e4b-104">SYNTAX</span></span>

### <span data-ttu-id="20e4b-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="20e4b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e4b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e4b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e4b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e4b-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20e4b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20e4b-108">DESCRIPTION</span></span>
<span data-ttu-id="20e4b-109">Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="20e4b-109">Remove an application insights resource</span></span>

## <span data-ttu-id="20e4b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20e4b-110">EXAMPLES</span></span>

### <span data-ttu-id="20e4b-111">Beispiel 1 Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="20e4b-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="20e4b-112">Entfernen einer Application Insights-Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="20e4b-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="20e4b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="20e4b-113">PARAMETERS</span></span>

### <span data-ttu-id="20e4b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="20e4b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="20e4b-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="20e4b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="20e4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e4b-116">-DefaultProfile</span></span>
<span data-ttu-id="20e4b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20e4b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20e4b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="20e4b-118">-Name</span></span>
<span data-ttu-id="20e4b-119">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="20e4b-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="20e4b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20e4b-120">-PassThru</span></span>
<span data-ttu-id="20e4b-121">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="20e4b-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="20e4b-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="20e4b-122">This parameter is optional.</span></span> <span data-ttu-id="20e4b-123">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="20e4b-123">Default value is false.</span></span>

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

### <span data-ttu-id="20e4b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20e4b-124">-ResourceGroupName</span></span>
<span data-ttu-id="20e4b-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20e4b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="20e4b-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="20e4b-126">-ResourceId</span></span>
<span data-ttu-id="20e4b-127">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="20e4b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="20e4b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20e4b-128">-Confirm</span></span>
<span data-ttu-id="20e4b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20e4b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e4b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e4b-130">-WhatIf</span></span>
<span data-ttu-id="20e4b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20e4b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e4b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20e4b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e4b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e4b-133">CommonParameters</span></span>
<span data-ttu-id="20e4b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e4b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e4b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e4b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e4b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20e4b-136">INPUTS</span></span>

### <span data-ttu-id="20e4b-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="20e4b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="20e4b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="20e4b-138">System.String</span></span>

## <span data-ttu-id="20e4b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20e4b-139">OUTPUTS</span></span>

### <span data-ttu-id="20e4b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20e4b-140">System.Boolean</span></span>

## <span data-ttu-id="20e4b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="20e4b-141">NOTES</span></span>

## <span data-ttu-id="20e4b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20e4b-142">RELATED LINKS</span></span>
