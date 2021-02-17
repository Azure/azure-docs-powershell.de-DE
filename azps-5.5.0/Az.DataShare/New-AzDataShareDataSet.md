---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 5dbf797ffabdf42b1d30d9d709ba6bb3153d8696
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155812"
---
# <span data-ttu-id="c98cd-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="c98cd-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="c98cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c98cd-103">Fügt Datensätze zur Azure-Datenfreigabe hinzu.</span><span class="sxs-lookup"><span data-stu-id="c98cd-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="c98cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c98cd-104">SYNTAX</span></span>

### <span data-ttu-id="c98cd-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c98cd-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98cd-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="c98cd-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98cd-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="c98cd-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98cd-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="c98cd-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c98cd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c98cd-109">DESCRIPTION</span></span>
<span data-ttu-id="c98cd-110">Das **Cmdlet "New-AzDataShareDataSet"** fügt Datensätze zum Azure-Datenfreigabe-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="c98cd-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="c98cd-111">Sie können Datensätze vom Typ BLOB, ADLS Gen2 und ADLS Gen1 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c98cd-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="c98cd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c98cd-112">EXAMPLES</span></span>

### <span data-ttu-id="c98cd-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c98cd-113">Example 1</span></span>
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

<span data-ttu-id="c98cd-114">Mit diesem Befehl wird ein Dataset namens "AdsDataSet" des Typs "BLOB-Container" zu "Azure Data Share AdsShare" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c98cd-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="c98cd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c98cd-115">PARAMETERS</span></span>

### <span data-ttu-id="c98cd-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c98cd-116">-AccountName</span></span>
<span data-ttu-id="c98cd-117">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="c98cd-117">Azure data share account name</span></span>

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

### <span data-ttu-id="c98cd-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="c98cd-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="c98cd-119">Azure Storage ADLS Gen1-Ordnerpfad</span><span class="sxs-lookup"><span data-stu-id="c98cd-119">Azure storage ADLS gen1 folder path</span></span>

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

### <span data-ttu-id="c98cd-120">-Container</span><span class="sxs-lookup"><span data-stu-id="c98cd-120">-Container</span></span>
<span data-ttu-id="c98cd-121">Containername des Azure -Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="c98cd-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="c98cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98cd-122">-DefaultProfile</span></span>
<span data-ttu-id="c98cd-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c98cd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c98cd-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="c98cd-124">-FileName</span></span>
<span data-ttu-id="c98cd-125">Azure Storage ADLS Gen1-Dateiname</span><span class="sxs-lookup"><span data-stu-id="c98cd-125">Azure storage ADLS gen1 file name</span></span>

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

### <span data-ttu-id="c98cd-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c98cd-126">-FilePath</span></span>
<span data-ttu-id="c98cd-127">Pfad der Azure-Speicherdatei</span><span class="sxs-lookup"><span data-stu-id="c98cd-127">Azure storage file path</span></span>

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

### <span data-ttu-id="c98cd-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="c98cd-128">-FileSystem</span></span>
<span data-ttu-id="c98cd-129">Name des Azure ADLS Gen2-Dateisystems</span><span class="sxs-lookup"><span data-stu-id="c98cd-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="c98cd-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="c98cd-130">-FolderPath</span></span>
<span data-ttu-id="c98cd-131">Pfad des Azure-Speicherordners</span><span class="sxs-lookup"><span data-stu-id="c98cd-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="c98cd-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c98cd-132">-Name</span></span>
<span data-ttu-id="c98cd-133">Name des Azure-Datensets</span><span class="sxs-lookup"><span data-stu-id="c98cd-133">Azure data set name</span></span>

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

### <span data-ttu-id="c98cd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98cd-134">-ResourceGroupName</span></span>
<span data-ttu-id="c98cd-135">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="c98cd-135">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c98cd-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c98cd-136">-ShareName</span></span>
<span data-ttu-id="c98cd-137">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="c98cd-137">Azure data share name</span></span>

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

### <span data-ttu-id="c98cd-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c98cd-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="c98cd-139">Azure Storage Account resourceId</span><span class="sxs-lookup"><span data-stu-id="c98cd-139">Azure storage account resourceId</span></span>

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

### <span data-ttu-id="c98cd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c98cd-140">-Confirm</span></span>
<span data-ttu-id="c98cd-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c98cd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c98cd-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c98cd-142">-WhatIf</span></span>
<span data-ttu-id="c98cd-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c98cd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c98cd-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c98cd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c98cd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98cd-145">CommonParameters</span></span>
<span data-ttu-id="c98cd-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98cd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98cd-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c98cd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98cd-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c98cd-148">INPUTS</span></span>

### <span data-ttu-id="c98cd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c98cd-149">System.String</span></span>

## <span data-ttu-id="c98cd-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c98cd-150">OUTPUTS</span></span>

### <span data-ttu-id="c98cd-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="c98cd-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="c98cd-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c98cd-152">NOTES</span></span>

## <span data-ttu-id="c98cd-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c98cd-153">RELATED LINKS</span></span>
