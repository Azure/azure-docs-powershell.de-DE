---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009645"
---
# <span data-ttu-id="cc360-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="cc360-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="cc360-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc360-102">SYNOPSIS</span></span>
<span data-ttu-id="cc360-103">Löscht eine Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="cc360-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="cc360-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc360-104">SYNTAX</span></span>

### <span data-ttu-id="cc360-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc360-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc360-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc360-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc360-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc360-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc360-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc360-108">DESCRIPTION</span></span>
<span data-ttu-id="cc360-109">Das Cmdlet **Remove-AzIpAllocation** löscht eine Azure-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="cc360-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="cc360-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc360-110">EXAMPLES</span></span>

### <span data-ttu-id="cc360-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc360-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="cc360-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc360-112">PARAMETERS</span></span>

### <span data-ttu-id="cc360-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc360-113">-AsJob</span></span>
<span data-ttu-id="cc360-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cc360-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc360-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc360-115">-DefaultProfile</span></span>
<span data-ttu-id="cc360-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc360-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc360-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cc360-117">-Force</span></span>
<span data-ttu-id="cc360-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="cc360-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc360-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc360-119">-InputObject</span></span>
<span data-ttu-id="cc360-120">{{Fill Inputobject Description}}</span><span class="sxs-lookup"><span data-stu-id="cc360-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc360-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cc360-121">-Name</span></span>
<span data-ttu-id="cc360-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="cc360-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc360-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc360-123">-PassThru</span></span>
<span data-ttu-id="cc360-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc360-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc360-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="cc360-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc360-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc360-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc360-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc360-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc360-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc360-128">-ResourceId</span></span>
<span data-ttu-id="cc360-129">IpAllocation-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cc360-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="cc360-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc360-130">-Confirm</span></span>
<span data-ttu-id="cc360-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc360-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc360-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc360-132">-WhatIf</span></span>
<span data-ttu-id="cc360-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc360-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc360-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc360-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc360-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc360-135">CommonParameters</span></span>
<span data-ttu-id="cc360-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc360-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc360-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc360-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc360-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc360-138">INPUTS</span></span>

### <span data-ttu-id="cc360-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cc360-139">System.String</span></span>

## <span data-ttu-id="cc360-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc360-140">OUTPUTS</span></span>

### <span data-ttu-id="cc360-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc360-141">System.Boolean</span></span>

## <span data-ttu-id="cc360-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc360-142">NOTES</span></span>

## <span data-ttu-id="cc360-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc360-143">RELATED LINKS</span></span>
