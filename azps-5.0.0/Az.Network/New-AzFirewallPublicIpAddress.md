---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178467"
---
# <span data-ttu-id="974cc-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="974cc-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="974cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="974cc-102">SYNOPSIS</span></span>
<span data-ttu-id="974cc-103">Dies ist der Platzhalter für die IP-Adresse, die für Multi PIP auf Azure Firewall verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="974cc-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="974cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="974cc-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="974cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="974cc-105">DESCRIPTION</span></span>
<span data-ttu-id="974cc-106">Dies ist der Platzhalter für die IP-Adresse, die für Multi PIP auf Azure Firewall verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="974cc-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="974cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="974cc-107">EXAMPLES</span></span>

### <span data-ttu-id="974cc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="974cc-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="974cc-109">$publicIp ist der Platzhalter für die IP-Adresse 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="974cc-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="974cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="974cc-110">PARAMETERS</span></span>

### <span data-ttu-id="974cc-111">-Adresse</span><span class="sxs-lookup"><span data-stu-id="974cc-111">-Address</span></span>
<span data-ttu-id="974cc-112">Die IP-Adressen der Firewall, die mit einem Hub verbunden ist</span><span class="sxs-lookup"><span data-stu-id="974cc-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="974cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974cc-113">-DefaultProfile</span></span>
<span data-ttu-id="974cc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="974cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="974cc-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="974cc-115">-Confirm</span></span>
<span data-ttu-id="974cc-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="974cc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="974cc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="974cc-117">-WhatIf</span></span>
<span data-ttu-id="974cc-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="974cc-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="974cc-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="974cc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="974cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974cc-120">CommonParameters</span></span>
<span data-ttu-id="974cc-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="974cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974cc-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="974cc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974cc-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="974cc-123">INPUTS</span></span>

### <span data-ttu-id="974cc-124">Keine</span><span class="sxs-lookup"><span data-stu-id="974cc-124">None</span></span>

## <span data-ttu-id="974cc-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="974cc-125">OUTPUTS</span></span>

### <span data-ttu-id="974cc-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="974cc-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="974cc-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="974cc-127">NOTES</span></span>

## <span data-ttu-id="974cc-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="974cc-128">RELATED LINKS</span></span>
