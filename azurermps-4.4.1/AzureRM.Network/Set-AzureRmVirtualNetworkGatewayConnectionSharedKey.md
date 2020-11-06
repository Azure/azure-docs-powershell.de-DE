---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497034"
---
# <span data-ttu-id="f0380-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f0380-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f0380-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0380-102">SYNOPSIS</span></span>
<span data-ttu-id="f0380-103">Konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f0380-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0380-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0380-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0380-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0380-105">DESCRIPTION</span></span>
<span data-ttu-id="f0380-106">Das Cmdlet " **festlegen-AzureRmVirtualNetworkGatewayConnectionSharedKey** " konfiguriert den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f0380-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f0380-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0380-107">EXAMPLES</span></span>

## <span data-ttu-id="f0380-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0380-108">PARAMETERS</span></span>

### <span data-ttu-id="f0380-109">-Force</span><span class="sxs-lookup"><span data-stu-id="f0380-109">-Force</span></span>
<span data-ttu-id="f0380-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f0380-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0380-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f0380-111">-Name</span></span>
<span data-ttu-id="f0380-112">Gibt den Namen des freigegebenen Schlüssels für virtuelles Netzwerkgateway an.</span><span class="sxs-lookup"><span data-stu-id="f0380-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="f0380-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0380-113">-ResourceGroupName</span></span>
<span data-ttu-id="f0380-114">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerkgateway gehört</span><span class="sxs-lookup"><span data-stu-id="f0380-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="f0380-115">-Wert</span><span class="sxs-lookup"><span data-stu-id="f0380-115">-Value</span></span>
<span data-ttu-id="f0380-116">Gibt den Wert des freigegebenen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="f0380-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="f0380-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0380-117">-Confirm</span></span>
<span data-ttu-id="f0380-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0380-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0380-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0380-119">-WhatIf</span></span>
<span data-ttu-id="f0380-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0380-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0380-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0380-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0380-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0380-122">-DefaultProfile</span></span>
<span data-ttu-id="f0380-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0380-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0380-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0380-124">CommonParameters</span></span>
<span data-ttu-id="f0380-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0380-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0380-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0380-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0380-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0380-127">INPUTS</span></span>

## <span data-ttu-id="f0380-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0380-128">OUTPUTS</span></span>

### <span data-ttu-id="f0380-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f0380-129">System.String</span></span>

## <span data-ttu-id="f0380-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0380-130">NOTES</span></span>

## <span data-ttu-id="f0380-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0380-131">RELATED LINKS</span></span>

[<span data-ttu-id="f0380-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f0380-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f0380-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f0380-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


