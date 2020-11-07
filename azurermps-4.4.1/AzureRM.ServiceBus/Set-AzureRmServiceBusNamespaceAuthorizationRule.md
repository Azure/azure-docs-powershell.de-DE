---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664722"
---
# <span data-ttu-id="a4d7e-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a4d7e-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a4d7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d7e-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für den angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4d7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d7e-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d7e-106">Das Cmdlet " **Satz-AzureRmServiceBusNamespaceAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="a4d7e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="a4d7e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4d7e-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="a4d7e-109">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a4d7e-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a4d7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d7e-110">PARAMETERS</span></span>

### <span data-ttu-id="a4d7e-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4d7e-111">-ResourceGroup</span></span>
<span data-ttu-id="a4d7e-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4d7e-113">-Rechte</span><span class="sxs-lookup"><span data-stu-id="a4d7e-113">-Rights</span></span>
<span data-ttu-id="a4d7e-114">Rechte Beispiel: @ ("Listen", "Senden", "verwalten").</span><span class="sxs-lookup"><span data-stu-id="a4d7e-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="a4d7e-115">Erforderlich, wenn **AuthruleObj** nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-115">Required if **AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d7e-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4d7e-116">-Confirm</span></span>
<span data-ttu-id="a4d7e-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d7e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d7e-118">-WhatIf</span></span>
<span data-ttu-id="a4d7e-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d7e-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d7e-121">-DefaultProfile</span></span>
<span data-ttu-id="a4d7e-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4d7e-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="a4d7e-123">-InputObj</span></span>
<span data-ttu-id="a4d7e-124">ServiceBus-Namespace-AuthorizationRule-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d7e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a4d7e-125">-Name</span></span>
<span data-ttu-id="a4d7e-126">AuthorizationRule-Name – erforderlich, wenn "AuthruleObj" nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="a4d7e-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4d7e-127">-Namespace</span></span>
<span data-ttu-id="a4d7e-128">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="a4d7e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d7e-129">CommonParameters</span></span>
<span data-ttu-id="a4d7e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d7e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d7e-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4d7e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d7e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4d7e-132">INPUTS</span></span>

### <span data-ttu-id="a4d7e-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4d7e-133">-ResourceGroup</span></span>
 <span data-ttu-id="a4d7e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d7e-134">System.String</span></span>

### <span data-ttu-id="a4d7e-135">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="a4d7e-135">-NamespaceName</span></span>
 <span data-ttu-id="a4d7e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d7e-136">System.String</span></span>

### <span data-ttu-id="a4d7e-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="a4d7e-137">-AuthRuleObj</span></span>
 <span data-ttu-id="a4d7e-138">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a4d7e-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a4d7e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4d7e-139">OUTPUTS</span></span>

### <span data-ttu-id="a4d7e-140">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a4d7e-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="a4d7e-141">ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/AuthorizationRules/AuthoRule1 Typ: Microsoft. ServiceBus/authorizationrules Name: AuthoRule1 Standort: Tags: Rechte: {hören, senden}</span><span class="sxs-lookup"><span data-stu-id="a4d7e-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="a4d7e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4d7e-142">NOTES</span></span>

## <span data-ttu-id="a4d7e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4d7e-143">RELATED LINKS</span></span>

