---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: ad205aabc12a2f0d6abffd16b83dadfc9a34ff4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004228"
---
# <span data-ttu-id="4720a-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4720a-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="4720a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4720a-102">SYNOPSIS</span></span>
<span data-ttu-id="4720a-103">Löscht ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="4720a-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="4720a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4720a-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4720a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4720a-105">DESCRIPTION</span></span>
<span data-ttu-id="4720a-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="4720a-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="4720a-107">Das Cmdlet **Remove-AzLocalNetworkGateway** löscht das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf Name und Ressourcengruppennamen.</span><span class="sxs-lookup"><span data-stu-id="4720a-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="4720a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4720a-108">EXAMPLES</span></span>

### <span data-ttu-id="4720a-109">1: Löschen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="4720a-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="4720a-110">Löscht das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" Hinweis: Sie müssen zuerst alle Verbindungen mit dem lokalen Netzwerkgateway löschen, indem Sie das Cmdlet **Remove-AzVirtualNetworkGatewayConnection** verwenden.</span><span class="sxs-lookup"><span data-stu-id="4720a-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="4720a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4720a-111">PARAMETERS</span></span>

### <span data-ttu-id="4720a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4720a-112">-AsJob</span></span>
<span data-ttu-id="4720a-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4720a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4720a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4720a-114">-DefaultProfile</span></span>
<span data-ttu-id="4720a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4720a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4720a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4720a-116">-Force</span></span>
<span data-ttu-id="4720a-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4720a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4720a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4720a-118">-Name</span></span>
<span data-ttu-id="4720a-119">Gibt den Namen des lokalen Netzwerkgateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4720a-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4720a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4720a-120">-PassThru</span></span>
<span data-ttu-id="4720a-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4720a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4720a-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="4720a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4720a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4720a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4720a-124">Gibt den Namen der Ressourcengruppe an, die das lokale Netzwerkgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="4720a-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="4720a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4720a-125">-Confirm</span></span>
<span data-ttu-id="4720a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4720a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4720a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4720a-127">-WhatIf</span></span>
<span data-ttu-id="4720a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4720a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4720a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4720a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4720a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4720a-130">CommonParameters</span></span>
<span data-ttu-id="4720a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4720a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4720a-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4720a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4720a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4720a-133">INPUTS</span></span>

### <span data-ttu-id="4720a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4720a-134">System.String</span></span>

## <span data-ttu-id="4720a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4720a-135">OUTPUTS</span></span>

### <span data-ttu-id="4720a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4720a-136">System.Boolean</span></span>

## <span data-ttu-id="4720a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4720a-137">NOTES</span></span>

## <span data-ttu-id="4720a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4720a-138">RELATED LINKS</span></span>

[<span data-ttu-id="4720a-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4720a-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="4720a-140">Neu – AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4720a-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="4720a-141">Satz-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4720a-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
