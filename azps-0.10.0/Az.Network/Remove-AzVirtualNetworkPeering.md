---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3bc816f690f39b534a134e80df1a86c7bbca5dc1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843740"
---
# <span data-ttu-id="d6f70-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d6f70-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="d6f70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6f70-102">SYNOPSIS</span></span>

## <span data-ttu-id="d6f70-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6f70-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6f70-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6f70-104">DESCRIPTION</span></span>

## <span data-ttu-id="d6f70-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6f70-105">EXAMPLES</span></span>

### <span data-ttu-id="d6f70-106">Beispiel 1: Entfernen eines virtuellen Netzwerk Peerings</span><span class="sxs-lookup"><span data-stu-id="d6f70-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="d6f70-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6f70-107">PARAMETERS</span></span>

### <span data-ttu-id="d6f70-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f70-108">-AsJob</span></span>
<span data-ttu-id="d6f70-109">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d6f70-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6f70-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f70-110">-DefaultProfile</span></span>
<span data-ttu-id="d6f70-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6f70-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6f70-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d6f70-112">-Force</span></span>
<span data-ttu-id="d6f70-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d6f70-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6f70-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d6f70-114">-Name</span></span>
<span data-ttu-id="d6f70-115">Der Name des virtuellen Netzwerk Peerings.</span><span class="sxs-lookup"><span data-stu-id="d6f70-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="d6f70-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6f70-116">-PassThru</span></span>
<span data-ttu-id="d6f70-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6f70-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6f70-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d6f70-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6f70-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f70-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6f70-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d6f70-120">The resource group name</span></span>

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

### <span data-ttu-id="d6f70-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d6f70-121">-VirtualNetworkName</span></span>
<span data-ttu-id="d6f70-122">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="d6f70-122">The virtual network name.</span></span>

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

### <span data-ttu-id="d6f70-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6f70-123">-Confirm</span></span>
<span data-ttu-id="d6f70-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6f70-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f70-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f70-125">-WhatIf</span></span>
<span data-ttu-id="d6f70-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f70-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f70-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6f70-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f70-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f70-128">CommonParameters</span></span>
<span data-ttu-id="d6f70-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f70-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f70-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f70-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f70-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6f70-131">INPUTS</span></span>

## <span data-ttu-id="d6f70-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6f70-132">OUTPUTS</span></span>

## <span data-ttu-id="d6f70-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6f70-133">NOTES</span></span>

## <span data-ttu-id="d6f70-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6f70-134">RELATED LINKS</span></span>

