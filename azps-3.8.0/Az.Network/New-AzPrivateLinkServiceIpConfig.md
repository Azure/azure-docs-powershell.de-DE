---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: e1d7c2d78bf58240cc87e7a224be1632828984d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003463"
---
# <span data-ttu-id="2f7db-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2f7db-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="2f7db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f7db-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7db-103">Erstellen einer IP-Konfiguration für einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="2f7db-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="2f7db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f7db-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f7db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f7db-105">DESCRIPTION</span></span>
<span data-ttu-id="2f7db-106">Das Cmdlet **New-AzPrivateLinkServiceIpConfig** erstellt eine IP-Konfiguration des privaten Verbindungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="2f7db-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="2f7db-107">Diese Konfiguration wird für die Quell-NAT verwendet, um den eingehenden Datenverkehr vom privaten Endpunkt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f7db-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="2f7db-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f7db-108">EXAMPLES</span></span>

### <span data-ttu-id="2f7db-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f7db-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="2f7db-110">In diesem Beispiel wird eine private Link Service-IP-Konfiguration im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="2f7db-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="2f7db-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f7db-111">PARAMETERS</span></span>

### <span data-ttu-id="2f7db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7db-112">-DefaultProfile</span></span>
<span data-ttu-id="2f7db-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f7db-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f7db-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2f7db-114">-Name</span></span>
<span data-ttu-id="2f7db-115">Der Name des IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="2f7db-115">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="2f7db-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2f7db-116">-PrivateIpAddress</span></span>
<span data-ttu-id="2f7db-117">Die private IP-Adresse des IPKonfigurationsdateiAddress, wenn die statische Zuweisung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f7db-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

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

### <span data-ttu-id="2f7db-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2f7db-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="2f7db-119">Die IP-Version der IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="2f7db-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7db-120">– Primär</span><span class="sxs-lookup"><span data-stu-id="2f7db-120">-Primary</span></span>
<span data-ttu-id="2f7db-121">Geben Sie an, dass die aktuelle IP-Konfiguration primär ist.</span><span class="sxs-lookup"><span data-stu-id="2f7db-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="2f7db-122">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="2f7db-122">-Subnet</span></span>
<span data-ttu-id="2f7db-123">Subnetz</span><span class="sxs-lookup"><span data-stu-id="2f7db-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7db-124">CommonParameters</span></span>
<span data-ttu-id="2f7db-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f7db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7db-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f7db-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7db-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f7db-127">INPUTS</span></span>

### <span data-ttu-id="2f7db-128">Keine</span><span class="sxs-lookup"><span data-stu-id="2f7db-128">None</span></span>

## <span data-ttu-id="2f7db-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f7db-129">OUTPUTS</span></span>

### <span data-ttu-id="2f7db-130">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f7db-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="2f7db-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f7db-131">NOTES</span></span>

## <span data-ttu-id="2f7db-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f7db-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f7db-133">Neu – AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2f7db-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)