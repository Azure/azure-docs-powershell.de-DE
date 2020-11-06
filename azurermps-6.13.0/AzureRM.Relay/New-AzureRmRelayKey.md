---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: c72cca2b3bf4d6276be14d85a363498c149a3a55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477726"
---
# <span data-ttu-id="2be10-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="2be10-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="2be10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2be10-102">SYNOPSIS</span></span>
<span data-ttu-id="2be10-103">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="2be10-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2be10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2be10-104">SYNTAX</span></span>

### <span data-ttu-id="2be10-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2be10-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2be10-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2be10-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2be10-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2be10-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2be10-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2be10-108">DESCRIPTION</span></span>
<span data-ttu-id="2be10-109">Das Cmdlet **New-AzureRmRelayKey** generiert die primären und sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2be10-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2be10-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2be10-110">EXAMPLES</span></span>

### <span data-ttu-id="2be10-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="2be10-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```
<span data-ttu-id="2be10-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-Namespace Entität erneut.</span><span class="sxs-lookup"><span data-stu-id="2be10-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="2be10-113">Beispiel für 1,1-Namespace-keywert bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="2be10-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```
<span data-ttu-id="2be10-114">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-Namespace Entität mit dem angegebenen Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="2be10-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="2be10-115">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2be10-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```
<span data-ttu-id="2be10-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-WcfRelay Entität erneut.</span><span class="sxs-lookup"><span data-stu-id="2be10-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="2be10-117">Beispiel für 2,1-WcfRelay-keywert bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="2be10-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```
<span data-ttu-id="2be10-118">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-WcfRelay Entität mit dem angegebenen Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="2be10-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="2be10-119">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2be10-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```
<span data-ttu-id="2be10-120">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2be10-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="2be10-121">Beispiel für 3,1-HybridConnection-keywert bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="2be10-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```
<span data-ttu-id="2be10-122">generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene Relay-HybridConnection Entität mit dem angegebenen Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="2be10-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="2be10-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="2be10-123">PARAMETERS</span></span>

### <span data-ttu-id="2be10-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be10-124">-DefaultProfile</span></span>
<span data-ttu-id="2be10-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2be10-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be10-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2be10-126">-HybridConnection</span></span>
<span data-ttu-id="2be10-127">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="2be10-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2be10-128">-Keywert</span><span class="sxs-lookup"><span data-stu-id="2be10-128">-KeyValue</span></span>
<span data-ttu-id="2be10-129">Ein Base64-codierter 256-Bit-Schlüssel zum Signieren und Validieren des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="2be10-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="2be10-130">-Name</span><span class="sxs-lookup"><span data-stu-id="2be10-130">-Name</span></span>
<span data-ttu-id="2be10-131">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="2be10-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2be10-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2be10-132">-Namespace</span></span>
<span data-ttu-id="2be10-133">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="2be10-133">Namespace Name.</span></span>

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

### <span data-ttu-id="2be10-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="2be10-134">-RegenerateKey</span></span>
<span data-ttu-id="2be10-135">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="2be10-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="2be10-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be10-136">-ResourceGroupName</span></span>
<span data-ttu-id="2be10-137">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2be10-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="2be10-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2be10-138">-WcfRelay</span></span>
<span data-ttu-id="2be10-139">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="2be10-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2be10-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2be10-140">-Confirm</span></span>
<span data-ttu-id="2be10-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2be10-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be10-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be10-142">-WhatIf</span></span>
<span data-ttu-id="2be10-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2be10-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be10-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2be10-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be10-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be10-145">CommonParameters</span></span>
<span data-ttu-id="2be10-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be10-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2be10-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be10-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be10-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2be10-148">INPUTS</span></span>

### <span data-ttu-id="2be10-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2be10-149">System.String</span></span>


## <span data-ttu-id="2be10-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2be10-150">OUTPUTS</span></span>

### <span data-ttu-id="2be10-151">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2be10-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>


## <span data-ttu-id="2be10-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="2be10-152">NOTES</span></span>

## <span data-ttu-id="2be10-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2be10-153">RELATED LINKS</span></span>
