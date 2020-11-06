---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504182"
---
# <span data-ttu-id="c9d0d-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c9d0d-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="c9d0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d0d-103">Erstellt ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9d0d-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d0d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9d0d-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d0d-106">Das Cmdlet **New-AzureRmDataLakeAnalyticsAccount** erstellt ein Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c9d0d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9d0d-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d0d-108">Beispiel 1: Erstellen eines Data Lake Analytics-Kontos</span><span class="sxs-lookup"><span data-stu-id="c9d0d-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="c9d0d-109">Mit diesem Befehl wird ein Data Lake Analytics-Konto mit dem Namen ContosoAdlAccount erstellt, das den ContosoAdlStore-Datenspeicher in der Ressourcengruppe namens ContosoOrg verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="c9d0d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9d0d-110">PARAMETERS</span></span>

### <span data-ttu-id="c9d0d-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c9d0d-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="c9d0d-112">Gibt den Namen des Daten Lake Store-Kontos an, das als Standarddatenquelle festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="c9d0d-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="c9d0d-113">-Location</span></span>
<span data-ttu-id="c9d0d-114">Gibt den Speicherort an, an dem das Data Lake Analytics-Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="c9d0d-115">Zurzeit wird nur East US 2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-115">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="c9d0d-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="c9d0d-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="c9d0d-117">Der optionale maximal unterstützte Grad an Parallelität für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="c9d0d-118">Wenn keine angegeben ist, wird standardmäßig 30 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-118">If none is specified, defaults to 30</span></span>

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

### <span data-ttu-id="c9d0d-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="c9d0d-119">-MaxJobCount</span></span>
<span data-ttu-id="c9d0d-120">Die optionalen maximal unterstützten Aufträge, die unter dem Konto gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="c9d0d-121">Wenn None angegeben ist, wird standardmäßig auf 3 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-121">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="c9d0d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c9d0d-122">-Name</span></span>
<span data-ttu-id="c9d0d-123">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-123">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c9d0d-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="c9d0d-124">-QueryStoreRetention</span></span>
<span data-ttu-id="c9d0d-125">Die optionale Anzahl von Tagen, an denen Auftrags Metadaten aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="c9d0d-126">Wenn keine angegeben wird, ist der Standardwert 30 Tage.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-126">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="c9d0d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d0d-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9d0d-128">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="c9d0d-129">Verwenden Sie das New-AzureRmResourceGroup-Cmdlet, um eine Ressourcengruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="c9d0d-130">-Tags</span><span class="sxs-lookup"><span data-stu-id="c9d0d-130">-Tags</span></span>
<span data-ttu-id="c9d0d-131">Gibt Schlüssel-Wert-Paare an, die verwendet werden können, um das Data Lake Analytics-Konto unter anderen Azure-Ressourcen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="c9d0d-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="c9d0d-132">-Tier</span></span>
<span data-ttu-id="c9d0d-133">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="c9d0d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d0d-134">-DefaultProfile</span></span>
<span data-ttu-id="c9d0d-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d0d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d0d-136">CommonParameters</span></span>
<span data-ttu-id="c9d0d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d0d-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d0d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d0d-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9d0d-139">INPUTS</span></span>

## <span data-ttu-id="c9d0d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9d0d-140">OUTPUTS</span></span>

### <span data-ttu-id="c9d0d-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c9d0d-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="c9d0d-142">Die Details des neu erstellten Kontos.</span><span class="sxs-lookup"><span data-stu-id="c9d0d-142">The details of the newly created account.</span></span>

## <span data-ttu-id="c9d0d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9d0d-143">NOTES</span></span>

## <span data-ttu-id="c9d0d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9d0d-144">RELATED LINKS</span></span>

[<span data-ttu-id="c9d0d-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c9d0d-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c9d0d-146">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c9d0d-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c9d0d-147">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c9d0d-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c9d0d-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c9d0d-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


