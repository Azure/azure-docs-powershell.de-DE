---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179836"
---
# <span data-ttu-id="e9a13-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e9a13-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="e9a13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9a13-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a13-103">Entfernen einer virtuellen Appliance-Website aus einer virtuellen Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e9a13-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="e9a13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a13-104">SYNTAX</span></span>

### <span data-ttu-id="e9a13-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9a13-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9a13-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9a13-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a13-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9a13-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9a13-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9a13-108">DESCRIPTION</span></span>
<span data-ttu-id="e9a13-109">Der Befehl Remove-AzVirtualApplianceSite entfernt eine Virtual Appliance-Website aus einer virtuellen Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e9a13-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="e9a13-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9a13-110">EXAMPLES</span></span>

### <span data-ttu-id="e9a13-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9a13-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="e9a13-112">Löschen einer Website Ressource einer virtuellen Appliance</span><span class="sxs-lookup"><span data-stu-id="e9a13-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="e9a13-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9a13-113">PARAMETERS</span></span>

### <span data-ttu-id="e9a13-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9a13-114">-AsJob</span></span>
<span data-ttu-id="e9a13-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e9a13-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9a13-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a13-116">-DefaultProfile</span></span>
<span data-ttu-id="e9a13-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9a13-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9a13-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e9a13-118">-Force</span></span>
<span data-ttu-id="e9a13-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e9a13-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e9a13-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e9a13-120">-Name</span></span>
<span data-ttu-id="e9a13-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e9a13-121">The resource name.</span></span>

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

### <span data-ttu-id="e9a13-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="e9a13-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="e9a13-123">Die Ressourcen-ID der virtuellen Netzwerk-Appliance, die dieser Website zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9a13-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="e9a13-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9a13-124">-PassThru</span></span>
<span data-ttu-id="e9a13-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e9a13-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e9a13-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e9a13-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9a13-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a13-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9a13-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e9a13-128">The resource group name.</span></span>

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

### <span data-ttu-id="e9a13-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e9a13-129">-ResourceId</span></span>
<span data-ttu-id="e9a13-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e9a13-130">The resource id.</span></span>

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

### <span data-ttu-id="e9a13-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e9a13-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="e9a13-132">Das Websiteobjekt der virtuellen Appliance.</span><span class="sxs-lookup"><span data-stu-id="e9a13-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="e9a13-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9a13-133">-Confirm</span></span>
<span data-ttu-id="e9a13-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9a13-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a13-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a13-135">-WhatIf</span></span>
<span data-ttu-id="e9a13-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a13-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a13-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9a13-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a13-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a13-138">CommonParameters</span></span>
<span data-ttu-id="e9a13-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a13-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a13-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9a13-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a13-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9a13-141">INPUTS</span></span>

### <span data-ttu-id="e9a13-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e9a13-142">System.String</span></span>

### <span data-ttu-id="e9a13-143">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e9a13-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="e9a13-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9a13-144">OUTPUTS</span></span>

### <span data-ttu-id="e9a13-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9a13-145">System.Boolean</span></span>

## <span data-ttu-id="e9a13-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9a13-146">NOTES</span></span>

## <span data-ttu-id="e9a13-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9a13-147">RELATED LINKS</span></span>
