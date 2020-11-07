---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849928"
---
# <span data-ttu-id="1543a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1543a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="1543a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1543a-102">SYNOPSIS</span></span>
<span data-ttu-id="1543a-103">Konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="1543a-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1543a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1543a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1543a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1543a-105">DESCRIPTION</span></span>
<span data-ttu-id="1543a-106">Das Cmdlet " **festlegen-AzureRmVirtualNetworkGatewayConnectionSharedKey** " konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="1543a-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="1543a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1543a-107">EXAMPLES</span></span>

### <span data-ttu-id="1543a-108">1:</span><span class="sxs-lookup"><span data-stu-id="1543a-108">1:</span></span>
```

```

## <span data-ttu-id="1543a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1543a-109">PARAMETERS</span></span>

### <span data-ttu-id="1543a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1543a-110">-DefaultProfile</span></span>
<span data-ttu-id="1543a-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1543a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1543a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="1543a-112">-Force</span></span>
<span data-ttu-id="1543a-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1543a-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1543a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1543a-114">-Name</span></span>
<span data-ttu-id="1543a-115">Gibt den Namen des freigegebenen Schlüssels für virtuelles Netzwerkgateway an.</span><span class="sxs-lookup"><span data-stu-id="1543a-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1543a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1543a-116">-ResourceGroupName</span></span>
<span data-ttu-id="1543a-117">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerkgateway gehört</span><span class="sxs-lookup"><span data-stu-id="1543a-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1543a-118">-Wert</span><span class="sxs-lookup"><span data-stu-id="1543a-118">-Value</span></span>
<span data-ttu-id="1543a-119">Gibt den Wert des freigegebenen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="1543a-119">Specifies the value of the shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1543a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1543a-120">-Confirm</span></span>
<span data-ttu-id="1543a-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1543a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1543a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1543a-122">-WhatIf</span></span>
<span data-ttu-id="1543a-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1543a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1543a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1543a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1543a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1543a-125">CommonParameters</span></span>
<span data-ttu-id="1543a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1543a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1543a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1543a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1543a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1543a-128">INPUTS</span></span>

## <span data-ttu-id="1543a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1543a-129">OUTPUTS</span></span>

### <span data-ttu-id="1543a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1543a-130">System.String</span></span>

## <span data-ttu-id="1543a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1543a-131">NOTES</span></span>

## <span data-ttu-id="1543a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1543a-132">RELATED LINKS</span></span>

[<span data-ttu-id="1543a-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1543a-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="1543a-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1543a-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


