---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 56c573f6806acf2d9c45f583bbbb880aa6fc5638
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941867"
---
# <span data-ttu-id="eaaf6-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="eaaf6-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="eaaf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="eaaf6-103">Erstellt die Datensatzzuordnung für das Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="eaaf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eaaf6-104">SYNTAX</span></span>

### <span data-ttu-id="eaaf6-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eaaf6-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaaf6-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="eaaf6-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaaf6-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaaf6-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaaf6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaaf6-108">DESCRIPTION</span></span>
<span data-ttu-id="eaaf6-109">Das **New-AzDataShareDataSetMapping-Cmdlet** erstellt eine Datensatzzuordnung zwischen den Quelldatensätzen und dem Senkenspeicherkonto im Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="eaaf6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eaaf6-110">EXAMPLES</span></span>

### <span data-ttu-id="eaaf6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eaaf6-111">Example 1</span></span>
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

<span data-ttu-id="eaaf6-112">Mit diesem Befehl wird eine Datensetzuordnung von AdsDataSetMapping zum Speicherkonto AdsStorage für das Freigabeabonnement AdsShareSubscription im WikiAdsAccount des Datenfreigabekontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="eaaf6-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eaaf6-113">PARAMETERS</span></span>

### <span data-ttu-id="eaaf6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eaaf6-114">-AccountName</span></span>
<span data-ttu-id="eaaf6-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="eaaf6-115">Azure data share account name</span></span>

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

### <span data-ttu-id="eaaf6-116">-Container</span><span class="sxs-lookup"><span data-stu-id="eaaf6-116">-Container</span></span>
<span data-ttu-id="eaaf6-117">Containername des Azure-Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="eaaf6-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="eaaf6-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="eaaf6-118">-DataSetId</span></span>
<span data-ttu-id="eaaf6-119">Verbraucherdatensatz-ID</span><span class="sxs-lookup"><span data-stu-id="eaaf6-119">Consumer data set id</span></span>

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

### <span data-ttu-id="eaaf6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaaf6-120">-DefaultProfile</span></span>
<span data-ttu-id="eaaf6-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaaf6-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="eaaf6-122">-FilePath</span></span>
<span data-ttu-id="eaaf6-123">Pfad der Azure-Speicherdatei</span><span class="sxs-lookup"><span data-stu-id="eaaf6-123">Azure storage file path</span></span>

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

### <span data-ttu-id="eaaf6-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="eaaf6-124">-FileSystem</span></span>
<span data-ttu-id="eaaf6-125">Name des Azure ADLS gen2-Dateisystems</span><span class="sxs-lookup"><span data-stu-id="eaaf6-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="eaaf6-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="eaaf6-126">-FolderPath</span></span>
<span data-ttu-id="eaaf6-127">Pfad des Azure-Speicherordners</span><span class="sxs-lookup"><span data-stu-id="eaaf6-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="eaaf6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="eaaf6-128">-Name</span></span>
<span data-ttu-id="eaaf6-129">Name der Azure-Datensatzzuordnung</span><span class="sxs-lookup"><span data-stu-id="eaaf6-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="eaaf6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaaf6-130">-ResourceGroupName</span></span>
<span data-ttu-id="eaaf6-131">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="eaaf6-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eaaf6-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="eaaf6-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="eaaf6-133">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="eaaf6-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="eaaf6-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="eaaf6-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="eaaf6-135">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="eaaf6-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="eaaf6-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eaaf6-136">-Confirm</span></span>
<span data-ttu-id="eaaf6-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaaf6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaaf6-138">-WhatIf</span></span>
<span data-ttu-id="eaaf6-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaaf6-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaaf6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaaf6-141">CommonParameters</span></span>
<span data-ttu-id="eaaf6-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaaf6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaaf6-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaaf6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaaf6-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eaaf6-144">INPUTS</span></span>

### <span data-ttu-id="eaaf6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="eaaf6-145">System.String</span></span>

## <span data-ttu-id="eaaf6-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eaaf6-146">OUTPUTS</span></span>

### <span data-ttu-id="eaaf6-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="eaaf6-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="eaaf6-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eaaf6-148">NOTES</span></span>

## <span data-ttu-id="eaaf6-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eaaf6-149">RELATED LINKS</span></span>
