---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479294"
---
# <span data-ttu-id="34913-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="34913-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="34913-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34913-102">SYNOPSIS</span></span>
<span data-ttu-id="34913-103">Ändert ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="34913-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34913-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34913-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34913-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34913-105">DESCRIPTION</span></span>
<span data-ttu-id="34913-106">Das Cmdlet " **Satz-AzureRmDataLakeAnalyticsAccount** " ändert ein Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="34913-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="34913-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34913-107">EXAMPLES</span></span>

### <span data-ttu-id="34913-108">Beispiel 1: Ändern der Datenquelle eines Kontos</span><span class="sxs-lookup"><span data-stu-id="34913-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="34913-109">Mit diesem Befehl werden die Standarddatenquelle und die Tags-Eigenschaft des Kontos geändert.</span><span class="sxs-lookup"><span data-stu-id="34913-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="34913-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34913-110">PARAMETERS</span></span>

### <span data-ttu-id="34913-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="34913-111">-AllowAzureIpState</span></span>
<span data-ttu-id="34913-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="34913-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34913-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="34913-113">-FirewallState</span></span>
<span data-ttu-id="34913-114">Aktivieren/Deaktivieren Sie optional vorhandene Firewall-Regeln.</span><span class="sxs-lookup"><span data-stu-id="34913-114">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34913-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="34913-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="34913-116">Das optionale maximal unterstützte Maß an Parallelität zum Aktualisieren des Kontos mit.</span><span class="sxs-lookup"><span data-stu-id="34913-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="34913-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="34913-117">-MaxJobCount</span></span>
<span data-ttu-id="34913-118">Die optionalen maximal unterstützten Aufträge, die unter dem Konto zur gleichen Zeit ausgeführt werden, um Sie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="34913-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="34913-119">-Name</span><span class="sxs-lookup"><span data-stu-id="34913-119">-Name</span></span>
<span data-ttu-id="34913-120">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="34913-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="34913-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="34913-121">-QueryStoreRetention</span></span>
<span data-ttu-id="34913-122">Die optionale Anzahl von Tagen, für die Auftrags Metadaten aufbewahrt werden, um Sie im Konto festzulegen.</span><span class="sxs-lookup"><span data-stu-id="34913-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="34913-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34913-123">-ResourceGroupName</span></span>
<span data-ttu-id="34913-124">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="34913-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34913-125">-Tags</span><span class="sxs-lookup"><span data-stu-id="34913-125">-Tags</span></span>
<span data-ttu-id="34913-126">Gibt Schlüssel-Wert-Paare an, die verwendet werden können, um das Data Lake Analytics-Konto unter anderen Azure-Ressourcen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="34913-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34913-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="34913-127">-Tier</span></span>
<span data-ttu-id="34913-128">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="34913-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="34913-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34913-129">-DefaultProfile</span></span>
<span data-ttu-id="34913-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34913-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34913-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34913-131">CommonParameters</span></span>
<span data-ttu-id="34913-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34913-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34913-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34913-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34913-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34913-134">INPUTS</span></span>

## <span data-ttu-id="34913-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34913-135">OUTPUTS</span></span>

### <span data-ttu-id="34913-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="34913-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="34913-137">Die aktualisierten Kontodetails.</span><span class="sxs-lookup"><span data-stu-id="34913-137">The updated account details.</span></span>

## <span data-ttu-id="34913-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="34913-138">NOTES</span></span>

## <span data-ttu-id="34913-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34913-139">RELATED LINKS</span></span>

[<span data-ttu-id="34913-140">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="34913-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="34913-141">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="34913-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="34913-142">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="34913-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="34913-143">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="34913-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


