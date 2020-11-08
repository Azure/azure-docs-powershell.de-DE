---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165360"
---
# <span data-ttu-id="6f1da-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="6f1da-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="6f1da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f1da-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1da-103">Entfernen eines Application Insights-API-Schlüssels für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="6f1da-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="6f1da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f1da-104">SYNTAX</span></span>

### <span data-ttu-id="6f1da-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f1da-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f1da-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f1da-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f1da-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f1da-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f1da-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f1da-108">DESCRIPTION</span></span>
<span data-ttu-id="6f1da-109">Entfernen eines Application Insights-API-Schlüssels für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="6f1da-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="6f1da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f1da-110">EXAMPLES</span></span>

### <span data-ttu-id="6f1da-111">Beispiel 1 Entfernen eines Application Insights-API-Schlüssels für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="6f1da-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="6f1da-112">Entfernen spezifischer Application Insights-API-Schlüssel diese ID lautet "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" für Ressource "Test" in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="6f1da-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="6f1da-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f1da-113">PARAMETERS</span></span>

### <span data-ttu-id="6f1da-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="6f1da-114">-ApiKeyId</span></span>
<span data-ttu-id="6f1da-115">API-Schlüssel-ID für Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6f1da-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="6f1da-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6f1da-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6f1da-117">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="6f1da-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6f1da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1da-118">-DefaultProfile</span></span>
<span data-ttu-id="6f1da-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f1da-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f1da-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6f1da-120">-Name</span></span>
<span data-ttu-id="6f1da-121">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="6f1da-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6f1da-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f1da-122">-PassThru</span></span>
<span data-ttu-id="6f1da-123">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6f1da-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6f1da-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f1da-124">This parameter is optional.</span></span> <span data-ttu-id="6f1da-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="6f1da-125">Default value is false.</span></span>

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

### <span data-ttu-id="6f1da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f1da-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f1da-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6f1da-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="6f1da-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6f1da-128">-ResourceId</span></span>
<span data-ttu-id="6f1da-129">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6f1da-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6f1da-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f1da-130">-Confirm</span></span>
<span data-ttu-id="6f1da-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f1da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f1da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f1da-132">-WhatIf</span></span>
<span data-ttu-id="6f1da-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f1da-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f1da-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f1da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f1da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1da-135">CommonParameters</span></span>
<span data-ttu-id="6f1da-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f1da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1da-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1da-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1da-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f1da-138">INPUTS</span></span>

### <span data-ttu-id="6f1da-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6f1da-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6f1da-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6f1da-140">System.String</span></span>

## <span data-ttu-id="6f1da-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f1da-141">OUTPUTS</span></span>

### <span data-ttu-id="6f1da-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f1da-142">System.Boolean</span></span>

## <span data-ttu-id="6f1da-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f1da-143">NOTES</span></span>

## <span data-ttu-id="6f1da-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f1da-144">RELATED LINKS</span></span>
