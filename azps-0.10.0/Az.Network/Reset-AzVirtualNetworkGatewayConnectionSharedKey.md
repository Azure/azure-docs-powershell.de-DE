---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843732"
---
# <span data-ttu-id="e7283-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e7283-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="e7283-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7283-102">SYNOPSIS</span></span>

## <span data-ttu-id="e7283-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7283-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7283-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7283-104">DESCRIPTION</span></span>

## <span data-ttu-id="e7283-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7283-105">EXAMPLES</span></span>

### <span data-ttu-id="e7283-106">1:</span><span class="sxs-lookup"><span data-stu-id="e7283-106">1:</span></span>
```

```

## <span data-ttu-id="e7283-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7283-107">PARAMETERS</span></span>

### <span data-ttu-id="e7283-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7283-108">-DefaultProfile</span></span>
<span data-ttu-id="e7283-109">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7283-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7283-110">-Force</span><span class="sxs-lookup"><span data-stu-id="e7283-110">-Force</span></span>
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

### <span data-ttu-id="e7283-111">-Keylength</span><span class="sxs-lookup"><span data-stu-id="e7283-111">-KeyLength</span></span>
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

### <span data-ttu-id="e7283-112">-Name</span><span class="sxs-lookup"><span data-stu-id="e7283-112">-Name</span></span>
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

### <span data-ttu-id="e7283-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7283-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e7283-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7283-114">-Confirm</span></span>
<span data-ttu-id="e7283-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7283-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7283-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7283-116">-WhatIf</span></span>
<span data-ttu-id="e7283-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7283-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7283-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7283-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7283-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7283-119">CommonParameters</span></span>
<span data-ttu-id="e7283-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7283-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7283-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7283-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7283-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7283-122">INPUTS</span></span>

## <span data-ttu-id="e7283-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7283-123">OUTPUTS</span></span>

### <span data-ttu-id="e7283-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e7283-124">System.String</span></span>

## <span data-ttu-id="e7283-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7283-125">NOTES</span></span>

## <span data-ttu-id="e7283-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7283-126">RELATED LINKS</span></span>

[<span data-ttu-id="e7283-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e7283-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="e7283-128">Satz-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e7283-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


