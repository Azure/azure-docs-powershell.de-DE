---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995720"
---
# <span data-ttu-id="978b6-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="978b6-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="978b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="978b6-102">SYNOPSIS</span></span>
<span data-ttu-id="978b6-103">Erstellen Sie eine Protokollkonfiguration, die zum Durchführen einer Testauswertung über TCP, http oder ICMP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="978b6-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="978b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="978b6-104">SYNTAX</span></span>

### <span data-ttu-id="978b6-105">TCP</span><span class="sxs-lookup"><span data-stu-id="978b6-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="978b6-106">HTTP</span><span class="sxs-lookup"><span data-stu-id="978b6-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="978b6-107">ICMP</span><span class="sxs-lookup"><span data-stu-id="978b6-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="978b6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="978b6-108">DESCRIPTION</span></span>
<span data-ttu-id="978b6-109">Das New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject-Cmdlet erstellt eine Protokollkonfiguration, die zum Durchführen einer Testauswertung über TCP, http oder ICMP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="978b6-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="978b6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="978b6-110">EXAMPLES</span></span>

### <span data-ttu-id="978b6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="978b6-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="978b6-112">Port: 80 DisableTraceRoute: falsch</span><span class="sxs-lookup"><span data-stu-id="978b6-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="978b6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="978b6-113">PARAMETERS</span></span>

### <span data-ttu-id="978b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978b6-114">-DefaultProfile</span></span>
<span data-ttu-id="978b6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="978b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978b6-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="978b6-116">-DisableTraceRoute</span></span>
<span data-ttu-id="978b6-117">Wert, der angibt, ob die Pfad Auswertung mit Ablauf Verfolgungs Route deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="978b6-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="978b6-118">-HttpProtocol</span></span>
<span data-ttu-id="978b6-119">HTTP-Protokollschalter</span><span class="sxs-lookup"><span data-stu-id="978b6-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="978b6-120">-IcmpProtocol</span></span>
<span data-ttu-id="978b6-121">ICMP-Protokollschalter</span><span class="sxs-lookup"><span data-stu-id="978b6-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-122">-Methode</span><span class="sxs-lookup"><span data-stu-id="978b6-122">-Method</span></span>
<span data-ttu-id="978b6-123">Die zu verwendende HTTP-Methode.</span><span class="sxs-lookup"><span data-stu-id="978b6-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-124">-Path</span><span class="sxs-lookup"><span data-stu-id="978b6-124">-Path</span></span>
<span data-ttu-id="978b6-125">Die Path-Komponente des URIs.</span><span class="sxs-lookup"><span data-stu-id="978b6-125">The path component of the URI.</span></span> <span data-ttu-id="978b6-126">Beispiel: \" /dir1/dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="978b6-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-127">-Port</span><span class="sxs-lookup"><span data-stu-id="978b6-127">-Port</span></span>
<span data-ttu-id="978b6-128">Der Port, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="978b6-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="978b6-129">-PreferHTTPS</span></span>
<span data-ttu-id="978b6-130">Wert, der angibt, ob HTTPS über HTTP bevorzugt wird, wenn die Auswahl nicht explizit ist.</span><span class="sxs-lookup"><span data-stu-id="978b6-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="978b6-131">-RequestHeader</span></span>
<span data-ttu-id="978b6-132">Die HTTP-Header, die mit der Anforderung übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="978b6-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="978b6-133">-TcpProtocol</span></span>
<span data-ttu-id="978b6-134">TCP-Protokollschalter</span><span class="sxs-lookup"><span data-stu-id="978b6-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="978b6-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="978b6-136">HTTP-Statuscodes, um erfolgreich zu sein.</span><span class="sxs-lookup"><span data-stu-id="978b6-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="978b6-137">Beispielsweise \" 2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="978b6-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978b6-138">CommonParameters</span></span>
<span data-ttu-id="978b6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978b6-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="978b6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978b6-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="978b6-141">INPUTS</span></span>

### <span data-ttu-id="978b6-142">Keine</span><span class="sxs-lookup"><span data-stu-id="978b6-142">None</span></span>

## <span data-ttu-id="978b6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="978b6-143">OUTPUTS</span></span>

### <span data-ttu-id="978b6-144">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="978b6-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="978b6-145">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="978b6-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="978b6-146">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="978b6-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="978b6-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="978b6-147">NOTES</span></span>

## <span data-ttu-id="978b6-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="978b6-148">RELATED LINKS</span></span>
