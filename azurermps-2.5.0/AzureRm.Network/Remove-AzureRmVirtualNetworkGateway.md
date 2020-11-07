---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 958ddffb02aaa6c8ac81f413cca6453f7f87c3a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849952"
---
# <span data-ttu-id="a8155-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8155-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="a8155-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8155-102">SYNOPSIS</span></span>
<span data-ttu-id="a8155-103">Löschen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="a8155-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8155-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8155-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8155-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8155-105">DESCRIPTION</span></span>
<span data-ttu-id="a8155-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8155-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="a8155-107">Das Cmdlet " **Get-AzureRmVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="a8155-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="a8155-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8155-108">EXAMPLES</span></span>

### <span data-ttu-id="a8155-109">1: Löschen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="a8155-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="a8155-110">Löscht das Objekt des virtuellen Netzwerkgateways mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG"</span><span class="sxs-lookup"><span data-stu-id="a8155-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="a8155-111">Hinweis: Sie müssen zuerst alle Verbindungen mit dem virtuellen Netzwerk Gateway mithilfe des Cmdlets **Remove-AzureRmVirtualNetworkGatewayConnection** löschen.</span><span class="sxs-lookup"><span data-stu-id="a8155-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="a8155-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8155-112">PARAMETERS</span></span>

### <span data-ttu-id="a8155-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8155-113">-AsJob</span></span>
<span data-ttu-id="a8155-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a8155-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8155-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8155-115">-DefaultProfile</span></span>
<span data-ttu-id="a8155-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8155-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8155-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a8155-117">-Force</span></span>
<span data-ttu-id="a8155-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a8155-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8155-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a8155-119">-Name</span></span>
<span data-ttu-id="a8155-120">Gibt den Namen des virtuellen Netzwerkgateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a8155-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8155-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8155-121">-PassThru</span></span>
<span data-ttu-id="a8155-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8155-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8155-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a8155-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8155-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8155-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8155-125">Gibt den Namen der Ressourcengruppe an, die das virtuelle Netzwerkgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="a8155-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="a8155-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8155-126">-Confirm</span></span>
<span data-ttu-id="a8155-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8155-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8155-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8155-128">-WhatIf</span></span>
<span data-ttu-id="a8155-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8155-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8155-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8155-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8155-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8155-131">CommonParameters</span></span>
<span data-ttu-id="a8155-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8155-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8155-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8155-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8155-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8155-134">INPUTS</span></span>

## <span data-ttu-id="a8155-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8155-135">OUTPUTS</span></span>

## <span data-ttu-id="a8155-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8155-136">NOTES</span></span>

## <span data-ttu-id="a8155-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8155-137">RELATED LINKS</span></span>

