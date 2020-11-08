---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180062"
---
# <span data-ttu-id="71e1c-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="71e1c-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="71e1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="71e1c-103">Ruft die aktuelle Nutzung des virtuellen Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="71e1c-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="71e1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71e1c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e1c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="71e1c-106">Das Cmdlet " **Get-AzVirtualNetworkUsageList** " erhält pro Subnetz-Nutzung für das angegebene virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="71e1c-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="71e1c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71e1c-107">EXAMPLES</span></span>

### <span data-ttu-id="71e1c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71e1c-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="71e1c-109">Ruft pro Subnetz aktuelle Nutzungswerte für usagetest virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="71e1c-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="71e1c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71e1c-110">PARAMETERS</span></span>

### <span data-ttu-id="71e1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e1c-111">-DefaultProfile</span></span>
<span data-ttu-id="71e1c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71e1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71e1c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="71e1c-113">-Name</span></span>
<span data-ttu-id="71e1c-114">Gibt den Namen des virtuellen Netzwerks an, für das die Verwendungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71e1c-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e1c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e1c-115">-ResourceGroupName</span></span>
<span data-ttu-id="71e1c-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="71e1c-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e1c-117">CommonParameters</span></span>
<span data-ttu-id="71e1c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e1c-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71e1c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e1c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71e1c-120">INPUTS</span></span>

### <span data-ttu-id="71e1c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="71e1c-121">System.String</span></span>

## <span data-ttu-id="71e1c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71e1c-122">OUTPUTS</span></span>

### <span data-ttu-id="71e1c-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="71e1c-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="71e1c-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="71e1c-124">NOTES</span></span>

## <span data-ttu-id="71e1c-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71e1c-125">RELATED LINKS</span></span>
