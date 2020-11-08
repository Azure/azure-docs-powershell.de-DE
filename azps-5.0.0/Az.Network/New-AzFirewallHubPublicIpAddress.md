---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178528"
---
# <span data-ttu-id="d9bad-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9bad-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="d9bad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9bad-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bad-103">Public IP assoicated to the Firewall on Virtual Hub</span><span class="sxs-lookup"><span data-stu-id="d9bad-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="d9bad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9bad-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9bad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9bad-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bad-106">Public IP assoicated to the Firewall on Virtual Hub</span><span class="sxs-lookup"><span data-stu-id="d9bad-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="d9bad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9bad-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bad-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9bad-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="d9bad-109">Dadurch werden 2 öffentliche IPS an der Firewall erstellt, die mit dem virtuellen Hub verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d9bad-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="d9bad-110">Dadurch wird die IP-Adresse im Back-End erstellt. Die IP-Webdienste können nicht explizit für eine neue Firewall bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9bad-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="d9bad-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d9bad-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="d9bad-112">Dadurch wird eine neue öffentliche IP-Adresse auf der Firewall erstellt, indem $publicIp 1, $publicIp 2, die bereits auf der Firewall vorhanden sind, beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d9bad-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="d9bad-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9bad-113">PARAMETERS</span></span>

### <span data-ttu-id="d9bad-114">-Adressen</span><span class="sxs-lookup"><span data-stu-id="d9bad-114">-Addresses</span></span>
<span data-ttu-id="d9bad-115">Die öffentlichen IP-Adressen der Firewall, die mit einem Hub verbunden ist</span><span class="sxs-lookup"><span data-stu-id="d9bad-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-116">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="d9bad-116">-Count</span></span>
<span data-ttu-id="d9bad-117">Die Anzahl der öffentlichen IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="d9bad-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bad-118">-DefaultProfile</span></span>
<span data-ttu-id="d9bad-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9bad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bad-120">CommonParameters</span></span>
<span data-ttu-id="d9bad-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bad-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9bad-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bad-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9bad-123">INPUTS</span></span>

### <span data-ttu-id="d9bad-124">Keine</span><span class="sxs-lookup"><span data-stu-id="d9bad-124">None</span></span>

## <span data-ttu-id="d9bad-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9bad-125">OUTPUTS</span></span>

### <span data-ttu-id="d9bad-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="d9bad-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="d9bad-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9bad-127">NOTES</span></span>

## <span data-ttu-id="d9bad-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9bad-128">RELATED LINKS</span></span>
