---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 4a34899a4e6c37ad3d4c84c173d07012110dcad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936155"
---
# <span data-ttu-id="926fd-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="926fd-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="926fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="926fd-102">SYNOPSIS</span></span>
<span data-ttu-id="926fd-103">Erstellt eine Ip-Konfiguration, die der PrivateLink-Konfiguration zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="926fd-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="926fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="926fd-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926fd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="926fd-105">DESCRIPTION</span></span>
<span data-ttu-id="926fd-106">Das **Cmdlet New-AzApplicationGatewayPrivateLinkIpConfiguration** erstellt eine Ip-Konfiguration, die der PrivateLink-Konfiguration für ein Azure-Anwendungsgateway zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="926fd-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="926fd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="926fd-107">EXAMPLES</span></span>

### <span data-ttu-id="926fd-108">Beispiel 1: PrivateLink-Ip-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="926fd-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="926fd-109">Mit diesem Befehl wird eine PrivateLink-IP-Konfiguration namens "ipConfig01" erstellt, in der das Ergebnis in der Variablen namens $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="926fd-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="926fd-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="926fd-110">PARAMETERS</span></span>

### <span data-ttu-id="926fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926fd-111">-DefaultProfile</span></span>
<span data-ttu-id="926fd-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="926fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="926fd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="926fd-113">-Name</span></span>
<span data-ttu-id="926fd-114">Der Name der IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="926fd-114">The name of the IpConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="926fd-115">-Primär</span><span class="sxs-lookup"><span data-stu-id="926fd-115">-Primary</span></span>
<span data-ttu-id="926fd-116">Geben Sie an, dass die IP-Konfiguration primär ist.</span><span class="sxs-lookup"><span data-stu-id="926fd-116">Indicate the ip configuration is primary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="926fd-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="926fd-117">-PrivateIpAddress</span></span>
<span data-ttu-id="926fd-118">Die private IP-Adresse der ipConfiguration, wenn statische Zuordnung gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="926fd-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="926fd-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="926fd-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="926fd-120">Die IP-Version der IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="926fd-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="926fd-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="926fd-121">-Subnet</span></span>
<span data-ttu-id="926fd-122">Subnetz</span><span class="sxs-lookup"><span data-stu-id="926fd-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="926fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926fd-123">CommonParameters</span></span>
<span data-ttu-id="926fd-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926fd-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="926fd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926fd-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="926fd-126">INPUTS</span></span>

### <span data-ttu-id="926fd-127">Keine</span><span class="sxs-lookup"><span data-stu-id="926fd-127">None</span></span>

## <span data-ttu-id="926fd-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="926fd-128">OUTPUTS</span></span>

### <span data-ttu-id="926fd-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="926fd-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="926fd-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="926fd-130">NOTES</span></span>

## <span data-ttu-id="926fd-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="926fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="926fd-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="926fd-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
