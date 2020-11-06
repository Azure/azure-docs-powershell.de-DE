---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481586"
---
# <span data-ttu-id="72b3a-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="72b3a-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="72b3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="72b3a-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für das ServiceBus-Thema neu.</span><span class="sxs-lookup"><span data-stu-id="72b3a-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72b3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72b3a-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72b3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="72b3a-106">Das Cmdlet **New-AzureRmServiceBusTopicKey** generiert eine neue primäre oder sekundäre Verbindungszeichenfolge für das angegebene Service Bus-Thema und die Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="72b3a-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="72b3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72b3a-107">EXAMPLES</span></span>

### <span data-ttu-id="72b3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72b3a-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="72b3a-109">Generiert die primäre Verbindungszeichenfolge für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="72b3a-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="72b3a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="72b3a-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="72b3a-111">Generiert die sekundäre Verbindungszeichenfolge für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="72b3a-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="72b3a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="72b3a-112">PARAMETERS</span></span>

### <span data-ttu-id="72b3a-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="72b3a-113">-RegenerateKeys</span></span>
<span data-ttu-id="72b3a-114">Gibt an, ob die primären oder sekundären Schlüssel neu generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72b3a-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b3a-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72b3a-115">-ResourceGroup</span></span>
<span data-ttu-id="72b3a-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72b3a-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="72b3a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72b3a-117">-Confirm</span></span>
<span data-ttu-id="72b3a-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72b3a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72b3a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72b3a-119">-WhatIf</span></span>
<span data-ttu-id="72b3a-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72b3a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72b3a-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72b3a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72b3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b3a-122">-DefaultProfile</span></span>
<span data-ttu-id="72b3a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72b3a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72b3a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="72b3a-124">-Name</span></span>
<span data-ttu-id="72b3a-125">Name der Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="72b3a-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b3a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="72b3a-126">-Namespace</span></span>
<span data-ttu-id="72b3a-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="72b3a-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b3a-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="72b3a-128">-Topic</span></span>
<span data-ttu-id="72b3a-129">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="72b3a-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b3a-130">CommonParameters</span></span>
<span data-ttu-id="72b3a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b3a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b3a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b3a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72b3a-133">INPUTS</span></span>

### <span data-ttu-id="72b3a-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72b3a-134">-ResourceGroup</span></span>
 <span data-ttu-id="72b3a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="72b3a-135">System.String</span></span>
 

### <span data-ttu-id="72b3a-136">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="72b3a-136">-NamespaceName</span></span>
 <span data-ttu-id="72b3a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="72b3a-137">System.String</span></span>
 

### <span data-ttu-id="72b3a-138">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="72b3a-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="72b3a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="72b3a-139">System.String</span></span>
 

### <span data-ttu-id="72b3a-140">-Topicname</span><span class="sxs-lookup"><span data-stu-id="72b3a-140">-TopicName</span></span>
 <span data-ttu-id="72b3a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="72b3a-141">System.String</span></span>
 

### <span data-ttu-id="72b3a-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="72b3a-142">-RegenerateKeys</span></span>
 <span data-ttu-id="72b3a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="72b3a-143">System.String</span></span>

## <span data-ttu-id="72b3a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72b3a-144">OUTPUTS</span></span>

### <span data-ttu-id="72b3a-145">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="72b3a-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="72b3a-146">PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-c_exampl1 SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-c_exampl1 Primär Primär: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="72b3a-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="72b3a-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="72b3a-147">NOTES</span></span>

## <span data-ttu-id="72b3a-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72b3a-148">RELATED LINKS</span></span>

