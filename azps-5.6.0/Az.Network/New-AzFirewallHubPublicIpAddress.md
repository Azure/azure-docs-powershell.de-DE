---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: 43a92375126411d392623095a6753072757f49a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935624"
---
# <span data-ttu-id="78d8d-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="78d8d-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="78d8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="78d8d-103">Öffentliche Ip-Zuordnung zur Firewall auf virtuellem Hub</span><span class="sxs-lookup"><span data-stu-id="78d8d-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="78d8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78d8d-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78d8d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="78d8d-106">Öffentliche Ip-Zuordnung zur Firewall auf virtuellem Hub</span><span class="sxs-lookup"><span data-stu-id="78d8d-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="78d8d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="78d8d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78d8d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="78d8d-109">Dadurch werden zwei öffentliche IPS für die firewall erstellt, die an den virtuellen Hub angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="78d8d-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="78d8d-110">Dadurch wird die IP-Adresse im Back-End erstellt. Wir können die ipaddresses nicht explizit für eine neue Firewall bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="78d8d-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="78d8d-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="78d8d-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="78d8d-112">Dadurch wird eine neue öffentliche IP für die Firewall erstellt, indem $publicIp 1, $publicIp 2 beibehalten wird, die bereits in der Firewall vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="78d8d-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="78d8d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="78d8d-113">PARAMETERS</span></span>

### <span data-ttu-id="78d8d-114">-Adressen</span><span class="sxs-lookup"><span data-stu-id="78d8d-114">-Addresses</span></span>
<span data-ttu-id="78d8d-115">Die an einen Hub angefügten öffentlichen IP-Adressen der Firewall</span><span class="sxs-lookup"><span data-stu-id="78d8d-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="78d8d-116">-Count</span><span class="sxs-lookup"><span data-stu-id="78d8d-116">-Count</span></span>
<span data-ttu-id="78d8d-117">Die Anzahl der öffentlichen IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="78d8d-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="78d8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d8d-118">-DefaultProfile</span></span>
<span data-ttu-id="78d8d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78d8d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d8d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d8d-120">CommonParameters</span></span>
<span data-ttu-id="78d8d-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d8d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d8d-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78d8d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d8d-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78d8d-123">INPUTS</span></span>

### <span data-ttu-id="78d8d-124">Keine</span><span class="sxs-lookup"><span data-stu-id="78d8d-124">None</span></span>

## <span data-ttu-id="78d8d-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78d8d-125">OUTPUTS</span></span>

### <span data-ttu-id="78d8d-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="78d8d-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="78d8d-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="78d8d-127">NOTES</span></span>

## <span data-ttu-id="78d8d-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="78d8d-128">RELATED LINKS</span></span>
