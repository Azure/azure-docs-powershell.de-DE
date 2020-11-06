---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502582"
---
# <span data-ttu-id="aa08f-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="aa08f-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="aa08f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa08f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa08f-103">Ruft die Primärschlüssel Details der angegebenen Event Hubs-Autorisierungsregel ab.</span><span class="sxs-lookup"><span data-stu-id="aa08f-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa08f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa08f-104">SYNTAX</span></span>

### <span data-ttu-id="aa08f-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa08f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa08f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa08f-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa08f-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa08f-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa08f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa08f-108">DESCRIPTION</span></span>
<span data-ttu-id="aa08f-109">Das Get-AzureRmEventHubKey-Cmdlet gibt die primären und sekundären connectionStrings-und Schlüssel Details der angegebenen Namespace-/Ereignis Hubs/Alias Autorisierungsregel zurück.</span><span class="sxs-lookup"><span data-stu-id="aa08f-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="aa08f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa08f-110">EXAMPLES</span></span>

### <span data-ttu-id="aa08f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa08f-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="aa08f-112">Ruft Details der primären und sekundären connectionStrings und Schlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="aa08f-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="aa08f-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa08f-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="aa08f-114">Ruft Details der primären, sekundären, AliasPrimary und AliasSecondary-connectionStrings und-Schlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="aa08f-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="aa08f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa08f-115">PARAMETERS</span></span>

### <span data-ttu-id="aa08f-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="aa08f-116">-AliasName</span></span>
<span data-ttu-id="aa08f-117">Alias Name</span><span class="sxs-lookup"><span data-stu-id="aa08f-117">Alias Name</span></span>

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

### <span data-ttu-id="aa08f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa08f-118">-DefaultProfile</span></span>
<span data-ttu-id="aa08f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa08f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa08f-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="aa08f-120">-EventHub</span></span>
<span data-ttu-id="aa08f-121">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="aa08f-121">EventHub Name</span></span>

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

### <span data-ttu-id="aa08f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aa08f-122">-Name</span></span>
<span data-ttu-id="aa08f-123">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="aa08f-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa08f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa08f-124">-Namespace</span></span>
<span data-ttu-id="aa08f-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="aa08f-125">Namespace Name</span></span>

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

### <span data-ttu-id="aa08f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa08f-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa08f-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="aa08f-127">Resource Group Name</span></span>

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

### <span data-ttu-id="aa08f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa08f-128">CommonParameters</span></span>
<span data-ttu-id="aa08f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa08f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aa08f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa08f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa08f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa08f-131">INPUTS</span></span>

### <span data-ttu-id="aa08f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="aa08f-132">System.String</span></span>


## <span data-ttu-id="aa08f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa08f-133">OUTPUTS</span></span>

### <span data-ttu-id="aa08f-134">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="aa08f-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="aa08f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa08f-135">NOTES</span></span>

## <span data-ttu-id="aa08f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa08f-136">RELATED LINKS</span></span>
