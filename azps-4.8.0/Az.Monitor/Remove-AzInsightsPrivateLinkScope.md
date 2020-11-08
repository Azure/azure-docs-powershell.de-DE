---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166496"
---
# <span data-ttu-id="6c21f-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="6c21f-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="6c21f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c21f-102">SYNOPSIS</span></span>
<span data-ttu-id="6c21f-103">Löschen eines privaten Verknüpfungsbereichs</span><span class="sxs-lookup"><span data-stu-id="6c21f-103">delete private link scope</span></span>

## <span data-ttu-id="6c21f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c21f-104">SYNTAX</span></span>

### <span data-ttu-id="6c21f-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c21f-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c21f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c21f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c21f-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c21f-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c21f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c21f-108">DESCRIPTION</span></span>
<span data-ttu-id="6c21f-109">Löschen eines privaten Verknüpfungsbereichs</span><span class="sxs-lookup"><span data-stu-id="6c21f-109">delete private link scope</span></span>

## <span data-ttu-id="6c21f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c21f-110">EXAMPLES</span></span>

### <span data-ttu-id="6c21f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c21f-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="6c21f-112">Löschen eines privaten Verknüpfungsbereichs mit dem Namen "scope_name" unter Ressourcengruppe "rg_name"</span><span class="sxs-lookup"><span data-stu-id="6c21f-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="6c21f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6c21f-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="6c21f-114">Löschen eines privaten Verknüpfungsbereichs mit Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6c21f-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="6c21f-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6c21f-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="6c21f-116">Löschen eines privaten Verknüpfungsbereichs mit einem privaten Link-Bereichsobjekt</span><span class="sxs-lookup"><span data-stu-id="6c21f-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="6c21f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c21f-117">PARAMETERS</span></span>

### <span data-ttu-id="6c21f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c21f-118">-DefaultProfile</span></span>
<span data-ttu-id="6c21f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c21f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c21f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c21f-120">-InputObject</span></span>
<span data-ttu-id="6c21f-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="6c21f-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c21f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6c21f-122">-Name</span></span>
<span data-ttu-id="6c21f-123">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="6c21f-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c21f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c21f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c21f-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6c21f-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c21f-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6c21f-126">-ResourceId</span></span>
<span data-ttu-id="6c21f-127">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6c21f-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c21f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c21f-128">-Confirm</span></span>
<span data-ttu-id="6c21f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c21f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c21f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c21f-130">-WhatIf</span></span>
<span data-ttu-id="6c21f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c21f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c21f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c21f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c21f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c21f-133">CommonParameters</span></span>
<span data-ttu-id="6c21f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c21f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c21f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c21f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c21f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c21f-136">INPUTS</span></span>

### <span data-ttu-id="6c21f-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="6c21f-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="6c21f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6c21f-138">System.String</span></span>

## <span data-ttu-id="6c21f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c21f-139">OUTPUTS</span></span>

### <span data-ttu-id="6c21f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c21f-140">System.Boolean</span></span>

## <span data-ttu-id="6c21f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c21f-141">NOTES</span></span>

## <span data-ttu-id="6c21f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c21f-142">RELATED LINKS</span></span>
