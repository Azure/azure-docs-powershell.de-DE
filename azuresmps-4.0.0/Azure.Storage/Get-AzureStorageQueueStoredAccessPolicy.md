---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475673"
---
# <span data-ttu-id="651bc-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="651bc-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="651bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="651bc-102">SYNOPSIS</span></span>
<span data-ttu-id="651bc-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure Storage-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="651bc-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="651bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="651bc-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="651bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="651bc-105">DESCRIPTION</span></span>
<span data-ttu-id="651bc-106">Das Cmdlet " **Get-AzureStorageQueueStoredAccessPolicy** " listet die gespeicherten Zugriffsrichtlinien oder Richtlinien für eine Azure-Speicherwarteschlange auf.</span><span class="sxs-lookup"><span data-stu-id="651bc-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="651bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="651bc-107">EXAMPLES</span></span>

### <span data-ttu-id="651bc-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="651bc-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="651bc-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy12 in der Speicherwarteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="651bc-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="651bc-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="651bc-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="651bc-111">Dieser Befehl ruft alle gespeicherten Zugriffsrichtlinien in der Warteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="651bc-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="651bc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="651bc-112">PARAMETERS</span></span>

### <span data-ttu-id="651bc-113">-Context</span><span class="sxs-lookup"><span data-stu-id="651bc-113">-Context</span></span>
<span data-ttu-id="651bc-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="651bc-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="651bc-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="651bc-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="651bc-116">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="651bc-116">-Policy</span></span>
<span data-ttu-id="651bc-117">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="651bc-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="651bc-118">-Queue</span><span class="sxs-lookup"><span data-stu-id="651bc-118">-Queue</span></span>
<span data-ttu-id="651bc-119">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="651bc-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651bc-120">CommonParameters</span></span>
<span data-ttu-id="651bc-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="651bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651bc-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651bc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651bc-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="651bc-123">INPUTS</span></span>

## <span data-ttu-id="651bc-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="651bc-124">OUTPUTS</span></span>

## <span data-ttu-id="651bc-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="651bc-125">NOTES</span></span>

## <span data-ttu-id="651bc-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="651bc-126">RELATED LINKS</span></span>

[<span data-ttu-id="651bc-127">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="651bc-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="651bc-128">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="651bc-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="651bc-129">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="651bc-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="651bc-130">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="651bc-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


