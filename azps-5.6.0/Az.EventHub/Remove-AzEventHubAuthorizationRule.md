---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 496806b6d5ab6b7d6e1c788b7b42424b7e97a8c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939592"
---
# <span data-ttu-id="c3429-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c3429-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c3429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3429-102">SYNOPSIS</span></span>
<span data-ttu-id="c3429-103">Entfernt die angegebene Ereignishubautorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="c3429-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="c3429-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3429-104">SYNTAX</span></span>

### <span data-ttu-id="c3429-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3429-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3429-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3429-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3429-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3429-107">DESCRIPTION</span></span>
<span data-ttu-id="c3429-108">Das Remove-AzEventHubAuthorizationRule-Cmdlet entfernt und löscht die angegebene Autorisierungsregel aus dem angegebenen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="c3429-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="c3429-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3429-109">EXAMPLES</span></span>

### <span data-ttu-id="c3429-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3429-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="c3429-111">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c3429-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c3429-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3429-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="c3429-113">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Ereignishub \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="c3429-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="c3429-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c3429-114">PARAMETERS</span></span>

### <span data-ttu-id="c3429-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3429-115">-DefaultProfile</span></span>
<span data-ttu-id="c3429-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3429-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3429-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c3429-117">-EventHub</span></span>
<span data-ttu-id="c3429-118">EventHub-Name</span><span class="sxs-lookup"><span data-stu-id="c3429-118">EventHub Name</span></span>

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

### <span data-ttu-id="c3429-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c3429-119">-Force</span></span>
<span data-ttu-id="c3429-120">Keine Bestätigung fordern</span><span class="sxs-lookup"><span data-stu-id="c3429-120">Do not ask for confirmation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3429-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c3429-121">-Name</span></span>
<span data-ttu-id="c3429-122">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="c3429-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c3429-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c3429-123">-Namespace</span></span>
<span data-ttu-id="c3429-124">Namespacename</span><span class="sxs-lookup"><span data-stu-id="c3429-124">Namespace Name</span></span>

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

### <span data-ttu-id="c3429-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3429-125">-PassThru</span></span>
<span data-ttu-id="c3429-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c3429-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c3429-127">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c3429-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3429-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3429-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3429-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c3429-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c3429-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3429-130">-Confirm</span></span>
<span data-ttu-id="c3429-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3429-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3429-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3429-132">-WhatIf</span></span>
<span data-ttu-id="c3429-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3429-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3429-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3429-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3429-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3429-135">CommonParameters</span></span>
<span data-ttu-id="c3429-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3429-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3429-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3429-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3429-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3429-138">INPUTS</span></span>

### <span data-ttu-id="c3429-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c3429-139">System.String</span></span>

## <span data-ttu-id="c3429-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3429-140">OUTPUTS</span></span>

### <span data-ttu-id="c3429-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3429-141">System.Boolean</span></span>

## <span data-ttu-id="c3429-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c3429-142">NOTES</span></span>

## <span data-ttu-id="c3429-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c3429-143">RELATED LINKS</span></span>
