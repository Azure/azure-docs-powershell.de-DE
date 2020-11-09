---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302590"
---
# <span data-ttu-id="e050f-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e050f-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="e050f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e050f-102">SYNOPSIS</span></span>
<span data-ttu-id="e050f-103">Entfernt die Autorisierungsregel eines HybridConnection aus den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e050f-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e050f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e050f-104">SYNTAX</span></span>

### <span data-ttu-id="e050f-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e050f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e050f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e050f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e050f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e050f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e050f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e050f-108">DESCRIPTION</span></span>
<span data-ttu-id="e050f-109">Das Cmdlet **Remove-AzRelayAuthorizationRule** entfernt die Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e050f-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e050f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e050f-110">EXAMPLES</span></span>

### <span data-ttu-id="e050f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e050f-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="e050f-112">Entfernt die Autorisierungsregel `AuthoRule1` des Namespaces `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="e050f-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="e050f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e050f-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="e050f-114">Entfernt die Autorisierungsregel `AuthoRule1` des WcfRelay `TestWcfRelay` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="e050f-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="e050f-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e050f-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="e050f-116">Entfernt die Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="e050f-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="e050f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e050f-117">PARAMETERS</span></span>

### <span data-ttu-id="e050f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e050f-118">-DefaultProfile</span></span>
<span data-ttu-id="e050f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e050f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e050f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e050f-120">-Force</span></span>
<span data-ttu-id="e050f-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e050f-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e050f-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e050f-122">-HybridConnection</span></span>
<span data-ttu-id="e050f-123">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="e050f-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="e050f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e050f-124">-Name</span></span>
<span data-ttu-id="e050f-125">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="e050f-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e050f-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e050f-126">-Namespace</span></span>
<span data-ttu-id="e050f-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="e050f-127">Namespace Name.</span></span>

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

### <span data-ttu-id="e050f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e050f-128">-PassThru</span></span>
<span data-ttu-id="e050f-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="e050f-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e050f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e050f-130">-ResourceGroupName</span></span>
<span data-ttu-id="e050f-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e050f-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="e050f-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e050f-132">-WcfRelay</span></span>
<span data-ttu-id="e050f-133">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="e050f-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e050f-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e050f-134">-Confirm</span></span>
<span data-ttu-id="e050f-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e050f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e050f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e050f-136">-WhatIf</span></span>
<span data-ttu-id="e050f-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e050f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e050f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e050f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e050f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e050f-139">CommonParameters</span></span>
<span data-ttu-id="e050f-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e050f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e050f-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e050f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e050f-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e050f-142">INPUTS</span></span>

### <span data-ttu-id="e050f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e050f-143">System.String</span></span>

## <span data-ttu-id="e050f-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e050f-144">OUTPUTS</span></span>

### <span data-ttu-id="e050f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e050f-145">System.Boolean</span></span>

## <span data-ttu-id="e050f-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e050f-146">NOTES</span></span>

## <span data-ttu-id="e050f-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e050f-147">RELATED LINKS</span></span>
