---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d44cf2faa4c7f50fcf1085fe528f638ba2e182df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169949"
---
# <span data-ttu-id="5ff67-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ff67-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="5ff67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ff67-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff67-103">Erstellt einen Back-End-Adresspool für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5ff67-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="5ff67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ff67-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ff67-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ff67-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff67-106">Das **Cmdlet "New-AzApplicationGatewayBackendAddressPool"** erstellt einen Back-End-Adresspool für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5ff67-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="5ff67-107">Eine Back-End-Adresse kann als IP-Adresse, als vollqualifizierter Domänenname (Fully Qualified Domain Name, FQDN) oder als IP-Konfigurations-ID angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5ff67-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="5ff67-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ff67-108">EXAMPLES</span></span>

### <span data-ttu-id="5ff67-109">Beispiel 1: Erstellen eines Back-End-Adresspools mithilfe des FQDNs eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="5ff67-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="5ff67-110">Dieser Befehl erstellt mithilfe der FQDNs der Back-End-Server einen Back-End-Adresspool namens Pool01 und speichert ihn in der $Pool Variable.</span><span class="sxs-lookup"><span data-stu-id="5ff67-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="5ff67-111">Beispiel 2: Erstellen eines Back-End-Adresspools mithilfe der IP-Adresse eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="5ff67-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="5ff67-112">Dieser Befehl erstellt einen Back-End-Adresspool namens Pool02 unter Verwendung der IP-Adressen von Back-End-Servern und speichert ihn in der $Pool Variable.</span><span class="sxs-lookup"><span data-stu-id="5ff67-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="5ff67-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ff67-113">PARAMETERS</span></span>

### <span data-ttu-id="5ff67-114">-Back-EndFqdns</span><span class="sxs-lookup"><span data-stu-id="5ff67-114">-BackendFqdns</span></span>
<span data-ttu-id="5ff67-115">Gibt eine Liste der Back-End-FQDNs an, die dieses Cmdlet dem Back-End-Serverpool zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="5ff67-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="5ff67-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="5ff67-116">-BackendIPAddresses</span></span>
<span data-ttu-id="5ff67-117">Gibt eine Liste der Back-End-IP-Adressen an, die dieses Cmdlet dem Back-End-Serverpool zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="5ff67-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="5ff67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff67-118">-DefaultProfile</span></span>
<span data-ttu-id="5ff67-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ff67-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ff67-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5ff67-120">-Name</span></span>
<span data-ttu-id="5ff67-121">Gibt den Namen des Back-End-Serverpools an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ff67-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ff67-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ff67-122">-Confirm</span></span>
<span data-ttu-id="5ff67-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ff67-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff67-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5ff67-124">-WhatIf</span></span>
<span data-ttu-id="5ff67-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ff67-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff67-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ff67-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff67-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff67-127">CommonParameters</span></span>
<span data-ttu-id="5ff67-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff67-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff67-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff67-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff67-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ff67-130">INPUTS</span></span>

### <span data-ttu-id="5ff67-131">Keine</span><span class="sxs-lookup"><span data-stu-id="5ff67-131">None</span></span>

## <span data-ttu-id="5ff67-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ff67-132">OUTPUTS</span></span>

### <span data-ttu-id="5ff67-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ff67-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="5ff67-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5ff67-134">NOTES</span></span>

## <span data-ttu-id="5ff67-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5ff67-135">RELATED LINKS</span></span>

[<span data-ttu-id="5ff67-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ff67-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="5ff67-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ff67-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="5ff67-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ff67-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="5ff67-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ff67-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


