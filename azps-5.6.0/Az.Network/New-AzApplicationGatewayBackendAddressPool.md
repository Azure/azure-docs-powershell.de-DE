---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 3ce9cb761bb945c777a39e728ac8ebea2c40b885
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947792"
---
# <span data-ttu-id="4f4e2-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f4e2-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4f4e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4e2-103">Erstellt einen Back-End-Adresspool für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="4f4e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f4e2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f4e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="4f4e2-106">Das **Cmdlet New-AzApplicationGatewayBackendAddressPool** erstellt einen Back-End-Adresspool für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="4f4e2-107">Eine Back-End-Adresse kann als IP-Adresse, als vollqualifizierter Domänenname (FQDN) oder als IP-Konfigurations-ID angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="4f4e2-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f4e2-108">EXAMPLES</span></span>

### <span data-ttu-id="4f4e2-109">Beispiel 1: Erstellen eines Back-End-Adresspools mithilfe des FQDNs eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="4f4e2-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="4f4e2-110">Mit diesem Befehl wird ein Back-End-Adresspool namens Pool01 mithilfe der FQDNs von Back-End-Servern erstellt und in der $Pool gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="4f4e2-111">Beispiel 2: Erstellen eines Back-End-Adresspools mithilfe der IP-Adresse eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="4f4e2-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="4f4e2-112">Mit diesem Befehl wird ein Back-End-Adresspool namens Pool02 mithilfe der IP-Adressen von Back-End-Servern erstellt und in der $Pool gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="4f4e2-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4f4e2-113">PARAMETERS</span></span>

### <span data-ttu-id="4f4e2-114">-Back-EndFqdns</span><span class="sxs-lookup"><span data-stu-id="4f4e2-114">-BackendFqdns</span></span>
<span data-ttu-id="4f4e2-115">Gibt eine Liste der Back-End-FQDNs an, die dieses Cmdlet dem Back-End-Serverpool zurät.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="4f4e2-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="4f4e2-116">-BackendIPAddresses</span></span>
<span data-ttu-id="4f4e2-117">Gibt eine Liste der Back-End-IP-Adressen an, die dieses Cmdlet mit dem Back-End-Serverpool verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="4f4e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4e2-118">-DefaultProfile</span></span>
<span data-ttu-id="4f4e2-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f4e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4f4e2-120">-Name</span></span>
<span data-ttu-id="4f4e2-121">Gibt den Namen des Back-End-Serverpools an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4f4e2-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f4e2-122">-Confirm</span></span>
<span data-ttu-id="4f4e2-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f4e2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f4e2-124">-WhatIf</span></span>
<span data-ttu-id="4f4e2-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f4e2-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f4e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4e2-127">CommonParameters</span></span>
<span data-ttu-id="4f4e2-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f4e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4e2-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4e2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4e2-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f4e2-130">INPUTS</span></span>

### <span data-ttu-id="4f4e2-131">Keine</span><span class="sxs-lookup"><span data-stu-id="4f4e2-131">None</span></span>

## <span data-ttu-id="4f4e2-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f4e2-132">OUTPUTS</span></span>

### <span data-ttu-id="4f4e2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f4e2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4f4e2-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4f4e2-134">NOTES</span></span>

## <span data-ttu-id="4f4e2-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4f4e2-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f4e2-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f4e2-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4f4e2-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f4e2-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4f4e2-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f4e2-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4f4e2-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f4e2-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


