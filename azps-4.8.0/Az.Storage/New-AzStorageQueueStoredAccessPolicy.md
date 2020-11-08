---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007722"
---
# <span data-ttu-id="975fe-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="975fe-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="975fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="975fe-102">SYNOPSIS</span></span>
<span data-ttu-id="975fe-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="975fe-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="975fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="975fe-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="975fe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="975fe-105">DESCRIPTION</span></span>
<span data-ttu-id="975fe-106">Das Cmdlet **New-AzStorageQueueStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="975fe-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="975fe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="975fe-107">EXAMPLES</span></span>

### <span data-ttu-id="975fe-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="975fe-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="975fe-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 in der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="975fe-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="975fe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="975fe-110">PARAMETERS</span></span>

### <span data-ttu-id="975fe-111">-Context</span><span class="sxs-lookup"><span data-stu-id="975fe-111">-Context</span></span>
<span data-ttu-id="975fe-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="975fe-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="975fe-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="975fe-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="975fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975fe-114">-DefaultProfile</span></span>
<span data-ttu-id="975fe-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="975fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="975fe-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="975fe-116">-ExpiryTime</span></span>
<span data-ttu-id="975fe-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="975fe-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975fe-118">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="975fe-118">-Permission</span></span>
<span data-ttu-id="975fe-119">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speicherwarteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="975fe-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="975fe-120">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="975fe-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975fe-121">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="975fe-121">-Policy</span></span>
<span data-ttu-id="975fe-122">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="975fe-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975fe-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="975fe-123">-Queue</span></span>
<span data-ttu-id="975fe-124">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="975fe-124">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="975fe-125">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="975fe-125">-StartTime</span></span>
<span data-ttu-id="975fe-126">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="975fe-126">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975fe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975fe-127">CommonParameters</span></span>
<span data-ttu-id="975fe-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="975fe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975fe-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="975fe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975fe-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="975fe-130">INPUTS</span></span>

### <span data-ttu-id="975fe-131">System. String</span><span class="sxs-lookup"><span data-stu-id="975fe-131">System.String</span></span>

### <span data-ttu-id="975fe-132">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="975fe-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="975fe-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="975fe-133">OUTPUTS</span></span>

### <span data-ttu-id="975fe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="975fe-134">System.String</span></span>

## <span data-ttu-id="975fe-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="975fe-135">NOTES</span></span>

## <span data-ttu-id="975fe-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="975fe-136">RELATED LINKS</span></span>

[<span data-ttu-id="975fe-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="975fe-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="975fe-138">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="975fe-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="975fe-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="975fe-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="975fe-140">Satz-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="975fe-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


