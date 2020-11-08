---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996985"
---
# <span data-ttu-id="ed47f-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ed47f-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="ed47f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed47f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed47f-103">Listet Speicher Warteschlangen auf.</span><span class="sxs-lookup"><span data-stu-id="ed47f-103">Lists storage queues.</span></span>

## <span data-ttu-id="ed47f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed47f-104">SYNTAX</span></span>

### <span data-ttu-id="ed47f-105">QueueName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed47f-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed47f-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="ed47f-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed47f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed47f-107">DESCRIPTION</span></span>
<span data-ttu-id="ed47f-108">Das Cmdlet " **Get-AzStorageQueue** " listet Speicher Warteschlangen auf, die einem Azure-Speicherkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ed47f-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="ed47f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed47f-109">EXAMPLES</span></span>

### <span data-ttu-id="ed47f-110">Beispiel 1: Auflisten aller Azure-Speicher Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="ed47f-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="ed47f-111">Dieser Befehl ruft eine Liste aller Speicher Warteschlangen für das aktuelle Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="ed47f-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="ed47f-112">Beispiel 2: Auflisten von Azure-Speicher Warteschlangen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="ed47f-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="ed47f-113">Dieser Befehl verwendet ein Platzhalterzeichen, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.</span><span class="sxs-lookup"><span data-stu-id="ed47f-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="ed47f-114">Beispiel 3: Auflisten von Azure-Speicher Warteschlangen mithilfe des Warteschlangennamen Präfix</span><span class="sxs-lookup"><span data-stu-id="ed47f-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="ed47f-115">In diesem Beispiel wird der *prefix* -Parameter verwendet, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.</span><span class="sxs-lookup"><span data-stu-id="ed47f-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="ed47f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed47f-116">PARAMETERS</span></span>

### <span data-ttu-id="ed47f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ed47f-117">-Context</span></span>
<span data-ttu-id="ed47f-118">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ed47f-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ed47f-119">Sie können Sie mithilfe des Cmdlets **New-AzStorageContext** erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed47f-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="ed47f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed47f-120">-DefaultProfile</span></span>
<span data-ttu-id="ed47f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed47f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed47f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ed47f-122">-Name</span></span>
<span data-ttu-id="ed47f-123">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="ed47f-123">Specifies a name.</span></span>
<span data-ttu-id="ed47f-124">Wenn kein Name angegeben wird, ruft das Cmdlet eine Liste aller Warteschlangen ab.</span><span class="sxs-lookup"><span data-stu-id="ed47f-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="ed47f-125">Wenn ein vollständiger oder partieller Name angegeben wird, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ed47f-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="ed47f-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="ed47f-126">-Prefix</span></span>
<span data-ttu-id="ed47f-127">Gibt ein Präfix an, das für den Namen der Warteschlangen verwendet wird, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="ed47f-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="ed47f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed47f-128">CommonParameters</span></span>
<span data-ttu-id="ed47f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed47f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed47f-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed47f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed47f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed47f-131">INPUTS</span></span>

### <span data-ttu-id="ed47f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ed47f-132">System.String</span></span>

### <span data-ttu-id="ed47f-133">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed47f-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ed47f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed47f-134">OUTPUTS</span></span>

### <span data-ttu-id="ed47f-135">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ed47f-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="ed47f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed47f-136">NOTES</span></span>

## <span data-ttu-id="ed47f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed47f-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed47f-138">Neu – AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ed47f-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="ed47f-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ed47f-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


