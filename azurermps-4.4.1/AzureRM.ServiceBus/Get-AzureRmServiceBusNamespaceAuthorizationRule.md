---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496861"
---
# <span data-ttu-id="d9b74-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9b74-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="d9b74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9b74-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b74-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen angegebenen Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="d9b74-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9b74-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9b74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9b74-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b74-106">Das Cmdlet " **Get-AzureRmServiceBusNamespaceAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="d9b74-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="d9b74-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9b74-107">EXAMPLES</span></span>

### <span data-ttu-id="d9b74-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9b74-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="d9b74-109">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="d9b74-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="d9b74-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9b74-110">PARAMETERS</span></span>

### <span data-ttu-id="d9b74-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9b74-111">-ResourceGroup</span></span>
<span data-ttu-id="d9b74-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9b74-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9b74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b74-113">-DefaultProfile</span></span>
<span data-ttu-id="d9b74-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9b74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b74-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d9b74-115">-Name</span></span>
<span data-ttu-id="d9b74-116">ServiceBus-Namespace-AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="d9b74-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b74-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d9b74-117">-Namespace</span></span>
<span data-ttu-id="d9b74-118">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d9b74-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b74-119">CommonParameters</span></span>
<span data-ttu-id="d9b74-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b74-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b74-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b74-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9b74-122">INPUTS</span></span>

### <span data-ttu-id="d9b74-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9b74-123">-ResourceGroup</span></span>
 <span data-ttu-id="d9b74-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d9b74-124">System.String</span></span>
 

### <span data-ttu-id="d9b74-125">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="d9b74-125">-NamespaceName</span></span>
 <span data-ttu-id="d9b74-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d9b74-126">System.String</span></span>
 

### <span data-ttu-id="d9b74-127">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="d9b74-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="d9b74-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d9b74-128">System.String</span></span>

## <span data-ttu-id="d9b74-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9b74-129">OUTPUTS</span></span>

### <span data-ttu-id="d9b74-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d9b74-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d9b74-131">ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/AuthorizationRules/AuthoRule1 Typ: Microsoft. ServiceBus/authorizationrules Name: AuthoRule1 Standort: Tags: Rechte: {hören, senden}</span><span class="sxs-lookup"><span data-stu-id="d9b74-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="d9b74-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9b74-132">NOTES</span></span>

## <span data-ttu-id="d9b74-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9b74-133">RELATED LINKS</span></span>

