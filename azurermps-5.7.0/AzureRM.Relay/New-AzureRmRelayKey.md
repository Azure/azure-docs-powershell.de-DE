---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501433"
---
# <span data-ttu-id="dd4e3-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="dd4e3-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="dd4e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd4e3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4e3-103">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="dd4e3-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd4e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd4e3-104">SYNTAX</span></span>

### <span data-ttu-id="dd4e3-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd4e3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4e3-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd4e3-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4e3-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd4e3-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd4e3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd4e3-108">DESCRIPTION</span></span>
<span data-ttu-id="dd4e3-109">Das Cmdlet **New-AzureRmRelayKey** generiert die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dd4e3-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dd4e3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd4e3-110">EXAMPLES</span></span>

### <span data-ttu-id="dd4e3-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="dd4e3-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="dd4e3-112">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dd4e3-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="dd4e3-113">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dd4e3-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="dd4e3-114">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dd4e3-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dd4e3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd4e3-115">PARAMETERS</span></span>

### <span data-ttu-id="dd4e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4e3-116">-DefaultProfile</span></span>
<span data-ttu-id="dd4e3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd4e3-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dd4e3-118">-HybridConnection</span></span>
<span data-ttu-id="dd4e3-119">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="dd4e3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dd4e3-120">-Name</span></span>
<span data-ttu-id="dd4e3-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="dd4e3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd4e3-122">-Namespace</span></span>
<span data-ttu-id="dd4e3-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-123">Namespace Name.</span></span>

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

### <span data-ttu-id="dd4e3-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="dd4e3-124">-RegenerateKey</span></span>
<span data-ttu-id="dd4e3-125">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="dd4e3-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4e3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4e3-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd4e3-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd4e3-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dd4e3-128">-WcfRelay</span></span>
<span data-ttu-id="dd4e3-129">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dd4e3-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd4e3-130">-Confirm</span></span>
<span data-ttu-id="dd4e3-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd4e3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4e3-132">-WhatIf</span></span>
<span data-ttu-id="dd4e3-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd4e3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd4e3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4e3-135">CommonParameters</span></span>
<span data-ttu-id="dd4e3-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4e3-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd4e3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4e3-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd4e3-138">INPUTS</span></span>

### <span data-ttu-id="dd4e3-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="dd4e3-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="dd4e3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4e3-140">System.String</span></span> 

### <span data-ttu-id="dd4e3-141">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="dd4e3-141">-NamespaceName</span></span>
 <span data-ttu-id="dd4e3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4e3-142">System.String</span></span> 
 

### <span data-ttu-id="dd4e3-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="dd4e3-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="dd4e3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4e3-144">System.String</span></span> 

### <span data-ttu-id="dd4e3-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="dd4e3-145">-WcfRelayName</span></span>
 <span data-ttu-id="dd4e3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4e3-146">System.String</span></span> 

### <span data-ttu-id="dd4e3-147">-Name</span><span class="sxs-lookup"><span data-stu-id="dd4e3-147">-Name</span></span>
 <span data-ttu-id="dd4e3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4e3-148">System.String</span></span>

### <span data-ttu-id="dd4e3-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="dd4e3-149">-RegenerateKeys</span></span>
 <span data-ttu-id="dd4e3-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4e3-150">System.String</span></span>

## <span data-ttu-id="dd4e3-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd4e3-151">OUTPUTS</span></span>

### <span data-ttu-id="dd4e3-152">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="dd4e3-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="dd4e3-153">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="dd4e3-153">Example 1 - Namespace</span></span>
<span data-ttu-id="dd4e3-154">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dd4e3-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="dd4e3-155">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dd4e3-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="dd4e3-156">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 Primary: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dd4e3-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="dd4e3-157">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dd4e3-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="dd4e3-158">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection Primary: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dd4e3-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="dd4e3-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd4e3-159">NOTES</span></span>

## <span data-ttu-id="dd4e3-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd4e3-160">RELATED LINKS</span></span>

