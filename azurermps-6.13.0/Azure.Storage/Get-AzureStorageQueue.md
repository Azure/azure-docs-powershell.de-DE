---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: 077d8139817c3998e27300d8c86c809b4da9e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482630"
---
# <span data-ttu-id="8f040-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8f040-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="8f040-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f040-102">SYNOPSIS</span></span>
<span data-ttu-id="8f040-103">Listet Speicher Warteschlangen auf.</span><span class="sxs-lookup"><span data-stu-id="8f040-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f040-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f040-104">SYNTAX</span></span>

### <span data-ttu-id="8f040-105">QueueName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f040-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f040-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="8f040-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f040-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f040-107">DESCRIPTION</span></span>
<span data-ttu-id="8f040-108">Das Cmdlet " **Get-AzureStorageQueue** " listet Speicher Warteschlangen auf, die einem Azure-Speicherkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8f040-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="8f040-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f040-109">EXAMPLES</span></span>

### <span data-ttu-id="8f040-110">Beispiel 1: Auflisten aller Azure-Speicher Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="8f040-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="8f040-111">Dieser Befehl ruft eine Liste aller Speicher Warteschlangen für das aktuelle Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="8f040-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="8f040-112">Beispiel 2: Auflisten von Azure-Speicher Warteschlangen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="8f040-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="8f040-113">Dieser Befehl verwendet ein Platzhalterzeichen, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.</span><span class="sxs-lookup"><span data-stu-id="8f040-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="8f040-114">Beispiel 3: Auflisten von Azure-Speicher Warteschlangen mithilfe des Warteschlangennamen Präfix</span><span class="sxs-lookup"><span data-stu-id="8f040-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="8f040-115">In diesem Beispiel wird der *prefix* -Parameter verwendet, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.</span><span class="sxs-lookup"><span data-stu-id="8f040-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="8f040-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f040-116">PARAMETERS</span></span>

### <span data-ttu-id="8f040-117">-Context</span><span class="sxs-lookup"><span data-stu-id="8f040-117">-Context</span></span>
<span data-ttu-id="8f040-118">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8f040-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8f040-119">Sie können Sie mithilfe des Cmdlets **New-AzureStorageContext** erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f040-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f040-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f040-120">-DefaultProfile</span></span>
<span data-ttu-id="8f040-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f040-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f040-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8f040-122">-Name</span></span>
<span data-ttu-id="8f040-123">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="8f040-123">Specifies a name.</span></span>
<span data-ttu-id="8f040-124">Wenn kein Name angegeben wird, ruft das Cmdlet eine Liste aller Warteschlangen ab.</span><span class="sxs-lookup"><span data-stu-id="8f040-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="8f040-125">Wenn ein vollständiger oder partieller Name angegeben wird, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8f040-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f040-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="8f040-126">-Prefix</span></span>
<span data-ttu-id="8f040-127">Gibt ein Präfix an, das für den Namen der Warteschlangen verwendet wird, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="8f040-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f040-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f040-128">CommonParameters</span></span>
<span data-ttu-id="8f040-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f040-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f040-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f040-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f040-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f040-131">INPUTS</span></span>

### <span data-ttu-id="8f040-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f040-132">System.String</span></span>

### <span data-ttu-id="8f040-133">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f040-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8f040-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f040-134">OUTPUTS</span></span>

### <span data-ttu-id="8f040-135">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8f040-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="8f040-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f040-136">NOTES</span></span>

## <span data-ttu-id="8f040-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f040-137">RELATED LINKS</span></span>

[<span data-ttu-id="8f040-138">Neu – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8f040-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="8f040-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8f040-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


