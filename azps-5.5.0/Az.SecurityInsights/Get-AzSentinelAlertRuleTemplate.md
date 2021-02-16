---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150777"
---
# <span data-ttu-id="b423b-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="b423b-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="b423b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b423b-102">SYNOPSIS</span></span>
<span data-ttu-id="b423b-103">"Analyseregelvorlage".</span><span class="sxs-lookup"><span data-stu-id="b423b-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="b423b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b423b-104">SYNTAX</span></span>

### <span data-ttu-id="b423b-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="b423b-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b423b-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="b423b-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b423b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b423b-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b423b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b423b-108">DESCRIPTION</span></span>
<span data-ttu-id="b423b-109">Das **Cmdlet "Get-AzSentinelAlertRuleTemplate"** ruft eine Warnungsregelvorlage aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="b423b-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="b423b-110">Wenn Sie den Parameter *"AlertRuleTemplateId"* angeben, wird ein einzelnes **"AlertRuleTemplate"-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b423b-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="b423b-111">Wenn Sie den Parameter *"AlertRuleTemplateId"* nicht angeben, wird ein Array zurückgegeben, das alle Warnungsregelvorlagen im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="b423b-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="b423b-112">Sie können das **"AlertRuleTemplate"-Objekt** verwenden, um eine neue Warnungsregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b423b-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="b423b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b423b-113">EXAMPLES</span></span>

### <span data-ttu-id="b423b-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b423b-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="b423b-115">Dieses Beispiel ruft alle **AlertRuleTemplates** im angegebenen Arbeitsbereich ab und speichert sie dann in der $AlertRuleTemplates Variable.</span><span class="sxs-lookup"><span data-stu-id="b423b-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="b423b-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b423b-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="b423b-117">In diesem Beispiel wird **eine "AlertRuleTemplate"** im angegebenen Arbeitsbereich ab- und dann in der $AlertRuleTemplate gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b423b-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="b423b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b423b-118">PARAMETERS</span></span>

### <span data-ttu-id="b423b-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="b423b-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="b423b-120">Vorlagen-Benachrichtigungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="b423b-120">Template Alert Rule Id.</span></span>

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

### <span data-ttu-id="b423b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b423b-121">-DefaultProfile</span></span>
<span data-ttu-id="b423b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b423b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b423b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b423b-123">-ResourceGroupName</span></span>
<span data-ttu-id="b423b-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b423b-124">Resource group name.</span></span>

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

### <span data-ttu-id="b423b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b423b-125">-ResourceId</span></span>
<span data-ttu-id="b423b-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b423b-126">Resource Id.</span></span>

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

### <span data-ttu-id="b423b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b423b-127">-WorkspaceName</span></span>
<span data-ttu-id="b423b-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="b423b-128">Workspace Name.</span></span>

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

### <span data-ttu-id="b423b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b423b-129">CommonParameters</span></span>
<span data-ttu-id="b423b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b423b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b423b-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b423b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b423b-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b423b-132">INPUTS</span></span>

### <span data-ttu-id="b423b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b423b-133">System.String</span></span>
## <span data-ttu-id="b423b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b423b-134">OUTPUTS</span></span>

### <span data-ttu-id="b423b-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="b423b-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="b423b-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b423b-136">NOTES</span></span>

## <span data-ttu-id="b423b-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b423b-137">RELATED LINKS</span></span>
