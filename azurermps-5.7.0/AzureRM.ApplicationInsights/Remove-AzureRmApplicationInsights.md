---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: a440dd37d26bf65f4deb8c7e4c4535f6460f76be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663798"
---
# <span data-ttu-id="83056-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="83056-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="83056-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83056-102">SYNOPSIS</span></span>
<span data-ttu-id="83056-103">Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="83056-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83056-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83056-104">SYNTAX</span></span>

### <span data-ttu-id="83056-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="83056-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83056-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83056-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83056-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83056-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83056-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83056-108">DESCRIPTION</span></span>
<span data-ttu-id="83056-109">Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="83056-109">Remove an application insights resource</span></span>

## <span data-ttu-id="83056-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83056-110">EXAMPLES</span></span>

### <span data-ttu-id="83056-111">Beispiel 1 Entfernen einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="83056-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="83056-112">Entfernen einer Webapplikation Insights-Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="83056-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="83056-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="83056-113">PARAMETERS</span></span>

### <span data-ttu-id="83056-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="83056-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="83056-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="83056-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="83056-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83056-116">-Confirm</span></span>
<span data-ttu-id="83056-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83056-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83056-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83056-118">-DefaultProfile</span></span>
<span data-ttu-id="83056-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83056-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83056-120">-Name</span><span class="sxs-lookup"><span data-stu-id="83056-120">-Name</span></span>
<span data-ttu-id="83056-121">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="83056-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="83056-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83056-122">-PassThru</span></span>
<span data-ttu-id="83056-123">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="83056-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="83056-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83056-124">This parameter is optional.</span></span> <span data-ttu-id="83056-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="83056-125">Default value is false.</span></span>

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

### <span data-ttu-id="83056-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83056-126">-ResourceGroupName</span></span>
<span data-ttu-id="83056-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="83056-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="83056-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="83056-128">-ResourceId</span></span>
<span data-ttu-id="83056-129">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="83056-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="83056-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83056-130">-WhatIf</span></span>
<span data-ttu-id="83056-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83056-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83056-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83056-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83056-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83056-133">CommonParameters</span></span>
<span data-ttu-id="83056-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83056-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83056-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83056-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83056-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83056-136">INPUTS</span></span>

### <span data-ttu-id="83056-137">System. String</span><span class="sxs-lookup"><span data-stu-id="83056-137">System.String</span></span>

## <span data-ttu-id="83056-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83056-138">OUTPUTS</span></span>

### <span data-ttu-id="83056-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="83056-139">System.Object</span></span>

## <span data-ttu-id="83056-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="83056-140">NOTES</span></span>

## <span data-ttu-id="83056-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83056-141">RELATED LINKS</span></span>

