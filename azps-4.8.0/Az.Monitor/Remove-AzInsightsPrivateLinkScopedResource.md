---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166319"
---
# <span data-ttu-id="70493-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="70493-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="70493-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70493-102">SYNOPSIS</span></span>
<span data-ttu-id="70493-103">Löschen für Ressource für privaten Linkbereich</span><span class="sxs-lookup"><span data-stu-id="70493-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="70493-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70493-104">SYNTAX</span></span>

### <span data-ttu-id="70493-105">ByScopeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="70493-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70493-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70493-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70493-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70493-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70493-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70493-108">DESCRIPTION</span></span>
<span data-ttu-id="70493-109">Löschen für Ressource für privaten Linkbereich</span><span class="sxs-lookup"><span data-stu-id="70493-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="70493-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70493-110">EXAMPLES</span></span>

### <span data-ttu-id="70493-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70493-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="70493-112">Ressource für privaten Linkbereich löschen</span><span class="sxs-lookup"><span data-stu-id="70493-112">delete private link scoped resource</span></span>

## <span data-ttu-id="70493-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="70493-113">PARAMETERS</span></span>

### <span data-ttu-id="70493-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70493-114">-DefaultProfile</span></span>
<span data-ttu-id="70493-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70493-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70493-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70493-116">-InputObject</span></span>
<span data-ttu-id="70493-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="70493-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="70493-118">-Name</span><span class="sxs-lookup"><span data-stu-id="70493-118">-Name</span></span>
<span data-ttu-id="70493-119">Name der Bereichs Ressource</span><span class="sxs-lookup"><span data-stu-id="70493-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="70493-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70493-120">-ResourceGroupName</span></span>
<span data-ttu-id="70493-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="70493-121">Resource Group Name</span></span>

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

### <span data-ttu-id="70493-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="70493-122">-ResourceId</span></span>
<span data-ttu-id="70493-123">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="70493-123">Resource Id</span></span>

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

### <span data-ttu-id="70493-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="70493-124">-ScopeName</span></span>
<span data-ttu-id="70493-125">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="70493-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="70493-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70493-126">-Confirm</span></span>
<span data-ttu-id="70493-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70493-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70493-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70493-128">-WhatIf</span></span>
<span data-ttu-id="70493-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70493-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70493-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70493-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70493-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70493-131">CommonParameters</span></span>
<span data-ttu-id="70493-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70493-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70493-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70493-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70493-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70493-134">INPUTS</span></span>

### <span data-ttu-id="70493-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="70493-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="70493-136">System. String</span><span class="sxs-lookup"><span data-stu-id="70493-136">System.String</span></span>

## <span data-ttu-id="70493-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70493-137">OUTPUTS</span></span>

### <span data-ttu-id="70493-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70493-138">System.Boolean</span></span>

## <span data-ttu-id="70493-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="70493-139">NOTES</span></span>

## <span data-ttu-id="70493-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70493-140">RELATED LINKS</span></span>
