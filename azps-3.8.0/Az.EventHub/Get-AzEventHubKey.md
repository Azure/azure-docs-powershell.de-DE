---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: ab305965c48a855caca8b165105f2dd216a8900a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003060"
---
# <span data-ttu-id="fa7eb-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="fa7eb-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="fa7eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7eb-103">Ruft die Primärschlüssel Details der angegebenen Event Hubs-Autorisierungsregel ab.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="fa7eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa7eb-104">SYNTAX</span></span>

### <span data-ttu-id="fa7eb-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa7eb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa7eb-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa7eb-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa7eb-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa7eb-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa7eb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa7eb-108">DESCRIPTION</span></span>
<span data-ttu-id="fa7eb-109">Das Get-AzEventHubKey-Cmdlet gibt die primären und sekundären connectionStrings-und Schlüssel Details der angegebenen Namespace-/Ereignis Hubs/Alias Autorisierungsregel zurück.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="fa7eb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa7eb-110">EXAMPLES</span></span>

### <span data-ttu-id="fa7eb-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="fa7eb-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="fa7eb-112">Beispiel 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="fa7eb-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="fa7eb-113">Ruft Details der primären und sekundären connectionStrings und Schlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="fa7eb-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="fa7eb-114">Beispiel 3-Alias (georecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="fa7eb-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="fa7eb-115">Ruft Details der primären, sekundären, AliasPrimary und AliasSecondary-connectionStrings und-Schlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="fa7eb-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="fa7eb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa7eb-116">PARAMETERS</span></span>

### <span data-ttu-id="fa7eb-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="fa7eb-117">-AliasName</span></span>
<span data-ttu-id="fa7eb-118">Alias Name</span><span class="sxs-lookup"><span data-stu-id="fa7eb-118">Alias Name</span></span>

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

### <span data-ttu-id="fa7eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7eb-119">-DefaultProfile</span></span>
<span data-ttu-id="fa7eb-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa7eb-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fa7eb-121">-EventHub</span></span>
<span data-ttu-id="fa7eb-122">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="fa7eb-122">EventHub Name</span></span>

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

### <span data-ttu-id="fa7eb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fa7eb-123">-Name</span></span>
<span data-ttu-id="fa7eb-124">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="fa7eb-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fa7eb-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fa7eb-125">-Namespace</span></span>
<span data-ttu-id="fa7eb-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fa7eb-126">Namespace Name</span></span>

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

### <span data-ttu-id="fa7eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa7eb-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fa7eb-128">Resource Group Name</span></span>

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

### <span data-ttu-id="fa7eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7eb-129">CommonParameters</span></span>
<span data-ttu-id="fa7eb-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7eb-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa7eb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7eb-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa7eb-132">INPUTS</span></span>

### <span data-ttu-id="fa7eb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fa7eb-133">System.String</span></span>

## <span data-ttu-id="fa7eb-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa7eb-134">OUTPUTS</span></span>

### <span data-ttu-id="fa7eb-135">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="fa7eb-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="fa7eb-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa7eb-136">NOTES</span></span>

## <span data-ttu-id="fa7eb-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa7eb-137">RELATED LINKS</span></span>
