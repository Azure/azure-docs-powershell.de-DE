---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 7b82cf189d912d000c143b20cca76c4f2683b7d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849567"
---
# <span data-ttu-id="f7ee2-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7ee2-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f7ee2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ee2-103">Entfernt einen Back-End-Adresspool von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7ee2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7ee2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7ee2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ee2-106">Das Cmdlet **Remove-AzureRmApplicationGatewayBackendAddressPool** entfernt einen Back-End-Adresspool von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="f7ee2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7ee2-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ee2-108">Beispiel 1: Entfernen eines Back-End-Adresspools von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="f7ee2-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="f7ee2-110">Mit dem zweiten Befehl wird der Back-End-Adresspool mit dem Namen BackEndPool02 aus dem Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="f7ee2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7ee2-111">PARAMETERS</span></span>

### <span data-ttu-id="f7ee2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-112">-ApplicationGateway</span></span>
<span data-ttu-id="f7ee2-113">Gibt das Anwendungsgateway an, aus dem dieses Cmdlet einen Back-End-Adresspool entfernt.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ee2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ee2-114">-DefaultProfile</span></span>
<span data-ttu-id="f7ee2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7ee2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f7ee2-116">-Name</span></span>
<span data-ttu-id="f7ee2-117">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7ee2-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7ee2-118">-Confirm</span></span>
<span data-ttu-id="f7ee2-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7ee2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7ee2-120">-WhatIf</span></span>
<span data-ttu-id="f7ee2-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7ee2-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7ee2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ee2-123">CommonParameters</span></span>
<span data-ttu-id="f7ee2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ee2-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ee2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ee2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7ee2-126">INPUTS</span></span>

### <span data-ttu-id="f7ee2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f7ee2-127">System.String</span></span>

## <span data-ttu-id="f7ee2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7ee2-128">OUTPUTS</span></span>

### <span data-ttu-id="f7ee2-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7ee2-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f7ee2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7ee2-130">NOTES</span></span>

## <span data-ttu-id="f7ee2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7ee2-131">RELATED LINKS</span></span>

[<span data-ttu-id="f7ee2-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7ee2-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f7ee2-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7ee2-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f7ee2-134">Neu – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7ee2-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f7ee2-135">Satz-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7ee2-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


