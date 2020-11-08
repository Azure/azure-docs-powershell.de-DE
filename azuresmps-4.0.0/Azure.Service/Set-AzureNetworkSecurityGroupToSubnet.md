---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006035"
---
# <span data-ttu-id="a40cb-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="a40cb-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="a40cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a40cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a40cb-103">Ordnet eine Netzwerksicherheitsgruppe einem Subnetz zu.</span><span class="sxs-lookup"><span data-stu-id="a40cb-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="a40cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a40cb-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a40cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a40cb-105">DESCRIPTION</span></span>
<span data-ttu-id="a40cb-106">Das Cmdlet " **Satz-AzureNetworkSecurityGroupToSubnet** " ordnet eine Azure Network Security-Gruppe einem Subnetz zu.</span><span class="sxs-lookup"><span data-stu-id="a40cb-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="a40cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a40cb-107">EXAMPLES</span></span>

## <span data-ttu-id="a40cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a40cb-108">PARAMETERS</span></span>

### <span data-ttu-id="a40cb-109">-Force</span><span class="sxs-lookup"><span data-stu-id="a40cb-109">-Force</span></span>
<span data-ttu-id="a40cb-110">Gibt an, dass Sie mit diesem Cmdlet nicht aufgefordert werden, das Entfernen einer vorherigen Netzwerksicherheitsgruppe aus dem Subnetz zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="a40cb-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="a40cb-111">-Name</span><span class="sxs-lookup"><span data-stu-id="a40cb-111">-Name</span></span>
<span data-ttu-id="a40cb-112">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet einem Subnetz zuordnet.</span><span class="sxs-lookup"><span data-stu-id="a40cb-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

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

### <span data-ttu-id="a40cb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a40cb-113">-PassThru</span></span>
<span data-ttu-id="a40cb-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a40cb-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a40cb-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a40cb-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a40cb-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="a40cb-116">-Profile</span></span>
<span data-ttu-id="a40cb-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a40cb-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a40cb-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a40cb-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a40cb-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a40cb-119">-SubnetName</span></span>
<span data-ttu-id="a40cb-120">Gibt den Namen eines Subnetzes an, dem dieses Cmdlet eine Netzwerksicherheitsgruppe anordnet.</span><span class="sxs-lookup"><span data-stu-id="a40cb-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="a40cb-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a40cb-121">-VirtualNetworkName</span></span>
<span data-ttu-id="a40cb-122">Gibt den Namen eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a40cb-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="a40cb-123">Dieses Cmdlet ordnet eine Netzwerksicherheitsgruppe einem Subnetz im virtuellen Netzwerk zu, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a40cb-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="a40cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40cb-124">CommonParameters</span></span>
<span data-ttu-id="a40cb-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40cb-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40cb-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a40cb-127">INPUTS</span></span>

## <span data-ttu-id="a40cb-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a40cb-128">OUTPUTS</span></span>

## <span data-ttu-id="a40cb-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a40cb-129">NOTES</span></span>

## <span data-ttu-id="a40cb-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a40cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="a40cb-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="a40cb-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="a40cb-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="a40cb-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


