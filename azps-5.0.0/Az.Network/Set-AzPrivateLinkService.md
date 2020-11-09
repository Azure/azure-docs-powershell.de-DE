---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303586"
---
# <span data-ttu-id="42293-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42293-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="42293-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42293-102">SYNOPSIS</span></span>
<span data-ttu-id="42293-103">Aktualisiert einen Dienst für private Links.</span><span class="sxs-lookup"><span data-stu-id="42293-103">Updates a private link service.</span></span>

## <span data-ttu-id="42293-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42293-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42293-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42293-105">DESCRIPTION</span></span>
<span data-ttu-id="42293-106">Das Cmdlet " **Satz-AzPrivateLinkService** " aktualisiert einen Dienst für private Links.</span><span class="sxs-lookup"><span data-stu-id="42293-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="42293-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42293-107">EXAMPLES</span></span>

### <span data-ttu-id="42293-108">1: erstellt einen privaten Link Dienst und aktualisiert dessen</span><span class="sxs-lookup"><span data-stu-id="42293-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="42293-109">In diesem Beispiel wird ein privater Link Dienst namens mypls erstellt.</span><span class="sxs-lookup"><span data-stu-id="42293-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="42293-110">Anschließend wird die ipConfigurations-Datei vom speicherresidenten ipConfiguratiuon-Objekt ersetzt.</span><span class="sxs-lookup"><span data-stu-id="42293-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="42293-111">Das Set-AzPrivateLinkService-Cmdlet wird dann verwendet, um den geänderten Dienstzustand des privaten Verbindungs Diensts auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="42293-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="42293-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42293-112">PARAMETERS</span></span>

### <span data-ttu-id="42293-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42293-113">-AsJob</span></span>
<span data-ttu-id="42293-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="42293-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42293-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42293-115">-DefaultProfile</span></span>
<span data-ttu-id="42293-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42293-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42293-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42293-117">-PrivateLinkService</span></span>
<span data-ttu-id="42293-118">Gibt ein privates Link Dienstobjekt an, das den Zustand darstellt, in dem der private Link Dienst festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="42293-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="42293-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42293-119">CommonParameters</span></span>
<span data-ttu-id="42293-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42293-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42293-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42293-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42293-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42293-122">INPUTS</span></span>

### <span data-ttu-id="42293-123">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42293-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="42293-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42293-124">OUTPUTS</span></span>

### <span data-ttu-id="42293-125">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42293-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="42293-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="42293-126">NOTES</span></span>

## <span data-ttu-id="42293-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42293-127">RELATED LINKS</span></span>

[<span data-ttu-id="42293-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42293-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="42293-129">Neu – AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42293-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="42293-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42293-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


