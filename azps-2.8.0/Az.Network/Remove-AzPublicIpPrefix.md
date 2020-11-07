---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821339"
---
# <span data-ttu-id="9cee0-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cee0-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="9cee0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cee0-102">SYNOPSIS</span></span>
<span data-ttu-id="9cee0-103">Entfernt ein öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="9cee0-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="9cee0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cee0-104">SYNTAX</span></span>

### <span data-ttu-id="9cee0-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9cee0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cee0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cee0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cee0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cee0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cee0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cee0-108">DESCRIPTION</span></span>
<span data-ttu-id="9cee0-109">Das Cmdlet **Remove-AzPublicIpPrefix** entfernt ein Azure Public IP-Präfix, solange keine öffentlichen IP-Adressen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="9cee0-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="9cee0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cee0-110">EXAMPLES</span></span>

### <span data-ttu-id="9cee0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9cee0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="9cee0-112">Entfernt das öffentliche IP-Präfix mit dem Namen $prefixName aus der Ressourcengruppe $rgName</span><span class="sxs-lookup"><span data-stu-id="9cee0-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="9cee0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cee0-113">PARAMETERS</span></span>

### <span data-ttu-id="9cee0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cee0-114">-AsJob</span></span>
<span data-ttu-id="9cee0-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9cee0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cee0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cee0-116">-DefaultProfile</span></span>
<span data-ttu-id="9cee0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cee0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cee0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9cee0-118">-Force</span></span>
<span data-ttu-id="9cee0-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9cee0-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9cee0-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9cee0-120">-InputObject</span></span>
<span data-ttu-id="9cee0-121">Ein PublicIpPrefix-Objekt</span><span class="sxs-lookup"><span data-stu-id="9cee0-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="9cee0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9cee0-122">-Name</span></span>
<span data-ttu-id="9cee0-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9cee0-123">The resource name.</span></span>

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

### <span data-ttu-id="9cee0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cee0-124">-PassThru</span></span>
<span data-ttu-id="9cee0-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9cee0-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cee0-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9cee0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9cee0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cee0-127">-ResourceGroupName</span></span>
<span data-ttu-id="9cee0-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cee0-128">The resource group name.</span></span>

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

### <span data-ttu-id="9cee0-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9cee0-129">-ResourceId</span></span>
<span data-ttu-id="9cee0-130">Die Ressourcenquelle für die zu entfernende Ressource</span><span class="sxs-lookup"><span data-stu-id="9cee0-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="9cee0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cee0-131">-Confirm</span></span>
<span data-ttu-id="9cee0-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cee0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cee0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cee0-133">-WhatIf</span></span>
<span data-ttu-id="9cee0-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cee0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cee0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cee0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cee0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cee0-136">CommonParameters</span></span>
<span data-ttu-id="9cee0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cee0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cee0-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cee0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cee0-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cee0-139">INPUTS</span></span>

### <span data-ttu-id="9cee0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9cee0-140">System.String</span></span>

### <span data-ttu-id="9cee0-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cee0-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="9cee0-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cee0-142">OUTPUTS</span></span>

### <span data-ttu-id="9cee0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cee0-143">System.Boolean</span></span>

## <span data-ttu-id="9cee0-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cee0-144">NOTES</span></span>

## <span data-ttu-id="9cee0-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cee0-145">RELATED LINKS</span></span>

[<span data-ttu-id="9cee0-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cee0-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="9cee0-147">Neu – AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cee0-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="9cee0-148">Satz-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cee0-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
