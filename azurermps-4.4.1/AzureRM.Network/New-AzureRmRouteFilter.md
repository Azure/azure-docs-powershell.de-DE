---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481874"
---
# <span data-ttu-id="e88e6-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e88e6-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="e88e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e88e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e88e6-103">Erstellt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="e88e6-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e88e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e88e6-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e88e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e88e6-105">DESCRIPTION</span></span>
<span data-ttu-id="e88e6-106">Das New-AzureRmRouteFilter-Cmdlet erstellt einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="e88e6-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="e88e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e88e6-107">EXAMPLES</span></span>

### <span data-ttu-id="e88e6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e88e6-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="e88e6-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="e88e6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e88e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e88e6-110">PARAMETERS</span></span>

### <span data-ttu-id="e88e6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e88e6-111">-Force</span></span>
<span data-ttu-id="e88e6-112">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits ein Routenfilter mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e88e6-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="e88e6-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="e88e6-113">-Location</span></span>
<span data-ttu-id="e88e6-114">Gibt den Azure-Bereich an, in dem mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e88e6-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="e88e6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e88e6-115">-Name</span></span>
<span data-ttu-id="e88e6-116">Gibt einen Namen für den Routenfilter an.</span><span class="sxs-lookup"><span data-stu-id="e88e6-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="e88e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="e88e6-118">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet ein Routenfilter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e88e6-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="e88e6-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="e88e6-119">-Rule</span></span>
<span data-ttu-id="e88e6-120">Gibt ein Array von Routenfilter Regel Objekten an, die dem Routenfilter zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e88e6-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="e88e6-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="e88e6-121">-Tag</span></span>
<span data-ttu-id="e88e6-122">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="e88e6-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e88e6-123">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e88e6-123">For example:</span></span>

<span data-ttu-id="e88e6-124">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="e88e6-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e88e6-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e88e6-125">-Confirm</span></span>
<span data-ttu-id="e88e6-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e88e6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88e6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88e6-127">-WhatIf</span></span>
<span data-ttu-id="e88e6-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e88e6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e88e6-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e88e6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88e6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88e6-130">-DefaultProfile</span></span>
<span data-ttu-id="e88e6-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e88e6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e88e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88e6-132">CommonParameters</span></span>
<span data-ttu-id="e88e6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88e6-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88e6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88e6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e88e6-135">INPUTS</span></span>

## <span data-ttu-id="e88e6-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e88e6-136">OUTPUTS</span></span>

### <span data-ttu-id="e88e6-137">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e88e6-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e88e6-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e88e6-138">NOTES</span></span>
<span data-ttu-id="e88e6-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e88e6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e88e6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e88e6-140">RELATED LINKS</span></span>

[<span data-ttu-id="e88e6-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e88e6-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="e88e6-142">Neu – AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e88e6-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="e88e6-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e88e6-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="e88e6-144">Satz-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e88e6-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
