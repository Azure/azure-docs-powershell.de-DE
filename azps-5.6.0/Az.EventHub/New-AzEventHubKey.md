---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: c03a3ef7151c360bbcf81e249090fe39e3c144b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932827"
---
# <span data-ttu-id="f99c5-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="f99c5-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="f99c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f99c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f99c5-103">Erstellt einen neuen Primär- oder Sekundärschlüssel für die angegebene Ereignishubautorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="f99c5-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f99c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f99c5-104">SYNTAX</span></span>

### <span data-ttu-id="f99c5-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f99c5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99c5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f99c5-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99c5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f99c5-107">DESCRIPTION</span></span>
<span data-ttu-id="f99c5-108">Das New-AzEventHubKey cmdlet regeneriert den primären oder sekundären SAS-Schlüssel für die angegebene Ereignishubautorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="f99c5-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f99c5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f99c5-109">EXAMPLES</span></span>

### <span data-ttu-id="f99c5-110">Beispiel 1: Namespace – AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f99c5-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f99c5-111">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` neu.</span><span class="sxs-lookup"><span data-stu-id="f99c5-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f99c5-112">Beispiel 2: EventHub – AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f99c5-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f99c5-113">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` neu.</span><span class="sxs-lookup"><span data-stu-id="f99c5-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f99c5-114">Beispiel 3: - Namespace – AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f99c5-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="f99c5-115">Beispiel 4: EventHub – AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f99c5-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="f99c5-116">Regeneriert den Sekundärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="f99c5-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="f99c5-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f99c5-117">PARAMETERS</span></span>

### <span data-ttu-id="f99c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99c5-118">-DefaultProfile</span></span>
<span data-ttu-id="f99c5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f99c5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f99c5-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f99c5-120">-EventHub</span></span>
<span data-ttu-id="f99c5-121">EventHub-Name</span><span class="sxs-lookup"><span data-stu-id="f99c5-121">EventHub Name</span></span>

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

### <span data-ttu-id="f99c5-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="f99c5-122">-KeyValue</span></span>
<span data-ttu-id="f99c5-123">Ein base64-codierter 256-Bit-Schlüssel zum Signieren und Überprüfen des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="f99c5-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="f99c5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f99c5-124">-Name</span></span>
<span data-ttu-id="f99c5-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="f99c5-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f99c5-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f99c5-126">-Namespace</span></span>
<span data-ttu-id="f99c5-127">Namespacename</span><span class="sxs-lookup"><span data-stu-id="f99c5-127">Namespace Name</span></span>

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

### <span data-ttu-id="f99c5-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f99c5-128">-RegenerateKey</span></span>
<span data-ttu-id="f99c5-129">Neu generieren von Schlüsseln – 'PrimaryKey'/'SecondaryKey'</span><span class="sxs-lookup"><span data-stu-id="f99c5-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="f99c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f99c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="f99c5-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f99c5-131">Resource Group Name</span></span>

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

### <span data-ttu-id="f99c5-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f99c5-132">-Confirm</span></span>
<span data-ttu-id="f99c5-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f99c5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99c5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99c5-134">-WhatIf</span></span>
<span data-ttu-id="f99c5-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f99c5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f99c5-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f99c5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99c5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99c5-137">CommonParameters</span></span>
<span data-ttu-id="f99c5-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f99c5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99c5-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99c5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99c5-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f99c5-140">INPUTS</span></span>

### <span data-ttu-id="f99c5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f99c5-141">System.String</span></span>

## <span data-ttu-id="f99c5-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f99c5-142">OUTPUTS</span></span>

### <span data-ttu-id="f99c5-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f99c5-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="f99c5-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f99c5-144">NOTES</span></span>

## <span data-ttu-id="f99c5-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f99c5-145">RELATED LINKS</span></span>
