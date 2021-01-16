---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306800"
---
# <span data-ttu-id="8f7f8-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="8f7f8-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="8f7f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7f8-103">Erstellen einer neuen Anwendungserkenntnissen fortlaufende Exportkonfiguration für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="8f7f8-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="8f7f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f7f8-104">SYNTAX</span></span>

### <span data-ttu-id="8f7f8-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f7f8-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7f8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f7f8-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7f8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f7f8-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7f8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f7f8-108">DESCRIPTION</span></span>
<span data-ttu-id="8f7f8-109">Erstellen einer neuen Anwendungserkenntnissen fortlaufende Exportkonfiguration für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="8f7f8-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="8f7f8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f7f8-110">EXAMPLES</span></span>

### <span data-ttu-id="8f7f8-111">Beispiel 1 Erstellen einer neuen fortlaufenden Exportkonfiguration für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="8f7f8-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
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

<span data-ttu-id="8f7f8-112">Erstellen Sie eine neue Anwendungserkenntnisse fortlaufende Exportkonfiguration, um die Dokumenttypen "Anforderung" und "Ablaufverfolgung" zu speichern, die "Testcontainer" im Speicherkonto "teststorageaccount" in der Ressourcengruppe "Testgruppe" enthalten.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="8f7f8-113">Das SAS-Token muss gültig sein und über Schreibberechtigungen für den Container verfügen, da das Feature für fortlaufende Exporte sonst nicht funktioniert. Wenn das SAS-Token abgelaufen ist, funktioniert das Feature für fortlaufende Exporte nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="8f7f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f7f8-114">PARAMETERS</span></span>

### <span data-ttu-id="8f7f8-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8f7f8-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8f7f8-116">Anwendungserkenntnisse-Komponentenobjekt.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8f7f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7f8-117">-DefaultProfile</span></span>
<span data-ttu-id="8f7f8-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7f8-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="8f7f8-119">-DocumentType</span></span>
<span data-ttu-id="8f7f8-120">Dokumenttypen, die exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="8f7f8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8f7f8-121">-Name</span></span>
<span data-ttu-id="8f7f8-122">Komponentenname.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-122">Component Name.</span></span>

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

### <span data-ttu-id="8f7f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f7f8-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f7f8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f7f8-125">-ResourceId</span></span>
<span data-ttu-id="8f7f8-126">Ressourcen-ID der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8f7f8-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8f7f8-127">-StorageAccountId</span></span>
<span data-ttu-id="8f7f8-128">Zielspeicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="8f7f8-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="8f7f8-129">-StorageLocation</span></span>
<span data-ttu-id="8f7f8-130">Zielspeicherort-ID.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="8f7f8-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="8f7f8-131">-StorageSASUri</span></span>
<span data-ttu-id="8f7f8-132">ZIELspeicher-SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="8f7f8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f7f8-133">-Confirm</span></span>
<span data-ttu-id="8f7f8-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7f8-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8f7f8-135">-WhatIf</span></span>
<span data-ttu-id="8f7f8-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f7f8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7f8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7f8-138">CommonParameters</span></span>
<span data-ttu-id="8f7f8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7f8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7f8-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7f8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7f8-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f7f8-141">INPUTS</span></span>

### <span data-ttu-id="8f7f8-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8f7f8-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8f7f8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8f7f8-143">System.String</span></span>

## <span data-ttu-id="8f7f8-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f7f8-144">OUTPUTS</span></span>

### <span data-ttu-id="8f7f8-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f7f8-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="8f7f8-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f7f8-146">NOTES</span></span>

## <span data-ttu-id="8f7f8-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f7f8-147">RELATED LINKS</span></span>
