---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 9bb6475f0e9ea688c9339980c1a8955ea011fbb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661290"
---
# <span data-ttu-id="50752-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50752-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="50752-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50752-102">SYNOPSIS</span></span>
<span data-ttu-id="50752-103">Ändert ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="50752-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="50752-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50752-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50752-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50752-105">DESCRIPTION</span></span>
<span data-ttu-id="50752-106">Das Cmdlet " **Satz-AzDataLakeAnalyticsAccount** " ändert ein Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="50752-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="50752-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50752-107">EXAMPLES</span></span>

### <span data-ttu-id="50752-108">Beispiel 1: Ändern der Datenquelle eines Kontos</span><span class="sxs-lookup"><span data-stu-id="50752-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="50752-109">Mit diesem Befehl werden die Standarddatenquelle und die Tags-Eigenschaft des Kontos geändert.</span><span class="sxs-lookup"><span data-stu-id="50752-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="50752-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="50752-110">PARAMETERS</span></span>

### <span data-ttu-id="50752-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="50752-111">-AllowAzureIpState</span></span>
<span data-ttu-id="50752-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="50752-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="50752-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50752-113">-DefaultProfile</span></span>
<span data-ttu-id="50752-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="50752-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50752-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="50752-115">-FirewallState</span></span>
<span data-ttu-id="50752-116">Aktivieren/Deaktivieren Sie optional vorhandene Firewall-Regeln.</span><span class="sxs-lookup"><span data-stu-id="50752-116">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="50752-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="50752-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="50752-118">Die optionalen maximal unterstützten Analyseeinheiten für die Aktualisierung des Kontos.</span><span class="sxs-lookup"><span data-stu-id="50752-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="50752-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="50752-119">-MaxJobCount</span></span>
<span data-ttu-id="50752-120">Die optionalen maximal unterstützten Aufträge, die unter dem Konto zur gleichen Zeit ausgeführt werden, um Sie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="50752-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="50752-121">-Name</span><span class="sxs-lookup"><span data-stu-id="50752-121">-Name</span></span>
<span data-ttu-id="50752-122">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="50752-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="50752-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="50752-123">-QueryStoreRetention</span></span>
<span data-ttu-id="50752-124">Die optionale Anzahl von Tagen, für die Auftrags Metadaten aufbewahrt werden, um Sie im Konto festzulegen.</span><span class="sxs-lookup"><span data-stu-id="50752-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="50752-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50752-125">-ResourceGroupName</span></span>
<span data-ttu-id="50752-126">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="50752-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="50752-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="50752-127">-Tag</span></span>
<span data-ttu-id="50752-128">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die diesem Konto zugeordnet sind, das die aktuelle Gruppe von Tags ersetzen soll</span><span class="sxs-lookup"><span data-stu-id="50752-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

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

### <span data-ttu-id="50752-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="50752-129">-Tier</span></span>
<span data-ttu-id="50752-130">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="50752-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="50752-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50752-131">CommonParameters</span></span>
<span data-ttu-id="50752-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50752-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50752-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50752-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50752-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50752-134">INPUTS</span></span>

### <span data-ttu-id="50752-135">System. String</span><span class="sxs-lookup"><span data-stu-id="50752-135">System.String</span></span>

### <span data-ttu-id="50752-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50752-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="50752-137">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="50752-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="50752-138">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. tiertype, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="50752-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="50752-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="50752-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="50752-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="50752-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="50752-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50752-141">OUTPUTS</span></span>

### <span data-ttu-id="50752-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50752-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="50752-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="50752-143">NOTES</span></span>

## <span data-ttu-id="50752-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50752-144">RELATED LINKS</span></span>

[<span data-ttu-id="50752-145">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50752-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50752-146">Neu – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50752-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50752-147">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50752-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50752-148">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50752-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


