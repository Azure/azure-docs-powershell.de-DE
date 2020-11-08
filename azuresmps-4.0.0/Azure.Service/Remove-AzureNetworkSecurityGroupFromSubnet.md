---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006356"
---
# <span data-ttu-id="bf929-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="bf929-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="bf929-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf929-102">SYNOPSIS</span></span>
<span data-ttu-id="bf929-103">Distanziert eine Netzwerksicherheitsgruppe von einem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="bf929-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="bf929-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf929-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf929-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf929-105">DESCRIPTION</span></span>
<span data-ttu-id="bf929-106">Das Cmdlet **Remove-AzureNetworkSecurityGroupFromSubnet** distanziert eine Azure Network Security-Gruppe von einem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="bf929-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="bf929-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf929-107">EXAMPLES</span></span>

## <span data-ttu-id="bf929-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf929-108">PARAMETERS</span></span>

### <span data-ttu-id="bf929-109">-Force</span><span class="sxs-lookup"><span data-stu-id="bf929-109">-Force</span></span>
<span data-ttu-id="bf929-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="bf929-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf929-111">-Name</span><span class="sxs-lookup"><span data-stu-id="bf929-111">-Name</span></span>
<span data-ttu-id="bf929-112">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet von einem Subnetz distanziert.</span><span class="sxs-lookup"><span data-stu-id="bf929-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf929-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf929-113">-PassThru</span></span>
<span data-ttu-id="bf929-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf929-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="bf929-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="bf929-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf929-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf929-116">-Profile</span></span>
<span data-ttu-id="bf929-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bf929-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bf929-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bf929-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf929-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bf929-119">-SubnetName</span></span>
<span data-ttu-id="bf929-120">Gibt den Namen eines Subnets an, von dem dieses Cmdlet eine Netzwerksicherheitsgruppe distanziert.</span><span class="sxs-lookup"><span data-stu-id="bf929-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="bf929-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bf929-121">-VirtualNetworkName</span></span>
<span data-ttu-id="bf929-122">Gibt den Namen eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="bf929-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="bf929-123">Dieses Cmdlet trennt eine Netzwerksicherheitsgruppe von einem Subnetz im virtuellen Netzwerk, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bf929-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf929-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf929-124">CommonParameters</span></span>
<span data-ttu-id="bf929-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf929-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf929-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf929-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf929-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf929-127">INPUTS</span></span>

## <span data-ttu-id="bf929-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf929-128">OUTPUTS</span></span>

## <span data-ttu-id="bf929-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf929-129">NOTES</span></span>

## <span data-ttu-id="bf929-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf929-130">RELATED LINKS</span></span>

[<span data-ttu-id="bf929-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="bf929-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="bf929-132">Satz-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="bf929-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


