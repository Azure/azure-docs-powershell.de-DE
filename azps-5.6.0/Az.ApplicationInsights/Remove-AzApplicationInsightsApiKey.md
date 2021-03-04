---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 95f99f629fd32333e06c6194fcaf51837224f4a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920659"
---
# <span data-ttu-id="40bed-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="40bed-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="40bed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40bed-102">SYNOPSIS</span></span>
<span data-ttu-id="40bed-103">Entfernen eines Apischlüssels für Anwendungseinblicke für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="40bed-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="40bed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40bed-104">SYNTAX</span></span>

### <span data-ttu-id="40bed-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="40bed-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40bed-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40bed-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40bed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40bed-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40bed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40bed-108">DESCRIPTION</span></span>
<span data-ttu-id="40bed-109">Entfernen eines Apischlüssels für Anwendungseinblicke für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="40bed-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="40bed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40bed-110">EXAMPLES</span></span>

### <span data-ttu-id="40bed-111">Beispiel 1 Entfernen eines Apischlüssels für Anwendungseinblicke für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="40bed-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="40bed-112">Entfernen Sie bestimmte Anwendungseinblicke-API-Schlüssel, die id ist "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" für Ressource "Test" in der Ressourcengruppe "testGroup".</span><span class="sxs-lookup"><span data-stu-id="40bed-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="40bed-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40bed-113">PARAMETERS</span></span>

### <span data-ttu-id="40bed-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="40bed-114">-ApiKeyId</span></span>
<span data-ttu-id="40bed-115">Application Insights API Key ID.</span><span class="sxs-lookup"><span data-stu-id="40bed-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="40bed-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="40bed-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="40bed-117">Application Insights Component Object.</span><span class="sxs-lookup"><span data-stu-id="40bed-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="40bed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bed-118">-DefaultProfile</span></span>
<span data-ttu-id="40bed-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40bed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40bed-120">-Name</span><span class="sxs-lookup"><span data-stu-id="40bed-120">-Name</span></span>
<span data-ttu-id="40bed-121">Application Insights Component Name.</span><span class="sxs-lookup"><span data-stu-id="40bed-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="40bed-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40bed-122">-PassThru</span></span>
<span data-ttu-id="40bed-123">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="40bed-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="40bed-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="40bed-124">This parameter is optional.</span></span> <span data-ttu-id="40bed-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="40bed-125">Default value is false.</span></span>

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

### <span data-ttu-id="40bed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bed-126">-ResourceGroupName</span></span>
<span data-ttu-id="40bed-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="40bed-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="40bed-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40bed-128">-ResourceId</span></span>
<span data-ttu-id="40bed-129">Application Insights Component Resource Id.</span><span class="sxs-lookup"><span data-stu-id="40bed-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="40bed-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40bed-130">-Confirm</span></span>
<span data-ttu-id="40bed-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40bed-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bed-132">-WhatIf</span></span>
<span data-ttu-id="40bed-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40bed-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bed-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40bed-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bed-135">CommonParameters</span></span>
<span data-ttu-id="40bed-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40bed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bed-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40bed-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bed-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40bed-138">INPUTS</span></span>

### <span data-ttu-id="40bed-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="40bed-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="40bed-140">System.String</span><span class="sxs-lookup"><span data-stu-id="40bed-140">System.String</span></span>

## <span data-ttu-id="40bed-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40bed-141">OUTPUTS</span></span>

### <span data-ttu-id="40bed-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40bed-142">System.Boolean</span></span>

## <span data-ttu-id="40bed-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40bed-143">NOTES</span></span>

## <span data-ttu-id="40bed-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40bed-144">RELATED LINKS</span></span>
