---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: e051bd56aa8c5b5da27e2179b8f4d58ec4e4196d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664532"
---
# <span data-ttu-id="06f38-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="06f38-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="06f38-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06f38-102">SYNOPSIS</span></span>
<span data-ttu-id="06f38-103">Setzt den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="06f38-103">Resets the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06f38-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06f38-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06f38-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06f38-105">DESCRIPTION</span></span>
<span data-ttu-id="06f38-106">Setzt den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="06f38-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="06f38-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06f38-107">EXAMPLES</span></span>

### <span data-ttu-id="06f38-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="06f38-108">Example 1:</span></span>
```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="06f38-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="06f38-109">PARAMETERS</span></span>

### <span data-ttu-id="06f38-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f38-110">-DefaultProfile</span></span>
<span data-ttu-id="06f38-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06f38-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06f38-112">-Force</span><span class="sxs-lookup"><span data-stu-id="06f38-112">-Force</span></span>
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

### <span data-ttu-id="06f38-113">-Keylength</span><span class="sxs-lookup"><span data-stu-id="06f38-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f38-114">-Name</span><span class="sxs-lookup"><span data-stu-id="06f38-114">-Name</span></span>
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

### <span data-ttu-id="06f38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f38-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="06f38-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06f38-116">-Confirm</span></span>
<span data-ttu-id="06f38-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06f38-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f38-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f38-118">-WhatIf</span></span>
<span data-ttu-id="06f38-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06f38-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f38-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06f38-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f38-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f38-121">CommonParameters</span></span>
<span data-ttu-id="06f38-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f38-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f38-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f38-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f38-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06f38-124">INPUTS</span></span>

### <span data-ttu-id="06f38-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06f38-125">System.String</span></span>

### <span data-ttu-id="06f38-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="06f38-126">System.UInt32</span></span>

## <span data-ttu-id="06f38-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06f38-127">OUTPUTS</span></span>

### <span data-ttu-id="06f38-128">System. String</span><span class="sxs-lookup"><span data-stu-id="06f38-128">System.String</span></span>

## <span data-ttu-id="06f38-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="06f38-129">NOTES</span></span>

## <span data-ttu-id="06f38-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06f38-130">RELATED LINKS</span></span>

[<span data-ttu-id="06f38-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="06f38-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="06f38-132">Satz-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="06f38-132">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


