---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 73aa26491a86b0eba01adb3898dba803f1ecf0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480630"
---
# <span data-ttu-id="a5619-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a5619-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a5619-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5619-102">SYNOPSIS</span></span>
<span data-ttu-id="a5619-103">Erstellen einer neuen Application Insights-fortlaufenden Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a5619-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5619-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5619-104">SYNTAX</span></span>

### <span data-ttu-id="a5619-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5619-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5619-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5619-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5619-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5619-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5619-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5619-108">DESCRIPTION</span></span>
<span data-ttu-id="a5619-109">Erstellen einer neuen Application Insights-fortlaufenden Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a5619-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a5619-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5619-110">EXAMPLES</span></span>

### <span data-ttu-id="a5619-111">Beispiel 1 Erstellen einer neuen fortlaufenden Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="a5619-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="a5619-112">Erstellen einer neuen Application Insights-fortlaufenden Exportkonfiguration zum Exportieren von Dokumenttypen "Request" und "Trace" in den Speicher enthalten "Testcontainer" im Speicherkonto "teststorageaccount" in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="a5619-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="a5619-113">Das SAS-Token muss gültig sein und über die Schreibberechtigung für den Container verfügen, andernfalls funktioniert die Funktion "kontinuierlicher Export" nicht. Wenn das SAS-Token abgelaufen ist, funktioniert das Feature für den fortlaufenden Export nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="a5619-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="a5619-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5619-114">PARAMETERS</span></span>

### <span data-ttu-id="a5619-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a5619-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a5619-116">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="a5619-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="a5619-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5619-117">-DefaultProfile</span></span>
<span data-ttu-id="a5619-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5619-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5619-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="a5619-119">-DocumentType</span></span>
<span data-ttu-id="a5619-120">Dokumenttypen, die exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a5619-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5619-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a5619-121">-Name</span></span>
<span data-ttu-id="a5619-122">Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="a5619-122">Component Name.</span></span>

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

### <span data-ttu-id="a5619-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5619-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5619-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5619-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5619-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5619-125">-ResourceId</span></span>
<span data-ttu-id="a5619-126">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a5619-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="a5619-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a5619-127">-StorageAccountId</span></span>
<span data-ttu-id="a5619-128">ID des Zielspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="a5619-128">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5619-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="a5619-129">-StorageLocation</span></span>
<span data-ttu-id="a5619-130">ID des Zielspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="a5619-130">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5619-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="a5619-131">-StorageSASUri</span></span>
<span data-ttu-id="a5619-132">SAS-URI für den Zielspeicher</span><span class="sxs-lookup"><span data-stu-id="a5619-132">Destination Storage SAS Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5619-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5619-133">-Confirm</span></span>
<span data-ttu-id="a5619-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5619-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5619-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5619-135">-WhatIf</span></span>
<span data-ttu-id="a5619-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5619-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5619-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5619-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5619-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5619-138">CommonParameters</span></span>
<span data-ttu-id="a5619-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5619-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5619-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5619-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5619-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5619-141">INPUTS</span></span>

### <span data-ttu-id="a5619-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a5619-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="a5619-143">Parameter: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5619-143">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="a5619-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a5619-144">System.String</span></span>

## <span data-ttu-id="a5619-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5619-145">OUTPUTS</span></span>

### <span data-ttu-id="a5619-146">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5619-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="a5619-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5619-147">NOTES</span></span>

## <span data-ttu-id="a5619-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5619-148">RELATED LINKS</span></span>
