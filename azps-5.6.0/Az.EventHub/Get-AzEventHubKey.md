---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: f9f4eb7f60683524eccec8b3d35926b86fa52bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921235"
---
# <span data-ttu-id="e5530-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="e5530-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="e5530-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5530-102">SYNOPSIS</span></span>
<span data-ttu-id="e5530-103">Ruft die Primärschlüsseldetails der angegebenen Ereignishubautorisierungsregel ab.</span><span class="sxs-lookup"><span data-stu-id="e5530-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="e5530-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5530-104">SYNTAX</span></span>

### <span data-ttu-id="e5530-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5530-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5530-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5530-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5530-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5530-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5530-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5530-108">DESCRIPTION</span></span>
<span data-ttu-id="e5530-109">Das Get-AzEventHubKey-Cmdlet gibt primäre und sekundäre Verbindungszeichenfolgen und Schlüsseldetails der angegebenen NameSpace-/Ereignishubs/Alias-Autorisierungsregel zurück.</span><span class="sxs-lookup"><span data-stu-id="e5530-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="e5530-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5530-110">EXAMPLES</span></span>

### <span data-ttu-id="e5530-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="e5530-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="e5530-112">Beispiel 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="e5530-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="e5530-113">Ruft Details zu primären und sekundären Verbindungszeichenfolgen und Schlüsseln für die Autorisierungsregel \` MyAuthRuleName \` ab.</span><span class="sxs-lookup"><span data-stu-id="e5530-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="e5530-114">Beispiel 3: Alias (GeoRecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="e5530-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="e5530-115">Ruft Details zu primären, sekundären, AliasPrimary- und AliasSecondary-Verbindungszeichenfolgen und Schlüsseln für die Autorisierungsregel \` MyAuthRuleName \` ab.</span><span class="sxs-lookup"><span data-stu-id="e5530-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="e5530-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e5530-116">PARAMETERS</span></span>

### <span data-ttu-id="e5530-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e5530-117">-AliasName</span></span>
<span data-ttu-id="e5530-118">Aliasname</span><span class="sxs-lookup"><span data-stu-id="e5530-118">Alias Name</span></span>

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

### <span data-ttu-id="e5530-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5530-119">-DefaultProfile</span></span>
<span data-ttu-id="e5530-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5530-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5530-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e5530-121">-EventHub</span></span>
<span data-ttu-id="e5530-122">EventHub-Name</span><span class="sxs-lookup"><span data-stu-id="e5530-122">EventHub Name</span></span>

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

### <span data-ttu-id="e5530-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e5530-123">-Name</span></span>
<span data-ttu-id="e5530-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="e5530-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5530-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5530-125">-Namespace</span></span>
<span data-ttu-id="e5530-126">Namespacename</span><span class="sxs-lookup"><span data-stu-id="e5530-126">Namespace Name</span></span>

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

### <span data-ttu-id="e5530-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5530-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5530-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e5530-128">Resource Group Name</span></span>

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

### <span data-ttu-id="e5530-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5530-129">CommonParameters</span></span>
<span data-ttu-id="e5530-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5530-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5530-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5530-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5530-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5530-132">INPUTS</span></span>

### <span data-ttu-id="e5530-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e5530-133">System.String</span></span>

## <span data-ttu-id="e5530-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5530-134">OUTPUTS</span></span>

### <span data-ttu-id="e5530-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="e5530-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="e5530-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e5530-136">NOTES</span></span>

## <span data-ttu-id="e5530-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e5530-137">RELATED LINKS</span></span>
