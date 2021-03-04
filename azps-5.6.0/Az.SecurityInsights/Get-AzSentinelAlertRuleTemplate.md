---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: db398fe5870a1ff304637c9aa33bf168c49a7759
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945718"
---
# <span data-ttu-id="6ab18-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="6ab18-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="6ab18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab18-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab18-103">Vorlage "Analytische Regel" erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ab18-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="6ab18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ab18-104">SYNTAX</span></span>

### <span data-ttu-id="6ab18-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ab18-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab18-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="6ab18-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab18-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab18-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ab18-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ab18-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab18-109">Das **Cmdlet Get-AzSentinelAlertRuleTemplate** ruft eine Warnungsregelvorlage aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="6ab18-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="6ab18-110">Wenn Sie den *Parameter AlertRuleTemplateId angeben,* wird ein einzelnes **AlertRuleTemplate-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ab18-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="6ab18-111">Wenn Sie den Parameter *AlertRuleTemplateId* nicht angeben, wird ein Array zurückgegeben, das alle Warnungsregelvorlagen im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="6ab18-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="6ab18-112">Sie können das **AlertRuleTemplate-Objekt** verwenden, um eine neue Warnungsregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ab18-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="6ab18-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ab18-113">EXAMPLES</span></span>

### <span data-ttu-id="6ab18-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ab18-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="6ab18-115">In diesem Beispiel werden alle **AlertRuleTemplates** im angegebenen Arbeitsbereich ab- und dann in der $AlertRuleTemplates gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6ab18-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="6ab18-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6ab18-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="6ab18-117">In diesem Beispiel wird **eine AlertRuleTemplate** im angegebenen Arbeitsbereich angezeigt und dann in der $AlertRuleTemplate gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6ab18-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="6ab18-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ab18-118">PARAMETERS</span></span>

### <span data-ttu-id="6ab18-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="6ab18-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="6ab18-120">Vorlagenbenachrichtigungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="6ab18-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab18-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab18-121">-DefaultProfile</span></span>
<span data-ttu-id="6ab18-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ab18-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab18-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab18-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ab18-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6ab18-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab18-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab18-125">-ResourceId</span></span>
<span data-ttu-id="6ab18-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6ab18-126">Resource Id.</span></span>

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

### <span data-ttu-id="6ab18-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ab18-127">-WorkspaceName</span></span>
<span data-ttu-id="6ab18-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="6ab18-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab18-129">CommonParameters</span></span>
<span data-ttu-id="6ab18-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab18-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ab18-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab18-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ab18-132">INPUTS</span></span>

### <span data-ttu-id="6ab18-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6ab18-133">System.String</span></span>
## <span data-ttu-id="6ab18-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ab18-134">OUTPUTS</span></span>

### <span data-ttu-id="6ab18-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="6ab18-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="6ab18-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6ab18-136">NOTES</span></span>

## <span data-ttu-id="6ab18-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6ab18-137">RELATED LINKS</span></span>
