---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172684"
---
# <span data-ttu-id="7ed4f-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ed4f-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="7ed4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed4f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed4f-103">Öffentliche IP-Zuordnung zur Firewall auf dem virtuellen Hub</span><span class="sxs-lookup"><span data-stu-id="7ed4f-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="7ed4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ed4f-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed4f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ed4f-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed4f-106">Öffentliche IP-Zuordnung zur Firewall auf dem virtuellen Hub</span><span class="sxs-lookup"><span data-stu-id="7ed4f-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="7ed4f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ed4f-107">EXAMPLES</span></span>

### <span data-ttu-id="7ed4f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ed4f-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="7ed4f-109">Dadurch werden zwei öffentliche IPS für die Firewall erstellt, die an den virtuellen Hub angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="7ed4f-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="7ed4f-110">Dadurch wird die ip-Adresse im Back-End erstellt. Wir können die ipaddresses nicht explizit für eine neue Firewall bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7ed4f-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="7ed4f-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7ed4f-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="7ed4f-112">Dadurch wird eine neue öffentliche IP für die Firewall erstellt, indem die $publicIp 1, $publicIp 2 beibehalten werden, die bereits in der Firewall vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7ed4f-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="7ed4f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ed4f-113">PARAMETERS</span></span>

### <span data-ttu-id="7ed4f-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="7ed4f-114">-Addresses</span></span>
<span data-ttu-id="7ed4f-115">Die öffentlichen IP-Adressen der Firewall, die an einen Hub angefügt sind</span><span class="sxs-lookup"><span data-stu-id="7ed4f-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="7ed4f-116">-Count</span><span class="sxs-lookup"><span data-stu-id="7ed4f-116">-Count</span></span>
<span data-ttu-id="7ed4f-117">Die Anzahl öffentlicher IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="7ed4f-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="7ed4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed4f-118">-DefaultProfile</span></span>
<span data-ttu-id="7ed4f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ed4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed4f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed4f-120">CommonParameters</span></span>
<span data-ttu-id="7ed4f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed4f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed4f-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ed4f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed4f-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ed4f-123">INPUTS</span></span>

### <span data-ttu-id="7ed4f-124">Keine</span><span class="sxs-lookup"><span data-stu-id="7ed4f-124">None</span></span>

## <span data-ttu-id="7ed4f-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ed4f-125">OUTPUTS</span></span>

### <span data-ttu-id="7ed4f-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="7ed4f-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="7ed4f-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ed4f-127">NOTES</span></span>

## <span data-ttu-id="7ed4f-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ed4f-128">RELATED LINKS</span></span>
