---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 3f09656caaccb103afa096ca0995489b3768e40e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822872"
---
# <span data-ttu-id="23a26-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23a26-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="23a26-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23a26-102">SYNOPSIS</span></span>
<span data-ttu-id="23a26-103">Löscht ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="23a26-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="23a26-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23a26-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23a26-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23a26-105">DESCRIPTION</span></span>
<span data-ttu-id="23a26-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="23a26-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="23a26-107">Das Cmdlet **Remove-AzLocalNetworkGateway** löscht das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf Name und Ressourcengruppennamen.</span><span class="sxs-lookup"><span data-stu-id="23a26-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="23a26-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23a26-108">EXAMPLES</span></span>

### <span data-ttu-id="23a26-109">1: Löschen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="23a26-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="23a26-110">Löscht das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" Hinweis: Sie müssen zuerst alle Verbindungen mit dem lokalen Netzwerkgateway löschen, indem Sie das Cmdlet **Remove-AzVirtualNetworkGatewayConnection** verwenden.</span><span class="sxs-lookup"><span data-stu-id="23a26-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="23a26-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="23a26-111">PARAMETERS</span></span>

### <span data-ttu-id="23a26-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23a26-112">-AsJob</span></span>
<span data-ttu-id="23a26-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="23a26-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23a26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a26-114">-DefaultProfile</span></span>
<span data-ttu-id="23a26-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23a26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23a26-116">-Force</span><span class="sxs-lookup"><span data-stu-id="23a26-116">-Force</span></span>
<span data-ttu-id="23a26-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="23a26-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23a26-118">-Name</span><span class="sxs-lookup"><span data-stu-id="23a26-118">-Name</span></span>
<span data-ttu-id="23a26-119">Gibt den Namen des lokalen Netzwerkgateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="23a26-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="23a26-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23a26-120">-PassThru</span></span>
<span data-ttu-id="23a26-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="23a26-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="23a26-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="23a26-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23a26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a26-123">-ResourceGroupName</span></span>
<span data-ttu-id="23a26-124">Gibt den Namen der Ressourcengruppe an, die das lokale Netzwerkgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="23a26-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="23a26-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23a26-125">-Confirm</span></span>
<span data-ttu-id="23a26-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23a26-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23a26-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23a26-127">-WhatIf</span></span>
<span data-ttu-id="23a26-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23a26-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23a26-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23a26-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23a26-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a26-130">CommonParameters</span></span>
<span data-ttu-id="23a26-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a26-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a26-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a26-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a26-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23a26-133">INPUTS</span></span>

### <span data-ttu-id="23a26-134">System. String</span><span class="sxs-lookup"><span data-stu-id="23a26-134">System.String</span></span>

## <span data-ttu-id="23a26-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23a26-135">OUTPUTS</span></span>

### <span data-ttu-id="23a26-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23a26-136">System.Boolean</span></span>

## <span data-ttu-id="23a26-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="23a26-137">NOTES</span></span>

## <span data-ttu-id="23a26-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23a26-138">RELATED LINKS</span></span>

[<span data-ttu-id="23a26-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23a26-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="23a26-140">Neu – AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23a26-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="23a26-141">Satz-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23a26-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
