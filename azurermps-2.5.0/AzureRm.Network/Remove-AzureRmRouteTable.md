---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: f78b888e75db758f254924dee9fbf501050717b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850615"
---
# <span data-ttu-id="1bda3-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1bda3-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="1bda3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bda3-102">SYNOPSIS</span></span>
<span data-ttu-id="1bda3-103">Entfernt eine Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1bda3-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bda3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bda3-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bda3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bda3-105">DESCRIPTION</span></span>
<span data-ttu-id="1bda3-106">Das Cmdlet **Remove-AzureRmRouteTable** entfernt eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1bda3-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="1bda3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bda3-107">EXAMPLES</span></span>

### <span data-ttu-id="1bda3-108">Beispiel 1: Entfernen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="1bda3-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="1bda3-109">Dieser Befehl entfernt die Routingtabelle mit dem Namen RouteTable01 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1bda3-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="1bda3-110">Das Cmdlet fordert Sie zur Bestätigung auf, bevor die Tabelle entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1bda3-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="1bda3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bda3-111">PARAMETERS</span></span>

### <span data-ttu-id="1bda3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bda3-112">-AsJob</span></span>
<span data-ttu-id="1bda3-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1bda3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bda3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bda3-114">-DefaultProfile</span></span>
<span data-ttu-id="1bda3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bda3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bda3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1bda3-116">-Force</span></span>
<span data-ttu-id="1bda3-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1bda3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1bda3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1bda3-118">-Name</span></span>
<span data-ttu-id="1bda3-119">Gibt den Namen der Arbeitsplan Tabelle an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1bda3-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1bda3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bda3-120">-PassThru</span></span>
<span data-ttu-id="1bda3-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1bda3-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1bda3-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1bda3-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1bda3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bda3-123">-ResourceGroupName</span></span>
<span data-ttu-id="1bda3-124">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet entfernte Arbeitsplan Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="1bda3-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1bda3-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bda3-125">-Confirm</span></span>
<span data-ttu-id="1bda3-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bda3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bda3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bda3-127">-WhatIf</span></span>
<span data-ttu-id="1bda3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bda3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bda3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bda3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bda3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bda3-130">CommonParameters</span></span>
<span data-ttu-id="1bda3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bda3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bda3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bda3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bda3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bda3-133">INPUTS</span></span>

## <span data-ttu-id="1bda3-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bda3-134">OUTPUTS</span></span>

## <span data-ttu-id="1bda3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bda3-135">NOTES</span></span>

## <span data-ttu-id="1bda3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bda3-136">RELATED LINKS</span></span>

[<span data-ttu-id="1bda3-137">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1bda3-137">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="1bda3-138">Neu – AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1bda3-138">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="1bda3-139">Satz-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1bda3-139">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


