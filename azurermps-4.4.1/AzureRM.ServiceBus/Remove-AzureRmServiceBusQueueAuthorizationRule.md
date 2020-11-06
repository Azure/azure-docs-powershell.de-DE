---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481577"
---
# <span data-ttu-id="eafaa-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eafaa-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="eafaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eafaa-102">SYNOPSIS</span></span>
<span data-ttu-id="eafaa-103">Entfernt die Autorisierungsregel einer Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="eafaa-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eafaa-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eafaa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eafaa-105">DESCRIPTION</span></span>
<span data-ttu-id="eafaa-106">Das Cmdlet **Remove-AzureRmServiceBusQueueAuthorizationRule** entfernt die Autorisierungsregel einer Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="eafaa-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="eafaa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eafaa-107">EXAMPLES</span></span>

### <span data-ttu-id="eafaa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eafaa-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="eafaa-109">Entfernt die Autorisierungsregel `SBAuthoRule1` der Warteschlange `SB-Queue_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="eafaa-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="eafaa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eafaa-110">PARAMETERS</span></span>

### <span data-ttu-id="eafaa-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eafaa-111">-ResourceGroup</span></span>
<span data-ttu-id="eafaa-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eafaa-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="eafaa-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eafaa-113">-Confirm</span></span>
<span data-ttu-id="eafaa-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eafaa-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eafaa-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eafaa-115">-WhatIf</span></span>
<span data-ttu-id="eafaa-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eafaa-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eafaa-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eafaa-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eafaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafaa-118">-DefaultProfile</span></span>
<span data-ttu-id="eafaa-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eafaa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eafaa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eafaa-120">-Name</span></span>
<span data-ttu-id="eafaa-121">AuthorizationRule-Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="eafaa-121">Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="eafaa-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eafaa-122">-Namespace</span></span>
<span data-ttu-id="eafaa-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="eafaa-123">Namespace Name.</span></span>

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

### <span data-ttu-id="eafaa-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="eafaa-124">-Queue</span></span>
<span data-ttu-id="eafaa-125">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="eafaa-125">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eafaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafaa-126">CommonParameters</span></span>
<span data-ttu-id="eafaa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafaa-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafaa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafaa-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eafaa-129">INPUTS</span></span>

### <span data-ttu-id="eafaa-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eafaa-130">-ResourceGroup</span></span>
 <span data-ttu-id="eafaa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="eafaa-131">System.String</span></span>

### <span data-ttu-id="eafaa-132">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="eafaa-132">-NamespaceName</span></span>
 <span data-ttu-id="eafaa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="eafaa-133">System.String</span></span>

### <span data-ttu-id="eafaa-134">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="eafaa-134">-QueueName</span></span>
 <span data-ttu-id="eafaa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="eafaa-135">System.String</span></span>

### <span data-ttu-id="eafaa-136">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="eafaa-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="eafaa-137">System. String</span><span class="sxs-lookup"><span data-stu-id="eafaa-137">System.String</span></span>

## <span data-ttu-id="eafaa-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eafaa-138">OUTPUTS</span></span>

### <span data-ttu-id="eafaa-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="eafaa-139">System.Object</span></span>

## <span data-ttu-id="eafaa-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="eafaa-140">NOTES</span></span>

## <span data-ttu-id="eafaa-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eafaa-141">RELATED LINKS</span></span>

