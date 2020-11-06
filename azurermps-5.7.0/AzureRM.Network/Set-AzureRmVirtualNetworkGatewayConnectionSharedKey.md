---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2f6af6dbbe8a7241cb25e1715859a68bec24598c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481109"
---
# <span data-ttu-id="3f591-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3f591-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="3f591-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f591-102">SYNOPSIS</span></span>
<span data-ttu-id="3f591-103">Konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3f591-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f591-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f591-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f591-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f591-105">DESCRIPTION</span></span>
<span data-ttu-id="3f591-106">Das Cmdlet " **festlegen-AzureRmVirtualNetworkGatewayConnectionSharedKey** " konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3f591-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="3f591-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f591-107">EXAMPLES</span></span>

## <span data-ttu-id="3f591-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f591-108">PARAMETERS</span></span>

### <span data-ttu-id="3f591-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f591-109">-DefaultProfile</span></span>
<span data-ttu-id="3f591-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f591-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f591-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3f591-111">-Force</span></span>
<span data-ttu-id="3f591-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3f591-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f591-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3f591-113">-Name</span></span>
<span data-ttu-id="3f591-114">Gibt den Namen des freigegebenen Schlüssels für virtuelles Netzwerkgateway an.</span><span class="sxs-lookup"><span data-stu-id="3f591-114">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="3f591-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f591-115">-ResourceGroupName</span></span>
<span data-ttu-id="3f591-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerkgateway gehört</span><span class="sxs-lookup"><span data-stu-id="3f591-116">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="3f591-117">-Wert</span><span class="sxs-lookup"><span data-stu-id="3f591-117">-Value</span></span>
<span data-ttu-id="3f591-118">Gibt den Wert des freigegebenen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="3f591-118">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="3f591-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f591-119">-Confirm</span></span>
<span data-ttu-id="3f591-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f591-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f591-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f591-121">-WhatIf</span></span>
<span data-ttu-id="3f591-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f591-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f591-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f591-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f591-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f591-124">CommonParameters</span></span>
<span data-ttu-id="3f591-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f591-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f591-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f591-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f591-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f591-127">INPUTS</span></span>

### <span data-ttu-id="3f591-128">Keine</span><span class="sxs-lookup"><span data-stu-id="3f591-128">None</span></span>
<span data-ttu-id="3f591-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3f591-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f591-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f591-130">OUTPUTS</span></span>

### <span data-ttu-id="3f591-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3f591-131">System.String</span></span>

## <span data-ttu-id="3f591-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f591-132">NOTES</span></span>

## <span data-ttu-id="3f591-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f591-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f591-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3f591-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="3f591-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3f591-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


