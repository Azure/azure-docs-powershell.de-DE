---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 7b426f7f6b494c92d86a41217000b2d2335c7d91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502641"
---
# <span data-ttu-id="dd880-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="dd880-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="dd880-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd880-102">SYNOPSIS</span></span>
<span data-ttu-id="dd880-103">Aktualisieren einer fortlaufenden Exportkonfiguration in einer Webapplikation Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="dd880-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd880-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd880-104">SYNTAX</span></span>

### <span data-ttu-id="dd880-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd880-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd880-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd880-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd880-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd880-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd880-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd880-108">DESCRIPTION</span></span>
<span data-ttu-id="dd880-109">Aktualisieren einer fortlaufenden Exportkonfiguration in einer Webapplikation Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="dd880-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="dd880-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd880-110">EXAMPLES</span></span>

### <span data-ttu-id="dd880-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd880-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="dd880-112">Aktualisieren Sie die fortlaufende Exportkonfiguration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" der Ressource "Test" in der Ressourcengruppe "Testgruppe", um "Request"-und "Trace"-Dokumente in den Speichercontainer "Testcontainer" in "teststorageaccount" zu exportieren. Das SAS-Token muss gültig sein und über die Schreibberechtigung für den Container verfügen, andernfalls funktioniert die Funktion "kontinuierlicher Export" nicht.</span><span class="sxs-lookup"><span data-stu-id="dd880-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="dd880-113">Wenn das SAS-Token abgelaufen ist, funktioniert das Feature für den fortlaufenden Export nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="dd880-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="dd880-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd880-114">PARAMETERS</span></span>

### <span data-ttu-id="dd880-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="dd880-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="dd880-116">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="dd880-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="dd880-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd880-117">-Confirm</span></span>
<span data-ttu-id="dd880-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd880-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd880-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd880-119">-DefaultProfile</span></span>
<span data-ttu-id="dd880-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd880-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd880-121">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd880-121">-DisableConfiguration</span></span>
<span data-ttu-id="dd880-122">Deaktivieren Sie den fortlaufenden Export.</span><span class="sxs-lookup"><span data-stu-id="dd880-122">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="dd880-123">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="dd880-123">-DocumentType</span></span>
<span data-ttu-id="dd880-124">Dokumenttypen, die exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="dd880-124">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-125">-Export-Nr</span><span class="sxs-lookup"><span data-stu-id="dd880-125">-ExportId</span></span>
<span data-ttu-id="dd880-126">Application Insights-fortlaufende Export-ID.</span><span class="sxs-lookup"><span data-stu-id="dd880-126">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-127">-Name</span><span class="sxs-lookup"><span data-stu-id="dd880-127">-Name</span></span>
<span data-ttu-id="dd880-128">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="dd880-128">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="dd880-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd880-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd880-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd880-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd880-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dd880-131">-ResourceId</span></span>
<span data-ttu-id="dd880-132">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="dd880-132">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="dd880-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dd880-133">-StorageAccountId</span></span>
<span data-ttu-id="dd880-134">ID des Zielspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="dd880-134">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-135">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="dd880-135">-StorageLocation</span></span>
<span data-ttu-id="dd880-136">ID des Zielspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="dd880-136">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-137">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="dd880-137">-StorageSASUri</span></span>
<span data-ttu-id="dd880-138">SAS-URI für den Zielspeicher</span><span class="sxs-lookup"><span data-stu-id="dd880-138">Destination Storage SAS uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd880-139">-WhatIf</span></span>
<span data-ttu-id="dd880-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd880-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd880-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd880-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd880-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd880-142">CommonParameters</span></span>
<span data-ttu-id="dd880-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd880-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd880-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd880-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd880-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd880-145">INPUTS</span></span>

### <span data-ttu-id="dd880-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dd880-146">System.String</span></span>
<span data-ttu-id="dd880-147">System. String [] System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd880-147">System.String[] System.Boolean</span></span>

## <span data-ttu-id="dd880-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd880-148">OUTPUTS</span></span>

### <span data-ttu-id="dd880-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd880-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="dd880-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd880-150">NOTES</span></span>

## <span data-ttu-id="dd880-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd880-151">RELATED LINKS</span></span>

