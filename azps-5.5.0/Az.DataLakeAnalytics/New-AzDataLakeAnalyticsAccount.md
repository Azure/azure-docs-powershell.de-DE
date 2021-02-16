---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170862"
---
# <span data-ttu-id="11bb1-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="11bb1-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="11bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="11bb1-103">Erstellt ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="11bb1-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="11bb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11bb1-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11bb1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="11bb1-106">Das **Cmdlet "New-AzDataLakeAnalyticsAccount"** erstellt ein Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="11bb1-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="11bb1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="11bb1-108">Beispiel 1: Erstellen eines Data Lake Analytics-Kontos</span><span class="sxs-lookup"><span data-stu-id="11bb1-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="11bb1-109">Mit diesem Befehl wird ein Data Lake Analytics-Konto namens "ContosoAdlAccount" erstellt, das den "ContosoAdlStore-Datenspeicher" in der Ressourcengruppe "ContosoOrg" verwendet.</span><span class="sxs-lookup"><span data-stu-id="11bb1-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="11bb1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11bb1-110">PARAMETERS</span></span>

### <span data-ttu-id="11bb1-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11bb1-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="11bb1-112">Gibt den Namen des Data Lake Store-Kontos an, das als Standarddatenquelle festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11bb1-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bb1-113">-DefaultProfile</span></span>
<span data-ttu-id="11bb1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="11bb1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11bb1-115">-Location</span><span class="sxs-lookup"><span data-stu-id="11bb1-115">-Location</span></span>
<span data-ttu-id="11bb1-116">Gibt den Speicherort an, an dem das Data Lake Analytics-Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11bb1-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="11bb1-117">Derzeit wird nur "USA 2, Osten" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11bb1-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="11bb1-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="11bb1-119">Die optional maximal unterstützten Analyseeinheiten für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="11bb1-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="11bb1-120">-MaxJobCount</span></span>
<span data-ttu-id="11bb1-121">Die optionalen maximal unterstützten Aufträge, die unter dem Konto gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="11bb1-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="11bb1-122">Ist keine angegeben, wird standardmäßig "3" verwendet.</span><span class="sxs-lookup"><span data-stu-id="11bb1-122">If none is specified, defaults to 3</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="11bb1-123">-Name</span></span>
<span data-ttu-id="11bb1-124">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="11bb1-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="11bb1-125">-QueryStoreRetention</span></span>
<span data-ttu-id="11bb1-126">Die optionale Anzahl von Tagen, in der Auftragsmetadaten aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="11bb1-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="11bb1-127">Ist keine Angabe angegeben, beträgt der Standardwert 30 Tage.</span><span class="sxs-lookup"><span data-stu-id="11bb1-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11bb1-128">-ResourceGroupName</span></span>
<span data-ttu-id="11bb1-129">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="11bb1-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="11bb1-130">Verwenden Sie zum Erstellen einer Ressourcengruppe das New-AzResourceGroup Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11bb1-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="11bb1-131">-Tag</span></span>
<span data-ttu-id="11bb1-132">Ein Zeichenfolgenverzeichnis der diesem Konto zugeordneten Tags</span><span class="sxs-lookup"><span data-stu-id="11bb1-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="11bb1-133">-Tier</span></span>
<span data-ttu-id="11bb1-134">Das gewünschte Verpflichtungsstufen für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="11bb1-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bb1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bb1-135">CommonParameters</span></span>
<span data-ttu-id="11bb1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11bb1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bb1-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11bb1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bb1-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11bb1-138">INPUTS</span></span>

### <span data-ttu-id="11bb1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="11bb1-139">System.String</span></span>

### <span data-ttu-id="11bb1-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="11bb1-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="11bb1-141">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11bb1-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="11bb1-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="11bb1-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="11bb1-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11bb1-143">OUTPUTS</span></span>

### <span data-ttu-id="11bb1-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="11bb1-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="11bb1-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="11bb1-145">NOTES</span></span>

## <span data-ttu-id="11bb1-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="11bb1-146">RELATED LINKS</span></span>

[<span data-ttu-id="11bb1-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="11bb1-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="11bb1-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="11bb1-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="11bb1-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="11bb1-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="11bb1-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="11bb1-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


