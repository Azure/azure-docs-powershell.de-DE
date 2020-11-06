---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: f5be63987e055a7a7b6053820c22522bae021ad3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499957"
---
# <span data-ttu-id="52ff9-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52ff9-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="52ff9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="52ff9-103">Erstellt einen Back-End-Adresspool für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="52ff9-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ff9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52ff9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ff9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="52ff9-106">Das Cmdlet **New-AzureRmApplicationGatewayBackendAddressPool** erstellt einen Back-End-Adresspool für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="52ff9-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="52ff9-107">Eine Back-End-Adresse kann als IP-Adresse, als vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder als IP-Konfigurations-ID angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="52ff9-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="52ff9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52ff9-108">EXAMPLES</span></span>

### <span data-ttu-id="52ff9-109">Beispiel 1: Erstellen eines Back-End-Adresspools mithilfe des FQDN eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="52ff9-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="52ff9-110">Dieser Befehl erstellt einen Back-End-Adresspool mit dem Namen Pool01, indem die FQDNs von Back-End-Servern verwendet und in der $Pool-Variablen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="52ff9-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="52ff9-111">Beispiel 2: Erstellen eines Back-End-Adresspools mithilfe der IP-Adresse eines Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="52ff9-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="52ff9-112">Dieser Befehl erstellt einen Back-End-Adresspool mit dem Namen Pool02 unter Verwendung der IP-Adressen von Back-End-Servern und speichert ihn in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="52ff9-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="52ff9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="52ff9-113">PARAMETERS</span></span>

### <span data-ttu-id="52ff9-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="52ff9-114">-BackendFqdns</span></span>
<span data-ttu-id="52ff9-115">Gibt eine Liste der Back-End-FQDNs an, die dieses Cmdlet dem Back-End-Serverpool anordnet.</span><span class="sxs-lookup"><span data-stu-id="52ff9-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ff9-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="52ff9-116">-BackendIPAddresses</span></span>
<span data-ttu-id="52ff9-117">Gibt eine Liste der Back-End-IP-Adressen an, die von diesem Cmdlet dem Back-End-Serverpool zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="52ff9-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ff9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="52ff9-118">-Name</span></span>
<span data-ttu-id="52ff9-119">Gibt den Namen des vom Cmdlet erstellten Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="52ff9-119">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="52ff9-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52ff9-120">-Confirm</span></span>
<span data-ttu-id="52ff9-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52ff9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ff9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ff9-122">-WhatIf</span></span>
<span data-ttu-id="52ff9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52ff9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ff9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52ff9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ff9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ff9-125">-DefaultProfile</span></span>
<span data-ttu-id="52ff9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52ff9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52ff9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ff9-127">CommonParameters</span></span>
<span data-ttu-id="52ff9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ff9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ff9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ff9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ff9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52ff9-130">INPUTS</span></span>

### <span data-ttu-id="52ff9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="52ff9-131">System.String</span></span>

## <span data-ttu-id="52ff9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52ff9-132">OUTPUTS</span></span>

### <span data-ttu-id="52ff9-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52ff9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="52ff9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="52ff9-134">NOTES</span></span>

## <span data-ttu-id="52ff9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52ff9-135">RELATED LINKS</span></span>

[<span data-ttu-id="52ff9-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52ff9-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="52ff9-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52ff9-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="52ff9-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52ff9-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="52ff9-139">Satz-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52ff9-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


