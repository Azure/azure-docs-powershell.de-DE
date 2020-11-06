---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481274"
---
# <span data-ttu-id="6658a-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6658a-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="6658a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6658a-102">SYNOPSIS</span></span>
<span data-ttu-id="6658a-103">Erstellt ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="6658a-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6658a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6658a-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6658a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6658a-105">DESCRIPTION</span></span>
<span data-ttu-id="6658a-106">Das Cmdlet **New-AzureRmDataLakeAnalyticsAccount** erstellt ein Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="6658a-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6658a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6658a-107">EXAMPLES</span></span>

### <span data-ttu-id="6658a-108">Beispiel 1: Erstellen eines Data Lake Analytics-Kontos</span><span class="sxs-lookup"><span data-stu-id="6658a-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="6658a-109">Mit diesem Befehl wird ein Data Lake Analytics-Konto mit dem Namen ContosoAdlAccount erstellt, das den ContosoAdlStore-Datenspeicher in der Ressourcengruppe namens ContosoOrg verwendet.</span><span class="sxs-lookup"><span data-stu-id="6658a-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="6658a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6658a-110">PARAMETERS</span></span>

### <span data-ttu-id="6658a-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6658a-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="6658a-112">Gibt den Namen des Daten Lake Store-Kontos an, das als Standarddatenquelle festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6658a-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6658a-113">-DefaultProfile</span></span>
<span data-ttu-id="6658a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6658a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6658a-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="6658a-115">-Location</span></span>
<span data-ttu-id="6658a-116">Gibt den Speicherort an, an dem das Data Lake Analytics-Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6658a-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="6658a-117">Zurzeit wird nur East US 2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6658a-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="6658a-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="6658a-119">Die optionalen maximal unterstützten Analyseeinheiten für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="6658a-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="6658a-120">-MaxJobCount</span></span>
<span data-ttu-id="6658a-121">Die optionalen maximal unterstützten Aufträge, die unter dem Konto gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6658a-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="6658a-122">Wenn None angegeben ist, wird standardmäßig auf 3 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="6658a-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6658a-123">-Name</span></span>
<span data-ttu-id="6658a-124">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6658a-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="6658a-125">-QueryStoreRetention</span></span>
<span data-ttu-id="6658a-126">Die optionale Anzahl von Tagen, an denen Auftrags Metadaten aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="6658a-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="6658a-127">Wenn keine angegeben wird, ist der Standardwert 30 Tage.</span><span class="sxs-lookup"><span data-stu-id="6658a-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6658a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6658a-129">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6658a-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="6658a-130">Verwenden Sie das New-AzureRmResourceGroup-Cmdlet, um eine Ressourcengruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6658a-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="6658a-131">-Tag</span></span>
<span data-ttu-id="6658a-132">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die diesem Konto zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="6658a-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="6658a-133">-Tier</span></span>
<span data-ttu-id="6658a-134">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="6658a-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6658a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6658a-135">CommonParameters</span></span>
<span data-ttu-id="6658a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6658a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6658a-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6658a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6658a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6658a-138">INPUTS</span></span>

### <span data-ttu-id="6658a-139">Keine</span><span class="sxs-lookup"><span data-stu-id="6658a-139">None</span></span>
<span data-ttu-id="6658a-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6658a-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6658a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6658a-141">OUTPUTS</span></span>

### <span data-ttu-id="6658a-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6658a-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="6658a-143">Die Details des neu erstellten Kontos.</span><span class="sxs-lookup"><span data-stu-id="6658a-143">The details of the newly created account.</span></span>

## <span data-ttu-id="6658a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="6658a-144">NOTES</span></span>

## <span data-ttu-id="6658a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6658a-145">RELATED LINKS</span></span>

[<span data-ttu-id="6658a-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6658a-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6658a-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6658a-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6658a-148">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6658a-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6658a-149">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6658a-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


