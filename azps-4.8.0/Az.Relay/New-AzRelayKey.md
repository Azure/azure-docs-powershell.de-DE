---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174902"
---
# <span data-ttu-id="6ac72-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="6ac72-101">New-AzRelayKey</span></span>

## <span data-ttu-id="6ac72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ac72-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac72-103">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="6ac72-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="6ac72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ac72-104">SYNTAX</span></span>

### <span data-ttu-id="6ac72-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ac72-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ac72-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ac72-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ac72-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ac72-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ac72-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ac72-108">DESCRIPTION</span></span>
<span data-ttu-id="6ac72-109">Das Cmdlet **New-AzRelayKey** generiert die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6ac72-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6ac72-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ac72-110">EXAMPLES</span></span>

### <span data-ttu-id="6ac72-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="6ac72-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6ac72-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-Namespace Entität erneut.</span><span class="sxs-lookup"><span data-stu-id="6ac72-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="6ac72-113">Beispiel für 1,1-Namespace-keywert bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="6ac72-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6ac72-114">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-Namespace Entität mit dem angegebenen Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="6ac72-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="6ac72-115">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6ac72-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6ac72-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-WcfRelay Entität erneut.</span><span class="sxs-lookup"><span data-stu-id="6ac72-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="6ac72-117">Beispiel für 2,1-WcfRelay-keywert bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="6ac72-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6ac72-118">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-WcfRelay Entität mit dem angegebenen Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="6ac72-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="6ac72-119">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6ac72-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6ac72-120">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6ac72-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="6ac72-121">Beispiel für 3,1-HybridConnection-keywert bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="6ac72-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6ac72-122">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-HybridConnection Entität mit dem angegebenen Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="6ac72-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="6ac72-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ac72-123">PARAMETERS</span></span>

### <span data-ttu-id="6ac72-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac72-124">-DefaultProfile</span></span>
<span data-ttu-id="6ac72-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ac72-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ac72-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6ac72-126">-HybridConnection</span></span>
<span data-ttu-id="6ac72-127">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="6ac72-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="6ac72-128">-Keywert</span><span class="sxs-lookup"><span data-stu-id="6ac72-128">-KeyValue</span></span>
<span data-ttu-id="6ac72-129">Ein Base64-codierter 256-Bit-Schlüssel zum Signieren und Validieren des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="6ac72-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="6ac72-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6ac72-130">-Name</span></span>
<span data-ttu-id="6ac72-131">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="6ac72-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6ac72-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6ac72-132">-Namespace</span></span>
<span data-ttu-id="6ac72-133">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="6ac72-133">Namespace Name.</span></span>

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

### <span data-ttu-id="6ac72-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6ac72-134">-RegenerateKey</span></span>
<span data-ttu-id="6ac72-135">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="6ac72-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="6ac72-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac72-136">-ResourceGroupName</span></span>
<span data-ttu-id="6ac72-137">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6ac72-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ac72-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6ac72-138">-WcfRelay</span></span>
<span data-ttu-id="6ac72-139">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="6ac72-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6ac72-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ac72-140">-Confirm</span></span>
<span data-ttu-id="6ac72-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ac72-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ac72-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac72-142">-WhatIf</span></span>
<span data-ttu-id="6ac72-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ac72-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ac72-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ac72-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ac72-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac72-145">CommonParameters</span></span>
<span data-ttu-id="6ac72-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac72-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac72-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac72-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac72-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ac72-148">INPUTS</span></span>

### <span data-ttu-id="6ac72-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6ac72-149">System.String</span></span>

## <span data-ttu-id="6ac72-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ac72-150">OUTPUTS</span></span>

### <span data-ttu-id="6ac72-151">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6ac72-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="6ac72-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ac72-152">NOTES</span></span>

## <span data-ttu-id="6ac72-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ac72-153">RELATED LINKS</span></span>
