---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: c887aab15e0874357ec32d9c815a9a9b1dd1227a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661047"
---
# <span data-ttu-id="71bdd-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="71bdd-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="71bdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="71bdd-103">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="71bdd-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="71bdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71bdd-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71bdd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="71bdd-106">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="71bdd-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="71bdd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="71bdd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71bdd-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="71bdd-109">Erstellt die Consumer-Gruppe \` MyConsumerGroupName \` im Ereignis \` -Hub \` -MyEventHubName mit dem Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="71bdd-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="71bdd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71bdd-110">PARAMETERS</span></span>

### <span data-ttu-id="71bdd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71bdd-111">-DefaultProfile</span></span>
<span data-ttu-id="71bdd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71bdd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71bdd-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="71bdd-113">-EventHub</span></span>
<span data-ttu-id="71bdd-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="71bdd-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71bdd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="71bdd-115">-Name</span></span>
<span data-ttu-id="71bdd-116">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="71bdd-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71bdd-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="71bdd-117">-Namespace</span></span>
<span data-ttu-id="71bdd-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="71bdd-118">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71bdd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71bdd-119">-ResourceGroupName</span></span>
<span data-ttu-id="71bdd-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="71bdd-120">Resource Group Name</span></span>

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

### <span data-ttu-id="71bdd-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="71bdd-121">-UserMetadata</span></span>
<span data-ttu-id="71bdd-122">Benutzer Metadaten für consumergroup</span><span class="sxs-lookup"><span data-stu-id="71bdd-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71bdd-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71bdd-123">-Confirm</span></span>
<span data-ttu-id="71bdd-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71bdd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71bdd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71bdd-125">-WhatIf</span></span>
<span data-ttu-id="71bdd-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71bdd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71bdd-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71bdd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71bdd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bdd-128">CommonParameters</span></span>
<span data-ttu-id="71bdd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71bdd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bdd-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71bdd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bdd-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71bdd-131">INPUTS</span></span>

### <span data-ttu-id="71bdd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="71bdd-132">System.String</span></span>

## <span data-ttu-id="71bdd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71bdd-133">OUTPUTS</span></span>

### <span data-ttu-id="71bdd-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="71bdd-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="71bdd-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="71bdd-135">NOTES</span></span>

## <span data-ttu-id="71bdd-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71bdd-136">RELATED LINKS</span></span>
