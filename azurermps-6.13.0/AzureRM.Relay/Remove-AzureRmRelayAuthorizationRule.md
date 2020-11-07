---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: cebc4680e4c24bb7e19342d32e4aedd57b960e55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662298"
---
# <span data-ttu-id="d79ff-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d79ff-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="d79ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d79ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d79ff-103">Entfernt die Autorisierungsregel eines HybridConnection aus den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="d79ff-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d79ff-104">SYNTAX</span></span>

### <span data-ttu-id="d79ff-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d79ff-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d79ff-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d79ff-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d79ff-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d79ff-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d79ff-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d79ff-108">DESCRIPTION</span></span>
<span data-ttu-id="d79ff-109">Das Cmdlet **Remove-AzureRmRelayAuthorizationRule** entfernt die Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="d79ff-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d79ff-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d79ff-110">EXAMPLES</span></span>

### <span data-ttu-id="d79ff-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d79ff-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="d79ff-112">Entfernt die Autorisierungsregel `AuthoRule1` des Namespaces `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="d79ff-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="d79ff-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d79ff-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="d79ff-114">Entfernt die Autorisierungsregel `AuthoRule1` des WcfRelay `TestWcfRelay` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="d79ff-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="d79ff-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d79ff-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="d79ff-116">Entfernt die Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="d79ff-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="d79ff-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d79ff-117">PARAMETERS</span></span>

### <span data-ttu-id="d79ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79ff-118">-DefaultProfile</span></span>
<span data-ttu-id="d79ff-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d79ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d79ff-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d79ff-120">-Force</span></span>
<span data-ttu-id="d79ff-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="d79ff-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d79ff-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d79ff-122">-HybridConnection</span></span>
<span data-ttu-id="d79ff-123">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="d79ff-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="d79ff-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d79ff-124">-Name</span></span>
<span data-ttu-id="d79ff-125">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="d79ff-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="d79ff-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d79ff-126">-Namespace</span></span>
<span data-ttu-id="d79ff-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="d79ff-127">Namespace Name.</span></span>

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

### <span data-ttu-id="d79ff-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d79ff-128">-PassThru</span></span>
<span data-ttu-id="d79ff-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="d79ff-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d79ff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79ff-130">-ResourceGroupName</span></span>
<span data-ttu-id="d79ff-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d79ff-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="d79ff-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d79ff-132">-WcfRelay</span></span>
<span data-ttu-id="d79ff-133">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="d79ff-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d79ff-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d79ff-134">-Confirm</span></span>
<span data-ttu-id="d79ff-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d79ff-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79ff-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79ff-136">-WhatIf</span></span>
<span data-ttu-id="d79ff-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d79ff-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79ff-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d79ff-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79ff-139">CommonParameters</span></span>
<span data-ttu-id="d79ff-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d79ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d79ff-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79ff-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79ff-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d79ff-142">INPUTS</span></span>

### <span data-ttu-id="d79ff-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d79ff-143">System.String</span></span>


## <span data-ttu-id="d79ff-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d79ff-144">OUTPUTS</span></span>

### <span data-ttu-id="d79ff-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d79ff-145">System.Boolean</span></span>


## <span data-ttu-id="d79ff-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="d79ff-146">NOTES</span></span>

## <span data-ttu-id="d79ff-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d79ff-147">RELATED LINKS</span></span>
