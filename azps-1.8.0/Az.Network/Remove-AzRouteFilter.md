---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 8f48cf6fb5b3c4489a116ef0f7ee5a32649d96ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660331"
---
# <span data-ttu-id="29d58-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="29d58-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="29d58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29d58-102">SYNOPSIS</span></span>
<span data-ttu-id="29d58-103">Entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="29d58-103">Removes a route filter.</span></span>

## <span data-ttu-id="29d58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29d58-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d58-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29d58-105">DESCRIPTION</span></span>
<span data-ttu-id="29d58-106">Das Cmdlet **Remove-AzRouteFilter** entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="29d58-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="29d58-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29d58-107">EXAMPLES</span></span>

### <span data-ttu-id="29d58-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29d58-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="29d58-109">Der Befehl entfernt den Routenfilter mit dem Namen RouteFilter01 in der Ressourcengruppe mit dem Namen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="29d58-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="29d58-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29d58-110">PARAMETERS</span></span>

### <span data-ttu-id="29d58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d58-111">-DefaultProfile</span></span>
<span data-ttu-id="29d58-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29d58-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29d58-113">-Force</span><span class="sxs-lookup"><span data-stu-id="29d58-113">-Force</span></span>
<span data-ttu-id="29d58-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="29d58-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="29d58-115">-Name</span><span class="sxs-lookup"><span data-stu-id="29d58-115">-Name</span></span>
<span data-ttu-id="29d58-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="29d58-116">The resource name.</span></span>

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

### <span data-ttu-id="29d58-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29d58-117">-PassThru</span></span>
<span data-ttu-id="29d58-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="29d58-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="29d58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d58-119">-ResourceGroupName</span></span>
<span data-ttu-id="29d58-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29d58-120">The resource group name.</span></span>

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

### <span data-ttu-id="29d58-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29d58-121">-Confirm</span></span>
<span data-ttu-id="29d58-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29d58-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d58-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d58-123">-WhatIf</span></span>
<span data-ttu-id="29d58-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29d58-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29d58-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29d58-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d58-126">CommonParameters</span></span>
<span data-ttu-id="29d58-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d58-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d58-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d58-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29d58-129">INPUTS</span></span>

### <span data-ttu-id="29d58-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29d58-130">System.String</span></span>

## <span data-ttu-id="29d58-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29d58-131">OUTPUTS</span></span>

### <span data-ttu-id="29d58-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29d58-132">System.Boolean</span></span>

## <span data-ttu-id="29d58-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="29d58-133">NOTES</span></span>

## <span data-ttu-id="29d58-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29d58-134">RELATED LINKS</span></span>

[<span data-ttu-id="29d58-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="29d58-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="29d58-136">Neu – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="29d58-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="29d58-137">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="29d58-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="29d58-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29d58-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="29d58-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29d58-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="29d58-140">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29d58-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="29d58-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29d58-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="29d58-142">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29d58-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
