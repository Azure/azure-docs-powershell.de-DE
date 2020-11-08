---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009561"
---
# <span data-ttu-id="16344-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="16344-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="16344-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16344-102">SYNOPSIS</span></span>
<span data-ttu-id="16344-103">Entfernt die Autorisierungsregel eines HybridConnection aus den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="16344-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="16344-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16344-104">SYNTAX</span></span>

### <span data-ttu-id="16344-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="16344-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16344-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="16344-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16344-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="16344-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16344-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16344-108">DESCRIPTION</span></span>
<span data-ttu-id="16344-109">Das Cmdlet **Remove-AzRelayAuthorizationRule** entfernt die Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="16344-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="16344-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16344-110">EXAMPLES</span></span>

### <span data-ttu-id="16344-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16344-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="16344-112">Entfernt die Autorisierungsregel `AuthoRule1` des Namespaces `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="16344-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="16344-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="16344-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="16344-114">Entfernt die Autorisierungsregel `AuthoRule1` des WcfRelay `TestWcfRelay` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="16344-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="16344-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="16344-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="16344-116">Entfernt die Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="16344-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="16344-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="16344-117">PARAMETERS</span></span>

### <span data-ttu-id="16344-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16344-118">-DefaultProfile</span></span>
<span data-ttu-id="16344-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16344-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16344-120">-Force</span><span class="sxs-lookup"><span data-stu-id="16344-120">-Force</span></span>
<span data-ttu-id="16344-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="16344-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16344-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="16344-122">-HybridConnection</span></span>
<span data-ttu-id="16344-123">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="16344-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16344-124">-Name</span><span class="sxs-lookup"><span data-stu-id="16344-124">-Name</span></span>
<span data-ttu-id="16344-125">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="16344-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16344-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16344-126">-Namespace</span></span>
<span data-ttu-id="16344-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="16344-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16344-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16344-128">-PassThru</span></span>
<span data-ttu-id="16344-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="16344-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="16344-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16344-130">-ResourceGroupName</span></span>
<span data-ttu-id="16344-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="16344-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="16344-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="16344-132">-WcfRelay</span></span>
<span data-ttu-id="16344-133">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="16344-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16344-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16344-134">-Confirm</span></span>
<span data-ttu-id="16344-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16344-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16344-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16344-136">-WhatIf</span></span>
<span data-ttu-id="16344-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16344-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16344-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16344-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16344-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16344-139">CommonParameters</span></span>
<span data-ttu-id="16344-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16344-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16344-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16344-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16344-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16344-142">INPUTS</span></span>

### <span data-ttu-id="16344-143">System. String</span><span class="sxs-lookup"><span data-stu-id="16344-143">System.String</span></span>

## <span data-ttu-id="16344-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16344-144">OUTPUTS</span></span>

### <span data-ttu-id="16344-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16344-145">System.Boolean</span></span>

## <span data-ttu-id="16344-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="16344-146">NOTES</span></span>

## <span data-ttu-id="16344-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16344-147">RELATED LINKS</span></span>
