---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662821"
---
# <span data-ttu-id="19f24-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="19f24-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="19f24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19f24-102">SYNOPSIS</span></span>
<span data-ttu-id="19f24-103">Entfernt die angegebene Ereignis-Hub-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="19f24-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19f24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19f24-104">SYNTAX</span></span>

### <span data-ttu-id="19f24-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="19f24-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f24-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="19f24-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19f24-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19f24-107">DESCRIPTION</span></span>
<span data-ttu-id="19f24-108">Das Remove-AzureRmEventHubAuthorizationRule-Cmdlet entfernt die angegebene Autorisierungsregel aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="19f24-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="19f24-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19f24-109">EXAMPLES</span></span>

### <span data-ttu-id="19f24-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19f24-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="19f24-111">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="19f24-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="19f24-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="19f24-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="19f24-113">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Ereignis \` -Hub \` -MyEventHubName.</span><span class="sxs-lookup"><span data-stu-id="19f24-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="19f24-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="19f24-114">PARAMETERS</span></span>

### <span data-ttu-id="19f24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f24-115">-DefaultProfile</span></span>
<span data-ttu-id="19f24-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19f24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19f24-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="19f24-117">-EventHub</span></span>
<span data-ttu-id="19f24-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="19f24-118">EventHub Name</span></span>

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

### <span data-ttu-id="19f24-119">-Force</span><span class="sxs-lookup"><span data-stu-id="19f24-119">-Force</span></span>
<span data-ttu-id="19f24-120">Keine Bestätigung anfordern</span><span class="sxs-lookup"><span data-stu-id="19f24-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="19f24-121">-Name</span><span class="sxs-lookup"><span data-stu-id="19f24-121">-Name</span></span>
<span data-ttu-id="19f24-122">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="19f24-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="19f24-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="19f24-123">-Namespace</span></span>
<span data-ttu-id="19f24-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="19f24-124">Namespace Name</span></span>

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

### <span data-ttu-id="19f24-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19f24-125">-PassThru</span></span>
<span data-ttu-id="19f24-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="19f24-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19f24-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="19f24-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19f24-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f24-128">-ResourceGroupName</span></span>
<span data-ttu-id="19f24-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="19f24-129">Resource Group Name</span></span>

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

### <span data-ttu-id="19f24-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19f24-130">-Confirm</span></span>
<span data-ttu-id="19f24-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19f24-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f24-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f24-132">-WhatIf</span></span>
<span data-ttu-id="19f24-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19f24-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19f24-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19f24-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f24-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f24-135">CommonParameters</span></span>
<span data-ttu-id="19f24-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f24-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f24-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f24-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f24-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19f24-138">INPUTS</span></span>

### <span data-ttu-id="19f24-139">System. String</span><span class="sxs-lookup"><span data-stu-id="19f24-139">System.String</span></span>

## <span data-ttu-id="19f24-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19f24-140">OUTPUTS</span></span>

### <span data-ttu-id="19f24-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19f24-141">System.Boolean</span></span>

## <span data-ttu-id="19f24-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="19f24-142">NOTES</span></span>

## <span data-ttu-id="19f24-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19f24-143">RELATED LINKS</span></span>
