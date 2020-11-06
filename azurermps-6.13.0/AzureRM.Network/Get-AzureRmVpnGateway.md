---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482329"
---
# <span data-ttu-id="994cf-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="994cf-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="994cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="994cf-102">SYNOPSIS</span></span>
<span data-ttu-id="994cf-103">Ruft eine VpnGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="994cf-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="994cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="994cf-104">SYNTAX</span></span>

### <span data-ttu-id="994cf-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="994cf-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="994cf-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994cf-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="994cf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="994cf-107">DESCRIPTION</span></span>
<span data-ttu-id="994cf-108">Ruft eine VpnGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="994cf-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="994cf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="994cf-109">EXAMPLES</span></span>

### <span data-ttu-id="994cf-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="994cf-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="994cf-111">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="994cf-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="994cf-112">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="994cf-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="994cf-113">Anschließend wird die VpnGateway-Schnittstelle unter Verwendung ihrer resourceGroupName und des Gateway-namens abgerufen.</span><span class="sxs-lookup"><span data-stu-id="994cf-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="994cf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="994cf-114">PARAMETERS</span></span>

### <span data-ttu-id="994cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994cf-115">-DefaultProfile</span></span>
<span data-ttu-id="994cf-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="994cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994cf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="994cf-117">-Name</span></span>
<span data-ttu-id="994cf-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="994cf-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="994cf-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="994cf-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994cf-121">CommonParameters</span></span>
<span data-ttu-id="994cf-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="994cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994cf-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994cf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994cf-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="994cf-124">INPUTS</span></span>

### <span data-ttu-id="994cf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="994cf-125">System.String</span></span>

## <span data-ttu-id="994cf-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="994cf-126">OUTPUTS</span></span>

### <span data-ttu-id="994cf-127">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="994cf-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="994cf-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="994cf-128">NOTES</span></span>

## <span data-ttu-id="994cf-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="994cf-129">RELATED LINKS</span></span>
