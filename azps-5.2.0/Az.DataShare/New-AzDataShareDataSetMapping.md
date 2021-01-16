---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290315"
---
# <span data-ttu-id="8bfa7-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="8bfa7-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="8bfa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bfa7-102">SYNOPSIS</span></span>
<span data-ttu-id="8bfa7-103">Erstellt eine Datensatzzuordnung für ein Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="8bfa7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bfa7-104">SYNTAX</span></span>

### <span data-ttu-id="8bfa7-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8bfa7-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bfa7-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="8bfa7-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bfa7-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bfa7-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bfa7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bfa7-108">DESCRIPTION</span></span>
<span data-ttu-id="8bfa7-109">Das **Cmdlet "New-AzDataShareDataSetMapping"** erstellt eine Datensetzuordnung zwischen den Quelldatensets und dem Senkespeicherkonto im Share-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="8bfa7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bfa7-110">EXAMPLES</span></span>

### <span data-ttu-id="8bfa7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8bfa7-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="8bfa7-112">Mit diesem Befehl wird eine Datensetzuordnung von AdsDataSetMapping zum Speicherkonto AdsStorage für das Freigabeabonnement AdsShareSubscription im WikiAdsAccount des Datenfreigabekontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="8bfa7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bfa7-113">PARAMETERS</span></span>

### <span data-ttu-id="8bfa7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8bfa7-114">-AccountName</span></span>
<span data-ttu-id="8bfa7-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="8bfa7-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-116">-Container</span><span class="sxs-lookup"><span data-stu-id="8bfa7-116">-Container</span></span>
<span data-ttu-id="8bfa7-117">Containername des Azure -Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8bfa7-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="8bfa7-118">-DataSetId</span></span>
<span data-ttu-id="8bfa7-119">Id des Consumerdatensets</span><span class="sxs-lookup"><span data-stu-id="8bfa7-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bfa7-120">-DefaultProfile</span></span>
<span data-ttu-id="8bfa7-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bfa7-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8bfa7-122">-FilePath</span></span>
<span data-ttu-id="8bfa7-123">Pfad der Azure-Speicherdatei</span><span class="sxs-lookup"><span data-stu-id="8bfa7-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="8bfa7-124">-FileSystem</span></span>
<span data-ttu-id="8bfa7-125">Name des Azure ADLS Gen2-Dateisystems</span><span class="sxs-lookup"><span data-stu-id="8bfa7-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="8bfa7-126">-FolderPath</span></span>
<span data-ttu-id="8bfa7-127">Pfad des Azure-Speicherordners</span><span class="sxs-lookup"><span data-stu-id="8bfa7-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8bfa7-128">-Name</span></span>
<span data-ttu-id="8bfa7-129">Name der Zuordnung von Azure-Datensets</span><span class="sxs-lookup"><span data-stu-id="8bfa7-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bfa7-130">-ResourceGroupName</span></span>
<span data-ttu-id="8bfa7-131">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="8bfa7-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8bfa7-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="8bfa7-133">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="8bfa7-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8bfa7-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="8bfa7-135">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bfa7-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bfa7-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bfa7-136">-Confirm</span></span>
<span data-ttu-id="8bfa7-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bfa7-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8bfa7-138">-WhatIf</span></span>
<span data-ttu-id="8bfa7-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bfa7-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bfa7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bfa7-141">CommonParameters</span></span>
<span data-ttu-id="8bfa7-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bfa7-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bfa7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bfa7-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bfa7-144">INPUTS</span></span>

### <span data-ttu-id="8bfa7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8bfa7-145">System.String</span></span>

## <span data-ttu-id="8bfa7-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bfa7-146">OUTPUTS</span></span>

### <span data-ttu-id="8bfa7-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="8bfa7-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="8bfa7-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8bfa7-148">NOTES</span></span>

## <span data-ttu-id="8bfa7-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8bfa7-149">RELATED LINKS</span></span>
