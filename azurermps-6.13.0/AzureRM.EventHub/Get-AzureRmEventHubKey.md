---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: c22bb41702bb4e338d0548be6c7544d597ef0230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500222"
---
# <span data-ttu-id="74dc0-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="74dc0-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="74dc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="74dc0-103">Ruft die Primärschlüssel Details der angegebenen Event Hubs-Autorisierungsregel ab.</span><span class="sxs-lookup"><span data-stu-id="74dc0-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74dc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74dc0-104">SYNTAX</span></span>

### <span data-ttu-id="74dc0-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74dc0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74dc0-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="74dc0-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74dc0-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="74dc0-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74dc0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74dc0-108">DESCRIPTION</span></span>
<span data-ttu-id="74dc0-109">Das Get-AzureRmEventHubKey-Cmdlet gibt die primären und sekundären connectionStrings-und Schlüssel Details der angegebenen Namespace-/Ereignis Hubs/Alias Autorisierungsregel zurück.</span><span class="sxs-lookup"><span data-stu-id="74dc0-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="74dc0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74dc0-110">EXAMPLES</span></span>

### <span data-ttu-id="74dc0-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="74dc0-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="74dc0-112">Beispiel 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="74dc0-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="74dc0-113">Ruft Details der primären und sekundären connectionStrings und Schlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="74dc0-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="74dc0-114">Beispiel 3-Alias (georecovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="74dc0-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="74dc0-115">Ruft Details der primären, sekundären, AliasPrimary und AliasSecondary-connectionStrings und-Schlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="74dc0-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="74dc0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="74dc0-116">PARAMETERS</span></span>

### <span data-ttu-id="74dc0-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="74dc0-117">-AliasName</span></span>
<span data-ttu-id="74dc0-118">Alias Name</span><span class="sxs-lookup"><span data-stu-id="74dc0-118">Alias Name</span></span>

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

### <span data-ttu-id="74dc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74dc0-119">-DefaultProfile</span></span>
<span data-ttu-id="74dc0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74dc0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74dc0-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="74dc0-121">-EventHub</span></span>
<span data-ttu-id="74dc0-122">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="74dc0-122">EventHub Name</span></span>

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

### <span data-ttu-id="74dc0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="74dc0-123">-Name</span></span>
<span data-ttu-id="74dc0-124">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="74dc0-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="74dc0-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="74dc0-125">-Namespace</span></span>
<span data-ttu-id="74dc0-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="74dc0-126">Namespace Name</span></span>

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

### <span data-ttu-id="74dc0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74dc0-127">-ResourceGroupName</span></span>
<span data-ttu-id="74dc0-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="74dc0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="74dc0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74dc0-129">CommonParameters</span></span>
<span data-ttu-id="74dc0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74dc0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74dc0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74dc0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74dc0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74dc0-132">INPUTS</span></span>

### <span data-ttu-id="74dc0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="74dc0-133">System.String</span></span>

## <span data-ttu-id="74dc0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74dc0-134">OUTPUTS</span></span>

### <span data-ttu-id="74dc0-135">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="74dc0-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="74dc0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="74dc0-136">NOTES</span></span>

## <span data-ttu-id="74dc0-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74dc0-137">RELATED LINKS</span></span>
