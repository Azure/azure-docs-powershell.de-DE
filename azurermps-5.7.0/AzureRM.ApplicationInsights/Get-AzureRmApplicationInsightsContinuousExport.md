---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 5e3b2feff3b59df30960856718911a3aeb699c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499094"
---
# <span data-ttu-id="537c1-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="537c1-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="537c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="537c1-102">SYNOPSIS</span></span>
<span data-ttu-id="537c1-103">Abrufen von Anwendungs Insights, fortlaufende Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="537c1-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="537c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="537c1-104">SYNTAX</span></span>

### <span data-ttu-id="537c1-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="537c1-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="537c1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="537c1-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="537c1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="537c1-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="537c1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="537c1-108">DESCRIPTION</span></span>
<span data-ttu-id="537c1-109">Abrufen von Anwendungs Insights, fortlaufende Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="537c1-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="537c1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="537c1-110">EXAMPLES</span></span>

### <span data-ttu-id="537c1-111">Beispiel 1 Abrufen des fortlaufenden Exports für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="537c1-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="537c1-112">Abrufen von Anwendungs Einblicken fortlaufende Export Konfigurationen für die Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="537c1-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="537c1-113">Beispiel 2 Abrufen des fortlaufenden Exports für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="537c1-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="537c1-114">Abrufen der fortlaufenden Exportkonfiguration für Application Insights mit der Export-ID "ZJrfffySPdtG3ESn3iRxVIEFuNY =" für die Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="537c1-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="537c1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="537c1-115">PARAMETERS</span></span>

### <span data-ttu-id="537c1-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="537c1-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="537c1-117">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="537c1-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="537c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537c1-118">-DefaultProfile</span></span>
<span data-ttu-id="537c1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="537c1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="537c1-120">-Export-Nr</span><span class="sxs-lookup"><span data-stu-id="537c1-120">-ExportId</span></span>
<span data-ttu-id="537c1-121">Application Insights-fortlaufende Export-ID.</span><span class="sxs-lookup"><span data-stu-id="537c1-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537c1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="537c1-122">-Name</span></span>
<span data-ttu-id="537c1-123">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="537c1-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="537c1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="537c1-124">-ResourceGroupName</span></span>
<span data-ttu-id="537c1-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="537c1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="537c1-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="537c1-126">-ResourceId</span></span>
<span data-ttu-id="537c1-127">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="537c1-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="537c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537c1-128">CommonParameters</span></span>
<span data-ttu-id="537c1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="537c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537c1-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="537c1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537c1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="537c1-131">INPUTS</span></span>

### <span data-ttu-id="537c1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="537c1-132">System.String</span></span>

## <span data-ttu-id="537c1-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="537c1-133">OUTPUTS</span></span>

### <span data-ttu-id="537c1-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="537c1-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="537c1-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="537c1-135">NOTES</span></span>

## <span data-ttu-id="537c1-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="537c1-136">RELATED LINKS</span></span>

