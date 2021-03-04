---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 836d566c9e75fdce825542ebb13520933c071cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935992"
---
# <span data-ttu-id="8fe54-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8fe54-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="8fe54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe54-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe54-103">Ruft eine Analyse (Warnungsregel) ab.</span><span class="sxs-lookup"><span data-stu-id="8fe54-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="8fe54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fe54-104">SYNTAX</span></span>

### <span data-ttu-id="8fe54-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fe54-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe54-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8fe54-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe54-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe54-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe54-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fe54-108">DESCRIPTION</span></span>
<span data-ttu-id="8fe54-109">Das **Cmdlet Get-AzSentinelAlertRule** ruft eine Analytische (Warnungsregel) aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="8fe54-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="8fe54-110">Wenn Sie den *Parameter AlertRuleId angeben,* wird ein einzelnes **AlertRule-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8fe54-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="8fe54-111">Wenn Sie den Parameter *AlertRuleId* nicht angeben, wird ein Array zurückgegeben, das alle Warnungsregeln im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="8fe54-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="8fe54-112">Sie können das **AlertRule-Objekt** verwenden, um die AlertRule zu aktualisieren, z. B. können Sie **die AlertRule deaktivieren.**</span><span class="sxs-lookup"><span data-stu-id="8fe54-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="8fe54-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8fe54-113">EXAMPLES</span></span>

### <span data-ttu-id="8fe54-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fe54-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="8fe54-115">In diesem Beispiel werden alle **AlertRules** im angegebenen Arbeitsbereich ab- und dann in der $AlertRules gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8fe54-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="8fe54-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8fe54-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="8fe54-117">In diesem Beispiel wird **eine AlertRule** im angegebenen Arbeitsbereich angezeigt und dann in der $AlertRule gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8fe54-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="8fe54-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8fe54-118">PARAMETERS</span></span>

### <span data-ttu-id="8fe54-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8fe54-119">-AlertRuleId</span></span>
<span data-ttu-id="8fe54-120">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="8fe54-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe54-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe54-121">-DefaultProfile</span></span>
<span data-ttu-id="8fe54-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fe54-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fe54-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe54-123">-ResourceGroupName</span></span>
<span data-ttu-id="8fe54-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8fe54-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe54-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe54-125">-ResourceId</span></span>
<span data-ttu-id="8fe54-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8fe54-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe54-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8fe54-127">-WorkspaceName</span></span>
<span data-ttu-id="8fe54-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="8fe54-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe54-129">CommonParameters</span></span>
<span data-ttu-id="8fe54-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe54-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fe54-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe54-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8fe54-132">INPUTS</span></span>

### <span data-ttu-id="8fe54-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8fe54-133">System.String</span></span>
## <span data-ttu-id="8fe54-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8fe54-134">OUTPUTS</span></span>

### <span data-ttu-id="8fe54-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8fe54-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="8fe54-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8fe54-136">NOTES</span></span>

## <span data-ttu-id="8fe54-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8fe54-137">RELATED LINKS</span></span>
