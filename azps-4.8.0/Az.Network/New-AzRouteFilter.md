---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174323"
---
# <span data-ttu-id="33edb-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33edb-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="33edb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33edb-102">SYNOPSIS</span></span>
<span data-ttu-id="33edb-103">Erstellt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="33edb-103">Creates a route filter.</span></span>

## <span data-ttu-id="33edb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33edb-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33edb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33edb-105">DESCRIPTION</span></span>
<span data-ttu-id="33edb-106">Das New-AzRouteFilter-Cmdlet erstellt einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="33edb-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="33edb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33edb-107">EXAMPLES</span></span>

### <span data-ttu-id="33edb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33edb-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="33edb-109">Der Befehl erstellt einen neuen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="33edb-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="33edb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="33edb-110">PARAMETERS</span></span>

### <span data-ttu-id="33edb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33edb-111">-AsJob</span></span>
<span data-ttu-id="33edb-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="33edb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33edb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33edb-113">-DefaultProfile</span></span>
<span data-ttu-id="33edb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33edb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33edb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="33edb-115">-Force</span></span>
<span data-ttu-id="33edb-116">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits ein Routenfilter mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="33edb-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="33edb-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="33edb-117">-Location</span></span>
<span data-ttu-id="33edb-118">Gibt den Azure-Bereich an, in dem mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="33edb-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="33edb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="33edb-119">-Name</span></span>
<span data-ttu-id="33edb-120">Gibt einen Namen für den Routenfilter an.</span><span class="sxs-lookup"><span data-stu-id="33edb-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="33edb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33edb-121">-ResourceGroupName</span></span>
<span data-ttu-id="33edb-122">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="33edb-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="33edb-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="33edb-123">-Rule</span></span>
<span data-ttu-id="33edb-124">Gibt ein Array von Routenfilter Regel Objekten an, die dem Routenfilter zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="33edb-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33edb-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="33edb-125">-Tag</span></span>
<span data-ttu-id="33edb-126">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="33edb-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="33edb-127">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="33edb-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33edb-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="33edb-128">-Confirm</span></span>
<span data-ttu-id="33edb-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="33edb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33edb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33edb-130">-WhatIf</span></span>
<span data-ttu-id="33edb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33edb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33edb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33edb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33edb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33edb-133">CommonParameters</span></span>
<span data-ttu-id="33edb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33edb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33edb-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33edb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33edb-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33edb-136">INPUTS</span></span>

### <span data-ttu-id="33edb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="33edb-137">System.String</span></span>

### <span data-ttu-id="33edb-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="33edb-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="33edb-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="33edb-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="33edb-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33edb-140">OUTPUTS</span></span>

### <span data-ttu-id="33edb-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33edb-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="33edb-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="33edb-142">NOTES</span></span>
<span data-ttu-id="33edb-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="33edb-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="33edb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33edb-144">RELATED LINKS</span></span>

[<span data-ttu-id="33edb-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33edb-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="33edb-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33edb-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="33edb-147">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33edb-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="33edb-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33edb-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33edb-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33edb-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33edb-150">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33edb-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33edb-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33edb-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33edb-152">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33edb-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
