---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 842b48e1645bb141650c2a53dc86bbb5e79acb80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927216"
---
# <span data-ttu-id="89d57-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="89d57-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="89d57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d57-102">SYNOPSIS</span></span>
<span data-ttu-id="89d57-103">Ruft die Details einer Autorisierungsregel ab oder ruft eine Liste der Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="89d57-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="89d57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89d57-104">SYNTAX</span></span>

### <span data-ttu-id="89d57-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="89d57-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89d57-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="89d57-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89d57-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="89d57-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89d57-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89d57-108">DESCRIPTION</span></span>
<span data-ttu-id="89d57-109">Das Get-AzEventHubAuthorizationRule-Cmdlet ruft entweder die Details einer Autorisierungsregel oder eine Liste aller Autorisierungsregeln für einen angegebenen Ereignishub ab.</span><span class="sxs-lookup"><span data-stu-id="89d57-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="89d57-110">Wenn der Name einer Autorisierungsregel angegeben wird, werden die Details dieser einzelnen Autorisierungsregel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d57-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="89d57-111">Wenn der Name einer Autorisierungsregel nicht angegeben wird, wird eine Liste aller Autorisierungsregeln für den angegebenen Ereignishub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d57-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="89d57-112">Wenn (Disaster Recovery) Aliasname angegeben wird, werden die Details der Autorisierungsregel des konfigurierten Namespaces für Alias zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d57-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="89d57-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89d57-113">EXAMPLES</span></span>

### <span data-ttu-id="89d57-114">Beispiel 1: AuthorizationRule für Namespace</span><span class="sxs-lookup"><span data-stu-id="89d57-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="89d57-115">Ruft die Autorisierungsregel \` MyAuthRuleName \` im Namespace \` MyNamespaceName \` ab.</span><span class="sxs-lookup"><span data-stu-id="89d57-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="89d57-116">Beispiel 2: AuthorizationRules für Namespace</span><span class="sxs-lookup"><span data-stu-id="89d57-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="89d57-117">Ruft eine Liste aller Autorisierungsregeln im Namespace \` MyNamespaceName \` ab.</span><span class="sxs-lookup"><span data-stu-id="89d57-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="89d57-118">Beispiel 3: AuthorizationRule für EventHub</span><span class="sxs-lookup"><span data-stu-id="89d57-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="89d57-119">Ruft die Autorisierungsregel \` MyAuthRuleName \` im Ereignishub MyEventHubName ab, der durch den \` \` Namespace \` MyNamespaceName begrenzt \` wird.</span><span class="sxs-lookup"><span data-stu-id="89d57-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="89d57-120">Beispiel 4: AuthorizationRules für EventHub</span><span class="sxs-lookup"><span data-stu-id="89d57-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="89d57-121">Ruft Listenautorisierungsregeln im Ereignishub MyEventHubName ab, der durch den \` \` Namespace \` MyNamespaceName begrenzt \` ist.</span><span class="sxs-lookup"><span data-stu-id="89d57-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="89d57-122">Beispiel 5: AuthorizationRule für Alias (GeoRecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="89d57-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="89d57-123">Ruft die Autorisierungsregel \` MyAuthRuleName \` im Namespace \` MyNamespaceName \` ab.</span><span class="sxs-lookup"><span data-stu-id="89d57-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="89d57-124">Beispiel 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="89d57-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="89d57-125">Ruft eine Liste aller Autorisierungsregel \` MyAuthRuleName \` im Namespace \` MyNamespaceName \` ab.</span><span class="sxs-lookup"><span data-stu-id="89d57-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="89d57-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="89d57-126">PARAMETERS</span></span>

### <span data-ttu-id="89d57-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="89d57-127">-AliasName</span></span>
<span data-ttu-id="89d57-128">Aliasname</span><span class="sxs-lookup"><span data-stu-id="89d57-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d57-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d57-129">-DefaultProfile</span></span>
<span data-ttu-id="89d57-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89d57-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d57-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="89d57-131">-Eventhub</span></span>
<span data-ttu-id="89d57-132">Eventhubname</span><span class="sxs-lookup"><span data-stu-id="89d57-132">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d57-133">-Name</span><span class="sxs-lookup"><span data-stu-id="89d57-133">-Name</span></span>
<span data-ttu-id="89d57-134">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="89d57-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d57-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="89d57-135">-Namespace</span></span>
<span data-ttu-id="89d57-136">Namespacename</span><span class="sxs-lookup"><span data-stu-id="89d57-136">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d57-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d57-137">-ResourceGroupName</span></span>
<span data-ttu-id="89d57-138">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="89d57-138">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d57-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d57-139">CommonParameters</span></span>
<span data-ttu-id="89d57-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d57-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d57-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d57-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d57-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89d57-142">INPUTS</span></span>

### <span data-ttu-id="89d57-143">System.String</span><span class="sxs-lookup"><span data-stu-id="89d57-143">System.String</span></span>

## <span data-ttu-id="89d57-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89d57-144">OUTPUTS</span></span>

### <span data-ttu-id="89d57-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="89d57-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="89d57-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="89d57-146">NOTES</span></span>

## <span data-ttu-id="89d57-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="89d57-147">RELATED LINKS</span></span>
