---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147361"
---
# <span data-ttu-id="37c9a-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="37c9a-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="37c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="37c9a-103">Erstellen eines privaten Verknüpfungsbereichs</span><span class="sxs-lookup"><span data-stu-id="37c9a-103">create private link scope</span></span>

## <span data-ttu-id="37c9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37c9a-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c9a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37c9a-105">DESCRIPTION</span></span>
<span data-ttu-id="37c9a-106">Erstellen eines privaten Verknüpfungsbereichs</span><span class="sxs-lookup"><span data-stu-id="37c9a-106">create private link scope</span></span>

## <span data-ttu-id="37c9a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37c9a-107">EXAMPLES</span></span>

### <span data-ttu-id="37c9a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37c9a-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="37c9a-109">Erstellen eines privaten Verknüpfungsbereichs mit dem Namen "scope_name" unter der Ressourcengruppe "rg_name" am Standort "eastus"</span><span class="sxs-lookup"><span data-stu-id="37c9a-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="37c9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37c9a-110">PARAMETERS</span></span>

### <span data-ttu-id="37c9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c9a-111">-DefaultProfile</span></span>
<span data-ttu-id="37c9a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37c9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c9a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="37c9a-113">-Location</span></span>
<span data-ttu-id="37c9a-114">Position</span><span class="sxs-lookup"><span data-stu-id="37c9a-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c9a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="37c9a-115">-Name</span></span>
<span data-ttu-id="37c9a-116">Name des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="37c9a-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="37c9a-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="37c9a-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c9a-119">-Tags</span><span class="sxs-lookup"><span data-stu-id="37c9a-119">-Tags</span></span>
<span data-ttu-id="37c9a-120">Kategorien</span><span class="sxs-lookup"><span data-stu-id="37c9a-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c9a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37c9a-121">-Confirm</span></span>
<span data-ttu-id="37c9a-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37c9a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c9a-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="37c9a-123">-WhatIf</span></span>
<span data-ttu-id="37c9a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37c9a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c9a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37c9a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c9a-126">CommonParameters</span></span>
<span data-ttu-id="37c9a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c9a-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37c9a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c9a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37c9a-129">INPUTS</span></span>

### <span data-ttu-id="37c9a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="37c9a-130">System.String</span></span>

## <span data-ttu-id="37c9a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37c9a-131">OUTPUTS</span></span>

### <span data-ttu-id="37c9a-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="37c9a-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="37c9a-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37c9a-133">NOTES</span></span>

## <span data-ttu-id="37c9a-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37c9a-134">RELATED LINKS</span></span>
