---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 07cc93cb75c7e6eab57fa03e663de700ee676432
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842363"
---
# <span data-ttu-id="a080b-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a080b-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="a080b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a080b-102">SYNOPSIS</span></span>
<span data-ttu-id="a080b-103">Ruft die Details einer Autorisierungsregel ab oder ruft eine Liste mit Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="a080b-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="a080b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a080b-104">SYNTAX</span></span>

### <span data-ttu-id="a080b-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a080b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a080b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a080b-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a080b-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="a080b-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a080b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a080b-108">DESCRIPTION</span></span>
<span data-ttu-id="a080b-109">Das Get-AzEventHubAuthorizationRule-Cmdlet ruft entweder die Details einer Autorisierungsregel oder eine Liste aller Autorisierungsregeln für einen angegebenen Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="a080b-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="a080b-110">Wenn der Name einer Autorisierungsregel angegeben wird, werden die Details dieser einzelnen Autorisierungsregel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a080b-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="a080b-111">Wenn der Name einer Autorisierungsregel nicht angegeben wird, wird eine Liste aller Autorisierungsregeln für den angegebenen Ereignis-Hub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a080b-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="a080b-112">Wenn der Alias Name (Disaster Recovery) bereitgestellt wird, werden die Details der Autorisierungsregel des Namespaces für Alias Konfiguration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a080b-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="a080b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a080b-113">EXAMPLES</span></span>

### <span data-ttu-id="a080b-114">Beispiel für 1,0-AuthorizationRule für Namespace</span><span class="sxs-lookup"><span data-stu-id="a080b-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="a080b-115">Ruft die Autorisierungsregel \` MyAuthRuleName \` im Namespace \` mynamespacename ab \` .</span><span class="sxs-lookup"><span data-stu-id="a080b-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="a080b-116">Beispiel 1,1-authorizationrules für Namespace</span><span class="sxs-lookup"><span data-stu-id="a080b-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="a080b-117">Ruft eine Liste aller Autorisierungsregeln im Namespace \` mynamespacename ab \` .</span><span class="sxs-lookup"><span data-stu-id="a080b-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="a080b-118">Beispiel 2,0-AuthorizationRule für EventHub</span><span class="sxs-lookup"><span data-stu-id="a080b-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="a080b-119">Ruft die Autorisierungsregel \` MyAuthRuleName \` in der Ereignis \` -Hub-MyEventHubName ab \` , die durch den Namespace \` mynamespacename beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="a080b-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="a080b-120">Beispiel 2,1-authorizationrules für EventHub</span><span class="sxs-lookup"><span data-stu-id="a080b-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="a080b-121">Ruft Listen Autorisierungsregeln im MyEventHubName des Ereignis Hubs ab \` \` , auf den der Namespace \` mynamespacename beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="a080b-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="a080b-122">Beispiel 3,0-AuthorizationRule für Alias (georecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="a080b-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="a080b-123">Ruft die Autorisierungsregel \` MyAuthRuleName \` im Namespace \` mynamespacename ab \` .</span><span class="sxs-lookup"><span data-stu-id="a080b-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="a080b-124">Beispiel 3,1-authorizationrules für Alias (georecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="a080b-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="a080b-125">Ruft eine Liste aller Autorisierungsregel- \` MyAuthRuleName \` im Namespace \` mynamespacename ab \` .</span><span class="sxs-lookup"><span data-stu-id="a080b-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="a080b-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="a080b-126">PARAMETERS</span></span>

### <span data-ttu-id="a080b-127">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="a080b-127">-AliasName</span></span>
<span data-ttu-id="a080b-128">Alias Name</span><span class="sxs-lookup"><span data-stu-id="a080b-128">Alias Name</span></span>

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

### <span data-ttu-id="a080b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a080b-129">-DefaultProfile</span></span>
<span data-ttu-id="a080b-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a080b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a080b-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="a080b-131">-Eventhub</span></span>
<span data-ttu-id="a080b-132">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="a080b-132">Eventhub Name</span></span>

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

### <span data-ttu-id="a080b-133">-Name</span><span class="sxs-lookup"><span data-stu-id="a080b-133">-Name</span></span>
<span data-ttu-id="a080b-134">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="a080b-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="a080b-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a080b-135">-Namespace</span></span>
<span data-ttu-id="a080b-136">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a080b-136">Namespace Name</span></span>

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

### <span data-ttu-id="a080b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a080b-137">-ResourceGroupName</span></span>
<span data-ttu-id="a080b-138">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a080b-138">Resource Group Name</span></span>

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

### <span data-ttu-id="a080b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a080b-139">CommonParameters</span></span>
<span data-ttu-id="a080b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a080b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a080b-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a080b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a080b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a080b-142">INPUTS</span></span>

### <span data-ttu-id="a080b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a080b-143">System.String</span></span>

## <span data-ttu-id="a080b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a080b-144">OUTPUTS</span></span>

### <span data-ttu-id="a080b-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a080b-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a080b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a080b-146">NOTES</span></span>

## <span data-ttu-id="a080b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a080b-147">RELATED LINKS</span></span>
