---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302710"
---
# <span data-ttu-id="59b2f-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="59b2f-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="59b2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="59b2f-103">Erstellen Sie eine Testkonfiguration für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="59b2f-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="59b2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59b2f-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59b2f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="59b2f-106">Das New-AzNetworkWatcherConnectionMonitorTestConfigurationObject-Cmdlet erstellt eine Testkonfiguration für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="59b2f-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="59b2f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="59b2f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59b2f-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="59b2f-109">Name: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"Port": 443; "Methode": "Get"; "RequestHeaders": [{"Name": "Allow"; "Wert": "Get"}], "ValidStatusCodeRanges": ["2xx"; "300-308"], "PreferHTTPS": true} SuccessThreshold: {"ChecksFailedPercent": "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="59b2f-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="59b2f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="59b2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b2f-111">-DefaultProfile</span></span>
<span data-ttu-id="59b2f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59b2f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59b2f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="59b2f-113">-Name</span></span>
<span data-ttu-id="59b2f-114">Der Name der Testkonfiguration des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="59b2f-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="59b2f-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="59b2f-115">-PreferredIPVersion</span></span>
<span data-ttu-id="59b2f-116">Die bevorzugte IP-Version, die Sie in der Testauswertung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="59b2f-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="59b2f-117">Der Verbindungsmonitor kann je nach anderen Parametern eine andere Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="59b2f-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="59b2f-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b2f-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="59b2f-119">Die Parameter, die zum Durchführen einer Testauswertung über ein Protokoll verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59b2f-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="59b2f-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="59b2f-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="59b2f-121">Der maximale Prozentsatz der fehlgeschlagenen Prüfungen, die für einen Test als erfolgreich ausgewertet werden können.</span><span class="sxs-lookup"><span data-stu-id="59b2f-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="59b2f-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="59b2f-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="59b2f-123">Die maximale Roundtrip-Zeit in Millisekunden, die für einen Test als erfolgreich ausgewertet werden darf.</span><span class="sxs-lookup"><span data-stu-id="59b2f-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="59b2f-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="59b2f-124">-TestFrequencySec</span></span>
<span data-ttu-id="59b2f-125">Die Häufigkeit der Testauswertung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="59b2f-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="59b2f-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59b2f-126">-Confirm</span></span>
<span data-ttu-id="59b2f-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59b2f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b2f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b2f-128">-WhatIf</span></span>
<span data-ttu-id="59b2f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59b2f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b2f-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59b2f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b2f-131">CommonParameters</span></span>
<span data-ttu-id="59b2f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b2f-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59b2f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b2f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59b2f-134">INPUTS</span></span>

### <span data-ttu-id="59b2f-135">Keine</span><span class="sxs-lookup"><span data-stu-id="59b2f-135">None</span></span>

## <span data-ttu-id="59b2f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59b2f-136">OUTPUTS</span></span>

### <span data-ttu-id="59b2f-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="59b2f-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="59b2f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="59b2f-138">NOTES</span></span>

## <span data-ttu-id="59b2f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59b2f-139">RELATED LINKS</span></span>
