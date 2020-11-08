---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003013"
---
# <span data-ttu-id="690e6-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="690e6-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="690e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="690e6-102">SYNOPSIS</span></span>
<span data-ttu-id="690e6-103">Aktualisieren einer fortlaufenden Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="690e6-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="690e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="690e6-104">SYNTAX</span></span>

### <span data-ttu-id="690e6-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="690e6-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690e6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="690e6-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690e6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="690e6-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690e6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="690e6-108">DESCRIPTION</span></span>
<span data-ttu-id="690e6-109">Aktualisieren einer fortlaufenden Exportkonfiguration in einer Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="690e6-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="690e6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="690e6-110">EXAMPLES</span></span>

### <span data-ttu-id="690e6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="690e6-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="690e6-112">Aktualisieren Sie die fortlaufende Exportkonfiguration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" der Ressource "Test" in der Ressourcengruppe "Testgruppe", um "Request"-und "Trace"-Dokumente in den Speichercontainer "Testcontainer" in "teststorageaccount" zu exportieren. Das SAS-Token muss gültig sein und über die Schreibberechtigung für den Container verfügen, ansonsten funktioniert das Feature für den fortlaufenden Export nicht.</span><span class="sxs-lookup"><span data-stu-id="690e6-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="690e6-113">Wenn das SAS-Token abgelaufen ist, funktioniert das Feature für den fortlaufenden Export nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="690e6-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="690e6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="690e6-114">PARAMETERS</span></span>

### <span data-ttu-id="690e6-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="690e6-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="690e6-116">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="690e6-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="690e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690e6-117">-DefaultProfile</span></span>
<span data-ttu-id="690e6-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="690e6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="690e6-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="690e6-119">-DisableConfiguration</span></span>
<span data-ttu-id="690e6-120">Deaktivieren Sie den fortlaufenden Export.</span><span class="sxs-lookup"><span data-stu-id="690e6-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="690e6-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="690e6-121">-DocumentType</span></span>
<span data-ttu-id="690e6-122">Dokumenttypen, die exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="690e6-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="690e6-123">-Export-Nr</span><span class="sxs-lookup"><span data-stu-id="690e6-123">-ExportId</span></span>
<span data-ttu-id="690e6-124">Application Insights-fortlaufende Export-ID.</span><span class="sxs-lookup"><span data-stu-id="690e6-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="690e6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="690e6-125">-Name</span></span>
<span data-ttu-id="690e6-126">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="690e6-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="690e6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690e6-127">-ResourceGroupName</span></span>
<span data-ttu-id="690e6-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="690e6-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="690e6-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="690e6-129">-ResourceId</span></span>
<span data-ttu-id="690e6-130">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="690e6-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="690e6-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="690e6-131">-StorageAccountId</span></span>
<span data-ttu-id="690e6-132">ID des Zielspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="690e6-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="690e6-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="690e6-133">-StorageLocation</span></span>
<span data-ttu-id="690e6-134">ID des Zielspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="690e6-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="690e6-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="690e6-135">-StorageSASUri</span></span>
<span data-ttu-id="690e6-136">SAS-URI für den Zielspeicher</span><span class="sxs-lookup"><span data-stu-id="690e6-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="690e6-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="690e6-137">-Confirm</span></span>
<span data-ttu-id="690e6-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="690e6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="690e6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690e6-139">-WhatIf</span></span>
<span data-ttu-id="690e6-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="690e6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="690e6-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="690e6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="690e6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690e6-142">CommonParameters</span></span>
<span data-ttu-id="690e6-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690e6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690e6-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690e6-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690e6-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="690e6-145">INPUTS</span></span>

### <span data-ttu-id="690e6-146">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="690e6-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="690e6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="690e6-147">System.String</span></span>

## <span data-ttu-id="690e6-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="690e6-148">OUTPUTS</span></span>

### <span data-ttu-id="690e6-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="690e6-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="690e6-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="690e6-150">NOTES</span></span>

## <span data-ttu-id="690e6-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="690e6-151">RELATED LINKS</span></span>
