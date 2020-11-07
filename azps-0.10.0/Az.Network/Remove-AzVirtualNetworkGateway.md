---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: bb63f9d56dc78943f9232107e39188ae3d29f43f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843764"
---
# <span data-ttu-id="c0cfb-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0cfb-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c0cfb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cfb-103">Löschen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="c0cfb-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="c0cfb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0cfb-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0cfb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="c0cfb-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="c0cfb-107">Das Cmdlet " **Get-AzVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c0cfb-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0cfb-108">EXAMPLES</span></span>

### <span data-ttu-id="c0cfb-109">1: Löschen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="c0cfb-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c0cfb-110">Löscht das Objekt des virtuellen Netzwerkgateways mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG"</span><span class="sxs-lookup"><span data-stu-id="c0cfb-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="c0cfb-111">Hinweis: Sie müssen zuerst alle Verbindungen mit dem virtuellen Netzwerk Gateway mithilfe des Cmdlets **Remove-AzVirtualNetworkGatewayConnection** löschen.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="c0cfb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0cfb-112">PARAMETERS</span></span>

### <span data-ttu-id="c0cfb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0cfb-113">-AsJob</span></span>
<span data-ttu-id="c0cfb-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c0cfb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0cfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cfb-115">-DefaultProfile</span></span>
<span data-ttu-id="c0cfb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0cfb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c0cfb-117">-Force</span></span>
<span data-ttu-id="c0cfb-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0cfb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c0cfb-119">-Name</span></span>
<span data-ttu-id="c0cfb-120">Gibt den Namen des virtuellen Netzwerkgateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c0cfb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0cfb-121">-PassThru</span></span>
<span data-ttu-id="c0cfb-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0cfb-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0cfb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cfb-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0cfb-125">Gibt den Namen der Ressourcengruppe an, die das virtuelle Netzwerkgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="c0cfb-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0cfb-126">-Confirm</span></span>
<span data-ttu-id="c0cfb-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0cfb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0cfb-128">-WhatIf</span></span>
<span data-ttu-id="c0cfb-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cfb-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0cfb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cfb-131">CommonParameters</span></span>
<span data-ttu-id="c0cfb-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0cfb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cfb-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0cfb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cfb-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0cfb-134">INPUTS</span></span>

## <span data-ttu-id="c0cfb-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0cfb-135">OUTPUTS</span></span>

## <span data-ttu-id="c0cfb-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0cfb-136">NOTES</span></span>

## <span data-ttu-id="c0cfb-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0cfb-137">RELATED LINKS</span></span>

