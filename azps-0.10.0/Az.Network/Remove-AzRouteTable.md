---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 434d70cbdce08750e69865e59197ebba5fb6e6fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843771"
---
# <span data-ttu-id="e1664-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1664-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="e1664-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1664-102">SYNOPSIS</span></span>
<span data-ttu-id="e1664-103">Entfernt eine Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e1664-103">Removes a route table.</span></span>

## <span data-ttu-id="e1664-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1664-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1664-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1664-105">DESCRIPTION</span></span>
<span data-ttu-id="e1664-106">Das Cmdlet **Remove-AzRouteTable** entfernt eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e1664-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="e1664-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1664-107">EXAMPLES</span></span>

### <span data-ttu-id="e1664-108">Beispiel 1: Entfernen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="e1664-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e1664-109">Dieser Befehl entfernt die Routingtabelle mit dem Namen RouteTable01 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e1664-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="e1664-110">Das Cmdlet fordert Sie zur Bestätigung auf, bevor die Tabelle entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e1664-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="e1664-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1664-111">PARAMETERS</span></span>

### <span data-ttu-id="e1664-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1664-112">-AsJob</span></span>
<span data-ttu-id="e1664-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e1664-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1664-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1664-114">-DefaultProfile</span></span>
<span data-ttu-id="e1664-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1664-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1664-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e1664-116">-Force</span></span>
<span data-ttu-id="e1664-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e1664-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1664-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e1664-118">-Name</span></span>
<span data-ttu-id="e1664-119">Gibt den Namen der Arbeitsplan Tabelle an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e1664-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e1664-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1664-120">-PassThru</span></span>
<span data-ttu-id="e1664-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e1664-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1664-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e1664-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1664-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1664-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1664-124">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet entfernte Arbeitsplan Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="e1664-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e1664-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1664-125">-Confirm</span></span>
<span data-ttu-id="e1664-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1664-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1664-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1664-127">-WhatIf</span></span>
<span data-ttu-id="e1664-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1664-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1664-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1664-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1664-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1664-130">CommonParameters</span></span>
<span data-ttu-id="e1664-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1664-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1664-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1664-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1664-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1664-133">INPUTS</span></span>

## <span data-ttu-id="e1664-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1664-134">OUTPUTS</span></span>

## <span data-ttu-id="e1664-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1664-135">NOTES</span></span>

## <span data-ttu-id="e1664-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1664-136">RELATED LINKS</span></span>

[<span data-ttu-id="e1664-137">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1664-137">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e1664-138">Neu – AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1664-138">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="e1664-139">Satz-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1664-139">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


