---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004209"
---
# <span data-ttu-id="b1410-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1410-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="b1410-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1410-102">SYNOPSIS</span></span>
<span data-ttu-id="b1410-103">Entfernt ein öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="b1410-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="b1410-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1410-104">SYNTAX</span></span>

### <span data-ttu-id="b1410-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1410-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1410-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1410-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1410-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1410-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1410-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1410-108">DESCRIPTION</span></span>
<span data-ttu-id="b1410-109">Das Cmdlet **Remove-AzPublicIpPrefix** entfernt ein Azure Public IP-Präfix, solange keine öffentlichen IP-Adressen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b1410-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="b1410-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1410-110">EXAMPLES</span></span>

### <span data-ttu-id="b1410-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1410-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="b1410-112">Entfernt das öffentliche IP-Präfix mit dem Namen $prefixName aus der Ressourcengruppe $rgName</span><span class="sxs-lookup"><span data-stu-id="b1410-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="b1410-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1410-113">PARAMETERS</span></span>

### <span data-ttu-id="b1410-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1410-114">-AsJob</span></span>
<span data-ttu-id="b1410-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1410-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1410-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1410-116">-DefaultProfile</span></span>
<span data-ttu-id="b1410-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1410-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1410-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b1410-118">-Force</span></span>
<span data-ttu-id="b1410-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b1410-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b1410-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1410-120">-InputObject</span></span>
<span data-ttu-id="b1410-121">Ein PublicIpPrefix-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1410-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1410-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b1410-122">-Name</span></span>
<span data-ttu-id="b1410-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b1410-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1410-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1410-124">-PassThru</span></span>
<span data-ttu-id="b1410-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b1410-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1410-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b1410-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1410-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1410-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1410-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b1410-128">The resource group name.</span></span>

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

### <span data-ttu-id="b1410-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b1410-129">-ResourceId</span></span>
<span data-ttu-id="b1410-130">Die Ressourcenquelle für die zu entfernende Ressource</span><span class="sxs-lookup"><span data-stu-id="b1410-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="b1410-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1410-131">-Confirm</span></span>
<span data-ttu-id="b1410-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1410-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1410-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1410-133">-WhatIf</span></span>
<span data-ttu-id="b1410-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1410-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1410-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1410-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1410-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1410-136">CommonParameters</span></span>
<span data-ttu-id="b1410-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1410-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1410-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1410-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1410-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1410-139">INPUTS</span></span>

### <span data-ttu-id="b1410-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b1410-140">System.String</span></span>

### <span data-ttu-id="b1410-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1410-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="b1410-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1410-142">OUTPUTS</span></span>

### <span data-ttu-id="b1410-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1410-143">System.Boolean</span></span>

## <span data-ttu-id="b1410-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1410-144">NOTES</span></span>

## <span data-ttu-id="b1410-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1410-145">RELATED LINKS</span></span>

[<span data-ttu-id="b1410-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1410-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="b1410-147">Neu – AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1410-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="b1410-148">Satz-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1410-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
