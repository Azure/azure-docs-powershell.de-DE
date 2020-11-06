---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483017"
---
# <span data-ttu-id="66605-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="66605-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="66605-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66605-102">SYNOPSIS</span></span>
<span data-ttu-id="66605-103">Ändert ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="66605-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66605-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66605-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66605-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66605-105">DESCRIPTION</span></span>
<span data-ttu-id="66605-106">Das Cmdlet " **Satz-AzureRmDataLakeAnalyticsAccount** " ändert ein Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="66605-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="66605-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66605-107">EXAMPLES</span></span>

### <span data-ttu-id="66605-108">Beispiel 1: Ändern der Datenquelle eines Kontos</span><span class="sxs-lookup"><span data-stu-id="66605-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="66605-109">Mit diesem Befehl werden die Standarddatenquelle und die Tags-Eigenschaft des Kontos geändert.</span><span class="sxs-lookup"><span data-stu-id="66605-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="66605-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66605-110">PARAMETERS</span></span>

### <span data-ttu-id="66605-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="66605-111">-AllowAzureIpState</span></span>
<span data-ttu-id="66605-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="66605-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66605-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66605-113">-DefaultProfile</span></span>
<span data-ttu-id="66605-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="66605-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66605-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="66605-115">-FirewallState</span></span>
<span data-ttu-id="66605-116">Aktivieren/Deaktivieren Sie optional vorhandene Firewall-Regeln.</span><span class="sxs-lookup"><span data-stu-id="66605-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66605-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="66605-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="66605-118">Die optionalen maximal unterstützten Analyseeinheiten für die Aktualisierung des Kontos.</span><span class="sxs-lookup"><span data-stu-id="66605-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="66605-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="66605-119">-MaxJobCount</span></span>
<span data-ttu-id="66605-120">Die optionalen maximal unterstützten Aufträge, die unter dem Konto zur gleichen Zeit ausgeführt werden, um Sie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="66605-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="66605-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66605-121">-Name</span></span>
<span data-ttu-id="66605-122">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="66605-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="66605-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="66605-123">-QueryStoreRetention</span></span>
<span data-ttu-id="66605-124">Die optionale Anzahl von Tagen, für die Auftrags Metadaten aufbewahrt werden, um Sie im Konto festzulegen.</span><span class="sxs-lookup"><span data-stu-id="66605-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="66605-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66605-125">-ResourceGroupName</span></span>
<span data-ttu-id="66605-126">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="66605-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66605-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="66605-127">-Tag</span></span>
<span data-ttu-id="66605-128">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die diesem Konto zugeordnet sind, das die aktuelle Gruppe von Tags ersetzen soll</span><span class="sxs-lookup"><span data-stu-id="66605-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66605-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="66605-129">-Tier</span></span>
<span data-ttu-id="66605-130">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="66605-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="66605-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66605-131">CommonParameters</span></span>
<span data-ttu-id="66605-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66605-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66605-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66605-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66605-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66605-134">INPUTS</span></span>

### <span data-ttu-id="66605-135">Keine</span><span class="sxs-lookup"><span data-stu-id="66605-135">None</span></span>
<span data-ttu-id="66605-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="66605-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66605-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66605-137">OUTPUTS</span></span>

### <span data-ttu-id="66605-138">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="66605-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="66605-139">Die aktualisierten Kontodetails.</span><span class="sxs-lookup"><span data-stu-id="66605-139">The updated account details.</span></span>

## <span data-ttu-id="66605-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="66605-140">NOTES</span></span>

## <span data-ttu-id="66605-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66605-141">RELATED LINKS</span></span>

[<span data-ttu-id="66605-142">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="66605-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="66605-143">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="66605-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="66605-144">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="66605-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="66605-145">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="66605-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


