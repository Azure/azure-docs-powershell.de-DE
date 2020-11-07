---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: f3268d78ac0630e18307646086689cb8d435c290
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663119"
---
# <span data-ttu-id="aae80-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aae80-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="aae80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aae80-102">SYNOPSIS</span></span>
<span data-ttu-id="aae80-103">Konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="aae80-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aae80-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aae80-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aae80-105">DESCRIPTION</span></span>
<span data-ttu-id="aae80-106">Das Cmdlet " **festlegen-AzureRmVirtualNetworkGatewayConnectionSharedKey** " konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="aae80-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="aae80-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aae80-107">EXAMPLES</span></span>

### <span data-ttu-id="aae80-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="aae80-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="aae80-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aae80-109">PARAMETERS</span></span>

### <span data-ttu-id="aae80-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae80-110">-DefaultProfile</span></span>
<span data-ttu-id="aae80-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aae80-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae80-112">-Force</span><span class="sxs-lookup"><span data-stu-id="aae80-112">-Force</span></span>
<span data-ttu-id="aae80-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="aae80-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aae80-114">-Name</span><span class="sxs-lookup"><span data-stu-id="aae80-114">-Name</span></span>
<span data-ttu-id="aae80-115">Gibt den Namen des freigegebenen Schlüssels für virtuelles Netzwerkgateway an.</span><span class="sxs-lookup"><span data-stu-id="aae80-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="aae80-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae80-116">-ResourceGroupName</span></span>
<span data-ttu-id="aae80-117">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerkgateway gehört</span><span class="sxs-lookup"><span data-stu-id="aae80-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="aae80-118">-Wert</span><span class="sxs-lookup"><span data-stu-id="aae80-118">-Value</span></span>
<span data-ttu-id="aae80-119">Gibt den Wert des freigegebenen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="aae80-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="aae80-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aae80-120">-Confirm</span></span>
<span data-ttu-id="aae80-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aae80-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae80-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae80-122">-WhatIf</span></span>
<span data-ttu-id="aae80-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aae80-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aae80-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aae80-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae80-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae80-125">CommonParameters</span></span>
<span data-ttu-id="aae80-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae80-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae80-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae80-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae80-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aae80-128">INPUTS</span></span>

### <span data-ttu-id="aae80-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aae80-129">System.String</span></span>

## <span data-ttu-id="aae80-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aae80-130">OUTPUTS</span></span>

### <span data-ttu-id="aae80-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aae80-131">System.String</span></span>

## <span data-ttu-id="aae80-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="aae80-132">NOTES</span></span>

## <span data-ttu-id="aae80-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aae80-133">RELATED LINKS</span></span>

[<span data-ttu-id="aae80-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aae80-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="aae80-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aae80-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


