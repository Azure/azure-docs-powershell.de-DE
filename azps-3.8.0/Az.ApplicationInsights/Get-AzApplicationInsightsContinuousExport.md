---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004354"
---
# <span data-ttu-id="a3dec-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a3dec-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a3dec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3dec-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dec-103">Abrufen von Anwendungs Insights, fortlaufende Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a3dec-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a3dec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3dec-104">SYNTAX</span></span>

### <span data-ttu-id="a3dec-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3dec-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3dec-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3dec-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3dec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3dec-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3dec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3dec-108">DESCRIPTION</span></span>
<span data-ttu-id="a3dec-109">Abrufen von Anwendungs Insights, fortlaufende Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a3dec-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a3dec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3dec-110">EXAMPLES</span></span>

### <span data-ttu-id="a3dec-111">Beispiel 1 Abrufen des fortlaufenden Exports für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a3dec-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="a3dec-112">Abrufen von Anwendungs Einblicken fortlaufende Export Konfigurationen für die Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="a3dec-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="a3dec-113">Beispiel 2 Abrufen des fortlaufenden Exports für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a3dec-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="a3dec-114">Abrufen der fortlaufenden Exportkonfiguration für Application Insights mit der Export-ID "ZJrfffySPdtG3ESn3iRxVIEFuNY =" für die Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="a3dec-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a3dec-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3dec-115">PARAMETERS</span></span>

### <span data-ttu-id="a3dec-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a3dec-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a3dec-117">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="a3dec-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="a3dec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dec-118">-DefaultProfile</span></span>
<span data-ttu-id="a3dec-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3dec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3dec-120">-Export-Nr</span><span class="sxs-lookup"><span data-stu-id="a3dec-120">-ExportId</span></span>
<span data-ttu-id="a3dec-121">Application Insights-fortlaufende Export-ID.</span><span class="sxs-lookup"><span data-stu-id="a3dec-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3dec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a3dec-122">-Name</span></span>
<span data-ttu-id="a3dec-123">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="a3dec-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="a3dec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3dec-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3dec-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3dec-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a3dec-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a3dec-126">-ResourceId</span></span>
<span data-ttu-id="a3dec-127">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a3dec-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="a3dec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dec-128">CommonParameters</span></span>
<span data-ttu-id="a3dec-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dec-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3dec-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dec-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3dec-131">INPUTS</span></span>

### <span data-ttu-id="a3dec-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a3dec-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a3dec-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a3dec-133">System.String</span></span>

## <span data-ttu-id="a3dec-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3dec-134">OUTPUTS</span></span>

### <span data-ttu-id="a3dec-135">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3dec-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="a3dec-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3dec-136">NOTES</span></span>

## <span data-ttu-id="a3dec-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3dec-137">RELATED LINKS</span></span>
