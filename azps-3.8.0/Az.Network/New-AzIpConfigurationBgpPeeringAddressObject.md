---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996513"
---
# <span data-ttu-id="28fb5-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="28fb5-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="28fb5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="28fb5-103">erstellt eine neue IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="28fb5-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="28fb5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28fb5-104">SYNTAX</span></span>

### <span data-ttu-id="28fb5-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="28fb5-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="28fb5-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28fb5-106">DESCRIPTION</span></span>
<span data-ttu-id="28fb5-107">Das **New-AzIpConfigurationBgpPeeringAddressObject** erstellt ein IpConfigurationBgpPeeringAddressObject-Objekt, das die BgpPeeringAddresses-Eigenschaft in Ihrem virtuellen Netzwerk-Gateway-bgpsettings darstellt.</span><span class="sxs-lookup"><span data-stu-id="28fb5-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="28fb5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28fb5-108">EXAMPLES</span></span>

### <span data-ttu-id="28fb5-109">1: Erstellen einer AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="28fb5-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="28fb5-110">Im obigen Beispiel wird ein IpConfigurationBgpPeeringAddressObject erstellt. dieses neue Objekt wird zu gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="28fb5-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="28fb5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="28fb5-111">PARAMETERS</span></span>

### <span data-ttu-id="28fb5-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28fb5-112">-Confirm</span></span>
<span data-ttu-id="28fb5-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28fb5-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fb5-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="28fb5-114">-CustomAddress</span></span>
<span data-ttu-id="28fb5-115">Die CustomAddress-Liste für virtuelles Netzwerk-Gateway für BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="28fb5-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28fb5-116">-DefaultProfile</span></span>
<span data-ttu-id="28fb5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28fb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28fb5-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="28fb5-118">-IpConfigurationId</span></span>
<span data-ttu-id="28fb5-119">Das virtuelle Netzwerkgateway IpConfigurationId für BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="28fb5-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="28fb5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28fb5-120">-WhatIf</span></span>
<span data-ttu-id="28fb5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28fb5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28fb5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28fb5-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fb5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28fb5-123">CommonParameters</span></span>
<span data-ttu-id="28fb5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28fb5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28fb5-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28fb5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28fb5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28fb5-126">INPUTS</span></span>

### <span data-ttu-id="28fb5-127">Keine</span><span class="sxs-lookup"><span data-stu-id="28fb5-127">None</span></span>

## <span data-ttu-id="28fb5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28fb5-128">OUTPUTS</span></span>

### <span data-ttu-id="28fb5-129">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="28fb5-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="28fb5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="28fb5-130">NOTES</span></span>

## <span data-ttu-id="28fb5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28fb5-131">RELATED LINKS</span></span>
