---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175079"
---
# <span data-ttu-id="4a95f-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a95f-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="4a95f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a95f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a95f-103">Erstellt eine IP-Konfiguration, die mit der PrivateLink-Konfiguration verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a95f-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="4a95f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a95f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a95f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a95f-105">DESCRIPTION</span></span>
<span data-ttu-id="4a95f-106">Das Cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** erstellt eine IP-Konfiguration, die mit der PrivateLink-Konfiguration für ein Azure Application Gateway verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a95f-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="4a95f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a95f-107">EXAMPLES</span></span>

### <span data-ttu-id="4a95f-108">Beispiel 1: PrivateLink IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4a95f-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="4a95f-109">Mit diesem Befehl wird eine PrivateLink-IP-Konfiguration mit dem Namen "ipConfig01" erstellt, die das Ergebnis in der Variablen mit dem Namen $PrivateLinkIpConfiguration speichert.</span><span class="sxs-lookup"><span data-stu-id="4a95f-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="4a95f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a95f-110">PARAMETERS</span></span>

### <span data-ttu-id="4a95f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a95f-111">-DefaultProfile</span></span>
<span data-ttu-id="4a95f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a95f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a95f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4a95f-113">-Name</span></span>
<span data-ttu-id="4a95f-114">Der Name des IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="4a95f-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="4a95f-115">– Primär</span><span class="sxs-lookup"><span data-stu-id="4a95f-115">-Primary</span></span>
<span data-ttu-id="4a95f-116">Geben Sie an, dass die IP-Konfiguration primär ist.</span><span class="sxs-lookup"><span data-stu-id="4a95f-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="4a95f-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4a95f-117">-PrivateIpAddress</span></span>
<span data-ttu-id="4a95f-118">Die private IP-Adresse des IPKonfigurationsdateiAddress, wenn eine statische Zuweisung erwünscht ist.</span><span class="sxs-lookup"><span data-stu-id="4a95f-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="4a95f-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="4a95f-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="4a95f-120">Die IP-Version der IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4a95f-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="4a95f-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="4a95f-121">-Subnet</span></span>
<span data-ttu-id="4a95f-122">Subnetz</span><span class="sxs-lookup"><span data-stu-id="4a95f-122">Subnet</span></span>

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

### <span data-ttu-id="4a95f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a95f-123">CommonParameters</span></span>
<span data-ttu-id="4a95f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a95f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a95f-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a95f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a95f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a95f-126">INPUTS</span></span>

### <span data-ttu-id="4a95f-127">Keine</span><span class="sxs-lookup"><span data-stu-id="4a95f-127">None</span></span>

## <span data-ttu-id="4a95f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a95f-128">OUTPUTS</span></span>

### <span data-ttu-id="4a95f-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a95f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="4a95f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a95f-130">NOTES</span></span>

## <span data-ttu-id="4a95f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a95f-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a95f-132">Neu – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a95f-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
