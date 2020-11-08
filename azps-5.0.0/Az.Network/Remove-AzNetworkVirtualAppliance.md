---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177090"
---
# <span data-ttu-id="5769f-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5769f-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="5769f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5769f-102">SYNOPSIS</span></span>
<span data-ttu-id="5769f-103">Entfernen Sie eine virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="5769f-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5769f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5769f-104">SYNTAX</span></span>

### <span data-ttu-id="5769f-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5769f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5769f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5769f-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5769f-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5769f-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5769f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5769f-108">DESCRIPTION</span></span>
<span data-ttu-id="5769f-109">Der Befehl Remove-AzNetworkVirtualAppliance entfernt eine virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="5769f-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5769f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5769f-110">EXAMPLES</span></span>

### <span data-ttu-id="5769f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5769f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="5769f-112">Löschen Sie eine virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="5769f-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5769f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5769f-113">PARAMETERS</span></span>

### <span data-ttu-id="5769f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5769f-114">-AsJob</span></span>
<span data-ttu-id="5769f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5769f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5769f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5769f-116">-DefaultProfile</span></span>
<span data-ttu-id="5769f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5769f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5769f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5769f-118">-Force</span></span>
<span data-ttu-id="5769f-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5769f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5769f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5769f-120">-Name</span></span>
<span data-ttu-id="5769f-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5769f-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5769f-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5769f-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="5769f-123">Das Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="5769f-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5769f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5769f-124">-PassThru</span></span>
<span data-ttu-id="5769f-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5769f-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="5769f-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5769f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5769f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5769f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5769f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5769f-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5769f-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5769f-129">-ResourceId</span></span>
<span data-ttu-id="5769f-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5769f-130">The Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5769f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5769f-131">-Confirm</span></span>
<span data-ttu-id="5769f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5769f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5769f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5769f-133">-WhatIf</span></span>
<span data-ttu-id="5769f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5769f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5769f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5769f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5769f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5769f-136">CommonParameters</span></span>
<span data-ttu-id="5769f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5769f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5769f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5769f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5769f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5769f-139">INPUTS</span></span>

### <span data-ttu-id="5769f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5769f-140">System.String</span></span>

### <span data-ttu-id="5769f-141">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5769f-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="5769f-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5769f-142">OUTPUTS</span></span>

### <span data-ttu-id="5769f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5769f-143">System.Boolean</span></span>

## <span data-ttu-id="5769f-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5769f-144">NOTES</span></span>

## <span data-ttu-id="5769f-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5769f-145">RELATED LINKS</span></span>
