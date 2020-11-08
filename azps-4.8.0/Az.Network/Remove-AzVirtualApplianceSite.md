---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009083"
---
# <span data-ttu-id="e0b36-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e0b36-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="e0b36-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0b36-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b36-103">Entfernen einer virtuellen Appliance-Website aus einer virtuellen Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e0b36-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="e0b36-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0b36-104">SYNTAX</span></span>

### <span data-ttu-id="e0b36-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0b36-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0b36-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b36-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b36-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b36-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b36-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0b36-108">DESCRIPTION</span></span>
<span data-ttu-id="e0b36-109">Der Befehl Remove-AzVirtualApplianceSite entfernt eine Virtual Appliance-Website aus einer virtuellen Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e0b36-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="e0b36-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0b36-110">EXAMPLES</span></span>

### <span data-ttu-id="e0b36-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0b36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="e0b36-112">Löschen einer Website Ressource einer virtuellen Appliance</span><span class="sxs-lookup"><span data-stu-id="e0b36-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="e0b36-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b36-113">PARAMETERS</span></span>

### <span data-ttu-id="e0b36-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0b36-114">-AsJob</span></span>
<span data-ttu-id="e0b36-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e0b36-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0b36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b36-116">-DefaultProfile</span></span>
<span data-ttu-id="e0b36-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0b36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b36-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e0b36-118">-Force</span></span>
<span data-ttu-id="e0b36-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e0b36-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e0b36-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e0b36-120">-Name</span></span>
<span data-ttu-id="e0b36-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e0b36-121">The resource name.</span></span>

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

### <span data-ttu-id="e0b36-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="e0b36-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="e0b36-123">Die Ressourcen-ID der virtuellen Netzwerk-Appliance, die dieser Website zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0b36-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="e0b36-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0b36-124">-PassThru</span></span>
<span data-ttu-id="e0b36-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e0b36-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e0b36-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e0b36-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0b36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b36-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0b36-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0b36-128">The resource group name.</span></span>

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

### <span data-ttu-id="e0b36-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e0b36-129">-ResourceId</span></span>
<span data-ttu-id="e0b36-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e0b36-130">The resource id.</span></span>

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

### <span data-ttu-id="e0b36-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e0b36-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="e0b36-132">Das Websiteobjekt der virtuellen Appliance.</span><span class="sxs-lookup"><span data-stu-id="e0b36-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b36-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0b36-133">-Confirm</span></span>
<span data-ttu-id="e0b36-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0b36-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b36-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b36-135">-WhatIf</span></span>
<span data-ttu-id="e0b36-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0b36-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b36-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0b36-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b36-138">CommonParameters</span></span>
<span data-ttu-id="e0b36-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b36-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0b36-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b36-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0b36-141">INPUTS</span></span>

### <span data-ttu-id="e0b36-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e0b36-142">System.String</span></span>

### <span data-ttu-id="e0b36-143">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e0b36-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="e0b36-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0b36-144">OUTPUTS</span></span>

### <span data-ttu-id="e0b36-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0b36-145">System.Boolean</span></span>

## <span data-ttu-id="e0b36-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0b36-146">NOTES</span></span>

## <span data-ttu-id="e0b36-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0b36-147">RELATED LINKS</span></span>
