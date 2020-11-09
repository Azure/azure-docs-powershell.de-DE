---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303663"
---
# <span data-ttu-id="b4412-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4412-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b4412-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4412-102">SYNOPSIS</span></span>
<span data-ttu-id="b4412-103">Entfernt einen Back-End-Adresspool von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b4412-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="b4412-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4412-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4412-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4412-105">DESCRIPTION</span></span>
<span data-ttu-id="b4412-106">Das Cmdlet **Remove-AzApplicationGatewayBackendAddressPool** entfernt einen Back-End-Adresspool von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b4412-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="b4412-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4412-107">EXAMPLES</span></span>

### <span data-ttu-id="b4412-108">Beispiel 1: Entfernen eines Back-End-Adresspools von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="b4412-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="b4412-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b4412-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="b4412-110">Mit dem zweiten Befehl wird der Back-End-Adresspool mit dem Namen BackEndPool02 aus dem Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4412-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="b4412-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4412-111">PARAMETERS</span></span>

### <span data-ttu-id="b4412-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4412-112">-ApplicationGateway</span></span>
<span data-ttu-id="b4412-113">Gibt das Anwendungsgateway an, aus dem dieses Cmdlet einen Back-End-Adresspool entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4412-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4412-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4412-114">-DefaultProfile</span></span>
<span data-ttu-id="b4412-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4412-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4412-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b4412-116">-Name</span></span>
<span data-ttu-id="b4412-117">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4412-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4412-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4412-118">-Confirm</span></span>
<span data-ttu-id="b4412-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4412-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4412-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4412-120">-WhatIf</span></span>
<span data-ttu-id="b4412-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4412-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4412-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4412-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4412-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4412-123">CommonParameters</span></span>
<span data-ttu-id="b4412-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4412-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4412-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4412-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4412-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4412-126">INPUTS</span></span>

### <span data-ttu-id="b4412-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4412-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4412-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4412-128">OUTPUTS</span></span>

### <span data-ttu-id="b4412-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4412-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b4412-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4412-130">NOTES</span></span>

## <span data-ttu-id="b4412-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4412-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4412-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4412-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b4412-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4412-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b4412-134">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4412-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b4412-135">Satz-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4412-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


