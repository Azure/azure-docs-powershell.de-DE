---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845116"
---
# <span data-ttu-id="b8e2c-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="b8e2c-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="b8e2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e2c-103">Löschen für Ressource für privaten Linkbereich</span><span class="sxs-lookup"><span data-stu-id="b8e2c-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="b8e2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8e2c-104">SYNTAX</span></span>

### <span data-ttu-id="b8e2c-105">ByScopeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8e2c-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e2c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8e2c-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e2c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8e2c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e2c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8e2c-108">DESCRIPTION</span></span>
<span data-ttu-id="b8e2c-109">Löschen für Ressource für privaten Linkbereich</span><span class="sxs-lookup"><span data-stu-id="b8e2c-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="b8e2c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="b8e2c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8e2c-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="b8e2c-112">Ressource für privaten Linkbereich löschen</span><span class="sxs-lookup"><span data-stu-id="b8e2c-112">delete private link scoped resource</span></span>

## <span data-ttu-id="b8e2c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8e2c-113">PARAMETERS</span></span>

### <span data-ttu-id="b8e2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e2c-114">-DefaultProfile</span></span>
<span data-ttu-id="b8e2c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b8e2c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8e2c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b8e2c-116">-InputObject</span></span>
<span data-ttu-id="b8e2c-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b8e2c-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="b8e2c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b8e2c-118">-Name</span></span>
<span data-ttu-id="b8e2c-119">Name der Bereichs Ressource</span><span class="sxs-lookup"><span data-stu-id="b8e2c-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e2c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e2c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b8e2c-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b8e2c-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e2c-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b8e2c-122">-ResourceId</span></span>
<span data-ttu-id="b8e2c-123">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b8e2c-123">Resource Id</span></span>

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

### <span data-ttu-id="b8e2c-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="b8e2c-124">-ScopeName</span></span>
<span data-ttu-id="b8e2c-125">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="b8e2c-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e2c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8e2c-126">-Confirm</span></span>
<span data-ttu-id="b8e2c-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8e2c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e2c-128">-WhatIf</span></span>
<span data-ttu-id="b8e2c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e2c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e2c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8e2c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e2c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e2c-131">CommonParameters</span></span>
<span data-ttu-id="b8e2c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e2c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e2c-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8e2c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e2c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8e2c-134">INPUTS</span></span>

### <span data-ttu-id="b8e2c-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b8e2c-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="b8e2c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b8e2c-136">System.String</span></span>

## <span data-ttu-id="b8e2c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8e2c-137">OUTPUTS</span></span>

### <span data-ttu-id="b8e2c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8e2c-138">System.Boolean</span></span>

## <span data-ttu-id="b8e2c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8e2c-139">NOTES</span></span>

## <span data-ttu-id="b8e2c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8e2c-140">RELATED LINKS</span></span>
