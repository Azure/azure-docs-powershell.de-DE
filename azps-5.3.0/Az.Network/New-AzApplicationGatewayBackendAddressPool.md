---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d44cf2faa4c7f50fcf1085fe528f638ba2e182df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379531"
---
# <span data-ttu-id="bca8a-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bca8a-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="bca8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bca8a-102">SYNOPSIS</span></span>
<span data-ttu-id="bca8a-103">Erstellt einen Back-End-Adresspool für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bca8a-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="bca8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bca8a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bca8a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bca8a-105">DESCRIPTION</span></span>
<span data-ttu-id="bca8a-106">Das **Cmdlet "New-AzApplicationGatewayBackendAddressPool"** erstellt einen Back-End-Adresspool für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bca8a-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="bca8a-107">Eine Back-End-Adresse kann als IP-Adresse, als vollqualifizierter Domänenname (Fully Qualified Domain Name, FQDN) oder als IP-Konfigurations-ID angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bca8a-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="bca8a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bca8a-108">EXAMPLES</span></span>

### <span data-ttu-id="bca8a-109">Beispiel 1: Erstellen eines Back-End-Adresspools mithilfe des FQDNs eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="bca8a-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="bca8a-110">Dieser Befehl erstellt mithilfe der FQDNs der Back-End-Server einen Back-End-Adresspool namens Pool01 und speichert ihn in der $Pool Variable.</span><span class="sxs-lookup"><span data-stu-id="bca8a-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="bca8a-111">Beispiel 2: Erstellen eines Back-End-Adresspools mithilfe der IP-Adresse eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="bca8a-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="bca8a-112">Dieser Befehl erstellt einen Back-End-Adresspool namens Pool02 unter Verwendung der IP-Adressen von Back-End-Servern und speichert ihn in der $Pool Variable.</span><span class="sxs-lookup"><span data-stu-id="bca8a-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="bca8a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bca8a-113">PARAMETERS</span></span>

### <span data-ttu-id="bca8a-114">-Back-EndFqdns</span><span class="sxs-lookup"><span data-stu-id="bca8a-114">-BackendFqdns</span></span>
<span data-ttu-id="bca8a-115">Gibt eine Liste der Back-End-FQDNs an, die dieses Cmdlet dem Back-End-Serverpool zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="bca8a-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca8a-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="bca8a-116">-BackendIPAddresses</span></span>
<span data-ttu-id="bca8a-117">Gibt eine Liste der Back-End-IP-Adressen an, die dieses Cmdlet dem Back-End-Serverpool zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="bca8a-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca8a-118">-DefaultProfile</span></span>
<span data-ttu-id="bca8a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bca8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bca8a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bca8a-120">-Name</span></span>
<span data-ttu-id="bca8a-121">Gibt den Namen des Back-End-Serverpools an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="bca8a-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bca8a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bca8a-122">-Confirm</span></span>
<span data-ttu-id="bca8a-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bca8a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca8a-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bca8a-124">-WhatIf</span></span>
<span data-ttu-id="bca8a-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bca8a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bca8a-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bca8a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca8a-127">CommonParameters</span></span>
<span data-ttu-id="bca8a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca8a-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca8a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca8a-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bca8a-130">INPUTS</span></span>

### <span data-ttu-id="bca8a-131">Keine</span><span class="sxs-lookup"><span data-stu-id="bca8a-131">None</span></span>

## <span data-ttu-id="bca8a-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bca8a-132">OUTPUTS</span></span>

### <span data-ttu-id="bca8a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bca8a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="bca8a-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bca8a-134">NOTES</span></span>

## <span data-ttu-id="bca8a-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bca8a-135">RELATED LINKS</span></span>

[<span data-ttu-id="bca8a-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bca8a-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bca8a-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bca8a-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bca8a-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bca8a-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bca8a-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bca8a-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


