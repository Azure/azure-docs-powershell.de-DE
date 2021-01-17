---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364019"
---
# <span data-ttu-id="e4739-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e4739-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="e4739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4739-102">SYNOPSIS</span></span>
<span data-ttu-id="e4739-103">Aktualisiert einen privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="e4739-103">Updates a private link service.</span></span>

## <span data-ttu-id="e4739-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4739-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4739-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4739-105">DESCRIPTION</span></span>
<span data-ttu-id="e4739-106">Das **Cmdlet Set-AzPrivateLinkService** aktualisiert einen privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="e4739-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="e4739-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4739-107">EXAMPLES</span></span>

### <span data-ttu-id="e4739-108">1: Erstellt einen privaten Linkdienst und aktualisiert dessen</span><span class="sxs-lookup"><span data-stu-id="e4739-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="e4739-109">In diesem Beispiel wird ein privater Linkdienst namens "mypls" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4739-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="e4739-110">Anschließend ersetzt sie die ipConfigurations durch das speicherinte ipConfiguratiuon-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e4739-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="e4739-111">Das Set-AzPrivateLinkService cmdlet wird dann verwendet, um den geänderten Dienststatus für private Links auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e4739-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="e4739-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4739-112">PARAMETERS</span></span>

### <span data-ttu-id="e4739-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4739-113">-AsJob</span></span>
<span data-ttu-id="e4739-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e4739-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4739-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4739-115">-DefaultProfile</span></span>
<span data-ttu-id="e4739-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4739-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4739-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e4739-117">-PrivateLinkService</span></span>
<span data-ttu-id="e4739-118">Gibt ein privates Verknüpfungsdienstobjekt an, das den Zustand darstellt, auf den der private Linkdienst festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4739-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4739-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4739-119">CommonParameters</span></span>
<span data-ttu-id="e4739-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4739-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4739-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4739-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4739-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4739-122">INPUTS</span></span>

### <span data-ttu-id="e4739-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e4739-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e4739-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4739-124">OUTPUTS</span></span>

### <span data-ttu-id="e4739-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e4739-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e4739-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e4739-126">NOTES</span></span>

## <span data-ttu-id="e4739-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e4739-127">RELATED LINKS</span></span>

[<span data-ttu-id="e4739-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e4739-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="e4739-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e4739-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="e4739-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e4739-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


