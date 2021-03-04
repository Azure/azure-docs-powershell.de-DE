---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 672286da502500101846d6fae694af059328c3cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922747"
---
# <span data-ttu-id="4dba0-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4dba0-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4dba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dba0-102">SYNOPSIS</span></span>
<span data-ttu-id="4dba0-103">Aktualisiert einen Back-End-Adresspool für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="4dba0-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="4dba0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dba0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dba0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dba0-105">DESCRIPTION</span></span>
<span data-ttu-id="4dba0-106">Das **Cmdlet Set-AzApplicationGatewayBackendAddressPool** aktualisiert einen Back-End-Adresspool für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="4dba0-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="4dba0-107">Back-End-Adressen können als IP-Adressen, vollqualifizierte Domänennamen (FQDN) oder IP-Konfigurations-IDs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4dba0-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="4dba0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4dba0-108">EXAMPLES</span></span>

### <span data-ttu-id="4dba0-109">Beispiel 1: Festlegen eines Back-End-Adresspools mithilfe von FQDNs</span><span class="sxs-lookup"><span data-stu-id="4dba0-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="4dba0-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="4dba0-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4dba0-111">Der zweite Befehl aktualisiert den Back-End-Adresspool des Anwendungsgateways in $AppGw mithilfe von FQDNs.</span><span class="sxs-lookup"><span data-stu-id="4dba0-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="4dba0-112">Beispiel 2: Festlegen eines Back-End-Adresspools mithilfe von Back-End-Server-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="4dba0-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="4dba0-113">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="4dba0-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4dba0-114">Der zweite Befehl aktualisiert den Back-End-Adresspool des Anwendungsgateways in $AppGw mithilfe von IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="4dba0-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="4dba0-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4dba0-115">PARAMETERS</span></span>

### <span data-ttu-id="4dba0-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dba0-116">-ApplicationGateway</span></span>
<span data-ttu-id="4dba0-117">Gibt das Anwendungsgateway an, dem dieses Cmdlet den Back-End-Adresspool zurät.</span><span class="sxs-lookup"><span data-stu-id="4dba0-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dba0-118">-Back-EndFqdns</span><span class="sxs-lookup"><span data-stu-id="4dba0-118">-BackendFqdns</span></span>
<span data-ttu-id="4dba0-119">Gibt eine Liste der Back-End-IP-Adressen an, die als Back-End-Serverpool verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dba0-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="4dba0-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="4dba0-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="4dba0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dba0-121">-DefaultProfile</span></span>
<span data-ttu-id="4dba0-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dba0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dba0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4dba0-123">-Name</span></span>
<span data-ttu-id="4dba0-124">Gibt den Namen des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="4dba0-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="4dba0-125">Dieser Back-End-Adresspool muss im Anwendungsgateway vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4dba0-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="4dba0-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4dba0-126">-Confirm</span></span>
<span data-ttu-id="4dba0-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dba0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dba0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dba0-128">-WhatIf</span></span>
<span data-ttu-id="4dba0-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dba0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dba0-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4dba0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dba0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dba0-131">CommonParameters</span></span>
<span data-ttu-id="4dba0-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dba0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dba0-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dba0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dba0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4dba0-134">INPUTS</span></span>

### <span data-ttu-id="4dba0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dba0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4dba0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4dba0-136">OUTPUTS</span></span>

### <span data-ttu-id="4dba0-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dba0-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4dba0-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4dba0-138">NOTES</span></span>

## <span data-ttu-id="4dba0-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4dba0-139">RELATED LINKS</span></span>

[<span data-ttu-id="4dba0-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4dba0-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4dba0-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4dba0-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4dba0-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4dba0-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4dba0-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4dba0-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


