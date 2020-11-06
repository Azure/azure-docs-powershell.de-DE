---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 7394ec382105b1d05bed589be95630f68ab79ae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501649"
---
# <span data-ttu-id="498b8-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="498b8-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="498b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="498b8-102">SYNOPSIS</span></span>
<span data-ttu-id="498b8-103">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="498b8-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="498b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="498b8-104">SYNTAX</span></span>

### <span data-ttu-id="498b8-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="498b8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498b8-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="498b8-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498b8-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="498b8-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="498b8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="498b8-108">DESCRIPTION</span></span>
<span data-ttu-id="498b8-109">Das Cmdlet **New-AzureRmRelayKey** generiert die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="498b8-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="498b8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="498b8-110">EXAMPLES</span></span>

### <span data-ttu-id="498b8-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="498b8-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="498b8-112">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="498b8-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="498b8-113">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="498b8-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="498b8-114">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="498b8-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="498b8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="498b8-115">PARAMETERS</span></span>

### <span data-ttu-id="498b8-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="498b8-116">-Confirm</span></span>
<span data-ttu-id="498b8-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="498b8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="498b8-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="498b8-118">-HybridConnection</span></span>
<span data-ttu-id="498b8-119">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="498b8-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="498b8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="498b8-120">-Name</span></span>
<span data-ttu-id="498b8-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="498b8-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="498b8-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="498b8-122">-Namespace</span></span>
<span data-ttu-id="498b8-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="498b8-123">Namespace Name.</span></span>

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

### <span data-ttu-id="498b8-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="498b8-124">-RegenerateKey</span></span>
<span data-ttu-id="498b8-125">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="498b8-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="498b8-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="498b8-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="498b8-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="498b8-128">-WcfRelay</span></span>
<span data-ttu-id="498b8-129">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="498b8-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="498b8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="498b8-130">-WhatIf</span></span>
<span data-ttu-id="498b8-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="498b8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="498b8-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="498b8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="498b8-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498b8-133">-DefaultProfile</span></span>
<span data-ttu-id="498b8-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="498b8-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="498b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498b8-135">CommonParameters</span></span>
<span data-ttu-id="498b8-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="498b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498b8-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="498b8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498b8-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="498b8-138">INPUTS</span></span>

### <span data-ttu-id="498b8-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="498b8-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="498b8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="498b8-140">System.String</span></span> 

### <span data-ttu-id="498b8-141">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="498b8-141">-NamespaceName</span></span>
 <span data-ttu-id="498b8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="498b8-142">System.String</span></span> 
 

### <span data-ttu-id="498b8-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="498b8-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="498b8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="498b8-144">System.String</span></span> 

### <span data-ttu-id="498b8-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="498b8-145">-WcfRelayName</span></span>
 <span data-ttu-id="498b8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="498b8-146">System.String</span></span> 

### <span data-ttu-id="498b8-147">-Name</span><span class="sxs-lookup"><span data-stu-id="498b8-147">-Name</span></span>
 <span data-ttu-id="498b8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="498b8-148">System.String</span></span>

### <span data-ttu-id="498b8-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="498b8-149">-RegenerateKeys</span></span>
 <span data-ttu-id="498b8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="498b8-150">System.String</span></span>

## <span data-ttu-id="498b8-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="498b8-151">OUTPUTS</span></span>

### <span data-ttu-id="498b8-152">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="498b8-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="498b8-153">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="498b8-153">Example 1 - Namespace</span></span>
<span data-ttu-id="498b8-154">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="498b8-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="498b8-155">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="498b8-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="498b8-156">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 Primary: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="498b8-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="498b8-157">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="498b8-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="498b8-158">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection Primary: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="498b8-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="498b8-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="498b8-159">NOTES</span></span>

## <span data-ttu-id="498b8-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="498b8-160">RELATED LINKS</span></span>

