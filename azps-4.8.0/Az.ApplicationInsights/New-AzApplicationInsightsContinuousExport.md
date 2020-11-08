---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008727"
---
# <span data-ttu-id="b7b92-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="b7b92-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="b7b92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7b92-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b92-103">Erstellen einer neuen Application Insights-fortlaufenden Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="b7b92-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="b7b92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b92-104">SYNTAX</span></span>

### <span data-ttu-id="b7b92-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7b92-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7b92-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7b92-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7b92-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7b92-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7b92-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7b92-108">DESCRIPTION</span></span>
<span data-ttu-id="b7b92-109">Erstellen einer neuen Application Insights-fortlaufenden Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="b7b92-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="b7b92-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7b92-110">EXAMPLES</span></span>

### <span data-ttu-id="b7b92-111">Beispiel 1 Erstellen einer neuen fortlaufenden Exportkonfiguration für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="b7b92-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="b7b92-112">Erstellen einer neuen Application Insights-fortlaufenden Exportkonfiguration zum Exportieren von Dokumenttypen "Request" und "Trace" in den Speicher enthalten "Testcontainer" im Speicherkonto "teststorageaccount" in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="b7b92-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="b7b92-113">Das SAS-Token muss gültig sein und über die Schreibberechtigung für den Container verfügen, ansonsten funktioniert das Feature für den fortlaufenden Export nicht. Wenn das SAS-Token abgelaufen ist, funktioniert das Feature für den fortlaufenden Export nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="b7b92-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="b7b92-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b92-114">PARAMETERS</span></span>

### <span data-ttu-id="b7b92-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b7b92-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b7b92-116">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="b7b92-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b7b92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b92-117">-DefaultProfile</span></span>
<span data-ttu-id="b7b92-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7b92-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b92-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="b7b92-119">-DocumentType</span></span>
<span data-ttu-id="b7b92-120">Dokumenttypen, die exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b7b92-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="b7b92-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b7b92-121">-Name</span></span>
<span data-ttu-id="b7b92-122">Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="b7b92-122">Component Name.</span></span>

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

### <span data-ttu-id="b7b92-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b92-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7b92-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b7b92-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7b92-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b7b92-125">-ResourceId</span></span>
<span data-ttu-id="b7b92-126">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b7b92-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b7b92-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b7b92-127">-StorageAccountId</span></span>
<span data-ttu-id="b7b92-128">ID des Zielspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="b7b92-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="b7b92-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="b7b92-129">-StorageLocation</span></span>
<span data-ttu-id="b7b92-130">ID des Zielspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="b7b92-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="b7b92-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="b7b92-131">-StorageSASUri</span></span>
<span data-ttu-id="b7b92-132">SAS-URI für den Zielspeicher</span><span class="sxs-lookup"><span data-stu-id="b7b92-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="b7b92-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7b92-133">-Confirm</span></span>
<span data-ttu-id="b7b92-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7b92-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b92-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b92-135">-WhatIf</span></span>
<span data-ttu-id="b7b92-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7b92-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7b92-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7b92-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7b92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b92-138">CommonParameters</span></span>
<span data-ttu-id="b7b92-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b92-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b92-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b92-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7b92-141">INPUTS</span></span>

### <span data-ttu-id="b7b92-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b7b92-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="b7b92-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b92-143">System.String</span></span>

## <span data-ttu-id="b7b92-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7b92-144">OUTPUTS</span></span>

### <span data-ttu-id="b7b92-145">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7b92-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="b7b92-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7b92-146">NOTES</span></span>

## <span data-ttu-id="b7b92-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7b92-147">RELATED LINKS</span></span>
