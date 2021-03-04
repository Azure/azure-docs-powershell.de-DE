---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2c32263d52f8e260c67395484b2a9a2e3e479ecb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929440"
---
# <span data-ttu-id="b9bd8-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b9bd8-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b9bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bd8-103">Konfiguriert den freigegebenen Schlüssel der Gatewayverbindung für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b9bd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9bd8-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9bd8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="b9bd8-106">Das **Cmdlet Set-AzVirtualNetworkGatewayConnectionSharedKey** konfiguriert den freigegebenen Schlüssel der Gatewayverbindung für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b9bd8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9bd8-107">EXAMPLES</span></span>

### <span data-ttu-id="b9bd8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9bd8-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="b9bd8-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b9bd8-109">PARAMETERS</span></span>

### <span data-ttu-id="b9bd8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bd8-110">-DefaultProfile</span></span>
<span data-ttu-id="b9bd8-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9bd8-112">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b9bd8-112">-Force</span></span>
<span data-ttu-id="b9bd8-113">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9bd8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b9bd8-114">-Name</span></span>
<span data-ttu-id="b9bd8-115">Gibt den Namen des freigegebenen Schlüssels des virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9bd8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9bd8-116">-ResourceGroupName</span></span>
<span data-ttu-id="b9bd8-117">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerkgateway gehört</span><span class="sxs-lookup"><span data-stu-id="b9bd8-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9bd8-118">-Wert</span><span class="sxs-lookup"><span data-stu-id="b9bd8-118">-Value</span></span>
<span data-ttu-id="b9bd8-119">Gibt den Wert des freigegebenen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-119">Specifies the value of the shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9bd8-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9bd8-120">-Confirm</span></span>
<span data-ttu-id="b9bd8-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9bd8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9bd8-122">-WhatIf</span></span>
<span data-ttu-id="b9bd8-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9bd8-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9bd8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bd8-125">CommonParameters</span></span>
<span data-ttu-id="b9bd8-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9bd8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bd8-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9bd8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bd8-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9bd8-128">INPUTS</span></span>

### <span data-ttu-id="b9bd8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b9bd8-129">System.String</span></span>

## <span data-ttu-id="b9bd8-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9bd8-130">OUTPUTS</span></span>

### <span data-ttu-id="b9bd8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b9bd8-131">System.String</span></span>

## <span data-ttu-id="b9bd8-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b9bd8-132">NOTES</span></span>

## <span data-ttu-id="b9bd8-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b9bd8-133">RELATED LINKS</span></span>

[<span data-ttu-id="b9bd8-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b9bd8-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b9bd8-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b9bd8-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
