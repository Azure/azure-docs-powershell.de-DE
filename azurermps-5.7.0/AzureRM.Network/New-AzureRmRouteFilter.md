---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 9ba5f47427dc8f542e1475a8431f5d82c63c5974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664635"
---
# <span data-ttu-id="07fca-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="07fca-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="07fca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07fca-102">SYNOPSIS</span></span>
<span data-ttu-id="07fca-103">Erstellt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="07fca-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07fca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07fca-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07fca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07fca-105">DESCRIPTION</span></span>
<span data-ttu-id="07fca-106">Das New-AzureRmRouteFilter-Cmdlet erstellt einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="07fca-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="07fca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07fca-107">EXAMPLES</span></span>

### <span data-ttu-id="07fca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07fca-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="07fca-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="07fca-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="07fca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07fca-110">PARAMETERS</span></span>

### <span data-ttu-id="07fca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07fca-111">-AsJob</span></span>
<span data-ttu-id="07fca-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="07fca-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07fca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07fca-113">-DefaultProfile</span></span>
<span data-ttu-id="07fca-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07fca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07fca-115">-Force</span><span class="sxs-lookup"><span data-stu-id="07fca-115">-Force</span></span>
<span data-ttu-id="07fca-116">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits ein Routenfilter mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="07fca-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="07fca-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="07fca-117">-Location</span></span>
<span data-ttu-id="07fca-118">Gibt den Azure-Bereich an, in dem mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="07fca-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="07fca-119">-Name</span><span class="sxs-lookup"><span data-stu-id="07fca-119">-Name</span></span>
<span data-ttu-id="07fca-120">Gibt einen Namen für den Routenfilter an.</span><span class="sxs-lookup"><span data-stu-id="07fca-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="07fca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07fca-121">-ResourceGroupName</span></span>
<span data-ttu-id="07fca-122">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="07fca-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="07fca-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="07fca-123">-Rule</span></span>
<span data-ttu-id="07fca-124">Gibt ein Array von Routenfilter Regel Objekten an, die dem Routenfilter zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07fca-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="07fca-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="07fca-125">-Tag</span></span>
<span data-ttu-id="07fca-126">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="07fca-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07fca-127">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="07fca-127">For example:</span></span>

<span data-ttu-id="07fca-128">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="07fca-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fca-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07fca-129">-Confirm</span></span>
<span data-ttu-id="07fca-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07fca-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07fca-131">-WhatIf</span></span>
<span data-ttu-id="07fca-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07fca-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07fca-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07fca-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fca-134">CommonParameters</span></span>
<span data-ttu-id="07fca-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07fca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fca-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07fca-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fca-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07fca-137">INPUTS</span></span>

### <span data-ttu-id="07fca-138">Keine</span><span class="sxs-lookup"><span data-stu-id="07fca-138">None</span></span>
<span data-ttu-id="07fca-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="07fca-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07fca-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07fca-140">OUTPUTS</span></span>

### <span data-ttu-id="07fca-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="07fca-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="07fca-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="07fca-142">NOTES</span></span>
<span data-ttu-id="07fca-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="07fca-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="07fca-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07fca-144">RELATED LINKS</span></span>

[<span data-ttu-id="07fca-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="07fca-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="07fca-146">Neu – AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07fca-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="07fca-147">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="07fca-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="07fca-148">Satz-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="07fca-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
