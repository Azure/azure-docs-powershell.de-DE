---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 1cbe4a76801de23357d6fc2b2c6400b7e0fb5ba6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820947"
---
# <span data-ttu-id="8819c-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8819c-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="8819c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8819c-102">SYNOPSIS</span></span>
<span data-ttu-id="8819c-103">Abrufen von Ressourcen für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="8819c-103">Get application insights resources</span></span>

## <span data-ttu-id="8819c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8819c-104">SYNTAX</span></span>

### <span data-ttu-id="8819c-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8819c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8819c-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8819c-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8819c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8819c-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8819c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8819c-108">DESCRIPTION</span></span>
<span data-ttu-id="8819c-109">Abrufen von Ressourcen für Anwendungs Einblicke in eine Ressourcengruppe oder eine bestimmte Ressource</span><span class="sxs-lookup"><span data-stu-id="8819c-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="8819c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8819c-110">EXAMPLES</span></span>

### <span data-ttu-id="8819c-111">Beispiel 1 Abrufen der Ressource "Anwendungs Einblicke"</span><span class="sxs-lookup"><span data-stu-id="8819c-111">Example 1 Get application insights resource</span></span>
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

<span data-ttu-id="8819c-112">Get Application Insights Resource mit dem Namen "Test" in der resoruce-Gruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="8819c-112">Get application insights resource named "test" in resoruce group "testgroup"</span></span>

### <span data-ttu-id="8819c-113">Beispiel 2 Abrufen von Application Insights-Ressourcen mit Informationen zum Preisplan</span><span class="sxs-lookup"><span data-stu-id="8819c-113">Example 2 Get application insights resource with pricing plan information</span></span>
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

<span data-ttu-id="8819c-114">Abrufen der Ressource für Anwendungs Einblicke und einbeziehen von Informationen zum Preisplan für die Ressource mit dem Namen "Test" in der resoruce-Gruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="8819c-114">Get application insights resource and include pricing plan information for resource named "test" in resoruce group "testgroup"</span></span>

## <span data-ttu-id="8819c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8819c-115">PARAMETERS</span></span>

### <span data-ttu-id="8819c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8819c-116">-DefaultProfile</span></span>
<span data-ttu-id="8819c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8819c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8819c-118">-Full</span><span class="sxs-lookup"><span data-stu-id="8819c-118">-Full</span></span>
<span data-ttu-id="8819c-119">Wenn angegeben, erhält Sie den Preisplan/Daily Cap und den Status der Komponente "Application Insights" zurück.</span><span class="sxs-lookup"><span data-stu-id="8819c-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

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

### <span data-ttu-id="8819c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8819c-120">-Name</span></span>
<span data-ttu-id="8819c-121">Ressourcen Name für Application Insights</span><span class="sxs-lookup"><span data-stu-id="8819c-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="8819c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8819c-122">-ResourceGroupName</span></span>
<span data-ttu-id="8819c-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8819c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="8819c-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8819c-124">-ResourceId</span></span>
<span data-ttu-id="8819c-125">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8819c-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8819c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8819c-126">CommonParameters</span></span>
<span data-ttu-id="8819c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8819c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8819c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8819c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8819c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8819c-129">INPUTS</span></span>

### <span data-ttu-id="8819c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8819c-130">System.String</span></span>

## <span data-ttu-id="8819c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8819c-131">OUTPUTS</span></span>

### <span data-ttu-id="8819c-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8819c-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="8819c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8819c-133">NOTES</span></span>

## <span data-ttu-id="8819c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8819c-134">RELATED LINKS</span></span>
