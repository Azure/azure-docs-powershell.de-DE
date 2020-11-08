---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009065"
---
# <span data-ttu-id="6c9a0-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6c9a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9a0-103">Setzt das skalierbare P2S-VPN-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="6c9a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c9a0-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c9a0-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c9a0-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c9a0-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6c9a0-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c9a0-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6c9a0-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9a0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c9a0-108">DESCRIPTION</span></span>
<span data-ttu-id="6c9a0-109">Setzt die P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="6c9a0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c9a0-110">EXAMPLES</span></span>

### <span data-ttu-id="6c9a0-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="6c9a0-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="6c9a0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c9a0-112">PARAMETERS</span></span>

### <span data-ttu-id="6c9a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c9a0-113">-AsJob</span></span>
<span data-ttu-id="6c9a0-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6c9a0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c9a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9a0-115">-DefaultProfile</span></span>
<span data-ttu-id="6c9a0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c9a0-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-117">-P2SVpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9a0-118">CommonParameters</span></span>
<span data-ttu-id="6c9a0-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9a0-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9a0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9a0-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c9a0-121">INPUTS</span></span>

### <span data-ttu-id="6c9a0-122">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="6c9a0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9a0-123">System.String</span></span>

## <span data-ttu-id="6c9a0-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c9a0-124">OUTPUTS</span></span>

### <span data-ttu-id="6c9a0-125">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="6c9a0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c9a0-126">NOTES</span></span>

## <span data-ttu-id="6c9a0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c9a0-127">RELATED LINKS</span></span>

[<span data-ttu-id="6c9a0-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="6c9a0-129">Neu – AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="6c9a0-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="6c9a0-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
