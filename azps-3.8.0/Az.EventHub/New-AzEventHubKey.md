---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: d701407ec770e49b699dfff3e36abcefcd9e7a48
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997045"
---
# <span data-ttu-id="69288-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="69288-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="69288-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69288-102">SYNOPSIS</span></span>
<span data-ttu-id="69288-103">Erstellt einen neuen primären oder sekundären Schlüssel für die angegebene Autorisierungsregel für Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="69288-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="69288-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69288-104">SYNTAX</span></span>

### <span data-ttu-id="69288-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69288-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69288-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="69288-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69288-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69288-107">DESCRIPTION</span></span>
<span data-ttu-id="69288-108">Das New-AzEventHubKey-Cmdlet generiert den primären oder sekundären SAS-Schlüssel für die angegebene Autorisierungsregel für Ereignis Hubs erneut.</span><span class="sxs-lookup"><span data-stu-id="69288-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="69288-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69288-109">EXAMPLES</span></span>

### <span data-ttu-id="69288-110">Beispiel 1,1-Namespace-AuthorizationRule Primär Primär</span><span class="sxs-lookup"><span data-stu-id="69288-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="69288-111">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="69288-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="69288-112">Beispiel 1,2-EventHub-AuthorizationRule Primär Primär</span><span class="sxs-lookup"><span data-stu-id="69288-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="69288-113">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="69288-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="69288-114">Beispiel 2,1-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="69288-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="69288-115">Beispiel 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="69288-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="69288-116">Generiert den Sekundärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="69288-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="69288-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="69288-117">PARAMETERS</span></span>

### <span data-ttu-id="69288-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69288-118">-DefaultProfile</span></span>
<span data-ttu-id="69288-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69288-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69288-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="69288-120">-EventHub</span></span>
<span data-ttu-id="69288-121">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="69288-121">EventHub Name</span></span>

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

### <span data-ttu-id="69288-122">-Keywert</span><span class="sxs-lookup"><span data-stu-id="69288-122">-KeyValue</span></span>
<span data-ttu-id="69288-123">Ein Base64-codierter 256-Bit-Schlüssel zum Signieren und Validieren des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="69288-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69288-124">-Name</span><span class="sxs-lookup"><span data-stu-id="69288-124">-Name</span></span>
<span data-ttu-id="69288-125">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="69288-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="69288-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="69288-126">-Namespace</span></span>
<span data-ttu-id="69288-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="69288-127">Namespace Name</span></span>

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

### <span data-ttu-id="69288-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="69288-128">-RegenerateKey</span></span>
<span data-ttu-id="69288-129">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="69288-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69288-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69288-130">-ResourceGroupName</span></span>
<span data-ttu-id="69288-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="69288-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69288-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69288-132">-Confirm</span></span>
<span data-ttu-id="69288-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69288-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69288-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69288-134">-WhatIf</span></span>
<span data-ttu-id="69288-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69288-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69288-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69288-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69288-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69288-137">CommonParameters</span></span>
<span data-ttu-id="69288-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69288-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69288-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69288-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69288-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69288-140">INPUTS</span></span>

### <span data-ttu-id="69288-141">System. String</span><span class="sxs-lookup"><span data-stu-id="69288-141">System.String</span></span>

## <span data-ttu-id="69288-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69288-142">OUTPUTS</span></span>

### <span data-ttu-id="69288-143">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="69288-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="69288-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="69288-144">NOTES</span></span>

## <span data-ttu-id="69288-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69288-145">RELATED LINKS</span></span>
