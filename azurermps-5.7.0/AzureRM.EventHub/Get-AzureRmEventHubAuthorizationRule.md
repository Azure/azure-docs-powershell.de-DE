---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502590"
---
# <span data-ttu-id="4d7ff-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4d7ff-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4d7ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7ff-103">Ruft die Details einer Autorisierungsregel ab oder ruft eine Liste mit Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d7ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d7ff-104">SYNTAX</span></span>

### <span data-ttu-id="4d7ff-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d7ff-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d7ff-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4d7ff-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d7ff-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="4d7ff-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d7ff-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d7ff-108">DESCRIPTION</span></span>
<span data-ttu-id="4d7ff-109">Das Get-AzureRmEventHubAuthorizationRule-Cmdlet ruft entweder die Details einer Autorisierungsregel oder eine Liste aller Autorisierungsregeln für einen angegebenen Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="4d7ff-110">Wenn der Name einer Autorisierungsregel angegeben wird, werden die Details dieser einzelnen Autorisierungsregel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="4d7ff-111">Wenn der Name einer Autorisierungsregel nicht angegeben wird, wird eine Liste aller Autorisierungsregeln für den angegebenen Ereignis-Hub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="4d7ff-112">Wenn der Alias Name (Disaster Recovery) bereitgestellt wird, werden die Details der Autorisierungsregel des Namespaces für Alias Konfiguration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="4d7ff-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d7ff-113">EXAMPLES</span></span>

### <span data-ttu-id="4d7ff-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d7ff-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="4d7ff-115">Ruft die Autorisierungsregel \` MyAuthRuleName \` in der Ereignis \` -Hub-MyEventHubName ab \` , die durch den Namespace \` mynamespacename beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="4d7ff-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4d7ff-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4d7ff-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="4d7ff-117">Ruft eine Liste aller Autorisierungsregeln im Ereignis-Hub \` -MyEventHubName ab \` , die durch den Namespace \` mynamespacename beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="4d7ff-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4d7ff-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4d7ff-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="4d7ff-119">Ruft die Autorisierungsregel \` MyAuthRuleName \` im Namespace \` mynamespacename ab \` .</span><span class="sxs-lookup"><span data-stu-id="4d7ff-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4d7ff-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d7ff-120">PARAMETERS</span></span>

### <span data-ttu-id="4d7ff-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="4d7ff-121">-AliasName</span></span>
<span data-ttu-id="4d7ff-122">Alias Name</span><span class="sxs-lookup"><span data-stu-id="4d7ff-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7ff-123">-DefaultProfile</span></span>
<span data-ttu-id="4d7ff-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7ff-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="4d7ff-125">-Eventhub</span></span>
<span data-ttu-id="4d7ff-126">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="4d7ff-126">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7ff-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4d7ff-127">-Name</span></span>
<span data-ttu-id="4d7ff-128">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="4d7ff-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7ff-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4d7ff-129">-Namespace</span></span>
<span data-ttu-id="4d7ff-130">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4d7ff-130">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7ff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d7ff-131">-ResourceGroupName</span></span>
<span data-ttu-id="4d7ff-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4d7ff-132">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7ff-133">CommonParameters</span></span>
<span data-ttu-id="4d7ff-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4d7ff-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d7ff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7ff-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d7ff-136">INPUTS</span></span>

### <span data-ttu-id="4d7ff-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4d7ff-137">System.String</span></span>


## <span data-ttu-id="4d7ff-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d7ff-138">OUTPUTS</span></span>

### <span data-ttu-id="4d7ff-139">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4d7ff-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="4d7ff-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d7ff-140">NOTES</span></span>

## <span data-ttu-id="4d7ff-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d7ff-141">RELATED LINKS</span></span>
