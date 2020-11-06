---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: f8c419f59c05b2160ef02fbf239ecc2815bf1109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496781"
---
# <span data-ttu-id="d3fc6-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d3fc6-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="d3fc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fc6-103">Listet Speicher Warteschlangen auf.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3fc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3fc6-104">SYNTAX</span></span>

### <span data-ttu-id="d3fc6-105">QueueName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3fc6-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d3fc6-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="d3fc6-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d3fc6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3fc6-107">DESCRIPTION</span></span>
<span data-ttu-id="d3fc6-108">Das Cmdlet " **Get-AzureStorageQueue** " listet Speicher Warteschlangen auf, die einem Azure-Speicherkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="d3fc6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3fc6-109">EXAMPLES</span></span>

### <span data-ttu-id="d3fc6-110">Beispiel 1: Auflisten aller Azure-Speicher Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="d3fc6-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="d3fc6-111">Dieser Befehl ruft eine Liste aller Speicher Warteschlangen für das aktuelle Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="d3fc6-112">Beispiel 2: Auflisten von Azure-Speicher Warteschlangen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="d3fc6-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="d3fc6-113">Dieser Befehl verwendet ein Platzhalterzeichen, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="d3fc6-114">Beispiel 3: Auflisten von Azure-Speicher Warteschlangen mithilfe des Warteschlangennamen Präfix</span><span class="sxs-lookup"><span data-stu-id="d3fc6-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="d3fc6-115">In diesem Beispiel wird der *prefix* -Parameter verwendet, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="d3fc6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3fc6-116">PARAMETERS</span></span>

### <span data-ttu-id="d3fc6-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d3fc6-117">-Context</span></span>
<span data-ttu-id="d3fc6-118">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d3fc6-119">Sie können Sie mithilfe des Cmdlets **New-AzureStorageContext** erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fc6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d3fc6-120">-Name</span></span>
<span data-ttu-id="d3fc6-121">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-121">Specifies a name.</span></span>
<span data-ttu-id="d3fc6-122">Wenn kein Name angegeben wird, ruft das Cmdlet eine Liste aller Warteschlangen ab.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="d3fc6-123">Wenn ein vollständiger oder partieller Name angegeben wird, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="d3fc6-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d3fc6-124">-Prefix</span></span>
<span data-ttu-id="d3fc6-125">Gibt ein Präfix an, das für den Namen der Warteschlangen verwendet wird, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fc6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fc6-126">CommonParameters</span></span>
<span data-ttu-id="d3fc6-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fc6-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3fc6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fc6-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3fc6-129">INPUTS</span></span>

### <span data-ttu-id="d3fc6-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3fc6-130">IStorageContext</span></span>

<span data-ttu-id="d3fc6-131">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d3fc6-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d3fc6-132">String</span></span>

<span data-ttu-id="d3fc6-133">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3fc6-133">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d3fc6-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3fc6-134">OUTPUTS</span></span>

### <span data-ttu-id="d3fc6-135">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d3fc6-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="d3fc6-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3fc6-136">NOTES</span></span>

## <span data-ttu-id="d3fc6-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3fc6-137">RELATED LINKS</span></span>

[<span data-ttu-id="d3fc6-138">Neu – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d3fc6-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="d3fc6-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d3fc6-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


