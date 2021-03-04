---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 12c0c4832d13e3e8637ab1cdb36a1f3fe3abb7d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927232"
---
# <span data-ttu-id="b85fc-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="b85fc-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="b85fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b85fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b85fc-103">Fügt Datensätze zur Azure-Datenfreigabe hinzu.</span><span class="sxs-lookup"><span data-stu-id="b85fc-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="b85fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b85fc-104">SYNTAX</span></span>

### <span data-ttu-id="b85fc-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b85fc-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85fc-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="b85fc-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85fc-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85fc-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85fc-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85fc-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85fc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b85fc-109">DESCRIPTION</span></span>
<span data-ttu-id="b85fc-110">Das **New-AzDataShareDataSet-Cmdlet** fügt Datensätze in azure data share des Datenfreigabekontos hinzu.</span><span class="sxs-lookup"><span data-stu-id="b85fc-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="b85fc-111">Sie können Datensätze vom Typ Blob, ADLS Gen2 und ADLS Gen1 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b85fc-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="b85fc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b85fc-112">EXAMPLES</span></span>

### <span data-ttu-id="b85fc-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b85fc-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="b85fc-114">Mit diesem Befehl wird ein Dataset mit dem Namen AdsDataSet vom Typ blob container zu Azure Data Share AdsShare hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b85fc-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="b85fc-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b85fc-115">PARAMETERS</span></span>

### <span data-ttu-id="b85fc-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b85fc-116">-AccountName</span></span>
<span data-ttu-id="b85fc-117">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="b85fc-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="b85fc-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="b85fc-119">Azure Storage ADLS gen1-Ordnerpfad</span><span class="sxs-lookup"><span data-stu-id="b85fc-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-120">-Container</span><span class="sxs-lookup"><span data-stu-id="b85fc-120">-Container</span></span>
<span data-ttu-id="b85fc-121">Containername des Azure-Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="b85fc-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="b85fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85fc-122">-DefaultProfile</span></span>
<span data-ttu-id="b85fc-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b85fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b85fc-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="b85fc-124">-FileName</span></span>
<span data-ttu-id="b85fc-125">Azure Storage ADLS gen1-Dateiname</span><span class="sxs-lookup"><span data-stu-id="b85fc-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b85fc-126">-FilePath</span></span>
<span data-ttu-id="b85fc-127">Pfad der Azure-Speicherdatei</span><span class="sxs-lookup"><span data-stu-id="b85fc-127">Azure storage file path</span></span>

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

### <span data-ttu-id="b85fc-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b85fc-128">-FileSystem</span></span>
<span data-ttu-id="b85fc-129">Name des Azure ADLS gen2-Dateisystems</span><span class="sxs-lookup"><span data-stu-id="b85fc-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="b85fc-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="b85fc-130">-FolderPath</span></span>
<span data-ttu-id="b85fc-131">Pfad des Azure-Speicherordners</span><span class="sxs-lookup"><span data-stu-id="b85fc-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="b85fc-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b85fc-132">-Name</span></span>
<span data-ttu-id="b85fc-133">Name des Azure-Datenspeichers</span><span class="sxs-lookup"><span data-stu-id="b85fc-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85fc-134">-ResourceGroupName</span></span>
<span data-ttu-id="b85fc-135">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="b85fc-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b85fc-136">-ShareName</span></span>
<span data-ttu-id="b85fc-137">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="b85fc-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="b85fc-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="b85fc-139">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="b85fc-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b85fc-140">-Confirm</span></span>
<span data-ttu-id="b85fc-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b85fc-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85fc-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85fc-142">-WhatIf</span></span>
<span data-ttu-id="b85fc-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b85fc-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85fc-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b85fc-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85fc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85fc-145">CommonParameters</span></span>
<span data-ttu-id="b85fc-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85fc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85fc-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b85fc-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85fc-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b85fc-148">INPUTS</span></span>

### <span data-ttu-id="b85fc-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b85fc-149">System.String</span></span>

## <span data-ttu-id="b85fc-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b85fc-150">OUTPUTS</span></span>

### <span data-ttu-id="b85fc-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="b85fc-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="b85fc-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b85fc-152">NOTES</span></span>

## <span data-ttu-id="b85fc-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b85fc-153">RELATED LINKS</span></span>
