---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 1aca9335da67bb3c1144f67fb8f14ad9b2a7f1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478418"
---
# <span data-ttu-id="73c1a-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73c1a-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="73c1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="73c1a-103">Löscht ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="73c1a-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73c1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73c1a-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="73c1a-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="73c1a-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="73c1a-107">Das Cmdlet **Remove-AzureRmLocalNetworkGateway** löscht das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf Name und Ressourcengruppennamen.</span><span class="sxs-lookup"><span data-stu-id="73c1a-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="73c1a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73c1a-108">EXAMPLES</span></span>

### <span data-ttu-id="73c1a-109">1: Löschen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="73c1a-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="73c1a-110">Löscht das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="73c1a-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="73c1a-111">Hinweis: Sie müssen zuerst alle Verbindungen mit dem lokalen Netzwerk Gateway mithilfe des Cmdlets **Remove-AzureRmVirtualNetworkGatewayConnection** löschen.</span><span class="sxs-lookup"><span data-stu-id="73c1a-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="73c1a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c1a-112">PARAMETERS</span></span>

### <span data-ttu-id="73c1a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73c1a-113">-AsJob</span></span>
<span data-ttu-id="73c1a-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="73c1a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73c1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c1a-115">-DefaultProfile</span></span>
<span data-ttu-id="73c1a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73c1a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73c1a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="73c1a-117">-Force</span></span>
<span data-ttu-id="73c1a-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="73c1a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73c1a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="73c1a-119">-Name</span></span>
<span data-ttu-id="73c1a-120">Gibt den Namen des lokalen Netzwerkgateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="73c1a-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="73c1a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73c1a-121">-PassThru</span></span>
<span data-ttu-id="73c1a-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="73c1a-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="73c1a-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="73c1a-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="73c1a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c1a-124">-ResourceGroupName</span></span>
<span data-ttu-id="73c1a-125">Gibt den Namen der Ressourcengruppe an, die das lokale Netzwerkgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="73c1a-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="73c1a-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73c1a-126">-Confirm</span></span>
<span data-ttu-id="73c1a-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73c1a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c1a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c1a-128">-WhatIf</span></span>
<span data-ttu-id="73c1a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73c1a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c1a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73c1a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c1a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c1a-131">CommonParameters</span></span>
<span data-ttu-id="73c1a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c1a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c1a-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c1a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c1a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73c1a-134">INPUTS</span></span>

### <span data-ttu-id="73c1a-135">Keine</span><span class="sxs-lookup"><span data-stu-id="73c1a-135">None</span></span>
<span data-ttu-id="73c1a-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="73c1a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73c1a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73c1a-137">OUTPUTS</span></span>

## <span data-ttu-id="73c1a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="73c1a-138">NOTES</span></span>

## <span data-ttu-id="73c1a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73c1a-139">RELATED LINKS</span></span>

[<span data-ttu-id="73c1a-140">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73c1a-140">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="73c1a-141">Neu – AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73c1a-141">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="73c1a-142">Satz-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73c1a-142">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


