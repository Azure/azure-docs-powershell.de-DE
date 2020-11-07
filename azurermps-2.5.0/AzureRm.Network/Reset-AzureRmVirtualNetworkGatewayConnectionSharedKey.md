---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850603"
---
# <span data-ttu-id="c9efe-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c9efe-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c9efe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9efe-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9efe-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9efe-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9efe-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9efe-104">DESCRIPTION</span></span>

## <span data-ttu-id="c9efe-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9efe-105">EXAMPLES</span></span>

### <span data-ttu-id="c9efe-106">1:</span><span class="sxs-lookup"><span data-stu-id="c9efe-106">1:</span></span>
```

```

## <span data-ttu-id="c9efe-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9efe-107">PARAMETERS</span></span>

### <span data-ttu-id="c9efe-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9efe-108">-DefaultProfile</span></span>
<span data-ttu-id="c9efe-109">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9efe-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9efe-110">-Force</span><span class="sxs-lookup"><span data-stu-id="c9efe-110">-Force</span></span>
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

### <span data-ttu-id="c9efe-111">-Keylength</span><span class="sxs-lookup"><span data-stu-id="c9efe-111">-KeyLength</span></span>
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

### <span data-ttu-id="c9efe-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c9efe-112">-Name</span></span>
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

### <span data-ttu-id="c9efe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9efe-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c9efe-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9efe-114">-Confirm</span></span>
<span data-ttu-id="c9efe-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9efe-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9efe-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9efe-116">-WhatIf</span></span>
<span data-ttu-id="c9efe-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9efe-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9efe-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9efe-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9efe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9efe-119">CommonParameters</span></span>
<span data-ttu-id="c9efe-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9efe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9efe-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9efe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9efe-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9efe-122">INPUTS</span></span>

## <span data-ttu-id="c9efe-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9efe-123">OUTPUTS</span></span>

### <span data-ttu-id="c9efe-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c9efe-124">System.String</span></span>

## <span data-ttu-id="c9efe-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9efe-125">NOTES</span></span>

## <span data-ttu-id="c9efe-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9efe-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9efe-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c9efe-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c9efe-128">Satz-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c9efe-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


