---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 3d2110b4d8f4caf75751745ef996cb18094ae7e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501997"
---
# <span data-ttu-id="d64e1-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d64e1-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d64e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d64e1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d64e1-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="d64e1-103">SYNTAX</span></span>

### <span data-ttu-id="d64e1-104">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d64e1-104">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d64e1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d64e1-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d64e1-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d64e1-106">DESCRIPTION</span></span>

## <span data-ttu-id="d64e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d64e1-107">EXAMPLES</span></span>

### <span data-ttu-id="d64e1-108">1: setzen Sie</span><span class="sxs-lookup"><span data-stu-id="d64e1-108">1: Set</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
```

## <span data-ttu-id="d64e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d64e1-109">PARAMETERS</span></span>

### <span data-ttu-id="d64e1-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d64e1-110">-BackendPort</span></span>
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

### <span data-ttu-id="d64e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64e1-111">-DefaultProfile</span></span>
<span data-ttu-id="d64e1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d64e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d64e1-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d64e1-113">-EnableFloatingIP</span></span>
<span data-ttu-id="d64e1-114">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d64e1-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="d64e1-115">Diese Einstellung ist bei Verwendung der SQL AlwaysOn-Verfügbarkeitsgruppen in SQL Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d64e1-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="d64e1-116">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d64e1-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="d64e1-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d64e1-117">-EnableTcpReset</span></span>
<span data-ttu-id="d64e1-118">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="d64e1-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d64e1-119">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="d64e1-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d64e1-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d64e1-120">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="d64e1-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d64e1-121">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="d64e1-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="d64e1-122">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="d64e1-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="d64e1-123">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="d64e1-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d64e1-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d64e1-125">Das Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="d64e1-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="d64e1-126">Der Wert kann zwischen 4 und 30 Minuten eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d64e1-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="d64e1-127">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="d64e1-127">The default value is 4 minutes.</span></span> <span data-ttu-id="d64e1-128">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="d64e1-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d64e1-129">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d64e1-129">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d64e1-130">-Name</span><span class="sxs-lookup"><span data-stu-id="d64e1-130">-Name</span></span>
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

### <span data-ttu-id="d64e1-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d64e1-131">-Protocol</span></span>
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

### <span data-ttu-id="d64e1-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d64e1-132">-Confirm</span></span>
<span data-ttu-id="d64e1-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d64e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64e1-134">-WhatIf</span></span>
<span data-ttu-id="d64e1-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d64e1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d64e1-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d64e1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64e1-137">CommonParameters</span></span>
<span data-ttu-id="d64e1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64e1-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64e1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64e1-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d64e1-140">INPUTS</span></span>

### <span data-ttu-id="d64e1-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d64e1-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="d64e1-142">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d64e1-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="d64e1-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d64e1-143">OUTPUTS</span></span>

### <span data-ttu-id="d64e1-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d64e1-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d64e1-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d64e1-145">NOTES</span></span>

## <span data-ttu-id="d64e1-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d64e1-146">RELATED LINKS</span></span>

[<span data-ttu-id="d64e1-147">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d64e1-147">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d64e1-148">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d64e1-148">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d64e1-149">Neu – AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d64e1-149">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d64e1-150">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d64e1-150">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


