---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165159"
---
# <span data-ttu-id="b0d1e-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b0d1e-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="b0d1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d1e-103">Entfernen Sie eine virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b0d1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0d1e-104">SYNTAX</span></span>

### <span data-ttu-id="b0d1e-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0d1e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d1e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0d1e-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d1e-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0d1e-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0d1e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0d1e-108">DESCRIPTION</span></span>
<span data-ttu-id="b0d1e-109">Der Befehl Remove-AzNetworkVirtualAppliance entfernt eine virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b0d1e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0d1e-110">EXAMPLES</span></span>

### <span data-ttu-id="b0d1e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0d1e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="b0d1e-112">Löschen Sie eine virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b0d1e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0d1e-113">PARAMETERS</span></span>

### <span data-ttu-id="b0d1e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0d1e-114">-AsJob</span></span>
<span data-ttu-id="b0d1e-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b0d1e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0d1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d1e-116">-DefaultProfile</span></span>
<span data-ttu-id="b0d1e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d1e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b0d1e-118">-Force</span></span>
<span data-ttu-id="b0d1e-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b0d1e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b0d1e-120">-Name</span></span>
<span data-ttu-id="b0d1e-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-121">The resource name.</span></span>

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

### <span data-ttu-id="b0d1e-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b0d1e-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="b0d1e-123">Das Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-123">The resource object.</span></span>

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

### <span data-ttu-id="b0d1e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0d1e-124">-PassThru</span></span>
<span data-ttu-id="b0d1e-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b0d1e-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b0d1e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d1e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0d1e-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-128">The resource group name.</span></span>

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

### <span data-ttu-id="b0d1e-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b0d1e-129">-ResourceId</span></span>
<span data-ttu-id="b0d1e-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-130">The Resource Id.</span></span>

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

### <span data-ttu-id="b0d1e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b0d1e-131">-Confirm</span></span>
<span data-ttu-id="b0d1e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0d1e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0d1e-133">-WhatIf</span></span>
<span data-ttu-id="b0d1e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0d1e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0d1e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d1e-136">CommonParameters</span></span>
<span data-ttu-id="b0d1e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d1e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d1e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0d1e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d1e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0d1e-139">INPUTS</span></span>

### <span data-ttu-id="b0d1e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b0d1e-140">System.String</span></span>

### <span data-ttu-id="b0d1e-141">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b0d1e-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="b0d1e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0d1e-142">OUTPUTS</span></span>

### <span data-ttu-id="b0d1e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0d1e-143">System.Boolean</span></span>

## <span data-ttu-id="b0d1e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0d1e-144">NOTES</span></span>

## <span data-ttu-id="b0d1e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0d1e-145">RELATED LINKS</span></span>
