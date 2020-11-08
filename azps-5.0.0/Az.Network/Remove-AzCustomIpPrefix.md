---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178450"
---
# <span data-ttu-id="9f85a-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9f85a-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="9f85a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f85a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f85a-103">Entfernt eine CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9f85a-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="9f85a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f85a-104">SYNTAX</span></span>

### <span data-ttu-id="9f85a-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f85a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f85a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f85a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f85a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f85a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f85a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f85a-108">DESCRIPTION</span></span>
<span data-ttu-id="9f85a-109">Das Cmdlet **Remove-AzCustomIpPrefix** entfernt eine CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="9f85a-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="9f85a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f85a-110">EXAMPLES</span></span>

### <span data-ttu-id="9f85a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f85a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="9f85a-112">Entfernt die CustomIpPrefix mit dem Namen $prefixName aus der Ressourcengruppe $rgName</span><span class="sxs-lookup"><span data-stu-id="9f85a-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="9f85a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f85a-113">PARAMETERS</span></span>

### <span data-ttu-id="9f85a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f85a-114">-AsJob</span></span>
<span data-ttu-id="9f85a-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9f85a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f85a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f85a-116">-DefaultProfile</span></span>
<span data-ttu-id="9f85a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f85a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f85a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9f85a-118">-Force</span></span>
<span data-ttu-id="9f85a-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9f85a-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9f85a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f85a-120">-InputObject</span></span>
<span data-ttu-id="9f85a-121">Ein customIpPrefix-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9f85a-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f85a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9f85a-122">-Name</span></span>
<span data-ttu-id="9f85a-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9f85a-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f85a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f85a-124">-PassThru</span></span>
<span data-ttu-id="9f85a-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9f85a-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f85a-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9f85a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f85a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f85a-127">-ResourceGroupName</span></span>
<span data-ttu-id="9f85a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f85a-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f85a-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9f85a-129">-ResourceId</span></span>
<span data-ttu-id="9f85a-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9f85a-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f85a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f85a-131">-Confirm</span></span>
<span data-ttu-id="9f85a-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f85a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f85a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f85a-133">-WhatIf</span></span>
<span data-ttu-id="9f85a-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f85a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f85a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f85a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f85a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f85a-136">CommonParameters</span></span>
<span data-ttu-id="9f85a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f85a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f85a-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f85a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f85a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f85a-139">INPUTS</span></span>

### <span data-ttu-id="9f85a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9f85a-140">System.String</span></span>

### <span data-ttu-id="9f85a-141">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9f85a-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="9f85a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f85a-142">OUTPUTS</span></span>

### <span data-ttu-id="9f85a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f85a-143">System.Boolean</span></span>

## <span data-ttu-id="9f85a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f85a-144">NOTES</span></span>

## <span data-ttu-id="9f85a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f85a-145">RELATED LINKS</span></span>

[<span data-ttu-id="9f85a-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9f85a-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="9f85a-147">Neu – AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9f85a-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="9f85a-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9f85a-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)