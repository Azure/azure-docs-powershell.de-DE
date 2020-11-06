---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: ef54976ed06eb47da803470a3d4c163a8b294743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505709"
---
# <span data-ttu-id="465b6-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="465b6-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="465b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="465b6-102">SYNOPSIS</span></span>
<span data-ttu-id="465b6-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="465b6-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="465b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="465b6-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="465b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="465b6-105">DESCRIPTION</span></span>
<span data-ttu-id="465b6-106">Das Cmdlet **New-AzureStorageQueueStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="465b6-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="465b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="465b6-107">EXAMPLES</span></span>

### <span data-ttu-id="465b6-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="465b6-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="465b6-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 in der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="465b6-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="465b6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="465b6-110">PARAMETERS</span></span>

### <span data-ttu-id="465b6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="465b6-111">-Context</span></span>
<span data-ttu-id="465b6-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="465b6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="465b6-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="465b6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="465b6-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="465b6-114">-ExpiryTime</span></span>
<span data-ttu-id="465b6-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="465b6-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="465b6-116">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="465b6-116">-Permission</span></span>
<span data-ttu-id="465b6-117">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speicherwarteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="465b6-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="465b6-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="465b6-118">-Policy</span></span>
<span data-ttu-id="465b6-119">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="465b6-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="465b6-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="465b6-120">-Queue</span></span>
<span data-ttu-id="465b6-121">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="465b6-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="465b6-122">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="465b6-122">-StartTime</span></span>
<span data-ttu-id="465b6-123">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="465b6-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="465b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465b6-124">CommonParameters</span></span>
<span data-ttu-id="465b6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="465b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465b6-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465b6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465b6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="465b6-127">INPUTS</span></span>

### <span data-ttu-id="465b6-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="465b6-128">IStorageContext</span></span>

<span data-ttu-id="465b6-129">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="465b6-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="465b6-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="465b6-130">String</span></span>

<span data-ttu-id="465b6-131">Der Parameter "Queue" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="465b6-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="465b6-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="465b6-132">OUTPUTS</span></span>

### <span data-ttu-id="465b6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="465b6-133">System.String</span></span>

## <span data-ttu-id="465b6-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="465b6-134">NOTES</span></span>

## <span data-ttu-id="465b6-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="465b6-135">RELATED LINKS</span></span>

[<span data-ttu-id="465b6-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="465b6-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="465b6-137">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="465b6-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="465b6-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="465b6-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="465b6-139">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="465b6-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


