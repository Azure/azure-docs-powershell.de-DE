---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: fe0bd94d87dce975f6d027bd8ffb9683bb57a1fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842300"
---
# <span data-ttu-id="ee87d-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ee87d-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="ee87d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee87d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee87d-103">Entfernt die angegebene Ereignis-Hub-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="ee87d-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="ee87d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee87d-104">SYNTAX</span></span>

### <span data-ttu-id="ee87d-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee87d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee87d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee87d-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee87d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee87d-107">DESCRIPTION</span></span>
<span data-ttu-id="ee87d-108">Das Remove-AzEventHubAuthorizationRule-Cmdlet entfernt die angegebene Autorisierungsregel aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="ee87d-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="ee87d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee87d-109">EXAMPLES</span></span>

### <span data-ttu-id="ee87d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ee87d-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="ee87d-111">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="ee87d-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="ee87d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ee87d-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="ee87d-113">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Ereignis \` -Hub \` -MyEventHubName.</span><span class="sxs-lookup"><span data-stu-id="ee87d-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="ee87d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee87d-114">PARAMETERS</span></span>

### <span data-ttu-id="ee87d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee87d-115">-DefaultProfile</span></span>
<span data-ttu-id="ee87d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee87d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee87d-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ee87d-117">-EventHub</span></span>
<span data-ttu-id="ee87d-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="ee87d-118">EventHub Name</span></span>

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

### <span data-ttu-id="ee87d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ee87d-119">-Force</span></span>
<span data-ttu-id="ee87d-120">Keine Bestätigung anfordern</span><span class="sxs-lookup"><span data-stu-id="ee87d-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="ee87d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ee87d-121">-Name</span></span>
<span data-ttu-id="ee87d-122">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="ee87d-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ee87d-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ee87d-123">-Namespace</span></span>
<span data-ttu-id="ee87d-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ee87d-124">Namespace Name</span></span>

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

### <span data-ttu-id="ee87d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee87d-125">-PassThru</span></span>
<span data-ttu-id="ee87d-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ee87d-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee87d-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ee87d-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee87d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee87d-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee87d-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ee87d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="ee87d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee87d-130">-Confirm</span></span>
<span data-ttu-id="ee87d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee87d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee87d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee87d-132">-WhatIf</span></span>
<span data-ttu-id="ee87d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee87d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee87d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee87d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee87d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee87d-135">CommonParameters</span></span>
<span data-ttu-id="ee87d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee87d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee87d-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee87d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee87d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee87d-138">INPUTS</span></span>

### <span data-ttu-id="ee87d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ee87d-139">System.String</span></span>

## <span data-ttu-id="ee87d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee87d-140">OUTPUTS</span></span>

### <span data-ttu-id="ee87d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee87d-141">System.Boolean</span></span>

## <span data-ttu-id="ee87d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee87d-142">NOTES</span></span>

## <span data-ttu-id="ee87d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee87d-143">RELATED LINKS</span></span>
