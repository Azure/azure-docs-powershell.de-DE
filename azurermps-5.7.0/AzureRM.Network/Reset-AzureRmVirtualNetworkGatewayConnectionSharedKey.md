---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504518"
---
# <span data-ttu-id="37ff9-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="37ff9-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="37ff9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37ff9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37ff9-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="37ff9-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37ff9-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37ff9-104">DESCRIPTION</span></span>

## <span data-ttu-id="37ff9-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37ff9-105">EXAMPLES</span></span>

## <span data-ttu-id="37ff9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37ff9-106">PARAMETERS</span></span>

### <span data-ttu-id="37ff9-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ff9-107">-DefaultProfile</span></span>
<span data-ttu-id="37ff9-108">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37ff9-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ff9-109">-Force</span><span class="sxs-lookup"><span data-stu-id="37ff9-109">-Force</span></span>
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

### <span data-ttu-id="37ff9-110">-Keylength</span><span class="sxs-lookup"><span data-stu-id="37ff9-110">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ff9-111">-Name</span><span class="sxs-lookup"><span data-stu-id="37ff9-111">-Name</span></span>
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

### <span data-ttu-id="37ff9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ff9-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="37ff9-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37ff9-113">-Confirm</span></span>
<span data-ttu-id="37ff9-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37ff9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ff9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ff9-115">-WhatIf</span></span>
<span data-ttu-id="37ff9-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37ff9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ff9-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37ff9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ff9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ff9-118">CommonParameters</span></span>
<span data-ttu-id="37ff9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ff9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ff9-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ff9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ff9-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37ff9-121">INPUTS</span></span>

### <span data-ttu-id="37ff9-122">Keine</span><span class="sxs-lookup"><span data-stu-id="37ff9-122">None</span></span>
<span data-ttu-id="37ff9-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="37ff9-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37ff9-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37ff9-124">OUTPUTS</span></span>

### <span data-ttu-id="37ff9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="37ff9-125">System.String</span></span>

## <span data-ttu-id="37ff9-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="37ff9-126">NOTES</span></span>

## <span data-ttu-id="37ff9-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37ff9-127">RELATED LINKS</span></span>

[<span data-ttu-id="37ff9-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="37ff9-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="37ff9-129">Satz-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="37ff9-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


