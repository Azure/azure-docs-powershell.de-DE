---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145428"
---
# <span data-ttu-id="b462d-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b462d-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="b462d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b462d-102">SYNOPSIS</span></span>
<span data-ttu-id="b462d-103">Listet Speicherwarteschlangen auf.</span><span class="sxs-lookup"><span data-stu-id="b462d-103">Lists storage queues.</span></span>

## <span data-ttu-id="b462d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b462d-104">SYNTAX</span></span>

### <span data-ttu-id="b462d-105">QueueName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b462d-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b462d-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="b462d-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b462d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b462d-107">DESCRIPTION</span></span>
<span data-ttu-id="b462d-108">Das **Cmdlet "Get-AzStorageQueue"** listet Speicherwarteschlangen auf, die einem Azure -Speicherkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b462d-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="b462d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b462d-109">EXAMPLES</span></span>

### <span data-ttu-id="b462d-110">Beispiel 1: Auflisten aller Azure Storage-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="b462d-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="b462d-111">Dieser Befehl ruft eine Liste aller Speicherwarteschlangen für das aktuelle Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="b462d-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="b462d-112">Beispiel 2: Auflisten von Azure Storage-Warteschlangen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="b462d-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="b462d-113">Dieser Befehl verwendet ein Platzhalterzeichen, um eine Liste der Speicherwarteschlangen zu erhalten, deren Name mit der Warteschlange beginnt.</span><span class="sxs-lookup"><span data-stu-id="b462d-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="b462d-114">Beispiel 3: Auflisten von Azure Storage-Warteschlangen mit dem Präfix "Warteschlangenname"</span><span class="sxs-lookup"><span data-stu-id="b462d-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="b462d-115">In diesem Beispiel wird der *Präfixparameter* verwendet, um eine Liste der Speicherwarteschlangen zu erhalten, deren Name mit der Warteschlange beginnt.</span><span class="sxs-lookup"><span data-stu-id="b462d-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="b462d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b462d-116">PARAMETERS</span></span>

### <span data-ttu-id="b462d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b462d-117">-Context</span></span>
<span data-ttu-id="b462d-118">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b462d-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b462d-119">Sie können sie mit dem **Cmdlet "New-AzStorageContext"** erstellen.</span><span class="sxs-lookup"><span data-stu-id="b462d-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="b462d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b462d-120">-DefaultProfile</span></span>
<span data-ttu-id="b462d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b462d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b462d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b462d-122">-Name</span></span>
<span data-ttu-id="b462d-123">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="b462d-123">Specifies a name.</span></span>
<span data-ttu-id="b462d-124">Wenn kein Name angegeben ist, ruft das Cmdlet eine Liste aller Warteschlangen ab.</span><span class="sxs-lookup"><span data-stu-id="b462d-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="b462d-125">Wenn ein vollständiger oder teilweiser Name angegeben wird, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b462d-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="b462d-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="b462d-126">-Prefix</span></span>
<span data-ttu-id="b462d-127">Gibt ein Präfix an, das im Namen der Warteschlangen verwendet wird, die Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="b462d-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="b462d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b462d-128">CommonParameters</span></span>
<span data-ttu-id="b462d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b462d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b462d-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b462d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b462d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b462d-131">INPUTS</span></span>

### <span data-ttu-id="b462d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b462d-132">System.String</span></span>

### <span data-ttu-id="b462d-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b462d-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b462d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b462d-134">OUTPUTS</span></span>

### <span data-ttu-id="b462d-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b462d-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="b462d-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b462d-136">NOTES</span></span>

## <span data-ttu-id="b462d-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b462d-137">RELATED LINKS</span></span>

[<span data-ttu-id="b462d-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b462d-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="b462d-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b462d-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


