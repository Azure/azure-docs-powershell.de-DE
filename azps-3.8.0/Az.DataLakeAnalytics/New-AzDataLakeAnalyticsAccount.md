---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995544"
---
# <span data-ttu-id="ec966-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ec966-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ec966-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec966-102">SYNOPSIS</span></span>
<span data-ttu-id="ec966-103">Erstellt ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="ec966-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ec966-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec966-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec966-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec966-105">DESCRIPTION</span></span>
<span data-ttu-id="ec966-106">Das Cmdlet **New-AzDataLakeAnalyticsAccount** erstellt ein Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="ec966-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ec966-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec966-107">EXAMPLES</span></span>

### <span data-ttu-id="ec966-108">Beispiel 1: Erstellen eines Data Lake Analytics-Kontos</span><span class="sxs-lookup"><span data-stu-id="ec966-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="ec966-109">Mit diesem Befehl wird ein Data Lake Analytics-Konto mit dem Namen ContosoAdlAccount erstellt, das den ContosoAdlStore-Datenspeicher in der Ressourcengruppe namens ContosoOrg verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec966-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="ec966-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec966-110">PARAMETERS</span></span>

### <span data-ttu-id="ec966-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec966-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="ec966-112">Gibt den Namen des Daten Lake Store-Kontos an, das als Standarddatenquelle festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec966-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="ec966-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec966-113">-DefaultProfile</span></span>
<span data-ttu-id="ec966-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ec966-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec966-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="ec966-115">-Location</span></span>
<span data-ttu-id="ec966-116">Gibt den Speicherort an, an dem das Data Lake Analytics-Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec966-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="ec966-117">Zurzeit wird nur East US 2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec966-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="ec966-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="ec966-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="ec966-119">Die optionalen maximal unterstützten Analyseeinheiten für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="ec966-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="ec966-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="ec966-120">-MaxJobCount</span></span>
<span data-ttu-id="ec966-121">Die optionalen maximal unterstützten Aufträge, die unter dem Konto gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec966-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="ec966-122">Wenn None angegeben ist, wird standardmäßig auf 3 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ec966-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="ec966-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ec966-123">-Name</span></span>
<span data-ttu-id="ec966-124">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ec966-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ec966-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="ec966-125">-QueryStoreRetention</span></span>
<span data-ttu-id="ec966-126">Die optionale Anzahl von Tagen, an denen Auftrags Metadaten aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="ec966-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="ec966-127">Wenn keine angegeben wird, ist der Standardwert 30 Tage.</span><span class="sxs-lookup"><span data-stu-id="ec966-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="ec966-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec966-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec966-129">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ec966-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="ec966-130">Verwenden Sie das New-AzResourceGroup-Cmdlet, um eine Ressourcengruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec966-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="ec966-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec966-131">-Tag</span></span>
<span data-ttu-id="ec966-132">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die diesem Konto zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="ec966-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="ec966-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="ec966-133">-Tier</span></span>
<span data-ttu-id="ec966-134">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="ec966-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ec966-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec966-135">CommonParameters</span></span>
<span data-ttu-id="ec966-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec966-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec966-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec966-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec966-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec966-138">INPUTS</span></span>

### <span data-ttu-id="ec966-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ec966-139">System.String</span></span>

### <span data-ttu-id="ec966-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ec966-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ec966-141">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec966-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec966-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. tiertype, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ec966-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ec966-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec966-143">OUTPUTS</span></span>

### <span data-ttu-id="ec966-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ec966-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ec966-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec966-145">NOTES</span></span>

## <span data-ttu-id="ec966-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec966-146">RELATED LINKS</span></span>

[<span data-ttu-id="ec966-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ec966-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ec966-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ec966-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ec966-149">Satz-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ec966-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ec966-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ec966-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


