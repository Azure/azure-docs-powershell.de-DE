---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295678"
---
# <span data-ttu-id="6eed8-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="6eed8-101">New-AzRelayKey</span></span>

## <span data-ttu-id="6eed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eed8-102">SYNOPSIS</span></span>
<span data-ttu-id="6eed8-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relayentitäten (Namespace/WcfRelay/HybridConnection) erneut.</span><span class="sxs-lookup"><span data-stu-id="6eed8-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="6eed8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eed8-104">SYNTAX</span></span>

### <span data-ttu-id="6eed8-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6eed8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eed8-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eed8-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6eed8-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eed8-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eed8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6eed8-108">DESCRIPTION</span></span>
<span data-ttu-id="6eed8-109">Das **Cmdlet "New-AzRelayKey"** generiert die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relayentitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6eed8-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6eed8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6eed8-110">EXAMPLES</span></span>

### <span data-ttu-id="6eed8-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="6eed8-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6eed8-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6eed8-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="6eed8-113">Beispiel 1.1 – Bereitgestellter Namespaceschlüsselwert</span><span class="sxs-lookup"><span data-stu-id="6eed8-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6eed8-114">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-Namespace mit bereitgestellten Schlüsselwert</span><span class="sxs-lookup"><span data-stu-id="6eed8-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="6eed8-115">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6eed8-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6eed8-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6eed8-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="6eed8-117">Beispiel 2.1 – Bereitgestellter WcfRelay-Schlüsselwert</span><span class="sxs-lookup"><span data-stu-id="6eed8-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6eed8-118">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-WcfRelay mit bereitgestellten Schlüsselwert</span><span class="sxs-lookup"><span data-stu-id="6eed8-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="6eed8-119">Beispiel 3: HybridVerbinden</span><span class="sxs-lookup"><span data-stu-id="6eed8-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6eed8-120">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relayentitäten (Namespace/WcfRelay/HybridConnection) erneut.</span><span class="sxs-lookup"><span data-stu-id="6eed8-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="6eed8-121">Beispiel 3.1 – Bereitgestellter KeyValue "HybridConnection"</span><span class="sxs-lookup"><span data-stu-id="6eed8-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6eed8-122">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-HybridConnection mit bereitgestellten Schlüsselwert</span><span class="sxs-lookup"><span data-stu-id="6eed8-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="6eed8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eed8-123">PARAMETERS</span></span>

### <span data-ttu-id="6eed8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eed8-124">-DefaultProfile</span></span>
<span data-ttu-id="6eed8-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6eed8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eed8-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6eed8-126">-HybridConnection</span></span>
<span data-ttu-id="6eed8-127">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="6eed8-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="6eed8-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="6eed8-128">-KeyValue</span></span>
<span data-ttu-id="6eed8-129">Ein base64-codierter 256-Bit-Schlüssel zum Signieren und Überprüfen des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="6eed8-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eed8-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6eed8-130">-Name</span></span>
<span data-ttu-id="6eed8-131">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="6eed8-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6eed8-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6eed8-132">-Namespace</span></span>
<span data-ttu-id="6eed8-133">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="6eed8-133">Namespace Name.</span></span>

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

### <span data-ttu-id="6eed8-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6eed8-134">-RegenerateKey</span></span>
<span data-ttu-id="6eed8-135">Generieren Sie schlüssel erneut – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="6eed8-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="6eed8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eed8-136">-ResourceGroupName</span></span>
<span data-ttu-id="6eed8-137">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6eed8-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="6eed8-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6eed8-138">-WcfRelay</span></span>
<span data-ttu-id="6eed8-139">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="6eed8-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6eed8-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eed8-140">-Confirm</span></span>
<span data-ttu-id="6eed8-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6eed8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eed8-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6eed8-142">-WhatIf</span></span>
<span data-ttu-id="6eed8-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6eed8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eed8-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6eed8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eed8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eed8-145">CommonParameters</span></span>
<span data-ttu-id="6eed8-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eed8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eed8-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eed8-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eed8-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6eed8-148">INPUTS</span></span>

### <span data-ttu-id="6eed8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="6eed8-149">System.String</span></span>

## <span data-ttu-id="6eed8-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6eed8-150">OUTPUTS</span></span>

### <span data-ttu-id="6eed8-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6eed8-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="6eed8-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6eed8-152">NOTES</span></span>

## <span data-ttu-id="6eed8-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6eed8-153">RELATED LINKS</span></span>
