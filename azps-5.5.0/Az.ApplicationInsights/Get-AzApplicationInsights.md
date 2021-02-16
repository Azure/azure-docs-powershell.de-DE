---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 943089433ca7007ef81648846a48ebdd5684bab2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162540"
---
# <span data-ttu-id="8efb5-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8efb5-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="8efb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8efb5-102">SYNOPSIS</span></span>
<span data-ttu-id="8efb5-103">Ressourcen für Anwendungserkenntnisse erhalten</span><span class="sxs-lookup"><span data-stu-id="8efb5-103">Get application insights resources</span></span>

## <span data-ttu-id="8efb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8efb5-104">SYNTAX</span></span>

### <span data-ttu-id="8efb5-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8efb5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8efb5-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8efb5-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8efb5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8efb5-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8efb5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8efb5-108">DESCRIPTION</span></span>
<span data-ttu-id="8efb5-109">Ressourcen für Anwendungserkenntnisse in einer Ressourcengruppe oder einer bestimmten Ressource erhalten</span><span class="sxs-lookup"><span data-stu-id="8efb5-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="8efb5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8efb5-110">EXAMPLES</span></span>

### <span data-ttu-id="8efb5-111">Beispiel 1: Ressourcen für Anwendungserkenntnisse erhalten</span><span class="sxs-lookup"><span data-stu-id="8efb5-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="8efb5-112">Erhalten Sie die Ressource "Test" für Anwendungserkenntnisse in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="8efb5-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="8efb5-113">Beispiel 2 Ressourcen zum Erhalten von Anwendungserkenntnissen mit Preisplaninformationen</span><span class="sxs-lookup"><span data-stu-id="8efb5-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="8efb5-114">Erhalten Sie Ressourcen für Anwendungserkenntnisse, und fügen Sie Preisplaninformationen für die Ressource mit dem Namen "Test" in die Ressourcengruppe "Testgruppe" ein.</span><span class="sxs-lookup"><span data-stu-id="8efb5-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8efb5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8efb5-115">PARAMETERS</span></span>

### <span data-ttu-id="8efb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efb5-116">-DefaultProfile</span></span>
<span data-ttu-id="8efb5-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8efb5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8efb5-118">-Full</span><span class="sxs-lookup"><span data-stu-id="8efb5-118">-Full</span></span>
<span data-ttu-id="8efb5-119">Falls angegeben, werden der Preisplan/tageshöchste Preis und der Status der Komponente für Anwendungseinblicke wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8efb5-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8efb5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8efb5-120">-Name</span></span>
<span data-ttu-id="8efb5-121">Ressourcenname von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8efb5-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="8efb5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8efb5-122">-ResourceGroupName</span></span>
<span data-ttu-id="8efb5-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8efb5-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="8efb5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8efb5-124">-ResourceId</span></span>
<span data-ttu-id="8efb5-125">Ressourcen-ID der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="8efb5-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8efb5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efb5-126">CommonParameters</span></span>
<span data-ttu-id="8efb5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8efb5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efb5-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8efb5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efb5-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8efb5-129">INPUTS</span></span>

### <span data-ttu-id="8efb5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8efb5-130">System.String</span></span>

## <span data-ttu-id="8efb5-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8efb5-131">OUTPUTS</span></span>

### <span data-ttu-id="8efb5-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8efb5-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="8efb5-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8efb5-133">NOTES</span></span>

## <span data-ttu-id="8efb5-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8efb5-134">RELATED LINKS</span></span>
