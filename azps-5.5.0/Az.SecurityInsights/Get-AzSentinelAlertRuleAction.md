---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158449"
---
# <span data-ttu-id="b4999-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="b4999-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="b4999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4999-102">SYNOPSIS</span></span>
<span data-ttu-id="b4999-103">Automatische Antwort erhalten (Warnungsregelaktion).</span><span class="sxs-lookup"><span data-stu-id="b4999-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="b4999-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4999-104">SYNTAX</span></span>

### <span data-ttu-id="b4999-105">AlertRuleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4999-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4999-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="b4999-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4999-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4999-107">DESCRIPTION</span></span>
<span data-ttu-id="b4999-108">Das **Cmdlet "Get-AzSentinelAlertRuleAction"** ruft eine Automatisierte Antwort (Warnungsregelaktion) aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="b4999-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="b4999-109">Wenn Sie die Parameter *"ActionId"* und *"AlertRuleId"* angeben, wird ein einzelnes **"AlertRuleAction"-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b4999-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="b4999-110">Wenn Sie den Parameter *"ActionId"* nicht angeben, wird ein Array zurückgegeben, das alle Aktionen für die spezifische Warnungsregel im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="b4999-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="b4999-111">Sie können das **Aktionsobjekt** verwenden, um die Aktion zu aktualisieren, beispielsweise können Sie die Aktion für **eine** Warnungsregel ändern.</span><span class="sxs-lookup"><span data-stu-id="b4999-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="b4999-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4999-112">EXAMPLES</span></span>

### <span data-ttu-id="b4999-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4999-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="b4999-114">Dieses Beispiel ruft alle Aktionen **für** die angegebene Warnungsregel im angegebenen Arbeitsbereich ab und speichert sie dann in der $AlertRuleActions Variable.</span><span class="sxs-lookup"><span data-stu-id="b4999-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="b4999-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b4999-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="b4999-116">In diesem Beispiel wird **ein AlertRuleAction-Konto** für die angegebene Warnungsregel im angegebenen Arbeitsbereich ruft und dann in der $AlertRuleAction gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b4999-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="b4999-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4999-117">PARAMETERS</span></span>

### <span data-ttu-id="b4999-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="b4999-118">-ActionId</span></span>
<span data-ttu-id="b4999-119">Aktions-ID.</span><span class="sxs-lookup"><span data-stu-id="b4999-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4999-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="b4999-120">-AlertRuleId</span></span>
<span data-ttu-id="b4999-121">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="b4999-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="b4999-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4999-122">-DefaultProfile</span></span>
<span data-ttu-id="b4999-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4999-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4999-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4999-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4999-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b4999-125">Resource group name.</span></span>

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

### <span data-ttu-id="b4999-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4999-126">-WorkspaceName</span></span>
<span data-ttu-id="b4999-127">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="b4999-127">Workspace Name.</span></span>

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

### <span data-ttu-id="b4999-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4999-128">CommonParameters</span></span>
<span data-ttu-id="b4999-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4999-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4999-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4999-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4999-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4999-131">INPUTS</span></span>

### <span data-ttu-id="b4999-132">Keine</span><span class="sxs-lookup"><span data-stu-id="b4999-132">None</span></span>
## <span data-ttu-id="b4999-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4999-133">OUTPUTS</span></span>

### <span data-ttu-id="b4999-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="b4999-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="b4999-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4999-135">NOTES</span></span>

## <span data-ttu-id="b4999-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4999-136">RELATED LINKS</span></span>
