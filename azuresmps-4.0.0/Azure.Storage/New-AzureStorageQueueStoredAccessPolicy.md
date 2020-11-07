---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661972"
---
# <span data-ttu-id="d36aa-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d36aa-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d36aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d36aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d36aa-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="d36aa-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="d36aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d36aa-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d36aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d36aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d36aa-106">Das Cmdlet **New-AzureStorageQueueStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="d36aa-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="d36aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d36aa-107">EXAMPLES</span></span>

### <span data-ttu-id="d36aa-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="d36aa-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="d36aa-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 in der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="d36aa-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="d36aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d36aa-110">PARAMETERS</span></span>

### <span data-ttu-id="d36aa-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d36aa-111">-Context</span></span>
<span data-ttu-id="d36aa-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d36aa-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d36aa-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d36aa-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d36aa-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d36aa-114">-ExpiryTime</span></span>
<span data-ttu-id="d36aa-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="d36aa-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36aa-116">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="d36aa-116">-Permission</span></span>
<span data-ttu-id="d36aa-117">Gibt die Ebene des öffentlichen Zugriffs auf diese Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="d36aa-117">Specifies the level of public access to this storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36aa-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d36aa-118">-Policy</span></span>
<span data-ttu-id="d36aa-119">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="d36aa-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36aa-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="d36aa-120">-Queue</span></span>
<span data-ttu-id="d36aa-121">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="d36aa-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d36aa-122">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="d36aa-122">-StartTime</span></span>
<span data-ttu-id="d36aa-123">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="d36aa-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36aa-124">CommonParameters</span></span>
<span data-ttu-id="d36aa-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d36aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36aa-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d36aa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36aa-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d36aa-127">INPUTS</span></span>

## <span data-ttu-id="d36aa-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d36aa-128">OUTPUTS</span></span>

## <span data-ttu-id="d36aa-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="d36aa-129">NOTES</span></span>

## <span data-ttu-id="d36aa-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d36aa-130">RELATED LINKS</span></span>

[<span data-ttu-id="d36aa-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d36aa-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d36aa-132">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d36aa-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d36aa-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d36aa-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d36aa-134">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d36aa-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


