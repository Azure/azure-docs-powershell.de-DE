---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: f2d295d31b0112a2adf73e2e4be064164df8fbb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502418"
---
# <span data-ttu-id="f1eef-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f1eef-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="f1eef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1eef-102">SYNOPSIS</span></span>
<span data-ttu-id="f1eef-103">Entfernt das Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f1eef-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1eef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1eef-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1eef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1eef-105">DESCRIPTION</span></span>
<span data-ttu-id="f1eef-106">Das Cmdlet **Remove-AzureRmServiceBusTopic** entfernt das Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f1eef-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f1eef-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1eef-107">EXAMPLES</span></span>

### <span data-ttu-id="f1eef-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1eef-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="f1eef-109">Entfernt das Thema `SB-Topic_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f1eef-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="f1eef-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1eef-110">PARAMETERS</span></span>

### <span data-ttu-id="f1eef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1eef-111">-DefaultProfile</span></span>
<span data-ttu-id="f1eef-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1eef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1eef-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f1eef-113">-Name</span></span>
<span data-ttu-id="f1eef-114">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="f1eef-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1eef-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1eef-115">-Namespace</span></span>
<span data-ttu-id="f1eef-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="f1eef-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1eef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1eef-117">-ResourceGroupName</span></span>
<span data-ttu-id="f1eef-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f1eef-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1eef-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1eef-119">-Confirm</span></span>
<span data-ttu-id="f1eef-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1eef-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1eef-121">-WhatIf</span></span>
<span data-ttu-id="f1eef-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1eef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1eef-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1eef-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1eef-124">CommonParameters</span></span>
<span data-ttu-id="f1eef-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1eef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1eef-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1eef-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1eef-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1eef-127">INPUTS</span></span>

### <span data-ttu-id="f1eef-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1eef-128">-ResourceGroup</span></span>
 <span data-ttu-id="f1eef-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f1eef-129">System.String</span></span>

### <span data-ttu-id="f1eef-130">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="f1eef-130">-NamespaceName</span></span>
 <span data-ttu-id="f1eef-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f1eef-131">System.String</span></span>

### <span data-ttu-id="f1eef-132">-Topicname</span><span class="sxs-lookup"><span data-stu-id="f1eef-132">-TopicName</span></span>
 <span data-ttu-id="f1eef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f1eef-133">System.String</span></span>

## <span data-ttu-id="f1eef-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1eef-134">OUTPUTS</span></span>

### <span data-ttu-id="f1eef-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="f1eef-135">System.Object</span></span>

## <span data-ttu-id="f1eef-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1eef-136">NOTES</span></span>

## <span data-ttu-id="f1eef-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1eef-137">RELATED LINKS</span></span>

