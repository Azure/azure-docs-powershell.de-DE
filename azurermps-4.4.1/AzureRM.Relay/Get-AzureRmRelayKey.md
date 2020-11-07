---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 44e1571dbd6da015e163a69716f06d3ed3cebde5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662621"
---
# <span data-ttu-id="1980a-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="1980a-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="1980a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1980a-102">SYNOPSIS</span></span>
<span data-ttu-id="1980a-103">Ruft die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1980a-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1980a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1980a-104">SYNTAX</span></span>

### <span data-ttu-id="1980a-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1980a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1980a-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1980a-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1980a-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1980a-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1980a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1980a-108">DESCRIPTION</span></span>
<span data-ttu-id="1980a-109">Das Cmdlet " **Get-AzureRmRelayKey** " gibt die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten zurück (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1980a-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1980a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1980a-110">EXAMPLES</span></span>

### <span data-ttu-id="1980a-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="1980a-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="1980a-112">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1980a-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="1980a-113">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1980a-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="1980a-114">Primäre und sekundäre Verbindungszeichenfolge zu den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1980a-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1980a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1980a-115">PARAMETERS</span></span>

### <span data-ttu-id="1980a-116">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1980a-116">-HybridConnection</span></span>
<span data-ttu-id="1980a-117">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="1980a-117">HybridConnection Name.</span></span>

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

### <span data-ttu-id="1980a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1980a-118">-Name</span></span>
<span data-ttu-id="1980a-119">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="1980a-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="1980a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1980a-120">-Namespace</span></span>
<span data-ttu-id="1980a-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="1980a-121">Namespace Name.</span></span>

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

### <span data-ttu-id="1980a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1980a-122">-ResourceGroupName</span></span>
<span data-ttu-id="1980a-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1980a-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="1980a-124">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1980a-124">-WcfRelay</span></span>
<span data-ttu-id="1980a-125">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="1980a-125">WcfRelay Name.</span></span>

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

### <span data-ttu-id="1980a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1980a-126">-DefaultProfile</span></span>
<span data-ttu-id="1980a-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1980a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1980a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1980a-128">CommonParameters</span></span>
<span data-ttu-id="1980a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1980a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1980a-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1980a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1980a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1980a-131">INPUTS</span></span>

### <span data-ttu-id="1980a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1980a-132">-ResourceGroupName</span></span>
 <span data-ttu-id="1980a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1980a-133">System.String</span></span> 

### <span data-ttu-id="1980a-134">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="1980a-134">-NamespaceName</span></span>
 <span data-ttu-id="1980a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1980a-135">System.String</span></span> 
 

### <span data-ttu-id="1980a-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="1980a-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="1980a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1980a-137">System.String</span></span> 

### <span data-ttu-id="1980a-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="1980a-138">-WcfRelayName</span></span>
 <span data-ttu-id="1980a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1980a-139">System.String</span></span> 

### <span data-ttu-id="1980a-140">-Name</span><span class="sxs-lookup"><span data-stu-id="1980a-140">-Name</span></span>
 <span data-ttu-id="1980a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1980a-141">System.String</span></span>

## <span data-ttu-id="1980a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1980a-142">OUTPUTS</span></span>

### <span data-ttu-id="1980a-143">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="1980a-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="1980a-144">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="1980a-144">Example 1 - Namespace</span></span>
<span data-ttu-id="1980a-145">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1980a-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="1980a-146">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1980a-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="1980a-147">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 Primary: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1980a-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="1980a-148">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1980a-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="1980a-149">PrimaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpunkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection Primary: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1980a-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="1980a-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="1980a-150">NOTES</span></span>

## <span data-ttu-id="1980a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1980a-151">RELATED LINKS</span></span>

