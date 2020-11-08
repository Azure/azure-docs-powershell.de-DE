---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009881"
---
# <span data-ttu-id="16123-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="16123-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="16123-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16123-102">SYNOPSIS</span></span>
<span data-ttu-id="16123-103">Erstellt eine Daten satzzuordnung für das Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16123-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="16123-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16123-104">SYNTAX</span></span>

### <span data-ttu-id="16123-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="16123-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16123-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="16123-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16123-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="16123-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16123-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16123-108">DESCRIPTION</span></span>
<span data-ttu-id="16123-109">Das Cmdlet **New-AzDataShareDataSetMapping** erstellt eine Daten satzzuordnung zwischen den Quelldatensätzen und dem empfängerspeicher Konto im Share-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16123-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="16123-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16123-110">EXAMPLES</span></span>

### <span data-ttu-id="16123-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16123-111">Example 1</span></span>
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

<span data-ttu-id="16123-112">Dieser Befehl erstellt eine Daten satzzuordnung AdsDataSetMapping zu Speicherkonto-AdsStorage für das Freigeben von Abonnement AdsShareSubscription in Datenfreigabe Konto WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="16123-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="16123-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="16123-113">PARAMETERS</span></span>

### <span data-ttu-id="16123-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="16123-114">-AccountName</span></span>
<span data-ttu-id="16123-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="16123-115">Azure data share account name</span></span>

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

### <span data-ttu-id="16123-116">-Container</span><span class="sxs-lookup"><span data-stu-id="16123-116">-Container</span></span>
<span data-ttu-id="16123-117">Name des Azure Storage-Konto Containers</span><span class="sxs-lookup"><span data-stu-id="16123-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="16123-118">-DataSet-Nr</span><span class="sxs-lookup"><span data-stu-id="16123-118">-DataSetId</span></span>
<span data-ttu-id="16123-119">Consumer-Daten Satz-ID</span><span class="sxs-lookup"><span data-stu-id="16123-119">Consumer data set id</span></span>

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

### <span data-ttu-id="16123-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16123-120">-DefaultProfile</span></span>
<span data-ttu-id="16123-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16123-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16123-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="16123-122">-FilePath</span></span>
<span data-ttu-id="16123-123">Azure Storage-Dateipfad</span><span class="sxs-lookup"><span data-stu-id="16123-123">Azure storage file path</span></span>

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

### <span data-ttu-id="16123-124">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="16123-124">-FileSystem</span></span>
<span data-ttu-id="16123-125">Azure ADLS Gen2 Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="16123-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="16123-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="16123-126">-FolderPath</span></span>
<span data-ttu-id="16123-127">Pfad des Azure-Speicherordners</span><span class="sxs-lookup"><span data-stu-id="16123-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="16123-128">-Name</span><span class="sxs-lookup"><span data-stu-id="16123-128">-Name</span></span>
<span data-ttu-id="16123-129">Name der Azure-Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="16123-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="16123-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16123-130">-ResourceGroupName</span></span>
<span data-ttu-id="16123-131">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="16123-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="16123-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="16123-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="16123-133">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="16123-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="16123-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="16123-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="16123-135">Azure Storage-Konto-Quell Code</span><span class="sxs-lookup"><span data-stu-id="16123-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="16123-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16123-136">-Confirm</span></span>
<span data-ttu-id="16123-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16123-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16123-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16123-138">-WhatIf</span></span>
<span data-ttu-id="16123-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16123-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16123-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16123-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16123-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16123-141">CommonParameters</span></span>
<span data-ttu-id="16123-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16123-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16123-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16123-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16123-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16123-144">INPUTS</span></span>

### <span data-ttu-id="16123-145">System. String</span><span class="sxs-lookup"><span data-stu-id="16123-145">System.String</span></span>

## <span data-ttu-id="16123-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16123-146">OUTPUTS</span></span>

### <span data-ttu-id="16123-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="16123-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="16123-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="16123-148">NOTES</span></span>

## <span data-ttu-id="16123-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16123-149">RELATED LINKS</span></span>
