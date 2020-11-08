---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178530"
---
# <span data-ttu-id="78f67-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="78f67-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="78f67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78f67-102">SYNOPSIS</span></span>
<span data-ttu-id="78f67-103">IP-Adressen assoicated der Firewall auf dem virtuellen Hub</span><span class="sxs-lookup"><span data-stu-id="78f67-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="78f67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78f67-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f67-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78f67-105">DESCRIPTION</span></span>
<span data-ttu-id="78f67-106">IP-Adressen assoicated der Firewall auf dem virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="78f67-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="78f67-107">Hierbei kann es sich um öffentliche und private Adressen handeln.</span><span class="sxs-lookup"><span data-stu-id="78f67-107">These can be public and private addresses</span></span>

## <span data-ttu-id="78f67-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78f67-108">EXAMPLES</span></span>

### <span data-ttu-id="78f67-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78f67-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="78f67-110">In diesem Beispiel wird ein Hub-IP-Adressen Objekt mit einer Anzahl von zwei öffentlichen IPS erstellt.</span><span class="sxs-lookup"><span data-stu-id="78f67-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="78f67-111">Das HubIPAddress-Objekt wird mit der Firewall auf dem virtuellen Hub ssociated.</span><span class="sxs-lookup"><span data-stu-id="78f67-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="78f67-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="78f67-112">PARAMETERS</span></span>

### <span data-ttu-id="78f67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f67-113">-DefaultProfile</span></span>
<span data-ttu-id="78f67-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78f67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f67-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="78f67-115">-PrivateIPAddress</span></span>
<span data-ttu-id="78f67-116">Die private IP-Adresse der Firewall, die mit einem Hub verbunden ist</span><span class="sxs-lookup"><span data-stu-id="78f67-116">The private Ip Address of the Firewall attached to a Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f67-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="78f67-117">-PublicIPs</span></span>
<span data-ttu-id="78f67-118">Die IP-Adressen der Firewall, die mit einem Hub verbunden ist</span><span class="sxs-lookup"><span data-stu-id="78f67-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f67-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78f67-119">-Confirm</span></span>
<span data-ttu-id="78f67-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78f67-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f67-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f67-121">-WhatIf</span></span>
<span data-ttu-id="78f67-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78f67-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78f67-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78f67-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f67-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f67-124">CommonParameters</span></span>
<span data-ttu-id="78f67-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f67-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f67-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78f67-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f67-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78f67-127">INPUTS</span></span>

### <span data-ttu-id="78f67-128">Keine</span><span class="sxs-lookup"><span data-stu-id="78f67-128">None</span></span>

## <span data-ttu-id="78f67-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78f67-129">OUTPUTS</span></span>

### <span data-ttu-id="78f67-130">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="78f67-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="78f67-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="78f67-131">NOTES</span></span>

## <span data-ttu-id="78f67-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78f67-132">RELATED LINKS</span></span>
