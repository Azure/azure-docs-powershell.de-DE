---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174548"
---
# <span data-ttu-id="d4087-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d4087-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="d4087-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4087-102">SYNOPSIS</span></span>
<span data-ttu-id="d4087-103">Entfernt einen virtuellen Netzwerk-Tap.</span><span class="sxs-lookup"><span data-stu-id="d4087-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="d4087-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4087-104">SYNTAX</span></span>

### <span data-ttu-id="d4087-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4087-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4087-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4087-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4087-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4087-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4087-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4087-108">DESCRIPTION</span></span>
<span data-ttu-id="d4087-109">Das Cmdlet " **Remove-AzVirtualNetworkTap** " entfernt einen virtuellen Azure-Netzwerk-Tap.</span><span class="sxs-lookup"><span data-stu-id="d4087-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="d4087-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4087-110">EXAMPLES</span></span>

### <span data-ttu-id="d4087-111">Beispiel 1: Entfernen eines virtuellen Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="d4087-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d4087-112">Dieser Befehl entfernt die VirtualNetworkTap1 in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d4087-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d4087-113">Da der Parameter *Force* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d4087-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="d4087-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4087-114">PARAMETERS</span></span>

### <span data-ttu-id="d4087-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4087-115">-AsJob</span></span>
<span data-ttu-id="d4087-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d4087-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4087-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4087-117">-DefaultProfile</span></span>
<span data-ttu-id="d4087-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4087-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4087-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d4087-119">-Force</span></span>
<span data-ttu-id="d4087-120">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="d4087-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="d4087-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4087-121">-InputObject</span></span>
<span data-ttu-id="d4087-122">Bezug auf die VirtualNetworkTap-Ressource</span><span class="sxs-lookup"><span data-stu-id="d4087-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4087-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d4087-123">-Name</span></span>
<span data-ttu-id="d4087-124">Der Name des Tap.</span><span class="sxs-lookup"><span data-stu-id="d4087-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4087-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4087-125">-PassThru</span></span>
<span data-ttu-id="d4087-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4087-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d4087-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d4087-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d4087-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4087-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4087-129">Der Ressourcengruppenname des virtuellen Netzwerks Tippen Sie auf.</span><span class="sxs-lookup"><span data-stu-id="d4087-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4087-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d4087-130">-ResourceId</span></span>
<span data-ttu-id="d4087-131">VirtualNetworkTap-Quell Code</span><span class="sxs-lookup"><span data-stu-id="d4087-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4087-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4087-132">-Confirm</span></span>
<span data-ttu-id="d4087-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4087-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4087-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4087-134">-WhatIf</span></span>
<span data-ttu-id="d4087-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4087-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4087-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4087-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4087-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4087-137">CommonParameters</span></span>
<span data-ttu-id="d4087-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4087-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4087-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4087-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4087-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4087-140">INPUTS</span></span>

### <span data-ttu-id="d4087-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d4087-141">System.String</span></span>

### <span data-ttu-id="d4087-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d4087-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d4087-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4087-143">OUTPUTS</span></span>

### <span data-ttu-id="d4087-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4087-144">System.Boolean</span></span>

## <span data-ttu-id="d4087-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4087-145">NOTES</span></span>

## <span data-ttu-id="d4087-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4087-146">RELATED LINKS</span></span>

[<span data-ttu-id="d4087-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d4087-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="d4087-148">Neu – AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d4087-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="d4087-149">Satz-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d4087-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
