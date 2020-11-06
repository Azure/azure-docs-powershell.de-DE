---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503954"
---
# <span data-ttu-id="070a3-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="070a3-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="070a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="070a3-102">SYNOPSIS</span></span>
<span data-ttu-id="070a3-103">Entfernt die Autorisierungsregel eines Themas aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="070a3-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="070a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="070a3-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="070a3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="070a3-105">DESCRIPTION</span></span>
<span data-ttu-id="070a3-106">Das Cmdlet **Remove-AzureRmServiceBusTopicAuthorizationRule** entfernt die Autorisierungsregel eines Themas aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="070a3-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="070a3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="070a3-107">EXAMPLES</span></span>

### <span data-ttu-id="070a3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="070a3-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="070a3-109">Entfernt die Autorisierungsregel `SBTopicAuthoRule1` des Themas `SB-Topic_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="070a3-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="070a3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="070a3-110">PARAMETERS</span></span>

### <span data-ttu-id="070a3-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="070a3-111">-ResourceGroup</span></span>
<span data-ttu-id="070a3-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="070a3-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="070a3-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="070a3-113">-Confirm</span></span>
<span data-ttu-id="070a3-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="070a3-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="070a3-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="070a3-115">-WhatIf</span></span>
<span data-ttu-id="070a3-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="070a3-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="070a3-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="070a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="070a3-118">-DefaultProfile</span></span>
<span data-ttu-id="070a3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="070a3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="070a3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="070a3-120">-Name</span></span>
<span data-ttu-id="070a3-121">Thema-AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="070a3-121">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="070a3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="070a3-122">-Namespace</span></span>
<span data-ttu-id="070a3-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="070a3-123">Namespace Name.</span></span>

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

### <span data-ttu-id="070a3-124">-Topic</span><span class="sxs-lookup"><span data-stu-id="070a3-124">-Topic</span></span>
<span data-ttu-id="070a3-125">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="070a3-125">Topic Name.</span></span>

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

### <span data-ttu-id="070a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="070a3-126">CommonParameters</span></span>
<span data-ttu-id="070a3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="070a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="070a3-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="070a3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="070a3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="070a3-129">INPUTS</span></span>

### <span data-ttu-id="070a3-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="070a3-130">-ResourceGroup</span></span>
 <span data-ttu-id="070a3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="070a3-131">System.String</span></span>

### <span data-ttu-id="070a3-132">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="070a3-132">-NamespaceName</span></span>
 <span data-ttu-id="070a3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="070a3-133">System.String</span></span>

### <span data-ttu-id="070a3-134">-Topicname</span><span class="sxs-lookup"><span data-stu-id="070a3-134">-TopicName</span></span>
 <span data-ttu-id="070a3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="070a3-135">System.String</span></span>

### <span data-ttu-id="070a3-136">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="070a3-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="070a3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="070a3-137">System.String</span></span>

## <span data-ttu-id="070a3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="070a3-138">OUTPUTS</span></span>

### <span data-ttu-id="070a3-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="070a3-139">System.Object</span></span>

## <span data-ttu-id="070a3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="070a3-140">NOTES</span></span>

## <span data-ttu-id="070a3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="070a3-141">RELATED LINKS</span></span>

