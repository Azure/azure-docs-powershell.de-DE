---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006620"
---
# <span data-ttu-id="14b67-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="14b67-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="14b67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14b67-102">SYNOPSIS</span></span>
<span data-ttu-id="14b67-103">Aktiviert oder deaktiviert ein VPN-Gateway für ein Azure-virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="14b67-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="14b67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14b67-104">SYNTAX</span></span>

### <span data-ttu-id="14b67-105">Verbinden (Standard)</span><span class="sxs-lookup"><span data-stu-id="14b67-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="14b67-106">Trennen</span><span class="sxs-lookup"><span data-stu-id="14b67-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="14b67-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14b67-107">DESCRIPTION</span></span>
<span data-ttu-id="14b67-108">Das Cmdlet " **Satz-AzureVNetGateway** " aktiviert oder deaktiviert ein VPN-Gateway (virtuelles privates Netzwerk) für ein Azure-virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="14b67-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="14b67-109">Ein virtuelles Netzwerkgateway ist ein VPN-Endpunkt zum Herstellen einer Verbindung mit einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="14b67-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="14b67-110">Geben Sie den Parameter *Connect* oder *Disconnect* an, um die VPN-Verbindung zwischen einer lokalen lokalen Netzwerk Website und einem virtuellen Netzwerk zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="14b67-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="14b67-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14b67-111">EXAMPLES</span></span>

### <span data-ttu-id="14b67-112">Beispiel 1: Aktivieren eines virtuellen Netzwerkgateways für ein virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="14b67-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="14b67-113">Mit diesem Befehl wird das virtuelle Netzwerkgateway zwischen dem virtuellen Azure-Netzwerk mit dem Namen ContosoProdNet und dem VPN-Gerät für die lokale Netzwerk Website mit dem Namen ContosoBranchOffice aktiviert.</span><span class="sxs-lookup"><span data-stu-id="14b67-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="14b67-114">Beispiel 2: Deaktivieren eines virtuellen Netzwerkgateways für ein virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="14b67-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="14b67-115">Mit diesem Befehl wird das virtuelle Netzwerkgateway zwischen dem virtuellen Azure-Netzwerk mit dem Namen ContosoProdNet und dem VPN-Gerät für die lokale Netzwerk Website mit dem Namen ContosoBranchOffice deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="14b67-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="14b67-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="14b67-116">PARAMETERS</span></span>

### <span data-ttu-id="14b67-117">-Connect</span><span class="sxs-lookup"><span data-stu-id="14b67-117">-Connect</span></span>
<span data-ttu-id="14b67-118">Gibt an, dass dieses Cmdlet die VPN-Verbindung zwischen einem virtuellen Netzwerk und einer lokalen Netzwerk Website aktiviert.</span><span class="sxs-lookup"><span data-stu-id="14b67-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b67-119">-Trennen</span><span class="sxs-lookup"><span data-stu-id="14b67-119">-Disconnect</span></span>
<span data-ttu-id="14b67-120">Gibt an, dass dieses Cmdlet die VPN-Verbindung zwischen einem virtuellen Netzwerk und einer lokalen Netzwerk Website deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="14b67-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b67-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="14b67-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="14b67-122">Gibt den Namen der lokalen lokalen Netzwerk Website an, für die dieses Cmdlet die VPN-Verbindung aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="14b67-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="14b67-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="14b67-123">-Profile</span></span>
<span data-ttu-id="14b67-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="14b67-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="14b67-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="14b67-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14b67-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="14b67-126">-VNetName</span></span>
<span data-ttu-id="14b67-127">Gibt das virtuelle Netzwerk an, für das dieses Cmdlet die VPN-Verbindung aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="14b67-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="14b67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b67-128">CommonParameters</span></span>
<span data-ttu-id="14b67-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b67-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b67-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b67-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14b67-131">INPUTS</span></span>

## <span data-ttu-id="14b67-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14b67-132">OUTPUTS</span></span>

## <span data-ttu-id="14b67-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="14b67-133">NOTES</span></span>

## <span data-ttu-id="14b67-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14b67-134">RELATED LINKS</span></span>

[<span data-ttu-id="14b67-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="14b67-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="14b67-136">Neu – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="14b67-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="14b67-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="14b67-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="14b67-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="14b67-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="14b67-139">Größe ändern – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="14b67-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


