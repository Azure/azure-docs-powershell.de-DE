---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170663"
---
# <span data-ttu-id="75cff-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="75cff-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="75cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cff-102">SYNOPSIS</span></span>
<span data-ttu-id="75cff-103">Ruft die Details einer Autorisierungsregel oder eine Liste der Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="75cff-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="75cff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75cff-104">SYNTAX</span></span>

### <span data-ttu-id="75cff-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="75cff-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75cff-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="75cff-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75cff-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="75cff-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75cff-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75cff-108">DESCRIPTION</span></span>
<span data-ttu-id="75cff-109">Das Get-AzEventHubAuthorizationRule-Cmdlet ruft entweder die Details einer Autorisierungsregel oder eine Liste aller Autorisierungsregeln für einen bestimmten Ereignishub ab.</span><span class="sxs-lookup"><span data-stu-id="75cff-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="75cff-110">Wenn der Name einer Autorisierungsregel angegeben wird, werden die Details dieser einzelnen Autorisierungsregel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75cff-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="75cff-111">Wenn der Name einer Autorisierungsregel nicht angegeben wird, wird eine Liste aller Autorisierungsregeln für den angegebenen Ereignishub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75cff-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="75cff-112">Wenn (Notfallwiederherstellung)-Aliasname angegeben wird, werden die Details der Autorisierungsregel des Namespaces für den konfigurierten Alias zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75cff-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="75cff-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75cff-113">EXAMPLES</span></span>

### <span data-ttu-id="75cff-114">Beispiel 1: AuthorizationRule für Namespace</span><span class="sxs-lookup"><span data-stu-id="75cff-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="75cff-115">Ruft die Autorisierungsregel \` "MyAuthRuleName" \` im Namespace \` "MyNamespaceName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="75cff-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="75cff-116">Beispiel 2: AuthorizationRules für Namespace</span><span class="sxs-lookup"><span data-stu-id="75cff-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="75cff-117">Ruft eine Liste aller Autorisierungsregeln im Namespace \` "MyNamespaceName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="75cff-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="75cff-118">Beispiel 3: AuthorizationRule für EventHub</span><span class="sxs-lookup"><span data-stu-id="75cff-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="75cff-119">Ruft die \` Autorisierungsregel "MyAuthRuleName" \` im Ereignishub \` "MyEventHubName" ab, der durch den \` Namespace \` "MyNamespaceName" begrenzt \` ist.</span><span class="sxs-lookup"><span data-stu-id="75cff-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="75cff-120">Beispiel 4: AuthorizationRules für EventHub</span><span class="sxs-lookup"><span data-stu-id="75cff-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="75cff-121">Ruft Listenautorisierungsregeln im Ereignishub \` "MyEventHubName" ab, der durch den \` Namespace \` "MyNamespaceName" begrenzt \` ist.</span><span class="sxs-lookup"><span data-stu-id="75cff-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="75cff-122">Beispiel 5: Autorisierungsplan für Alias (GeoRecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="75cff-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="75cff-123">Ruft die Autorisierungsregel \` "MyAuthRuleName" \` im Namespace \` "MyNamespaceName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="75cff-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="75cff-124">Beispiel 6: AuthorizationRules for Alias (GeoRecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="75cff-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="75cff-125">Ruft eine Liste aller Autorisierungsregel \` "MyAuthRuleName" \` im Namespace \` "MyNamespaceName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="75cff-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="75cff-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cff-126">PARAMETERS</span></span>

### <span data-ttu-id="75cff-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="75cff-127">-AliasName</span></span>
<span data-ttu-id="75cff-128">Aliasname</span><span class="sxs-lookup"><span data-stu-id="75cff-128">Alias Name</span></span>

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

### <span data-ttu-id="75cff-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cff-129">-DefaultProfile</span></span>
<span data-ttu-id="75cff-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75cff-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75cff-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="75cff-131">-Eventhub</span></span>
<span data-ttu-id="75cff-132">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="75cff-132">Eventhub Name</span></span>

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

### <span data-ttu-id="75cff-133">-Name</span><span class="sxs-lookup"><span data-stu-id="75cff-133">-Name</span></span>
<span data-ttu-id="75cff-134">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="75cff-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="75cff-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75cff-135">-Namespace</span></span>
<span data-ttu-id="75cff-136">Namespacename</span><span class="sxs-lookup"><span data-stu-id="75cff-136">Namespace Name</span></span>

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

### <span data-ttu-id="75cff-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75cff-137">-ResourceGroupName</span></span>
<span data-ttu-id="75cff-138">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="75cff-138">Resource Group Name</span></span>

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

### <span data-ttu-id="75cff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cff-139">CommonParameters</span></span>
<span data-ttu-id="75cff-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cff-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75cff-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cff-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75cff-142">INPUTS</span></span>

### <span data-ttu-id="75cff-143">System.String</span><span class="sxs-lookup"><span data-stu-id="75cff-143">System.String</span></span>

## <span data-ttu-id="75cff-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75cff-144">OUTPUTS</span></span>

### <span data-ttu-id="75cff-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="75cff-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="75cff-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75cff-146">NOTES</span></span>

## <span data-ttu-id="75cff-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75cff-147">RELATED LINKS</span></span>
