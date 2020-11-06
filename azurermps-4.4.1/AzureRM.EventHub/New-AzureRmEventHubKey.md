---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505010"
---
# <span data-ttu-id="f1a32-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="f1a32-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="f1a32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1a32-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a32-103">Erstellt einen neuen primären oder sekundären Schlüssel für die angegebene Autorisierungsregel für Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="f1a32-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1a32-104">SYNTAX</span></span>

### <span data-ttu-id="f1a32-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1a32-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f1a32-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1a32-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f1a32-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1a32-107">DESCRIPTION</span></span>
<span data-ttu-id="f1a32-108">Das New-AzureRmEventHubKey-Cmdlet generiert den primären oder sekundären SAS-Schlüssel für die angegebene Autorisierungsregel für Ereignis Hubs erneut.</span><span class="sxs-lookup"><span data-stu-id="f1a32-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f1a32-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1a32-109">EXAMPLES</span></span>

### <span data-ttu-id="f1a32-110">Beispiel 1,1</span><span class="sxs-lookup"><span data-stu-id="f1a32-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f1a32-111">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="f1a32-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f1a32-112">Beispiel 1,2</span><span class="sxs-lookup"><span data-stu-id="f1a32-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f1a32-113">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="f1a32-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f1a32-114">Beispiel 2,1</span><span class="sxs-lookup"><span data-stu-id="f1a32-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="f1a32-115">Beispiel 2,2</span><span class="sxs-lookup"><span data-stu-id="f1a32-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="f1a32-116">Generiert den Sekundärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="f1a32-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="f1a32-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1a32-117">PARAMETERS</span></span>

### <span data-ttu-id="f1a32-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f1a32-118">-RegenerateKey</span></span>
<span data-ttu-id="f1a32-119">Schlüssel zum Regenerieren: \` Primärschlüssel \` oder \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="f1a32-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a32-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1a32-120">-Confirm</span></span>
<span data-ttu-id="f1a32-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1a32-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a32-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a32-122">-WhatIf</span></span>
<span data-ttu-id="f1a32-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1a32-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a32-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1a32-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a32-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f1a32-125">-EventHub</span></span>
<span data-ttu-id="f1a32-126">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="f1a32-126">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a32-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f1a32-127">-Name</span></span>
<span data-ttu-id="f1a32-128">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="f1a32-128">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a32-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1a32-129">-Namespace</span></span>
<span data-ttu-id="f1a32-130">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="f1a32-130">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a32-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a32-131">-ResourceGroupName</span></span>
<span data-ttu-id="f1a32-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1a32-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f1a32-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1a32-133">INPUTS</span></span>

### <span data-ttu-id="f1a32-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a32-134">System.String</span></span>

## <span data-ttu-id="f1a32-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1a32-135">OUTPUTS</span></span>

### <span data-ttu-id="f1a32-136">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f1a32-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="f1a32-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1a32-137">NOTES</span></span>

## <span data-ttu-id="f1a32-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1a32-138">RELATED LINKS</span></span>

