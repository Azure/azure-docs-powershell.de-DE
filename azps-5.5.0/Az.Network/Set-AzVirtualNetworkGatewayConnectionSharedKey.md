---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146553"
---
# <span data-ttu-id="ce9bb-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce9bb-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ce9bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9bb-103">Konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgatewayverbindung.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="ce9bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce9bb-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce9bb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce9bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ce9bb-106">Das **Cmdlet Set-AzVirtualNetworkGatewayConnectionSharedKey** konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgatewayverbindung.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="ce9bb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce9bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ce9bb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce9bb-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="ce9bb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce9bb-109">PARAMETERS</span></span>

### <span data-ttu-id="ce9bb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9bb-110">-DefaultProfile</span></span>
<span data-ttu-id="ce9bb-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce9bb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="ce9bb-112">-Force</span></span>
<span data-ttu-id="ce9bb-113">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce9bb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ce9bb-114">-Name</span></span>
<span data-ttu-id="ce9bb-115">Gibt den Namen des freigegebenen Schlüssels des virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="ce9bb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9bb-116">-ResourceGroupName</span></span>
<span data-ttu-id="ce9bb-117">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerkgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="ce9bb-118">-Value</span><span class="sxs-lookup"><span data-stu-id="ce9bb-118">-Value</span></span>
<span data-ttu-id="ce9bb-119">Gibt den Wert des freigegebenen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="ce9bb-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce9bb-120">-Confirm</span></span>
<span data-ttu-id="ce9bb-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce9bb-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce9bb-122">-WhatIf</span></span>
<span data-ttu-id="ce9bb-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce9bb-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce9bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9bb-125">CommonParameters</span></span>
<span data-ttu-id="ce9bb-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce9bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9bb-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce9bb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9bb-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce9bb-128">INPUTS</span></span>

### <span data-ttu-id="ce9bb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ce9bb-129">System.String</span></span>

## <span data-ttu-id="ce9bb-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce9bb-130">OUTPUTS</span></span>

### <span data-ttu-id="ce9bb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ce9bb-131">System.String</span></span>

## <span data-ttu-id="ce9bb-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce9bb-132">NOTES</span></span>

## <span data-ttu-id="ce9bb-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce9bb-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce9bb-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce9bb-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ce9bb-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce9bb-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
