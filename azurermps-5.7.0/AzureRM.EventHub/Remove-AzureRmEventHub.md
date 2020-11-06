---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505525"
---
# <span data-ttu-id="7f40d-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="7f40d-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="7f40d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f40d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f40d-103">Entfernt den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="7f40d-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f40d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f40d-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f40d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f40d-105">DESCRIPTION</span></span>
<span data-ttu-id="7f40d-106">Das Remove-AzureRmEventHub-Cmdlet entfernt und löscht den angegebenen Ereignis-Hub aus dem angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="7f40d-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="7f40d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f40d-107">EXAMPLES</span></span>

### <span data-ttu-id="7f40d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f40d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="7f40d-109">Entfernt den Ereignis \` -Hub \` -MyEventHubName.</span><span class="sxs-lookup"><span data-stu-id="7f40d-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="7f40d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f40d-110">PARAMETERS</span></span>

### <span data-ttu-id="7f40d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f40d-111">-DefaultProfile</span></span>
<span data-ttu-id="7f40d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f40d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f40d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7f40d-113">-Name</span></span>
<span data-ttu-id="7f40d-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="7f40d-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f40d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7f40d-115">-Namespace</span></span>
<span data-ttu-id="7f40d-116">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="7f40d-116">Namespace Name</span></span>

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

### <span data-ttu-id="7f40d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f40d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f40d-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7f40d-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f40d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f40d-119">-Confirm</span></span>
<span data-ttu-id="7f40d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f40d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f40d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f40d-121">-WhatIf</span></span>
<span data-ttu-id="7f40d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f40d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f40d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f40d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f40d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f40d-124">CommonParameters</span></span>
<span data-ttu-id="7f40d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f40d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f40d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f40d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f40d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f40d-127">INPUTS</span></span>

### <span data-ttu-id="7f40d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7f40d-128">System.String</span></span>


## <span data-ttu-id="7f40d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f40d-129">OUTPUTS</span></span>

### <span data-ttu-id="7f40d-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="7f40d-130">System.Object</span></span>

## <span data-ttu-id="7f40d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f40d-131">NOTES</span></span>

## <span data-ttu-id="7f40d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f40d-132">RELATED LINKS</span></span>
