---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298664"
---
# <span data-ttu-id="47105-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="47105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47105-102">SYNOPSIS</span></span>
<span data-ttu-id="47105-103">Setzt das skalierbare VPN-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="47105-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="47105-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47105-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47105-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="47105-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47105-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="47105-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47105-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="47105-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47105-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47105-108">DESCRIPTION</span></span>
<span data-ttu-id="47105-109">Setzt das VpnGateway zurück.</span><span class="sxs-lookup"><span data-stu-id="47105-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="47105-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47105-110">EXAMPLES</span></span>

### <span data-ttu-id="47105-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="47105-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="47105-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47105-112">PARAMETERS</span></span>

### <span data-ttu-id="47105-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47105-113">-AsJob</span></span>
<span data-ttu-id="47105-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="47105-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47105-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47105-115">-DefaultProfile</span></span>
<span data-ttu-id="47105-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47105-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47105-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-117">-VpnGateway</span></span>
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

### <span data-ttu-id="47105-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47105-118">CommonParameters</span></span>
<span data-ttu-id="47105-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47105-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47105-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47105-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47105-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47105-121">INPUTS</span></span>

### <span data-ttu-id="47105-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="47105-123">System.String</span><span class="sxs-lookup"><span data-stu-id="47105-123">System.String</span></span>

## <span data-ttu-id="47105-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47105-124">OUTPUTS</span></span>

### <span data-ttu-id="47105-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="47105-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47105-126">NOTES</span></span>

## <span data-ttu-id="47105-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47105-127">RELATED LINKS</span></span>

[<span data-ttu-id="47105-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="47105-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="47105-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="47105-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47105-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
