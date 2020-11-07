---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841280"
---
# <span data-ttu-id="06e1d-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06e1d-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="06e1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="06e1d-103">Erstellt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="06e1d-103">Creates a route filter.</span></span>

## <span data-ttu-id="06e1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e1d-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06e1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06e1d-105">DESCRIPTION</span></span>
<span data-ttu-id="06e1d-106">Das New-AzRouteFilter-Cmdlet erstellt einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="06e1d-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="06e1d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06e1d-107">EXAMPLES</span></span>

### <span data-ttu-id="06e1d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06e1d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="06e1d-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="06e1d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="06e1d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="06e1d-110">PARAMETERS</span></span>

### <span data-ttu-id="06e1d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06e1d-111">-AsJob</span></span>
<span data-ttu-id="06e1d-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="06e1d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06e1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e1d-113">-DefaultProfile</span></span>
<span data-ttu-id="06e1d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06e1d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06e1d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06e1d-115">-Force</span></span>
<span data-ttu-id="06e1d-116">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits ein Routenfilter mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="06e1d-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="06e1d-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="06e1d-117">-Location</span></span>
<span data-ttu-id="06e1d-118">Gibt den Azure-Bereich an, in dem mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="06e1d-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="06e1d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="06e1d-119">-Name</span></span>
<span data-ttu-id="06e1d-120">Gibt einen Namen für den Routenfilter an.</span><span class="sxs-lookup"><span data-stu-id="06e1d-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="06e1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="06e1d-122">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="06e1d-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="06e1d-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="06e1d-123">-Rule</span></span>
<span data-ttu-id="06e1d-124">Gibt ein Array von Routenfilter Regel Objekten an, die dem Routenfilter zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06e1d-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="06e1d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="06e1d-125">-Tag</span></span>
<span data-ttu-id="06e1d-126">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="06e1d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="06e1d-127">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="06e1d-127">For example:</span></span>

<span data-ttu-id="06e1d-128">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="06e1d-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="06e1d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06e1d-129">-Confirm</span></span>
<span data-ttu-id="06e1d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06e1d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e1d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e1d-131">-WhatIf</span></span>
<span data-ttu-id="06e1d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06e1d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06e1d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06e1d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e1d-134">CommonParameters</span></span>
<span data-ttu-id="06e1d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e1d-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e1d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e1d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06e1d-137">INPUTS</span></span>

## <span data-ttu-id="06e1d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06e1d-138">OUTPUTS</span></span>

### <span data-ttu-id="06e1d-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06e1d-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="06e1d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="06e1d-140">NOTES</span></span>
<span data-ttu-id="06e1d-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="06e1d-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="06e1d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06e1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="06e1d-143">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06e1d-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="06e1d-144">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="06e1d-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="06e1d-145">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06e1d-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="06e1d-146">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06e1d-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
