---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 37cc56714712d71ab34adee14a8b758cd9dd1113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935995"
---
# <span data-ttu-id="5444c-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="5444c-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="5444c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5444c-102">SYNOPSIS</span></span>
<span data-ttu-id="5444c-103">Automatische Antwort (Warnungsregelaktion)</span><span class="sxs-lookup"><span data-stu-id="5444c-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="5444c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5444c-104">SYNTAX</span></span>

### <span data-ttu-id="5444c-105">AlertRuleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="5444c-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5444c-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="5444c-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5444c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5444c-107">DESCRIPTION</span></span>
<span data-ttu-id="5444c-108">Das **Cmdlet Get-AzSentinelAlertRuleAction** ruft eine automatisierte Antwort (Warnungsregelaktion) aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="5444c-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="5444c-109">Wenn Sie die *Parameter ActionId* und *AlertRuleId angeben,* wird ein einzelnes **AlertRuleAction-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5444c-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="5444c-110">Wenn Sie den Parameter *ActionId* nicht angeben, wird ein Array zurückgegeben, das alle Aktionen für die spezifische Warnungsregel im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="5444c-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="5444c-111">Sie können das **Action-Objekt** verwenden, um die Aktion zu aktualisieren, z. B. können Sie die Aktion für **eine** Warnungsregel ändern.</span><span class="sxs-lookup"><span data-stu-id="5444c-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="5444c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5444c-112">EXAMPLES</span></span>

### <span data-ttu-id="5444c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5444c-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="5444c-114">In diesem Beispiel werden alle **Aktionen** für die angegebene Warnungsregel im angegebenen Arbeitsbereich ab- und dann in der $AlertRuleActions gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5444c-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="5444c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5444c-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="5444c-116">In diesem Beispiel wird **eine AlertRuleAction** für die angegebene Warnungsregel im angegebenen Arbeitsbereich und dann in der $AlertRuleAction gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5444c-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="5444c-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5444c-117">PARAMETERS</span></span>

### <span data-ttu-id="5444c-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="5444c-118">-ActionId</span></span>
<span data-ttu-id="5444c-119">Aktions-ID.</span><span class="sxs-lookup"><span data-stu-id="5444c-119">Action Id.</span></span>

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

### <span data-ttu-id="5444c-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="5444c-120">-AlertRuleId</span></span>
<span data-ttu-id="5444c-121">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="5444c-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="5444c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5444c-122">-DefaultProfile</span></span>
<span data-ttu-id="5444c-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5444c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5444c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5444c-124">-ResourceGroupName</span></span>
<span data-ttu-id="5444c-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5444c-125">Resource group name.</span></span>

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

### <span data-ttu-id="5444c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5444c-126">-WorkspaceName</span></span>
<span data-ttu-id="5444c-127">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="5444c-127">Workspace Name.</span></span>

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

### <span data-ttu-id="5444c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5444c-128">CommonParameters</span></span>
<span data-ttu-id="5444c-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5444c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5444c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5444c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5444c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5444c-131">INPUTS</span></span>

### <span data-ttu-id="5444c-132">Keine</span><span class="sxs-lookup"><span data-stu-id="5444c-132">None</span></span>
## <span data-ttu-id="5444c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5444c-133">OUTPUTS</span></span>

### <span data-ttu-id="5444c-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="5444c-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="5444c-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5444c-135">NOTES</span></span>

## <span data-ttu-id="5444c-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5444c-136">RELATED LINKS</span></span>
