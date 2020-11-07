---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 62d37b30f20cf6d0738cfc927c266d6869be5586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663446"
---
# <span data-ttu-id="864bb-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="864bb-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="864bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="864bb-102">SYNOPSIS</span></span>
<span data-ttu-id="864bb-103">Entfernt die Autorisierungsregel eines HybridConnection aus den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="864bb-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="864bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="864bb-104">SYNTAX</span></span>

### <span data-ttu-id="864bb-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="864bb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="864bb-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="864bb-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="864bb-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="864bb-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="864bb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="864bb-108">DESCRIPTION</span></span>
<span data-ttu-id="864bb-109">Das Cmdlet **Remove-AzureRmRelayAuthorizationRule** entfernt die Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="864bb-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="864bb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="864bb-110">EXAMPLES</span></span>

### <span data-ttu-id="864bb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="864bb-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="864bb-112">Entfernt die Autorisierungsregel `AuthoRule1` des Namespaces `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="864bb-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="864bb-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="864bb-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="864bb-114">Entfernt die Autorisierungsregel `AuthoRule1` des WcfRelay `TestWcfRelay` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="864bb-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="864bb-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="864bb-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="864bb-116">Entfernt die Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="864bb-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="864bb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="864bb-117">PARAMETERS</span></span>

### <span data-ttu-id="864bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864bb-118">-DefaultProfile</span></span>
<span data-ttu-id="864bb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="864bb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="864bb-120">-Force</span></span>
<span data-ttu-id="864bb-121">Keine Bestätigung anfordern</span><span class="sxs-lookup"><span data-stu-id="864bb-121">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="864bb-122">-HybridConnection</span></span>
<span data-ttu-id="864bb-123">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="864bb-123">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="864bb-124">-Name</span></span>
<span data-ttu-id="864bb-125">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="864bb-125">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="864bb-126">-Namespace</span></span>
<span data-ttu-id="864bb-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="864bb-127">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="864bb-128">-PassThru</span></span>
<span data-ttu-id="864bb-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="864bb-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="864bb-130">-ResourceGroupName</span></span>
<span data-ttu-id="864bb-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="864bb-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="864bb-132">-WcfRelay</span></span>
<span data-ttu-id="864bb-133">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="864bb-133">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="864bb-134">-Confirm</span></span>
<span data-ttu-id="864bb-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="864bb-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="864bb-136">-WhatIf</span></span>
<span data-ttu-id="864bb-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="864bb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="864bb-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="864bb-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864bb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864bb-139">CommonParameters</span></span>
<span data-ttu-id="864bb-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="864bb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864bb-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="864bb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864bb-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="864bb-142">INPUTS</span></span>

### <span data-ttu-id="864bb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="864bb-143">System.String</span></span>

## <span data-ttu-id="864bb-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="864bb-144">OUTPUTS</span></span>

### <span data-ttu-id="864bb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="864bb-145">System.Boolean</span></span>

## <span data-ttu-id="864bb-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="864bb-146">NOTES</span></span>

## <span data-ttu-id="864bb-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="864bb-147">RELATED LINKS</span></span>

