---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4c2d5c4e3c46c79caa4bd8b47fdc178da4fd6450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660690"
---
# <span data-ttu-id="8bd49-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bd49-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="8bd49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bd49-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd49-103">Ruft ein virtuelles Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="8bd49-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="8bd49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bd49-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bd49-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bd49-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd49-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="8bd49-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="8bd49-107">Das Cmdlet " **Get-AzVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="8bd49-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8bd49-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bd49-108">EXAMPLES</span></span>

### <span data-ttu-id="8bd49-109">1: Abrufen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="8bd49-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="8bd49-110">Gibt das Objekt des virtuellen Netzwerkgateways mit dem Namen "myGateway1" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="8bd49-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="8bd49-111">2: Abrufen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="8bd49-111">2: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="8bd49-112">Gibt alle virtuellen Netzwerkgateways zurück, die mit "mygateway" in der Ressourcengruppe "myRG" beginnen.</span><span class="sxs-lookup"><span data-stu-id="8bd49-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="8bd49-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bd49-113">PARAMETERS</span></span>

### <span data-ttu-id="8bd49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd49-114">-DefaultProfile</span></span>
<span data-ttu-id="8bd49-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8bd49-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bd49-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8bd49-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8bd49-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd49-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8bd49-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd49-118">CommonParameters</span></span>
<span data-ttu-id="8bd49-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd49-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd49-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bd49-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd49-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bd49-121">INPUTS</span></span>

### <span data-ttu-id="8bd49-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd49-122">System.String</span></span>

## <span data-ttu-id="8bd49-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bd49-123">OUTPUTS</span></span>

### <span data-ttu-id="8bd49-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bd49-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8bd49-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bd49-125">NOTES</span></span>

## <span data-ttu-id="8bd49-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bd49-126">RELATED LINKS</span></span>

[<span data-ttu-id="8bd49-127">Neu – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bd49-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8bd49-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bd49-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8bd49-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bd49-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8bd49-130">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bd49-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8bd49-131">Satz-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bd49-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
