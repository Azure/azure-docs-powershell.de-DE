---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478926"
---
# <span data-ttu-id="7f33d-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7f33d-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="7f33d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f33d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f33d-103">Entfernt das Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7f33d-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f33d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f33d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f33d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f33d-105">DESCRIPTION</span></span>
<span data-ttu-id="7f33d-106">Das Cmdlet **Remove-AzureRmServiceBusTopic** entfernt das Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7f33d-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7f33d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f33d-107">EXAMPLES</span></span>

### <span data-ttu-id="7f33d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f33d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="7f33d-109">Entfernt das Thema `SB-Topic_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7f33d-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7f33d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f33d-110">PARAMETERS</span></span>

### <span data-ttu-id="7f33d-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f33d-111">-Confirm</span></span>
<span data-ttu-id="7f33d-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f33d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f33d-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f33d-113">-WhatIf</span></span>
<span data-ttu-id="7f33d-114">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f33d-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f33d-115">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f33d-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f33d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f33d-116">-DefaultProfile</span></span>
<span data-ttu-id="7f33d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f33d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f33d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7f33d-118">-Name</span></span>
<span data-ttu-id="7f33d-119">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="7f33d-119">Topic Name.</span></span>

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

### <span data-ttu-id="7f33d-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7f33d-120">-Namespace</span></span>
<span data-ttu-id="7f33d-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="7f33d-121">Namespace Name.</span></span>

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

### <span data-ttu-id="7f33d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f33d-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f33d-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7f33d-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f33d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f33d-124">CommonParameters</span></span>
<span data-ttu-id="7f33d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f33d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f33d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f33d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f33d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f33d-127">INPUTS</span></span>

### <span data-ttu-id="7f33d-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f33d-128">-ResourceGroup</span></span>
 <span data-ttu-id="7f33d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7f33d-129">System.String</span></span>

### <span data-ttu-id="7f33d-130">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="7f33d-130">-NamespaceName</span></span>
 <span data-ttu-id="7f33d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7f33d-131">System.String</span></span>

### <span data-ttu-id="7f33d-132">-Topicname</span><span class="sxs-lookup"><span data-stu-id="7f33d-132">-TopicName</span></span>
 <span data-ttu-id="7f33d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7f33d-133">System.String</span></span>

## <span data-ttu-id="7f33d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f33d-134">OUTPUTS</span></span>

### <span data-ttu-id="7f33d-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="7f33d-135">System.Object</span></span>

## <span data-ttu-id="7f33d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f33d-136">NOTES</span></span>

## <span data-ttu-id="7f33d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f33d-137">RELATED LINKS</span></span>

