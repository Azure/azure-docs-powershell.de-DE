---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 097377cd1ca4cb4be4fe62e2008f899c05c194fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504342"
---
# <span data-ttu-id="c4746-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c4746-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c4746-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4746-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4746-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4746-103">SYNTAX</span></span>

### <span data-ttu-id="c4746-104">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4746-104">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4746-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4746-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4746-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4746-106">DESCRIPTION</span></span>

## <span data-ttu-id="c4746-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4746-107">EXAMPLES</span></span>

### <span data-ttu-id="c4746-108">1: neu</span><span class="sxs-lookup"><span data-stu-id="c4746-108">1: New</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="c4746-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4746-109">PARAMETERS</span></span>

### <span data-ttu-id="c4746-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c4746-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4746-111">-DefaultProfile</span></span>
<span data-ttu-id="c4746-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4746-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4746-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c4746-113">-EnableFloatingIP</span></span>
<span data-ttu-id="c4746-114">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c4746-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="c4746-115">Diese Einstellung ist bei Verwendung der SQL AlwaysOn-Verfügbarkeitsgruppen in SQL Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4746-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="c4746-116">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c4746-116">This setting can't be changed after you create the endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c4746-117">-EnableTcpReset</span></span>
<span data-ttu-id="c4746-118">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="c4746-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c4746-119">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c4746-119">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4746-120">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c4746-121">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c4746-122">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="c4746-123">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c4746-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c4746-125">Das Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="c4746-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="c4746-126">Der Wert kann zwischen 4 und 30 Minuten eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c4746-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="c4746-127">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="c4746-127">The default value is 4 minutes.</span></span> <span data-ttu-id="c4746-128">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c4746-128">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c4746-129">-Name</span></span>
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

### <span data-ttu-id="c4746-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c4746-130">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4746-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4746-131">-Confirm</span></span>
<span data-ttu-id="c4746-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4746-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4746-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4746-133">-WhatIf</span></span>
<span data-ttu-id="c4746-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4746-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4746-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4746-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4746-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4746-136">CommonParameters</span></span>
<span data-ttu-id="c4746-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4746-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4746-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4746-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4746-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4746-139">INPUTS</span></span>

### <span data-ttu-id="c4746-140">Keine</span><span class="sxs-lookup"><span data-stu-id="c4746-140">None</span></span>

## <span data-ttu-id="c4746-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4746-141">OUTPUTS</span></span>

### <span data-ttu-id="c4746-142">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="c4746-142">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="c4746-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4746-143">NOTES</span></span>

## <span data-ttu-id="c4746-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4746-144">RELATED LINKS</span></span>
