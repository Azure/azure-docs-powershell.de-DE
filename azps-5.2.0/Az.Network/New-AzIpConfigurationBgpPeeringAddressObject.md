---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299611"
---
# <span data-ttu-id="76ea3-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="76ea3-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="76ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="76ea3-103">erstellt eine neue IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="76ea3-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="76ea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76ea3-104">SYNTAX</span></span>

### <span data-ttu-id="76ea3-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="76ea3-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="76ea3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76ea3-106">DESCRIPTION</span></span>
<span data-ttu-id="76ea3-107">Die **Neue-AzIpConfigurationBgpPeeringAddressObject** erstellt ein IpConfigurationBgpPeeringAddressObject-Objekt, das die Eigenschaft "BgpPeeringAddresses" in Ihren bgpsettings des virtuellen Netzwerkgateways darstellt.</span><span class="sxs-lookup"><span data-stu-id="76ea3-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="76ea3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76ea3-108">EXAMPLES</span></span>

### <span data-ttu-id="76ea3-109">1: Erstellen einer AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="76ea3-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="76ea3-110">Im vorstehenden Beispiel wird eine IpConfigurationBgpPeeringAddressObject.Dieses neue Objekt wird "gw1ipconfBgp1" erstellt.</span><span class="sxs-lookup"><span data-stu-id="76ea3-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="76ea3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76ea3-111">PARAMETERS</span></span>

### <span data-ttu-id="76ea3-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76ea3-112">-Confirm</span></span>
<span data-ttu-id="76ea3-113">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76ea3-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76ea3-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="76ea3-114">-CustomAddress</span></span>
<span data-ttu-id="76ea3-115">Das virtuelle Netzwerkgateway CustomAddress List für BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="76ea3-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="76ea3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ea3-116">-DefaultProfile</span></span>
<span data-ttu-id="76ea3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76ea3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76ea3-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="76ea3-118">-IpConfigurationId</span></span>
<span data-ttu-id="76ea3-119">Das virtuelle Netzwerkgateway IpConfigurationId für BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="76ea3-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="76ea3-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76ea3-120">-WhatIf</span></span>
<span data-ttu-id="76ea3-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76ea3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76ea3-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76ea3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76ea3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ea3-123">CommonParameters</span></span>
<span data-ttu-id="76ea3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ea3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ea3-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76ea3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ea3-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76ea3-126">INPUTS</span></span>

### <span data-ttu-id="76ea3-127">Keine</span><span class="sxs-lookup"><span data-stu-id="76ea3-127">None</span></span>

## <span data-ttu-id="76ea3-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76ea3-128">OUTPUTS</span></span>

### <span data-ttu-id="76ea3-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="76ea3-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="76ea3-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76ea3-130">NOTES</span></span>

## <span data-ttu-id="76ea3-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76ea3-131">RELATED LINKS</span></span>
