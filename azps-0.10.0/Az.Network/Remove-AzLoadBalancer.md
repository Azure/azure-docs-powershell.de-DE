---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 1602c9e5fb0244239eea4eec53661c3392ac0354
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841163"
---
# <span data-ttu-id="403dd-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="403dd-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="403dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="403dd-102">SYNOPSIS</span></span>
<span data-ttu-id="403dd-103">Entfernt ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="403dd-103">Removes a load balancer.</span></span>

## <span data-ttu-id="403dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="403dd-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="403dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="403dd-105">DESCRIPTION</span></span>
<span data-ttu-id="403dd-106">Das Cmdlet **Remove-AzLoadBalancer** entfernt ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="403dd-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="403dd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="403dd-107">EXAMPLES</span></span>

### <span data-ttu-id="403dd-108">Beispiel 1: Entfernen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="403dd-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="403dd-109">Mit diesem Befehl wird ein Lastenausgleichsmodul mit dem Namen MyLoadBalancer in der Ressourcengruppe "myresourcegroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="403dd-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="403dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="403dd-110">PARAMETERS</span></span>

### <span data-ttu-id="403dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="403dd-111">-AsJob</span></span>
<span data-ttu-id="403dd-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="403dd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="403dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403dd-113">-DefaultProfile</span></span>
<span data-ttu-id="403dd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="403dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="403dd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="403dd-115">-Force</span></span>
<span data-ttu-id="403dd-116">Gibt an, dass das Load Balancer vom Cmdlet entfernt wird, unabhängig davon, ob ihm Ressourcen zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="403dd-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="403dd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="403dd-117">-Name</span></span>
<span data-ttu-id="403dd-118">Gibt den Namen des zu entfernenden Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="403dd-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="403dd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="403dd-119">-PassThru</span></span>
<span data-ttu-id="403dd-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="403dd-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="403dd-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="403dd-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="403dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="403dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="403dd-123">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Load Balancer enthält.</span><span class="sxs-lookup"><span data-stu-id="403dd-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="403dd-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="403dd-124">-Confirm</span></span>
<span data-ttu-id="403dd-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="403dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="403dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="403dd-126">-WhatIf</span></span>
<span data-ttu-id="403dd-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="403dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="403dd-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="403dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="403dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403dd-129">CommonParameters</span></span>
<span data-ttu-id="403dd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="403dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403dd-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="403dd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403dd-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="403dd-132">INPUTS</span></span>

## <span data-ttu-id="403dd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="403dd-133">OUTPUTS</span></span>

## <span data-ttu-id="403dd-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="403dd-134">NOTES</span></span>

## <span data-ttu-id="403dd-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="403dd-135">RELATED LINKS</span></span>

[<span data-ttu-id="403dd-136">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="403dd-136">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="403dd-137">Neu – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="403dd-137">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="403dd-138">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="403dd-138">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


