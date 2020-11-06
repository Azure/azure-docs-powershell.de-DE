---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500697"
---
# <span data-ttu-id="fc8b0-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="fc8b0-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="fc8b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8b0-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für den ServiceBus-Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc8b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc8b0-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc8b0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc8b0-105">DESCRIPTION</span></span>
<span data-ttu-id="fc8b0-106">Das Cmdlet **New-AzureRmServiceBusNamespace** generiert neue primäre oder sekundäre Verbindungszeichenfolgen für den angegebenen Namespace und die Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="fc8b0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc8b0-107">EXAMPLES</span></span>

### <span data-ttu-id="fc8b0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc8b0-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="fc8b0-109">Generiert die primären oder sekundären Verbindungszeichenfolgen für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="fc8b0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc8b0-110">PARAMETERS</span></span>

### <span data-ttu-id="fc8b0-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="fc8b0-111">-RegenerateKeys</span></span>
<span data-ttu-id="fc8b0-112">Schlüssel neu generieren: Primärschlüssel/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

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

### <span data-ttu-id="fc8b0-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc8b0-113">-ResourceGroup</span></span>
<span data-ttu-id="fc8b0-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8b0-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc8b0-115">-Confirm</span></span>
<span data-ttu-id="fc8b0-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8b0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc8b0-117">-WhatIf</span></span>
<span data-ttu-id="fc8b0-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc8b0-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8b0-120">-DefaultProfile</span></span>
<span data-ttu-id="fc8b0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc8b0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fc8b0-122">-Name</span></span>
<span data-ttu-id="fc8b0-123">Name der Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="fc8b0-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="fc8b0-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc8b0-124">-Namespace</span></span>
<span data-ttu-id="fc8b0-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-125">Namespace Name.</span></span>

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

### <span data-ttu-id="fc8b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8b0-126">CommonParameters</span></span>
<span data-ttu-id="fc8b0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8b0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8b0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8b0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc8b0-129">INPUTS</span></span>

### <span data-ttu-id="fc8b0-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc8b0-130">-ResourceGroup</span></span>
 <span data-ttu-id="fc8b0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8b0-131">System.String</span></span>
 

### <span data-ttu-id="fc8b0-132">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="fc8b0-132">-NamespaceName</span></span>
 <span data-ttu-id="fc8b0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8b0-133">System.String</span></span>
 

### <span data-ttu-id="fc8b0-134">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="fc8b0-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="fc8b0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8b0-135">System.String</span></span>
 

### <span data-ttu-id="fc8b0-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="fc8b0-136">-RegenerateKeys</span></span>
 <span data-ttu-id="fc8b0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8b0-137">System.String</span></span>

## <span data-ttu-id="fc8b0-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc8b0-138">OUTPUTS</span></span>

### <span data-ttu-id="fc8b0-139">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="fc8b0-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="fc8b0-140">PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Wert} SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Wert} Primär Primär: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="fc8b0-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="fc8b0-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc8b0-141">NOTES</span></span>

## <span data-ttu-id="fc8b0-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc8b0-142">RELATED LINKS</span></span>

