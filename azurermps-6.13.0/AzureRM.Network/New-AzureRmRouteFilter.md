---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: a28fe30424b5b1d29c3b671e5cec266fc75d9dbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502009"
---
# <span data-ttu-id="1388c-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1388c-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="1388c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1388c-102">SYNOPSIS</span></span>
<span data-ttu-id="1388c-103">Erstellt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="1388c-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1388c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1388c-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1388c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1388c-105">DESCRIPTION</span></span>
<span data-ttu-id="1388c-106">Das New-AzureRmRouteFilter-Cmdlet erstellt einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="1388c-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="1388c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1388c-107">EXAMPLES</span></span>

### <span data-ttu-id="1388c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1388c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="1388c-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="1388c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1388c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1388c-110">PARAMETERS</span></span>

### <span data-ttu-id="1388c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1388c-111">-AsJob</span></span>
<span data-ttu-id="1388c-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1388c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1388c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1388c-113">-DefaultProfile</span></span>
<span data-ttu-id="1388c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1388c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1388c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1388c-115">-Force</span></span>
<span data-ttu-id="1388c-116">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits ein Routenfilter mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1388c-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="1388c-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="1388c-117">-Location</span></span>
<span data-ttu-id="1388c-118">Gibt den Azure-Bereich an, in dem mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1388c-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="1388c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1388c-119">-Name</span></span>
<span data-ttu-id="1388c-120">Gibt einen Namen für den Routenfilter an.</span><span class="sxs-lookup"><span data-stu-id="1388c-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="1388c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1388c-121">-ResourceGroupName</span></span>
<span data-ttu-id="1388c-122">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1388c-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="1388c-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="1388c-123">-Rule</span></span>
<span data-ttu-id="1388c-124">Gibt ein Array von Routenfilter Regel Objekten an, die dem Routenfilter zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1388c-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1388c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1388c-125">-Tag</span></span>
<span data-ttu-id="1388c-126">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="1388c-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1388c-127">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="1388c-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1388c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1388c-128">-Confirm</span></span>
<span data-ttu-id="1388c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1388c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1388c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1388c-130">-WhatIf</span></span>
<span data-ttu-id="1388c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1388c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1388c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1388c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1388c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1388c-133">CommonParameters</span></span>
<span data-ttu-id="1388c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1388c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1388c-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1388c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1388c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1388c-136">INPUTS</span></span>

### <span data-ttu-id="1388c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1388c-137">System.String</span></span>

### <span data-ttu-id="1388c-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1388c-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1388c-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1388c-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1388c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1388c-140">OUTPUTS</span></span>

### <span data-ttu-id="1388c-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1388c-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1388c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="1388c-142">NOTES</span></span>
<span data-ttu-id="1388c-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="1388c-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1388c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1388c-144">RELATED LINKS</span></span>

[<span data-ttu-id="1388c-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1388c-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="1388c-146">Neu – AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1388c-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="1388c-147">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1388c-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="1388c-148">Satz-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1388c-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
