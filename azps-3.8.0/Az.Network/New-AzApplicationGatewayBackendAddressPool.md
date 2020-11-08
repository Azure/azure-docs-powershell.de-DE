---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d44cf2faa4c7f50fcf1085fe528f638ba2e182df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005049"
---
# <span data-ttu-id="39339-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39339-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="39339-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39339-102">SYNOPSIS</span></span>
<span data-ttu-id="39339-103">Erstellt einen Back-End-Adresspool für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="39339-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="39339-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39339-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39339-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39339-105">DESCRIPTION</span></span>
<span data-ttu-id="39339-106">Das Cmdlet **New-AzApplicationGatewayBackendAddressPool** erstellt einen Back-End-Adresspool für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="39339-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="39339-107">Eine Back-End-Adresse kann als IP-Adresse, als vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder als IP-Konfigurations-ID angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="39339-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="39339-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39339-108">EXAMPLES</span></span>

### <span data-ttu-id="39339-109">Beispiel 1: Erstellen eines Back-End-Adresspools mithilfe des FQDN eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="39339-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="39339-110">Dieser Befehl erstellt einen Back-End-Adresspool mit dem Namen Pool01, indem die FQDNs von Back-End-Servern verwendet und in der $Pool-Variablen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="39339-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="39339-111">Beispiel 2: Erstellen eines Back-End-Adresspools mithilfe der IP-Adresse eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="39339-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="39339-112">Dieser Befehl erstellt einen Back-End-Adresspool mit dem Namen Pool02 unter Verwendung der IP-Adressen von Back-End-Servern und speichert ihn in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="39339-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="39339-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="39339-113">PARAMETERS</span></span>

### <span data-ttu-id="39339-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="39339-114">-BackendFqdns</span></span>
<span data-ttu-id="39339-115">Gibt eine Liste der Back-End-FQDNs an, die dieses Cmdlet dem Back-End-Serverpool anordnet.</span><span class="sxs-lookup"><span data-stu-id="39339-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="39339-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="39339-116">-BackendIPAddresses</span></span>
<span data-ttu-id="39339-117">Gibt eine Liste der Back-End-IP-Adressen an, die von diesem Cmdlet dem Back-End-Serverpool zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="39339-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="39339-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39339-118">-DefaultProfile</span></span>
<span data-ttu-id="39339-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39339-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39339-120">-Name</span><span class="sxs-lookup"><span data-stu-id="39339-120">-Name</span></span>
<span data-ttu-id="39339-121">Gibt den Namen des vom Cmdlet erstellten Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="39339-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="39339-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39339-122">-Confirm</span></span>
<span data-ttu-id="39339-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39339-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39339-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39339-124">-WhatIf</span></span>
<span data-ttu-id="39339-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39339-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39339-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39339-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39339-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39339-127">CommonParameters</span></span>
<span data-ttu-id="39339-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39339-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39339-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39339-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39339-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39339-130">INPUTS</span></span>

### <span data-ttu-id="39339-131">Keine</span><span class="sxs-lookup"><span data-stu-id="39339-131">None</span></span>

## <span data-ttu-id="39339-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39339-132">OUTPUTS</span></span>

### <span data-ttu-id="39339-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39339-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="39339-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="39339-134">NOTES</span></span>

## <span data-ttu-id="39339-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39339-135">RELATED LINKS</span></span>

[<span data-ttu-id="39339-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39339-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="39339-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39339-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="39339-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39339-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="39339-139">Satz-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39339-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


