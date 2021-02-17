---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169817"
---
# <span data-ttu-id="b07c7-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b07c7-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="b07c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b07c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b07c7-103">Erstellen Sie eine Testkonfiguration für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="b07c7-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="b07c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b07c7-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b07c7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b07c7-105">DESCRIPTION</span></span>
<span data-ttu-id="b07c7-106">Das New-AzNetworkWatcherConnectionMonitorTestConfigurationObject erstellt eine Testkonfiguration für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="b07c7-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="b07c7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b07c7-107">EXAMPLES</span></span>

### <span data-ttu-id="b07c7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b07c7-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="b07c7-109">Name: httpTC TestFrequencySec : 120 PreferredIPVersion : ProtocolConfiguration : { "Port": 443, "Methode": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span><span class="sxs-lookup"><span data-stu-id="b07c7-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="b07c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b07c7-110">PARAMETERS</span></span>

### <span data-ttu-id="b07c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07c7-111">-DefaultProfile</span></span>
<span data-ttu-id="b07c7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07c7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b07c7-113">-Name</span></span>
<span data-ttu-id="b07c7-114">Der Name der Testkonfiguration des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="b07c7-114">The name of the connection monitor test configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07c7-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="b07c7-115">-PreferredIPVersion</span></span>
<span data-ttu-id="b07c7-116">Die bevorzugte IP-Version, die bei der Testauswertung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b07c7-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="b07c7-117">Je nach anderen Parametern kann der Verbindungsmonitor eine andere Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="b07c7-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07c7-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b07c7-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="b07c7-119">Die Parameter, die für die Testauswertung über ein Protokoll verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07c7-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07c7-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="b07c7-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="b07c7-121">Der maximale Prozentsatz der fehlgeschlagenen Prüfungen, der für einen Test als erfolgreich ausgewertet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b07c7-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07c7-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="b07c7-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="b07c7-123">Die maximale Roundtripzeit in Millisekunden, die für einen Test als erfolgreich ausgewertet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b07c7-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07c7-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="b07c7-124">-TestFrequencySec</span></span>
<span data-ttu-id="b07c7-125">Die Häufigkeit der Testauswertung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b07c7-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07c7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b07c7-126">-Confirm</span></span>
<span data-ttu-id="b07c7-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b07c7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07c7-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b07c7-128">-WhatIf</span></span>
<span data-ttu-id="b07c7-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b07c7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07c7-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b07c7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07c7-131">CommonParameters</span></span>
<span data-ttu-id="b07c7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07c7-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b07c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07c7-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b07c7-134">INPUTS</span></span>

### <span data-ttu-id="b07c7-135">Keine</span><span class="sxs-lookup"><span data-stu-id="b07c7-135">None</span></span>

## <span data-ttu-id="b07c7-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b07c7-136">OUTPUTS</span></span>

### <span data-ttu-id="b07c7-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b07c7-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="b07c7-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b07c7-138">NOTES</span></span>

## <span data-ttu-id="b07c7-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b07c7-139">RELATED LINKS</span></span>
